# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "Deb9OffMag" # Название вирт. машины для обращения через Vagrant
  config.vm.box = "debian/stretch64" # ОС
  config.vm.synced_folder ".", "/Vagrant", disable: true
  config.vm.disk :disk, name: "storage", size: "10GB" #Конф-ия диска 
  config.vm.network "private_network", type: "dhcp" # IP адрес получаем по DHCP
  
  config.vm.provider "virtualbox" do |v| # Конф-ия VM
   v.gui = true
   v.name = "Deb9OffMag" # Имя виртуальной машины
   v.memory = "2048" # Кол-во оперативной памяти
   v.cpus = "2" #Кол-во процессоров
   v.customize ["modifyvm", :id, "--cpuexecutioncap", "70"] # Ограничение нагрузки процессора на вирт. машину
   end
end
