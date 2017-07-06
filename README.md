#### Intro
**DEPRECATED**

I have rewrote this and have a better bosh release to manage certs, auto renewal with letsencrypt and use credhub for storing cert (here)[https://github.com/govau/nginx-tlsconfig-release].
_____

This release should be used together with the [nginx-release](https://github.com/cloudfoundry-community/nginx-release).
This release add 1 additional job which populate multiple  certificates and configuration files for each server block in nginx.
Using this approach we can leverage credhub to store our cert and keys securely

```
git clone https://github.com/santrancisco/nginx-multi-cert-release.git
bosh2 create-release --tarball=release.tgz
bosh2 -e vbox upload-release release.tgz
```

Check out example code to see how you may use this to add multiple certs and keys to your bosh nginx release.
