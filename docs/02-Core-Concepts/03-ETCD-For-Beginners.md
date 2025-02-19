# ETCD for Beginners
  - Take me to the [Video Tutorial](https://kodekloud.com/topic/etcd-for-beginners/)

  In this section, we will take a quick look at introduction to ETCD for beginners. 
  - What is ETCD?
  - What is a Key-Value Store?
  - How to get started quickly with ETCD?
  - How to operate ETCD?
  
 ## What is a ETCD?
     - ETCD is a distributed reliable key-value store that is simple, secure & Fast.
     
## What is a Key-Value Store
   - Traditionally, databases have been in tabular format, you must have heared about SQL or Relational databases. They store data in rows and columns
       
     ![relational-dbs](../../images/relational-dbs.PNG)
     
   - A Key-Value Store stores information in a Key and Value format.
       
     ![key-value](../../images/key-value.PNG)
       
## Install ETCD
  ### Older versions of ETCD use the verb "set" for write operations, while newer versions use "put"
  In the examples below, for the old version use
    ```
    ETCD_VERSION=v3.3.11 
    ```
  and for the new version use
    ```
    ETCD_VERSION=v3.5.2 
    ```
   - Its easy to install and get started with **`ETCD`**.
     - Download the relevant binary for your operating system from github releases page (https://github.com/etcd-io/etcd/releases)
       ```
       For Example: To download ETCD ${ETCD_VERSION}, run the below curl command
         
       $ https://github.com/etcd-io/etcd/releases/download/${ETCD_VERSION}/etcd-${ETCD_VERSION}-linux-amd64.tar.gz
       ```
     - Extract it.
       ```
       $ tar xvzf etcd-${ETCD_VERSION}-linux-amd64.tar.gz 
       ```
     - Run the ETCD Service
       ```
       $ ./etcd
       ```
     - When you start **`ETCD`** it will by default listens on port **`2379`**
      - The default client that comes with **`ETCD`** is the [**`etcdctl`**](https://github.com/etcd-io/etcd/tree/main/etcdctl) client. You can use it to store and retrieve key-value pairs.
        ```
        Syntax: To Store a Key-Value pair
        $ ./etcdctl set key1 value1 # older syntax
        ```
        or
        ```
        $ ./etcdctl put key1 value1 # newer syntax
        ```
        ```
        Syntax: To retrieve the stored data
        $ ./etcdctl get key1
        ```
        ```
        Syntax: To view more commands. Run etcdctl without any arguments
        $ ./etcdctl
        ```
        
        ![etcdctl](../../images/etcdctl.PNG)
        
       K8s Reference Docs:
       - https://kubernetes.io/docs/concepts/overview/components/
       - https://etcd.io/docs/
       - https://kubernetes.io/docs/tasks/administer-cluster/configure-upgrade-etcd/
       
