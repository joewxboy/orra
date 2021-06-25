# Converting the EdgeX Foundry, Ireland Release

## Create and publish Service Definition Files

### Start with the Docker Compose file



### Create dependency map

![ireland-service-dependency-map.png]

### Validate and publish Service Definition files



## Create and publish Deployment Policy file

hzn exchange service publish -P -f device-rest.json

hzn exchange service addpolicy --json-file=deployment.policy.json myorg/intel.edgex-device-rest_1.1.1_amd64

hzn exchange service listpolicy myorg/intel.edgex-device-rest_1.1.1_amd64

hzn exchange node addpolicy --json-file=../node.policy node1

### Test the policy to see if it matches the node policy



## Watch Agreement being formed and debug if it doesn't



