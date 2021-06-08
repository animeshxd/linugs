
```bash
Error on LinuxOne: This usually is caused by a system where /tmp is mounted noexec. Please remount without noexec and run the upgrade again.
```  
  - solution
    ```bash
    sudo mount -o remount,exec /tmp
    ```
### failed to install lxml
```bash
Building lxml version 4.6.3.
    Building without Cython.
    Error: Please make sure the libxml2 and libxslt development packages are installed.
```
- solution
   ```bash
   sudo apt-get install libxml2-dev libxslt1-dev cython3
   ```

### Failed to upgrade

```bash
Setting up systemd-timesyncd (245.4-4ubuntu3.6) ...
adduser: The user `systemd-timesync' already exists, but is not a system user. Exiting.
dpkg: error processing package systemd-timesyncd (--configure):
 installed systemd-timesyncd package post-installation script subprocess returned error exit status 1
Processing triggers for libc-bin (2.31-0ubuntu9.2) ...
Errors were encountered while processing:
 systemd-timesyncd
E: Sub-process /usr/bin/dpkg returned an error code (1)
```
- solution  
  ```bash
  sudo userdel systemd-timesync -f
  ```
  
