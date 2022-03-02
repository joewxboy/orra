# Converting the EdgeX Foundry, Ireland Release

## Create and publish Service Definition Files

### Start with the Docker Compose file



### Create dependency map

![ireland-service-dependency-map.png]

### Validate and publish Service Definition files



## Create and publish Deployment Policy file

hzn exchange service publish -P -f device-rest.json

hzn exchange service addpolicy --json-file=service.policy.json myorg/intel.edgex-device-rest_1.1.1_amd64

hzn exchange service listpolicy myorg/intel.edgex-device-rest_1.1.1_amd64

hzn exchange deployment addpolicy -f deployment.policy.json myorg/policy-intel.edgex-device-rest_1.1.1

hzn exchange deployment listpolicy myorg/policy-intel.edgex-device-rest_1.1.1

hzn register --policy ../node.policy

watch hzn agreement list

"2021-06-25 18:52:24:   Error starting containers: API error (400): create ./res/device-rest-go/: \"./res/device-rest-go/\" includes invalid characters for a local volume name, only \"[a-zA-Z0-9][a-zA-Z0-9_.-]\" are allowed. If you intended to pass a host directory, use absolute path"

hzn service log -f intel.edgex-device-rest

hzn eventlog list

hzn exchange node addpolicy --json-file=../node.policy node1

### Test the policy to see if it matches the node policy



## Watch Agreement being formed and debug if it doesn't



