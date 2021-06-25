# Run this project
## For local run
### Install dependencies
```
sudo apt-get install ruby ruby-dev make build-essential
sudo gem install -V bundler
bundle
```

### Run jekyll locally
```shell
make
```

## For custome domain (custome domain ko lagi maile CNAME file delete gardeko xu tyo file add garyara  madanbaduwal.com.np yati add garni)
.np domain have no option CNAME so we follow cloudflare
### Steps
#### 1. Go to the https://www.cloudflare.com/en-au/
*  Redirected: Domani name point at ip address(A record)>DNS point ip address to another domain name(CNAME)

```A record : Madanbaduwal.com.np points to  185.199.108.153(githubip)
   A record : Madanbaduwal.com.np points to  185.199.109.153(githubip)
   A record : Madanbaduwal.com.np points to  185.199.110.153(githubip)
   A record : Madanbaduwal.com.np points to  185.199.111.153(githubip)
   
   CNAME record : MadanBaduwal.com.np is an alise of madanbaduwal.github.io
```

  Note : githubip are same  for all users.

* look your Primary name server and Secondary name server from cloudfair
Note : Primary name server and Secondary name server are different for all users so try to copy other , look in your cloudfair account.


#### 2. Go to the register.com.np
* Pest you Primary name server and Secondary name server from cloudfair

#### 3. After 24 hours you will gate update

#### 4. Check whether my domain is Primary name server and Secondary name server from cloudfair

* https://dnschecker.org/all-dns-records-of-domain.php?query=madanbaduwal.com.np&rtype=ANY

#### 5. CNAME(no any extension) file in github

* You can create CNAME file manually in github project(CNAME align with index.html) with madanbaduwal.com.np.
 or 
* In project setting if we set custome domain it create CNAME file automatically with it body.

#### 6.SSL setup ( For secure)

Unfortunately Github pages does't support SSL on GIithub pages for custome domain , so do that in cloudfair
* Goto the SSL/TLS and make 
``` Full
Encrypts end-to-end, using a self signed certificate on the server
```
and 
* SSL/TLS Recommender ON

* Goto the Page rule  set the following two rules
``` 
madanbaduwal.com.np/*    : Always Use HTTPS

www.madanbaduwal.com.np/*  :Always Use HTTPS

```

#### 7. You can setup many rules in cloudfair for your website.

#### 8.Visiable in google + SEO 

* Go throw : https://mmistakes.github.io/minimal-mistakes/

* Google webmaster + Google search console 
* Verified your website by copy provided text and pest in DNS(cloudfair) as TXT record.

```
TXT record : Madanbaduwal.com.np points to  <text copy from google search console>.
```
* Submite your sitemap : https://madanbaduwal.com.np/sitemap.xml , in google search console.

#### 9.[Reference](https://mmistakes.github.io/minimal-mistakes)


# 10. Creating a pages

## 1. Goto _data and add title and url
```
main:
  - title: "Posts"
    url: /posts/
  - title: "Post collections"
    url: /postcollections/
  - title: "About"
    url: /about/
    
```
## 1. Goto _pages folder and create pages.
```
permalink: /about/
title: "About"
classes: wide
excerpt: Learn about me, who iam and what I do.

```

**Be sure the permalink: matches the url in navigation.yml file.**

Note: page ma click garni bitikai auni banaunai kura haru yahi lekhni .
Yadi post haru lekhnu x vanya post ma lekhni.


# 11. Creating posts

## 1. Goto _posts folder and create posts.


Page vs post
* page ma classes: wide vanyara hunxa 
* post ma layout : categories,posts  vanyara hunxa.
# Note if page and post configuration properly set vayo vanya thyakka mathi bar ma yellow point dekhinxa github action pass vanyara.
![image](https://github.com/MadanBaduwal/MadanBaduwal.github.io/blob/main/images/info.png)

# NOte : Directly write by markdown language on .md file.

.md means mark-down so we can write markdown language.
