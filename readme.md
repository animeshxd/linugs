
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

