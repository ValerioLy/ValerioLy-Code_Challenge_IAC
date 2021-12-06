Vagrant.configure("2") do |config|
  config.vm.box = "generic/centos8" 
  config.ssh.forward_agent = true

  N = 2
  (1..N).each do |machine_id|
    config.vm.define "server#{machine_id}" do |machine|
      machine.vm.hostname = "server#{machine_id}"
      machine.vm.network "private_network", ip: "192.168.0.#{104+machine_id}"
  

      if machine_id == N
        machine.vm.provision :ansible do |ansible|
          ansible.limit = "all"
          ansible.playbook = "docker.yml"
        end
      end
    end
 end
end