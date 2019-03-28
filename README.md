# filebeat_bsd
* Follow the 6.6 contribution instructions and install go 1.11.5 and clone the git repo appropriately
* Checkout the 6.6 branch
* go to vendor/goland.org/x/crypto/blake2b
* Replace the following with the files from this commit https://github.com/harshavardhana/mc/tree/c131e0d6fcf0925069b9ed5288bd348c2701cca6/vendor/golang.org/x/crypto/blake2b :
  1. blake2b.go
  2. blake2bAVX2_amd64.go
  3. blake2bAVX2_amd64.s
  4. blake2b_amd64.go
  5. blake2b_amd64.s
* Update the vendor/vendor.json appropriately
* go to vendor/github.com/elastic/gosigar/sigar_freebsd.go
* add an import for "runtime"
* navigate to beats/filebeat
* build using GNU Make as you normally would "gmake"
