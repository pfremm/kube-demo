###Installation
This will provide steps to install a local development kubernetes environment following the multi-node vagrant directions on [Kubernetes.io](http://kubernetes.io/).  The steps specified in the gist in step 4 only run on a mac.

1. Install Virtualbox [Virtualbox](https://www.virtualbox.org/wiki/Downloads)
2. Install Virtualbox Extensions [Virtualbox Extensions](http://download.virtualbox.org/virtualbox/5.0.18/Oracle_VM_VirtualBox_Extension_Pack-5.0.18-106667.vbox-extpack)
3. Install Vagrant [Virtualbox](https://www.virtualbox.org/wiki/Downloads)
4. In a terminal window run the following command:
```shell
curl -s https://gist.githubusercontent.com/pfremm/28a696b0b23a68730e36ff0476b1a42d/raw/d104d3e7fb897dc7b96e0d4a3d65089bcfc5b673/kubeup.sh > kubeup.sh && bash kubeup.sh
```
5. After Step 4 completes run:
```shell
nohup kubectl proxy --port=9090 &
```
6. Finally run the command below to launch chrome to the appropriate page.
```shell
/usr/bin/open -a "/Applications/Google Chrome.app" 'http://localhost:9090/api/v1/proxy/namespaces/kube-system/services/kubernetes-dashboard'

```
