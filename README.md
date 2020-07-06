# crypto-portfolio

This is a crypto-wallet-portfolio application.
The aim is to keep track of mutliple user entered wallets with different
amounts of crypto-coins and in different currencies.

## Front-end To Do

The front end is setup with nuxt.
Nuxt allows for easy routing and static page management. 

```
[ ] Setup NUXT 

[ ] Fetch Data from API
[ ] Display data on page 

[ ] Create a minimal design
 [ ] CRUD Design
  [ ] Table for Crypto Items
  [ ] Item add Form 

[ ] 1st Prototype design in Adobe XD 
```

## Back-end To Do

The back end is setup with Ruby on Rails.

```
[ ] Setup Ruby on Rails

[ ] Create cryptoDB Database
[ ] Create Crypto-item layout

[ ] Create an API 
 [ ] GET -Data Api :Get data from DB 
 [ ] POST -Data Update Api: Update existing values in DB
 [ ] POST -Data Create Api: Create a new Item in DB
 [ ] POST -Data Destroy Api: Destroy an Item in DB

[ ] Test api with postman
```

## Application Architecture 

Here is a visual representation of our application architecture

```
                        +--------------------------------------+
                      |                                      |
                      |       Cypto Portfolio (Front)        |
                      |       [NUXT]                         |
                      |                                      |
                      |                                      |
                      +-----------+----------------^---------+
                                  |                |
                                  |                |
                          +-------v------+  +------+------+
                          |              |  |             |
         +----------------+ API Request  |  |             |
         |                | is sent to   |  | API return  |
+--------+--------+       | back end     |  | value       |
|                 |       |              |  |             |
|  APIs are       |       |              |  |             |
|  configured     |       +-------+------+  +------^------+
|  in the         |               |                |
|  back end       |               |                |              +---------------------------+
|                 |   +-----------v----------------+---------+    |                           |
|                 |   |                                      |    |                           |
+--------+--------+   |    Rails evaluates the request       |    |        CryptoDB           |
         |            |    and sends a return              +------------+  Holds all data     |
         |            |    [RAILS]                           |    |        for crypto items   |
         +------------+                                      |    |        [PostGRE]          |
                      +--------------------------------------+    |                           |
                                                                  +---------------------------+



```
