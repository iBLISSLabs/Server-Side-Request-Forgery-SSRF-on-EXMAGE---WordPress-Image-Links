# Server Side Request Forgery (SSRF) in EXMAGE - WordPress Image Links

This PoC describe how to exploit SSRF on EXMAGE - WordPress Image Links version 1.0.3

# Description

The EXMAGE plugin - WordPress Image Links version 1.0.3 does not have protections against SSRF, so it is possible to forge requests to internal services, enumerate services that are not directly exposed and find out what the local IP address of the server in this case

![1](https://user-images.githubusercontent.com/70114276/159179186-ae0cb72c-b725-4ac0-a5a0-ba3fc4103856.png)


## Attack Scenario

Let's say there is a web service that is running locally

![3](https://user-images.githubusercontent.com/70114276/159179198-d4eb6860-c4f9-4b49-959c-209cc4e0d184.png)

After trying to directly access the service, we are not successful

![4](https://user-images.githubusercontent.com/70114276/159179204-0e87a630-2e12-42d5-8da0-6490b37fda93.png)

Then, we can perform an enumeration of this service through the SSRF present in the EXMAGE plugin - WordPress Image Links

![5](https://user-images.githubusercontent.com/70114276/159179223-e99c5622-57cd-44cc-a362-8e036f14eb09.png)

![6](https://user-images.githubusercontent.com/70114276/159179226-196f41fe-68d4-43ef-9139-d96cd2b1ef4d.png)

![7](https://user-images.githubusercontent.com/70114276/159179232-96e00abe-a162-45ee-84d8-d0513f8e1886.png)
