# Yarn 

Kill all running jobs on the cluster.
```bash 
for x in $(yarn application -list -appStates RUNNING | awk 'NR > 2 { print $1 }'); do yarn application -kill $x; done
```
