Vagrant.configure("2") do |config|
  config.vm.box = "generic/centos8" 

  config.vm.define "server1" do |server1|
    server1.vm.hostname = "server1"
    server1.vm.network "private_network", ip: "192.168.0.105"
    server1.vm.provision :ansible do |ansible|
      ansible.limit = "all"
      ansible.playbook = 'partition.yml'
    end
  end
 # config.vm.define "server2" do |server2|
 #   server2.vm.hostname = "server2"
 #   server2.vm.network "private_network", ip: "192.168.0.106"
 #   server2.vm.provision :ansible do |ansible|
 #     ansible.limit = "all"
 #     ansible.playbook = 'main.yml'
 #   end
 # end
  
end