## Task 1: Find the CIDR range for the Instance Connect service

Choose the following link to open the JSON file that provides the IP address ranges for AWS services.

```
AWS services IP ranges
```

Search the file for the EC2_INSTANCE_CONNECT entries, and stop when you find the entry for the us-east-1 region.

    Hint: You can use either the browser menu or ctrl F (for Mac, use command F) to open the search box.

The entry will be similar to the following example:

     "ip_prefix": "18.206.107.24/29",
       "region": "us-east-1",
       "service": "EC2_INSTANCE_CONNECT",
       "network_border_group": "us-east-1"
     },

Copy the ip_prefix value for the EC2_INSTANCE_CONNECT entry.

![screenshot](./screenshots/ip-range.png)

## Task 2: Allow access from the EC2 Instance Connect service
You must update the security group that is assigned to the Amazon EC2 instance to allow communication with the EC2 Instance Connect service.

In the AWS Management Console on the Services menu, enter 
``````
EC2
``````
From the search results, choose 

    EC2

In the left navigation pane, choose 

    Instances

Select the instance named  

    Lab Server.

In the bottom pane, choose the 

    Security tab

Under Security groups, choose the link for 

    Lab Security Group

Choose the 

    Inbound rules tab

Choose 

    Edit inbound rules

Choose 

    Save rules

    