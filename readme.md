## Terraform Tips and Tricks

[![Check Links](https://github.com/jakewalsh90/Terraform-Tips/actions/workflows/links.yml/badge.svg)](https://github.com/jakewalsh90/Terraform-Tips/actions/workflows/links.yml)

This Repo is all about sharing Tips and Tricks learnt using whilst Terraform. It will contain small examples, samples, snippets, and more. With each tip or trick a code sample is included, along with an explanation, and screenshots if necessary. 

#### ❓ Want to Contribute a Tip or Trick? Please read the guide [here](contributing.md).

<hr>

### List of Tips and Tricks:

1. [Using Count and Length together.](https://github.com/jakewalsh90/Terraform-Tips#1-using-count-and-length-together)

<hr>

#### 1. Using Count and Length together

This example uses Count to create a number of Subnets, and then uses Length within an NSG Association Resource block to apply that NSG to all created Subnets:

![Using Count with Length](https://raw.githubusercontent.com/jakewalsh90/Terraform-Tips/main/Count-and-Length/CountLength.png)

Once you have created the primary resource (using Count), you can then use length(original_resource_name) to create other resources/associations/actions that will be carried out based on the value used within Count. This saves you from using a Count number or variable in multiple locations, so results in cleaner code. A Code example is here: [Count-and-Length.tf](https://github.com/jakewalsh90/Terraform-Tips/blob/main/Count-and-length.tf)