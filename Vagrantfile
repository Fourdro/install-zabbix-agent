Vagrant.configure("2") do |config|

 #config.vm.box = "ubuntu/trusty64"
config.ssh.insert_key = false
config.vm.synced_folder ".", "/vagrant", disabled: true
config.vm.provider :virtualbox do |v|
v.memory = 512
v.linked_clone = true
end

  # Application server 1. ubuntu 16.04
config.vm.define "app1" do |app|
app.vm.box = "ubuntu/xenial64"
  app.vm.hostname = "app1.test"
  app.vm.network :private_network, ip: "192.168.60.2"
end

  # Application server 2. ubuntu 18.04
config.vm.define "app2" do |app|
app.vm.box = "ubuntu/bionic64"
  app.vm.hostname = "app2.test"
  app.vm.network :private_network, ip: "192.168.60.3"
end

  # Application server 3.ubuntu 20.04
config.vm.define "app3" do |app|
app.vm.box = "ubuntu/focal64"
  app.vm.hostname = "app3.test"
  app.vm.network :private_network, ip: "192.168.60.4"
end

end
