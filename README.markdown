Merb Sequel Stack
=======================

This gem provides a stack of Sequel, Rspec, JQuery, along with Merb-Auth.

To use, install the gem and simply choose 'sequel-app' from the list of merb-gen options:

~/git/merb-sequel-stack (master)$ merb-gen
Usage: merb-gen generator_name [options] [args]

Generate components for your application or entirely new applications.

Available generators
    app                              Generates a new "jump start" Merb application with support for DataMapper,
    ar-app                           This generates a "prepackaged" (or "opinionated") Merb application that uses ActiveRecord,
    controller                       Generates a new controller.
    core                             Generates a new Merb application with Ruby on Rails like structure.
    flat                             Generates a new flat Merb application: all code in one file except for config files and
    helper                           Generates a new helper.
    layout                           Generates a new layout.
    mailer                           Generates a mailer
    merb_story_setup                 Generates setup code for plain text stories
    migration                        Generates a new database migration.
    model                            Generates a new model. You can specify an ORM different from what the rest
    part                             Generates a new part controller.
    plugin                           Generates a new Merb plugin.
    resource                         Generates a new resource.
    resource_controller              Generates a new resource controller.
    sequel-app                       This generates a "prepackaged" (or "opinionated") Merb application that uses Sequel,
....<snip>
  
This generates your app with certain things configured for you to use Sequel. 