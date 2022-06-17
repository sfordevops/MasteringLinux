# DAS NAS AND SAN

  - Now that you are familiar with basic of storage in Linux lets learn about external storage.

  - DAS - Direct Attached Storage, external storage is attached directly to the host system tha requires the space.
  - NAS - Network Attached Storage quite similar to NFS server.
  - SAN - Storage Aread Network, this technology uses a fiber channel for providing high-speed storage.

  #### NFS
  
  - NFS - Does not store data in blocks. Instead, it saves data in form of files. It works on service-client model.

  - NFS server maintains an export configuration file at **`/etc/exports`** that defines the clients which should be able to 
  access the directories on the server. **`/etc/exports`** looks like this

    ```
    [~]$ /etc/exports
    /software/repos 10.61.35.201 10.61.35.202 10.61.35.203
    ```

  - To exports all the mounts defined in **`/etc/exports`** use 

    ```
    [~]$ exportfs -a
    ```

  - To manually export a directory use below command

    ```
    [~]$ exportfs -o 10.61.35.201:/software/repos
    ```
  