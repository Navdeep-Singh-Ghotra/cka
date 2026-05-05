get podIp 
`k get po -o wide | grep -v Name| awk '{print $1,$6}'`

jump into debug po

k run tmp --rm -it --image=busybox -- sh

