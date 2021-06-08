
```bash
Error on LinuxOne: This usually is caused by a system where /tmp is mounted noexec. Please remount without noexec and run the upgrade again.
```  
  - solution
    ```bash
    sudo mount -o remount,exec /tmp
    ```
