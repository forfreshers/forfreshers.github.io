---
layout: post
title: "How to Deploy WordPress On GCP - Step by step"
date:   2020-05-22 20:20:00 +0000
author: admin
intro: Step-By-Step Guide to deploy wordpress on gcp and configure a website from scratch! You need a credit card or Debit card to get started with Google cloud patform (GCP).
description: Step-By-Step Guide to deploy wordpress on gcp and configure a website from scratch! You need a credit card or Debit card to get started with Google cloud patform (GCP).
permalink: /deploy-wordpress-on-gcp/
---


### How to Deploy WordPress Website On Google Cloud Platform (GCP). 


![Google Cloud Platform](images/svg.png)


Step-By-Step Guide to configure a website from scratch! You need a credit card or Debit card to get started with Google cloud patform (GCP).and You Need Domain name for the best Practice, Otherwise you can purchase domain name from domains.google.com or bigrock.in, or GoDaddy.com, etc.

{% include article-adsense.html %}

#STEP #1
Setup Google Cloud Platform
at cloud.google.com using a free google account.
#STEP #2
Deploy WordPress Website by Bitnami
#STEP #3
Create a Static IP Address to point to the website.
#STEP #4
Create SSL Certificate
& Setup SSL Certificate AutoRenew
```javascript
sudo /opt/bitnami/letsencrypt/scripts/generate-certificate.sh -m giftinknot@gmail.com -d giftinknot.com -d www.giftinknot.com
```
Add code to Configuration file
```javascript
sudo nano /opt/bitnami/apache2/conf/bitnami/bitnami.conf

RewriteEngine On
RewriteCond %{HTTPS} !=on
RewriteRule ^/(.*) https://www.giftinknot.com/$1 [R,L]
```
Restart Apache Server
```javascript
sudo /opt/bitnami/ctlscript.sh restart apache
```

#STEP #5
Increase Performance using a CDN Content Delivery Network)
www.CouldFlare.com/CDN

#STEP #6
Remove Bitnami Banner Ad
```javascript
sudo /opt/bitnami/apps/wordpress/bnconfig –disable_banner 1
```
Restart Apache Server
```javascript
sudo /opt/bitnami/ctlscript.sh restart apache
```

{% include article-adsense.html %}

Thanks For Reading!