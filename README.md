# hello_ceph

`hello_ceph` is a small project that uses Vagrant to create and provision a one node Ceph 'cluster' suitable for development or testing on a local workstation.

### Installation

Clone this repository and its submodules

```
$ git clone --recursive https://github.com/aisrael/hello_ceph.git
```

### Usage

Boot up the Ceph VM

```
$ vagrant up
```

SSH into the Ceph VM

```
$ vagrant ssh
vagrant@hello-ceph:~$
```

Check that Ceph was properly installed

```
vagrant@hello-ceph:~$ sudo ceph -s
    cluster 4a158d27-f750-41d5-9e7f-26ce4c9d2d45
     health HEALTH_OK
     monmap e1: 1 mons at {hello-ceph=192.168.42.100:6789/0}
            election epoch 2, quorum 0 hello-ceph
     mdsmap e5: 1/1/1 up {0=hello-ceph=up:active}
     osdmap e8: 1 osds: 1 up, 1 in
      pgmap v11: 128 pgs, 3 pools, 1962 bytes data, 20 objects
            35296 kB used, 859 MB / 894 MB avail
                 128 active+clean
  client io 896 B/s wr, 3 op/s
```
