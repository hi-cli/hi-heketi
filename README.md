# Heketi hi-cli module

## Installation guide:

### 1. Install [hi-cli](https://github.com/hi-cli/hi-cli)

### 2. Install heketi module

```bash
hi package install heketi
```

### 3. Usage

```bash
hi heketi help

usages:

create pv, volume size 10G:
  hi heketi create pv size=10
create pv, volume size 8G, then create pvc, name my-pvc-name, uid is 27, the uid is the user id of targe
t pod
  hi heketi create pv size=8 pvc name=my-pvc-name uid=27
delete pv, name my-pv-name, (run oc get pv to query pv name)
  hi heketi delete pv name=my-pv-name
delete pv and pvc, pvc name is my-pvc-name
  hi heketi delete pvc name=my-pvc-name
exec command line inside glusterfs by specify pv name
  hi heketi exec pv name=my-pvc-name cmd='ls -l {}'
  (NOTES: above example exec the ls -l command, {} is the pv )

```