---
layout: post
title: Deep Dive Week In Review
---

My coding mentor instructed me last week to "Dive Deep" while working on my current App. Essentially he wanted me to spend time understanding the whys and hows of all the commands, connections, methods, assets, interactions between components of the MVC, calls to the ORM... Anything I touched I was supposed to deepen my understanding of. I even took notes longhand << with a pen << in a paper notebook for some of these.

The following (non)exhaustive list of what I touched upon (and sometimes snorkeled in) during my Curricular Annotations this past week includes:

* Il8n - Internationalization: [il8n API](http://guides.rubyonrails.org/i18n.html#overview-of-the-i18n-api-features), [il8n Railscast](http://railscasts.com/episodes/138-i18n)
* RESTful Archetecture: [Representational State Transfer](https://en.wikipedia.org/wiki/Representational_state_transfer), [Custom REST actions Railscast](http://railscasts.com/episodes/35-custom-rest-actions)
* HTTP Verbs: [rfc2616 - a friendly version](http://www.w3.org/Protocols/rfc2616/rfc2616-sec9.html)
* [Parameters:](http://guides.rubyonrails.org/action_controller_overview.html#parameters) (String vs. Post & Strong)
* Params Hash/Indifferent Access: [Jocellyn](http://jocellyn.cz/2014/05/03/hash-with-indifferent-access.html), [CodeFolio](http://codefol.io/posts/Deep-Rails-Understanding-HashWithIndifferentAccess-Understanding-the-Params-Hash)
* RAKE and Rakefiles: [Using Rake Build Language](http://martinfowler.com/articles/rake.html), [Erik's](http://erik.debill.org/2011/12/04/rake-for-rails-developers), [On Rake](http://www.jbarnette.com/2009/08/27/on-rake.html), [Custom Rake Tasks RailsCast](http://railscasts.com/episodes/66-custom-rake-tasks), [rakefile](http://ruby-doc.org/core-1.9.3/doc/rake/rakefile_rdoc.html)
* Imperatives, Declaratives, Dependencies
* [Memoization](http://www.justinweiss.com/articles/4-simple-memoization-patterns-in-ruby-and-one-gem/)
* Rails [helper_methods](http://6ftdan.com/allyourdev/2015/01/28/rails-helper-methods/)
* ActiveRecord migrations (how to [generate/name](http://edgeguides.rubyonrails.org/active_record_migrations.html#creating-a-standalone-migration) them so that they pre-populate)
* FactoryGirl Factories (best way to generate test data with table dependencies to test validations): [Dependent Attributes](http://stackoverflow.com/questions/4410854/dependent-attributes-in-factory-girl)
* [Flash and Status codes](http://guides.rubyonrails.org/action_controller_overview.html#the-flash)
* [Rails Layouts and Rendering](http://guides.rubyonrails.org/layouts_and_rendering.html)
* [Rails Resource Routing](http://guides.rubyonrails.org/routing.html)
* Started on [Active Support Core Extensions](http://guides.rubyonrails.org/active_support_core_extensions.html)
* Peeked at [Slim](http://slim-lang.com/) and [Jade](http://naltatis.github.io/jade-syntax-docs/) Templating engines: [FredWu](http://fredwu.me/post/1338899831/slim-a-fast-and-lightweight-rails-template)
* [git commit --amend](https://git-scm.com/docs/git-commit), [Awesome Tutorials](https://www.atlassian.com/git/tutorials/rewriting-history/git-commit--amend/)
* CSS Units for fonts and responsive CSS: [Awesome Dev Tips](https://www.youtube.com/watch?v=qrduUUdxBSY)<sup>1</sup>, [CSS for responsive centered image](http://stackoverflow.com/a/18462893#18462893)
* Even bookmarked another Framework: [Clearwater](http://jgaskins.org/blog/2015/01/17/clearwater-a-front-end-web-framework-in-ruby)

Yeah. The ones without links are still cooking. Suffice it to say I've been drinking from the Firehose this past week. And I have more homework/leads to research more of for the COMING week. No big surprise there, I've still got lots to learn and tons to review. I'm pushing myself to progress as far as I can prior to the start of my Group Project, now slated to kick off come Saturday... 5 days from now.

Caught somewhere between nervous and eager at this point. I should write some test classes to help me determine which way is UP once we get going. But would they be Functional or Unit tests? Functional tests on the GravitationalForcesController?

Something to contemplate.

~AMP

<small> 1. It TRULY pays to read community posts! - Thanks to community-active FHP alumnus Colin Rubbert for the link to that Dev Tips! </small>