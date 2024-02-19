---
slides: https://bath-prod-sss1.s3.eu-west-1.amazonaws.com/89/78/8978126d83ef0b0cf0453eff62138633af46429f?response-content-disposition=inline%3B%20filename%3D%22Week%2021%20-%20Support%20Vector%20Machines.pdf%22&response-content-type=application%2Fpdf&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJBFBMNJTZPM2NVZA%2F20240219%2Feu-west-1%2Fs3%2Faws4_request&X-Amz-Date=20240219T151651Z&X-Amz-SignedHeaders=host&X-Amz-Expires=21549&X-Amz-Signature=c90614bc65f3273479eff487e3d89dd78e897a7a3ed07ccdee5974c7991efca4
---
### The Limits of Linear Regression:![[SV0.png]]
How do we know if our line is actually any good?
What if we introduce a new point that's closer to one group, but classified as another?
![[ClassifiedWrong1.png]]
Here, the blue X is closer to the greens than the reds — you're much more likely to pass here!

What can we do?
### Maximal Margin Classifiers
![[SVM1.png]]