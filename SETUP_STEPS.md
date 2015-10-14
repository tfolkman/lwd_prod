1. Get VPS
    a. change root password
2. Create prod keys
    a. ssh-keygen -t rsa -b 2048
    b. cp prod_key.pub authorized_keys
3. Use Fabric to setup Server
    a. Modify inputs in code
4. Create virtual environment
    a. pip install fabric==1.10.2
5. Run fabric code
    a. fab bootstrap