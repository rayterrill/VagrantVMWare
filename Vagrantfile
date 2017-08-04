Vagrant.configure("2") do |config|
  config.vm.box = 'dummyVSphere'
  config.vm.box_url = '.\dummyVSphere.box'
  
  #looks like this is required because the rsync functionality is currently broken
  config.vm.synced_folder '.', '/vagrant', disabled: true

  config.vm.provider :vsphere do |vsphere|
    vsphere.host = 'VSPHERE_HOST'
    vsphere.data_center_name = 'DATACENTER'
    vsphere.compute_resource_name = 'CLUSTER_OR_VMHOST'
    vsphere.template_name = 'VagrantTemplate1'
    vsphere.name = 'VAGRANT1'
    vsphere.user = 'YOUR_USERNAME'
    vsphere.password = :ask
    vsphere.insecure = true
  end
  
  # winrm config
  config.vm.communicator = "winrm"
  config.winrm.username = "vagrant"
  config.winrm.password = "vagrant"
end