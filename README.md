# godigo

Start or stop machine session

# Dependency

## [machine_time_client](http://devel.misasa.okayama-u.ac.jp/gitlab/gems/machine_time_client/tree/master "follow instruction")

# Installation

Add this line to your application's Gemfile:

    gem 'godigo'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem source -a http://dream.misasa.okayama-u.ac.jp/rubygems
    $ gem install godigo

# Commands

Commands are summarized as:

| command              | description                                                         | note                |
|----------------------|---------------------------------------------------------------------|---------------------|
| godigo-session       | Start, stop, or sync machine session                                |                     |
| godigo-session-start | Start a machine session                                             |                     |
| godigo-session-stop  | Stop a machine session                                              |                     |
| godigo-session-sync  | Sync a machine session                                              |                     |

# Usage

See online document with option `--help`.

# Developer's guide

1. This project is hosted in the Git server ( http://devel.misasa.okayama-u.ac.jp/gitlab/gems/godigo/tree/master ).

2. Run test.

    $ cd ~/devel-godigo/gems/godigo
    $ bundle exec rspec spec/godigo/commands/session_command_spec.rb --tag show_help:true

3. Push to the Git server.

4. Access the Jenkins server ( http://devel.misasa.okayama-u.ac.jp/jenkins/job/Godigo/ ), login,
   and run a job.  This is scheduled and if you are not in hurry, skip
   this and the next step.

5. Update DREAM's homepage to have the newest gem available.

    $ ssh falcon@dream.misasa.okayama-u.ac.jp
    dream$ cd public_html/dream/documentation
    dream$ git pull

6. Uninstall and install gem module locally by following command.

    $ sudo gem uninstall godigo
    $ sudo gem install godigo

# Contributing

1. Fork it ( https://github.com/[my-github-username]/godigo/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
