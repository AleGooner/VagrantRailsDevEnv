Vagrantfile and Puppet Provisions for a Rails Development Environment on Ubuntu
=================================================

A virtual Rails Development  Environment running on Ubuntu 14.04  (Trusty), configured
using Vagrant and Puppet.

What you get:
    -   Ubuntu Trusty 14.04
    -   Ruby 2.1.1
    -   Rails 4.2.0


In order to get this running on your machine you'll need to install VirtualBox and Vagrant.
Useful links:
Install Virtual Box:
        https://www.virtualbox.org/wiki/Downloads

Install Vagrant:
        http://www.vagrantup.com/downloads.html

Both sites provide instructions and brief tutorials on how to get things running.
Exert  your programming mojo!

Once your machine is set, make a project folder, cd into it and clone this repository.

You should now see this README.md file, a Vagrantfile, a folder named 'myrailsproject', and a folder
named 'provision'. This last folder contains the configuration used by Puppet to build the
Rails environment you'll be using.

Next, vagrant up and wait for Vagrant to configure your environment. Once Vagrant is done,
log into your freshly configured virtual machine using 'vagrant ssh'.

Next, check everything is installed as expected.
For example, do:  'ruby -v'

You should get  'ruby 2.1.5p273 (2014-11-13 revision 48405) [x86_64-linux-gnu]', since
this is what we provided in the corresponding Vagrantfile.

Inside your environment, you'll find a folder named 'myrailsprojects'. This is the synced folder and you
should place here all your rails app. There's  a demo rails app named 'toy_app' within 'myrailsprojects'.
You can erased this app or play around with it. If you decide to use this skeleton app, remember to run
'bundle install' first.

To start a  rails server from your current terminal (remember this is your virtual environment), use:
'rails s -b 0.0.0.0'. On you browser go then to localhost:3030 to see your app running.

