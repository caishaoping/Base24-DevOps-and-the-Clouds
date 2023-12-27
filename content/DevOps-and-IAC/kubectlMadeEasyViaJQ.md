

## how to use JQ to retrieve pod information for all pods defined under given namespace:
Assume that you have multiple Pods running under namespace of "dev" and you want to quickly get all pods' name, spec image and actually running image, you can pipe json output to jq to query:

kubectl -n dev get pod -ojson | jq '.items[].metadata.name, .items[].spec.containers[].image, .items[].containerStatuses[].image'

## how to use JQ to retrieve raw data info (without enclosed dobuble quotoes):
To get certificate for one csr:
kubectl -n default get csr csr1 -ojson | jq -r '.status.certificate'

To get certificates for multiple csrs:
kubectl -n default get csr -ojson | jq -r '.items[].status.certificate'

controlplane $ k get csr -ojson | jq -r '.items[].status.certificate'
LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSURCVENDQWUyZ0F3SUJBZ0lSQU03dXR1dzNLd2dWR1dXd2w3THpQS0V3RFFZSktvWklodmNOQVFFTEJRQXcKRlRFVE1CRUdBMVVFQXhNS2EzVmlaWEp1WlhSbGN6QWVGdzB5TXpFeU1qY3hOVE00TlRoYUZ3MHlNekV5TWpneApOVE00TlRoYU1COHhIVEFiQmdOVkJBTU1GRFl3TURrNVFHbHVkR1Z5Ym1Gc0xuVnpaWEp6TUlJQkl
.
.
.
aWG1wCi0tLS0tRU5EIENFUlRJRklDQVRFLS0tLS0K
controlplane $ 
controlplane $ 
controlplane $ 
controlplane $ k get csr -ojson | jq '.items[].status.certificate'
"LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSURCVENDQWUyZ0F3SUJBZ0lSQU03dXR1dzNLd2dWR1dXd2w3THpQS0V3RFFZSktvWklodmNOQVFFTEJRQXcKRlRFVE1CRUdBMVVFQXhNS2EzVmlaWEp1WlhSbGN6QWVGdzB5TXpFeU1qY3hOVE00TlRoYUZ3MHlNekV5TWpneApOVE00TlRoYU1COHhIVEFiQmdOVkJBTU1GRFl3TURrNVFHbHVkR1Z5Ym1Gc0xuVnpaWEp6TUlJQk
.
.
.
haWG1wCi0tLS0tRU5EIENFUlRJRklDQVRFLS0tLS0K"





