## how to find out more info if kube-apiserver is not coming up after changes

kube-apiserver is static pod
where is kube-apiserver's pod definition:  it is on controlpanel node's  /etc/kubernetes/manifests/kube-apiserver.yaml
syslog location:  /var/log/syslog
pod log location: /var/log/pods/kube*api*/*api*/*.log
container log location: /var/log/containers/kube-apiserver*.log
Tools to check: 
watch crictl ps   or crictl ps
crictl logs





