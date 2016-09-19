---
published: true
layout: post
title: rake stats M/C column explained
---
I just spent the better part of an hour trying to figure out what the "M/C" stands for in the output of `rake stats`.

For those of you at home who have never run `rake stats`, here's a sample output:

```
$ rake stats
+----------------------+-------+-------+---------+---------+-----+-------+
| Name                 | Lines |   LOC | Classes | Methods | M/C | LOC/M |
+----------------------+-------+-------+---------+---------+-----+-------+
| Controllers          |   207 |   156 |       6 |      29 |   4 |     3 |
| Helpers              |    56 |    52 |       0 |       5 |   0 |     8 |
| Models               |    54 |    39 |       4 |       2 |   0 |    17 |
| Mailers              |    14 |    12 |       2 |       1 |   0 |    10 |
| Javascripts          |    28 |     0 |       0 |       0 |   0 |     0 |
| Libraries            |     0 |     0 |       0 |       0 |   0 |     0 |
| Controller specs     |   313 |   265 |       0 |       0 |   0 |     0 |
| Helper specs         |    45 |     9 |       0 |       0 |   0 |     0 |
| Mailer specs         |    27 |    19 |       1 |       0 |   0 |     0 |
| Model specs          |    18 |    13 |       0 |       0 |   0 |     0 |
+----------------------+-------+-------+---------+---------+-----+-------+
| Total                |   762 |   565 |      13 |      37 |   2 |    13 |
+----------------------+-------+-------+---------+---------+-----+-------+
  Code LOC: 259     Test LOC: 306     Code to Test Ratio: 1:1.2
```

I wasn't able to find anyone's friendly blog post explaining it (or verifying for me what I considered the 'obvious' answer) so I guess it's up to ME to share what I found.

After asking the great and powerful Google in every permutation I could think of including:

```
"what is the "M/C" in rake stats"
"columns in rake stats"
"columns in "rake stats" rails"
"rake stats explained"
"rake stats "M/C" column"
```

I finally ended up asking `"where is the source file of rake tasks in rails?"` which led me through Stack Overflow into the rails/rails repo into a file called [statistics.rake](https://github.com/rails/rails/blob/master/railties/lib/rails/tasks/statistics.rake) which lists the directories rake will scan when running `rake stats`.

That wasn't quite what I needed, but this require statement in the actual stats task at the end of the file `require "rails/code_statistics"` got me the rest of the way to the [code_statistics.rb](https://github.com/rails/rails/blob/master/railties/lib/rails/code_statistics.rb) file where I FOUND the answer I had been seeking in the method `print_line`.

So to end what I'm sure is UNBEARABLE suspense:

YES... it's the obvious answer.  The "M/C" column IS Methods/Classes... they just round all of the fractions to the next lowest integer rather than dealing with floats so even if you have 4.8 it rounds down to 4 which is why the addition in the Total row seems a little off.  (Each row is a calculation that rounds any remainder DOWN.)

So THERE.  Now we know.  I'm sure there will be exuberant rejoicing far and wide.

Perhaps if enough people share this I won't have to bother with Google SEO to get this answer into the top ten results so that the next person who asks will get an answer instead of a longer search.

~AMP
