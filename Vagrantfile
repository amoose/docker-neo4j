VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.provision "docker" do |d|
    d.build_image ". --name=neo4j"
  end


  config.vm.define "neo4j" do |v|
    v.vm.provider "docker" do |d|
      d.build_dir = "."
      d.ports = ["7474:7474"]
      d.vagrant_vagrantfile = "./Vagrantfile.proxy"

    end
  end

end
