Vagrant.configure(2) do |config|

  config.vm.box_url = 'http://software.apidb.org/vagrant/webdev.json'
  config.vm.box = 'ebrc/webdev'

  config.ssh.forward_agent = true

  config.vm.hostname = 'webdev.vm.apidb.org'

  config.vm.provider "virtualbox" do |v|
    v.memory = 4096
  end

  config.vm.network 'private_network', type: 'dhcp'
  config.vm.synced_folder '.', '/vagrant', type: 'nfs'

  if Vagrant.has_plugin?('landrush')
    config.landrush.enabled = true
    config.landrush.tld = 'vm.apidb.org'
  end

end
