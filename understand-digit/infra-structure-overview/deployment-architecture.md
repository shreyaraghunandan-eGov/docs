---
description: >-
  How DIGIT deployment is architected. What it takes to deploy in a sample cloud
  Azure. What are the various activities in sequence of action to provision
  required infra and deploy DIGIT
---

# Deployment Architecture

### High level action to deploy DIGIT

1. [Provisioning the kubernetes Cluster](https://medium.com/better-programming/build-your-own-multi-node-kubernetes-cluster-with-monitoring-346a7e2ef6e2) in any of the 
   1. [Commercial cloud](https://learn.hashicorp.com/terraform?track=kubernetes#kubernetes) or 
   2. [Private State datacenter](https://medium.com/faun/10-useful-kubernetes-tools-ddffa62089cc) \(SDC\) or 
   3. [National Cloud](https://cloud.gov.in/services.php) \(NIC\)
2. Setting up the [persistent disk volumes](https://medium.com/asl19-developers/create-readwritemany-persistentvolumeclaims-on-your-kubernetes-cluster-3a8db51f98e3) to attach to DIGIT backbone [stateful containers](https://medium.com/swlh/stupid-simple-kubernetes-persistent-volumes-explained-by-examples-29f8fec08c4) like
   1. ZooKeeper
   2. Kafka
   3. Elastic Search 
3. Setting up the PostGres DB
4. Preparing Deployment configuration for required DIGIT services using [Helm](https://medium.com/better-programming/docker-kubernetes-and-helm-4b5a5a87bc8f) Templates from the [InfraOps](https://github.com/egovernments/Train-InfraOps) like the following
   1. K8s Secrets
   2. K8s ConfigMaps
   3. Environment variables of each microservices
   4. Preparing DIGIT Service [helm templates](https://medium.com/ingeniouslysimple/deploying-kubernetes-applications-with-helm-81c9c931f9d3) to deploy on kubernetes cluster
5. Setting up Jenkins Job to build, bake images and deploy the components for the rolling updates.
6. Setup [Application monitoring](https://medium.com/@Alibaba_Cloud/system-monitoring-using-prometheus-and-grafana-8007d3aaf400), [Distributed Tracing](https://medium.com/velotio-perspectives/a-comprehensive-tutorial-to-implementing-opentracing-with-jaeger-a01752e1a8ce), [Alert management](https://medium.com/@abhishekbhardwaj510/alertmanager-integration-in-prometheus-197e03bfabdf) 

