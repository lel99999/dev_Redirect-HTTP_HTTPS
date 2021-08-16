# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"
#Check if you have the good Vagrant version to use docker provider...
#Vagrant.require_version ">= 1.6.0"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  ENV['VAGRANT_DEFAULT_PROVIDER'] = 'docker'

  config.vm.provider "docker" do |d|
    d.build_dir = "."
    d.has_ssh = true
  end
  config.ssh.port = 22

end


#Vagrant.configure("2") do |config|
#  config.vm.provider "virtualbox" do |v|
#    v.memory = "1024"
#    v.cpus = 2
#    v.customize ["modifyvm", :id, "--cpuexecutioncap", "70"]
#  end
## config.trigger.after :up do |trigger|
##   run "subscription-manager register --username <username> --password <password> --auto-attach
##   trigger.name = "After-Up Trigger ..."
##   trigger.info = "Trigger Execution ..."
##   trigger.run = { path:"subscription-manager register --username <username> --password <password> --auto-attach"}
## end
#
#  config.vm.define "jupyterRH7" do |jupyterRH7|
##   jupyterRH7.vm.box = "generic/rhel7"
#    jupyterRH7.vm.box = "clouddood/RH7.5_baserepo"
#    jupyterRH7.vm.hostname = "jupyterRH7"
#    jupyterRH7.vm.network "private_network", ip: "192.168.60.141"
#    jupyterRH7.vm.provision "shell", :inline => "sudo echo '192.168.60.141 jupyterRH7.local jupyterRH7' >> /etc/hosts"
#    jupyterRH7.vm.provision "ansible" do |ansible|
#      ansible.playbook = "deploy_jupyterRH7_DEV.local.yml"
##     ansible.playbook = "deploy_jupyterRH7.yml"
#      ansible.inventory_path = "vagrant_hosts"
#      #ansible.tags = ansible_tags
#      #ansible.verbose = ansible_verbosity
#      #ansible.extra_vars = ansible_extra_vars
#      #ansible.limit = ansible_limit
#    end
#  end
## config.trigger.before :destroy do |trigger|
##   run "rm -Rf /tmp/abc/*"
#    # subscription-manager remove --all
#    # subscription-manager unregister
#    # subscription-manager clean
##   trigger.name = "Destroy Trigger ..."
##   trigger.info = "Destroy Trigger Execution ..."
##   trigger.run = { path: "subscription-manager remove --all"}
##   trigger.run = { path: "subscription-manager unregister"}
##   trigger.run = { path: "subscription-manager clean"}
## end
#end
