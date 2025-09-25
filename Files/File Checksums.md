# File Checksums

### File checksums are cryptographic hashes that provide a unique fingerprint for a file - allowing us to verify the authenticity of a file. Every file has its own unique file checksum.

---

#### Example of generating a file checksum using md5sum command:
```bash
#!/bin/bash

calculate_md5sum() {
  local file_path=$1
  md5sum "$file_path"

}

calculate_md5sum "read.txt"
```
---

#### Example of generating a file checksum using sha256sum
```bash
#!/bin/bash

calculate_sha256sum() {
  local file_path=$1
  sha256sum "$file_path"
}

calculate_sha256sum "read.txt"
```
---

#### Example of comparing of checksums
```bash
compare_checksums() {
  local checksum1=$1
  local checksum2=$2

  if [[ "$checksum1" == "$checksum2" ]]; then
    echo " Checksums match. File is intact."
  else
    echo "Checksums do not match. File integrity is compromised!"
  fi
}

compare_checksums "123" "1234"
```
#### The output is as follows:
- `Checksums do not match. File integrity is compromised.`

