

## how to use JQ to retrieve pod information for all pods defined under given namespace:
Assume that you have multiple Pods running under namespace of "dev" and you want to quickly get all pods' name, spec image and actually running image, you can pipe json output to jq to query:

kubectl -n dev get pod -ojson | jq '.items[].metadata.name, .items[].spec.containers[].image, .items[].containerStatuses[].image'



