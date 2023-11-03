# Overview
## Purpose of module

TechRaj\CustomerGraphql module is responsible for get customer by email id
# Deployment
## System requirements

## Install
### Add repository
Repositry : composer config repositories.rajtech-customer-graphql git https://github.com/pawarrajendra200/magento2-customer-graphql.git
### Install the Extension using Composer
composer require tech-raj/customer-graphql
### Enable the Extension

php bin/magento module:enable TechRaj_CustomerGraphql

### Last execute magento commanads
1) php bin/magento setup:upgrade
2) php bin/magento setup:di:compile
3) php bin/magento setup:static-content:deploy
4) php bin/magento setup:cache:flush

## GrapQl

URL : {base url}/graphql
Type : POST
Body QUERY : 
{
    getCustomerByEmail(email: "rajendra@czargroup.net") {
        entity_id
        firstname
        lastname
        email
        created_in
        created_at
    }
} 