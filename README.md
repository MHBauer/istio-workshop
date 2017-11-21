## Workshop Setup
- [Exercise 1 - Access Kubernetes cluster](exercise-1/README.md)

## Exploring Kubernetes

- [Exercise 2 - Deploying a microservice to Kubernetes](exercise-2/README.md)
- [Exercise 3 - Creating a Kubernetes Service](exercise-3/README.md)
- [Exercise 4 - Scaling In and Out](exercise-4/README.md)

## Creating a Service Mesh with Istio

- [Exercise 5 - Installing Istio](exercise-5/README.md)
- [Exercise 6 - Creating a Service Mesh with Istio Proxy](exercise-6/README.md)
- [Exercise 7 - Istio Ingress Controller](exercise-7/README.md)
- [Exercise 8 - Telemetry](exercise-8/README.md)
- [Exercise 9 - Request Routing and Canary Deployments](exercise-9/README.md)
- [Exercise 10 - Fault Injection and Rate Limiting](exercise-10/README.md)


## Credits
These workshop exercises are built with the help from a number of amazing Kubernetes and Istio Experts from Google and Grand Cloud.

#### Ray Tsang  [@saturnism](https://twitter.com/saturnism)
The Kubernetes and Istio Exercises are dervied from the work of Ray Tsang  [@saturnism](https://twitter.com/saturnism) and these repositories:

[https://github.com/saturnism/spring-boot-docker](https://github.com/saturnism/spring-boot-docker)

[https://github.com/saturnism/istio-by-example-java](https://github.com/saturnism/istio-by-example-java)

#### Zach Butcher [@ZachButcher](https://twitter.com/ZackButcher)
Zach was insturmental in helping write the Istio tutorials.

####  Kelsey Hightower [@kelseyhightower](https://twitter.com/kelseyhightower)
The Istio Ingress Tutorial is largely based on the work of Kelsey and this repository:

[https://github.com/kelseyhightower/istio-ingress-tutorial](https://github.com/kelseyhightower/istio-ingress-tutorial)

Kelsey's tutorial uses more advance features of Kubernetes to taint some of the nodes so that the ingress controller runs on dedicated nodes.  The ingress controller is then deployed as a daemonset.
