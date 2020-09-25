Ansible Role: pki
=================

Creates and manages a public key infrastructure

Certificates and keys are stored on the ansible controller in a configurable folder (var `pki_local_data_dir`). Multiple certificate authorities are separated via the var `pki_name`.

Requirements
------------

* OpenSSL on the ansible controller

Role Variables
--------------

```yaml
# dir that will be used for storage on the ansible controller
pki_local_data_dir: # mandatory
# separates multiple managed certificate authorities
pki_name: main

# settings for private key generation
pki_key_type: ECC
pki_key_curve: secp384r1

# settings for certificate generation
# filename base for generated certificate files
cert_name:
# defaults a common name of the given cert_name
cert_subject:
cert_san: []
```
