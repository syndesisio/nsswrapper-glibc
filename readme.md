NSS Wrapper Installer Image
---

This image intends to `provide` the nss wrapper library and configuration, so that other containers can use.

The problem that it tries to solve is to handle Openshift Arbitrary User Ids as described in [Openshift Enterprise Specific Guidelines](https://docs.openshift.com/enterprise/3.2/creating_images/guidelines.html#openshift-enterprise-specific-guidelines) using composition rather than creating a new image.

The idea is instead of re-wrapping an image into an Openshift in order to add nss wrapper, you use this image as an init container that provides binaries and configuration to the container of interest.
