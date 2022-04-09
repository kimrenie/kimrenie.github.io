---
layout: post
title:  "S7. Modularization"
date:   2022-04-09 01:00:00 -0700
categories: senior design
---
<html><head><link rel="stylesheet" type="text/css" href="/../style2.css"></head><style>img {width: 75%}</style></html>

# Modularization

Modularization is used in programming in order to separate a program into smaller sub-sections. This is useful because more often than not, multi-line code can be arduous and difficult to navigate through. The management of this code can also become too complicated to sift through and edit if a problem with the code were to arise. When we are able to break down multiple lines of code into smaller forms of ingestible files, we are able to fully organize our maintenance and management of that program. 

> Another advantage to modularizing your code is the ability to separate code that only serve a specific function away from the main code that is doing the majority of our operations. Being able to separate these sub-functions into a reusable module allows a developer to maintain clean code.

In Terraform, the usage of these modules can be seen through the usage of a particular folder structure:

```
Terraform
    - modules
        - example
            - main.tf
            - input.tf
            - output.tf
            - resources.tf
    - main.tf
```

As seen above, our specific "example module folder" contains multiple terraform files within it. The most common miles used within our module are going to be input, output, and variables. Our input.tf file would serve to accept the value that come in from the main.tf file and take them is as variables. Our output.tf file would serve to return results back out to the main.tf file that originally made the request. Our resources.tf file would serve to define any objets that the module would need to utilize during this process. These terms can of course be change around to suit a particular project but this structure of having would still remain the same. 

> A main file will serve to handle major tasks within a module such as initilizing variables and specifying subnet ranges. Another file would cantain the varaibles that the main file needs to reference. A final file would handle exporting values back out to main. 


# References

[https://learn.hashicorp.com/tutorials/terraform/module](https://learn.hashicorp.com/tutorials/terraform/module)

[https://learn.hashicorp.com/tutorials/terraform/module-create](https://learn.hashicorp.com/tutorials/terraform/module-create)

[https://www.terraform.io/language/modules/develop](https://www.terraform.io/language/modules/develop )

[https://www.freecodecamp.org/news/terraform-modules-explained/](https://www.freecodecamp.org/news/terraform-modules-explained/)