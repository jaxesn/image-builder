# EKS-D instructions
  1. make deps-ami
  2. make build-ami-amazon-2

### New Commits
  1. change to cni tar extension, upstream assumes .tgz eks-d is .tar.gz. goss script assumes image has no prefix, eks-d images have eks-distro/kubernetes in the name.  *Look for ways to upstream a change to support both of these*
  2. ami visibility setup
  3. eks-d 1.19.6 support

  If we could upstream a change for commit #1, our build process could be as simple as cloning upstream and applying our json config for the given version/ami visibilty. 


# Image Builder for Cluster API

The Image Builder can be used to build images intended for use with Kubernetes [CAPI](https://cluster-api.sigs.k8s.io/) providers. Each provider has its own format of images that it can work with. For example, AWS instances use AMIs, and vSphere uses OVAs.

For detailed documentation, see https://image-builder.sigs.k8s.io/capi/capi.html.
