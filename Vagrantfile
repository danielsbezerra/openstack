Vagrant.configure("2") do |config|

  # Deployment host - Ubuntu 18.04
  config.vm.define "Deployment_host" do |dh|

    dh.vm.box = "ubuntu/trusty64"
    dh.vm.box_version = "20181203.0.1"
    dh.vm.hostname = "deployment"

    dh.vm.network "private_network", ip: '192.168.56.5'

    # Provider setting
    dh.vm.provider "virtualbox" do |vb|
      # Customize the amount of memory on the VM:
      vb.memory = "4096"
      vb.cpus = 4
    end
  end
  # End Deployment host


  # Target host - CentOS
  config.vm.define "Target_host" do |th|

    th.vm.box = "centos/7"
    th.vm.box_version = "1811.02"
    th.vm.hostname = "target"

    th.vm.network "private_network", ip: '192.168.56.6'

    # Provider setting
    th.vm.provider "virtualbox" do |vb|
      # Customize the amount of memory on the VM:
      vb.memory = "4096"
      vb.cpus = 4
    end
  end
  # End Target host

end