# VPC---Networking



# Creating a VPC

Steps

1. select vpc from aws services
    
    A. ensure region is ireland

2. create vpc from vpc menu not wizard
    
    A. tag = ' Easier to remember name '
    
    B. Ipv4 CIDR block = ' IP Address you want here '
   
    C. leave everything else >> create vpc

3. create internet gateway
    
    A. click on internet gateway - create
    
    B. tag = ' Easier to remember name '
    
    C. attach to vpc
   
    D. select yours, attach gateway

4. create public subnet

    A. click on subnets - create subnet
    
    B. tag = ' Easier to remember name '
   
    C. select your vpc
    
    D. ' IP Address you want here ' in IPv4 block
    
    E. create

5. create private subnet
    
    A. click on subnets - create subnet
    
    B. tag = ' Easier to remember name '
    
    C. select your vpc
    
    D. ip = ' IP Address you want here ', create

6.create route table
    A. check route table not assoicated with VPC already
    
    - want to build in rigidity to limit damage from lack of understanding junior member might do
    
    - make clear connecting to internet
    
    - want to default to private
    
    - keep for now
    
    - rename
   
    B. Select route tables, create route table
    
    C. Add tag =' Easier to remember name '
    
    D. select your vpc
    
    E. create vpc
   
    F. Edit Route - add 0.0.0.0/0
        
        - target = internet gateway, choose your internet gateway
    
    G. Subnet associations
        
        - edit subnet associations
        
        - add public subnet

7. Security group
    
    egress rules
    
    default 0.0.0.0/0 auto set
    
    allows everything to exit
        
    ingress rules (rules for entry)
    
        webapp needs

            nacls for public
            
                by default outbound traffic is denie	
                
                is stateless?
                
                rule numbers matter
                
                can deny IP as well as allow
                    
                    
            ingress rules 
            
                port 22 from our IP
                
                80 for inter
                
                443
                
                ephemeral on 0.0.0.0/0
                
                27017 to allow connection to private (db) subnet
                
            
            egress rules
            
                allow all for now
            
                rules for public server
                
                allow all outbound traffic to public server (' IP Address you want here ')xc
            
            ingress 27017 from public server (' IP Address you want here ')
            
                A. create new nacl
                
                B. tag = ' Easier to remember name '
                
                C. add rules
