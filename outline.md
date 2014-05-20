# Modular Architecture in JS

## We have a problem with fanaticism in JS

* We become so invested in one framework, set of tools, and try to use it for everything
  * "When you have a hammer, everything's a nail."
* This is preventing us from building the best software possible
  * We're limiting ourselves to the solutions provided to us via our chose over-arching system

## Modular Architecture in JS

* Build you applications piece by piece, looking at each task and selecting the right tool to complete the task
  * We need to stop asking "How is [X] like [my favorite]" and ask "How does [X] help me build better JS applications?"
* Be passionate, but not fanatic, about the tools you use
  * Be excited, and spread knowledge, but keep new approaches in mind.
* Avoid 'developer truisms' - using a tool because 'that's just what you use'
  * Example: using JQuery all the time
    * If you aren't supporting older browsers, maybe you don't need jquery
    * If you're using it for animations, perhaps CSS?
* I'm not saying don't use a framework, but:
  * Be aware of what your framework is really bringing to your application
    * Is it bringing extra stuff in?
    * Does it allow you to bring in the tools you need easily? Or only if it's written with the framework in mind?
    * How much work do you need to put in to learn the framework? How much work will your new devs have to put in to get started?
  * Consider frameworks that fit the definition of the word: "essential supporting structure."

## Module-based systems cause spaghetti code

Argument: "If I make a module-based system, I'll have spaghetti code tying them together, and my app will become an unmaintainable mess. My framework prevents this by having a plugin system."

Example of fanaticism: At a place I worked, when we approached a project, we picked a framework first. When I asked why, I was told "So we know what to build around, and don't just write code willy-nilly." Because apparently we can't write code as a team without being told exactly how to do it.

Counter-point:

* Keep your business logic separate from your module choices
  * Abstraction layers, functional mixins
    * Abstraction layers mean you can swap out modules by editing that layer once instead of every instance of use.
      * Example of an abstraction layer: Primus
    * Functional mixins means you can augment your own modules with third-party code, without creating a direct dependency.
      * Show an example of functional mixins (either find, or write)
  * These techniques allow you to swap out modules without breaking your own code.
* I'm not saying don't use a framework. I'm saying pick your framework carefully
  * There are frameworks that encourage modular systems while providing a common system
    * Flight, Backbone - client-side
    * Restify, Flatiron - server-side
* Testing is easier with module-base architectures
  * When you create an abstraction layer, with a stable API, you write tests once.
  * When you swap modules, just make sure the tests still pass.

## My framework does everything I need. Why would I want to find a bunch of modules to replicate what my framework does?

Argument: "When i use a framework, I have everything I need. I can get things done quickly this way, while modular development would take forever."

Example of fanaticism: I gave a talk about Flight, and three Ember fans walked up to me saying they re-wrote my example in <10 mins, proving...what, exactly?

Counter-point:

* Frameworks often require a lot of buy-in
  * This can leave new developers in the cold for a long time
* What if you want/need to bring third-party code into your framework-based app?
  * You sometimes have to fight the framework to do this
  * Especially if the task is considered a core feature
    * 'Magic' in frameworks gets in the way here a LOT.
* When you develop modularly, you can pick each tool and bring it in easily
  * With frameworks, sometimes you have to sacrifice on some tasks in order to get the parts of the framework you think you wanted.

## Third-party module management is a nightmare, my framework does this for me.

Argument: "I don't want to have to deal with module upgrades, depracation, and this approach means I'll have to track dozens of modules."

Example of fanaticism: "We need to use a framework because we don't want to keep track of libraries all over the place"

Counter-point:

* We have the technology:
  * npm/bower: manage package versions, install pacakages, keep dependency versions locked down
  * require/browserify: get the modules into your app, optimize bundled code
  * Build tools like grunt/gulp: automate build tasks, installation tasks, etc.
  * CI tools like TravisCI: notified when modules update/deprecate, keep track of module stability/tests
* These tools, and others like them, have solved these problems.
* In fact, in a module-based system, you can easily include, and keep up-to-date, all the modules you need, while removing the ones you don't.

## Conclusion

### We need to put down our fanaticism

* Be excited, not fanatic, about your tools. Keep an open mind.
* You should be skeptical of a framework that requires a ton of buy-in
* You should look at each task you need to accomplish, and find the correct module to do so.
* If you use a framework, use it judiciously- consider what it does to help you, and ways it may hinder you.

### modular architectures make your app cleaner, more maintainable, and easier to dive into

* Abstractions create a common language/way of doing things
* Everything you need, nothing you don't
* Modules with good APIs == easier, less brittle testing.

### Because developer hapiness is contagious.

### Contact me, questions slide
