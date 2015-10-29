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
*. chmod 600 prod_key

*. Create deploy key locally
*. pg_dump -C lwd | ssh -i ./prod_key -C  deployer@159.203.243.23 "psql lwd"

6. pip install ansible
6a. Update group_vars/all
6b. Update hosts 
7. Run deploy_prod.sh


Notes:

ssh -i ./prod_key deployer@
