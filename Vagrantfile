# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.ssh.forward_agent = true

  config.vm.provider "virtualbox" do |vb|
    vb.gui = false
    vb.memory = "1024"
  end

  # Forward default port where livereload listens
  config.vm.network "forwarded_port", guest: 35729, host: 35729

  # Install ruby, ruby-dev and bundler
  config.vm.provision :shell, inline: <<-EOF
    apt-get update
    apt-get install -y git curl zlib1g-dev build-essential libssl-dev libreadline-dev libyaml-dev libxml2-dev libxslt1-dev libcurl4-openssl-dev python-software-properties libffi-dev
    apt-add-repository -y ppa:brightbox/ruby-ng
    apt-get update
    apt-get install -y ruby2.2 ruby2.2-dev bundler
  EOF
end
