# veewee

## Introduction
Use to create VM images for the following providers:
* VirtualBox - exports to OVF filetype
* VMware (Fusion) - exports to OVA filetype
* KVM - exports to IMG filetype
* Parallels - none yet, but can export to parallels format (provided by vagrant-parallels)

## Install VeeWee on Mac OSX 10.10
```
$ sudo gem install veewee --no-ri --no-rdoc
```
```
$ cd ~/Projects/
$ git clone http://www.ida-gds.com/stash/scm/dev/veewee.git
```

## Install vagrant plugin
https://github.com/jedi4ever/veewee/issues/607
```
$ vagrant plugin install veewee
```

## Create CentOS-7 image for virtualbox
```
$ veewee vbox build 'CentOS-7-x86_64'
```

## Export CentOS-7 image for virtualbox
```
$ veewee vbox export 'CentOS-7-x86_64'
```

## Import CentOS-7 image (box) for virtualbox
```
$ vagrant box add 'CentOS-7-x86_64' '~/Projects/veewee/CentOS-7-x86_64.box'
```

## Use new CentOS-7 image (box) with vagrant and virtualbox
```
$ vagrant init 'CentOS-7-x86_64'
$ vagrant up
$ vagrant ssh
```
