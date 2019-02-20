# Istio - Cleanup

* Remove the Bookinfo application and clean it up (delete the routing rules
  and terminate the application pods):

```bash
# Clean everything - remove port-forward, Bookinfo application, all Istio VirtualServices, Gateways, DestinationRules
killall kubectl siege
sed -i "/read NAMESPACE/d" ./samples/bookinfo/platform/kube/cleanup.sh
./samples/bookinfo/platform/kube/cleanup.sh
```