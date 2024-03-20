# caprover and issue
Lưu các issue đã từng gặp và đã xử lý được

### 1. Use SSH Key:

- Sử dụng ssh key với caprover và github để CICD
- Theo hướng dẫn:
  - 1. Steps to reproduce the problem:
    Generating new key:
    ```
    ssh-keygen
    ```
  - 2. Copy contents: `cat ~/.ssh/id_rsa`
  - 3. Paste into the SSH key field in CapRover
  - 4. Copy contents of pubkey: `cat ~/.ssh/id_rsa.pub`
  - 5. Add public key to repository deploy key on GitHub.
  - 6. Click save and then force deploy.

- Issue: Sẽ gặp lỗi trả về từ caprover khi build, lỗi báo về quyền của SSH Key public
  ```
  Build started for satis
  Build has failed!
  ----------------------
  Deploy failed!
  Error: Cloning into '/captain/temp/image_raw/satis/6/source_files'...
  Permission denied (publickey).
  fatal: Could not read from remote repository.

  Please make sure you have the correct access rights
  and the repository exists.
  ```

- Xử lý vấn đề: it has to be in PEM format, and ssh-keygen doesn't use that anymore by default
  ```
  ssh-keygen -m PEM -t rsa -b 4096 -C "caprover" -f ./key -q -N ""
  ```
- Link gốc hướng dẫn xử lý lỗi: https://github.com/caprover/caprover/issues/464
