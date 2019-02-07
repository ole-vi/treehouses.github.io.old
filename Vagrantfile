# -*- mode: ruby -*-
# vi: set ft=ruby :

# The most common configuration options are documented and commented below.
# For a complete reference, please see the online documentation at
# https://docs.vagrantup.com.

Vagrant.configure(2) do |config|

  if Vagrant.has_plugin?("vagrant-vbguest")
    config.vbguest.auto_update = false
  end

  BOX = "ole/stretch64"
  BOX_VERSION = "0.7.3"

  # production VM
  config.vm.define "io" do |io|
    io.vm.box = BOX
    io.vm.box_version = BOX_VERSION

    io.vm.hostname = "io"

    io.vm.provider "virtualbox" do |vb|
      vb.name = "io"
    end

    io.vm.provider "virtualbox" do |vb|
      vb.memory = "666"
    end

    # Port expose for docker inside vagrant (2300:2300 = CouchDB 3100:3100 = App)
    io.vm.network "forwarded_port", guest: 4000, host: 4000, auto_correct: true
    io.vm.network "forwarded_port", guest: 22, host: 2224, host_ip: "0.0.0.0", id: "ssh", auto_correct: true

    # Prevent TTY Errors (copied from laravel/homestead: "homestead.rb" file)... By default this is "bash -l".
    io.ssh.shell = "bash -c 'BASH_ENV=/etc/profile exec bash'"

    io.vm.provision "shell", inline: <<-SHELL
      # docker-compose in install mode ... ?
    SHELL

    # Start docker on every startup
    io.vm.provision "shell", run: "always", inline: <<-SHELL
      docker-compose up -d
    SHELL
  end

end
