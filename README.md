# Terraform Cloud and Sentinel Policies Demo on Azure


![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>


# Common functions for use with the Azure provider

##### Imports #####
import "tfplan/v2" as tfplan

##### Functions #####

### find_resources_with_standard_tags ###
find_resources_with_standard_tags = func(resource_types) {
  resources = filter tfplan.resource_changes as address, rc {
    rc.provider_name matches "(.*)azurerm$" and
    rc.type in resource_types and
  	rc.mode is "managed" and
  	(rc.change.actions contains "create" or rc.change.actions contains "update" or
     rc.change.actions contains "read" or rc.change.actions contains "no-op")
  }

  return resources
}

![](https://i.imgur.com/waxVImv.png)
# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact Me]
* [Name: Nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)
* [PayPal.me](https://www.paypal.com/paypalme/nholuongut)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟