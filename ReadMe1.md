# VPC---Networking



# Creating a VPC

Check you region is Ireland

Go to the main AWS Services webpage, and type in VPC it should pop up

Click on Your VPCs

Click Create VPC 

    Enter a Name that stands out 
    
    Enter a CIDR Block " 000.000.000.000/0" = This is the format you want it in, depending on how many Octets you use the number after the slash will be: 8-16-24-32
    
    Enter No for IPv6 
    
    Tenancy is default
    
Click create and your VPC is created!
\
# Create a internet gateway

Navigate to the VPC area within AWS

On the left sidebar, scroll down till you find internet gateway and click it 

Once inside, click create internet gateway 
    
    Enter a Name that stands out 

Click next and you have now created a Internet gateway!

Click on your gateway, navigate to the actions and click attach to VPC 
    
    Attach to the VPC you created earlier - Just type the name in 

You have now attached your Internet gateway to your VPC!
\
# Creating Subnets - Private and Public 

Navigate to the VPC area within AWS

On the left sidebar, scroll down till you find Subnets and click it 

We will begin with a Private Subnet first 

Once in, click create Subnet 
    
    Enter a Name that stands out, as your Private Subnet
    
    Attach your VPC 
    
    Availability zone is left as - No Preference
    
    Ipv4 CIDR block - needs to be same as the VPC id with the 3rd octet being different - with the addition of the 3rd octet the / will be 24 as we are using 3 octets
    
You have now created a Private subnet! 
\
\
Now the Public one!

Once in, click create Subnet 
    
    Enter a Name that stands out, as your Public Subnet
    
    Attach your VPC 
    
    Availability zone is left as - No Preference
    
    Ipv4 CIDR block - needs to be same as the VPC id with the 3rd octet being different - with the addition of the 3rd octet the / will be 24 as we are using 3 octets - 
    add 1 to the Private one you made earlier as it will be easier for you to read and understand!
    
You have Now Created a Private and Public Subnet!

# Creating Route Tables
Navigate to the VPC area within AWS

On the left sidebar, scroll down till you find Route Tables and click it 

We will begin with a Public Route Table first 

Click on Create Route Table 

    Enter a Name that stands out
    
    Attach your VPC 
    
    Add a Tag - Key is Name - Value is the Name you created 
    
Click Create, You have now have a Public Route Table!
\
\
You will see that you now have a blank name Route table, this will be your Private Route Table
    
    Add a Name that stands out

You have now have a Private Route Table!   

\
\
Now to add routes to your Public Route Table
    
    Look at the splash box below
    
    Click on Routes 