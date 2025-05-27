# OCI Uploader 🚀

A PHP library for uploading files to Oracle Cloud Infrastructure (OCI) Object Storage.


---

### ❗Required Environment variables

```php
OCI_REGION=us-phoenix-1
OCI_USER=ocid1.user.oc1..aaaaaaaa...
OCI_FINGERPRINT=12:34:56:78:90:ab:cd:ef...
OCI_TENANCY=ocid1.tenancy.oc1..aaaaaaaa...
OCI_NAMESPACE=your-namespace
OCI_BUCKET_NAME=your-bucket
OCI_KEY_FILE=path/to/private_key.pem
```
---
### ℹ️ Installation [🔗 Packagist](https://packagist.org/packages/maxicare/oci-uploader)
```bash
composer require maxicare/oci-uploader
```

---


### 🚀 Usage

```php
<?php

namespace MyLaravelApp;

use Maxicare\Uploader;

public function testUpload() {
    $ociUploader = new Uploader();

    $ociUploader->testConnection(); # Test Connection / Configuration

    $ociUploader->upload(file_get_contents(base_path() . "/.dummy/dog.png"), "dog.png"); # Upload using contents to OCI
    $ociUploader->uploadFile(base_path() . "/.dummy/dog.png") # Upload object to OCI
    $ociUploader->download("dog.png"); # Download
    $ociUploader->delete("dog.png"); # Delete
}

```

### 📝License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).