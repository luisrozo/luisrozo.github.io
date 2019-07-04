---
layout: post
title: Aplicación descentralizada basada en Ethereum para la compra venta de datos personales
author: Luis
---

I'm going to talk about this project, which represents the final project of my degree. 

I developed a decentralized application (or dApp) based on **blockchain**, especially using Ethereum ecosystem. Other technologies were used too, such as ReactJS, IPFS, etc.

<img src="{{site.url}}/assets/images/myproject_eth1.png" style="display: block; margin: auto; max-width:80%; height:auto; " />

## General information

This project aims to prove that, using modern technologies, the problematic of personal data can be solved in any ambit. However, this project is focused on medical paradigmatic case. Users can validate their own medical data, in order to be sold through the platform. Others users will be able to buy (using *Ether* as coin) batches (known in the platform as *offers*) of users registers in order to gain access to that information. This batches are created by the custodian entity (which could be a hospital in a real world situation). Each purchase will create a block in the blockchain, registring all activity in the system.

## Storing information: on-chain & off-chain

Not all information is stored on the blockchain (this would be extremly non-viable as explained later). This project uses the InterPlanetary File System, aka IPFS, to store the rest of information in a decentralized way (too). 

<img src="{{site.url}}/assets/images/myproject_eth2.png" style="display: block; margin: auto; max-width:80%; height:auto; " />

There's some files in the offer creation process which are stored on IPFS. We only store in the blockchain the final IPFS hash, which links to the rest of this files chain.

## Why IPFS?

Let's make some estimate, bearing in mind that storing 8 bytes has a cost of 20,000 gas; having each gas an equivalent of 4 gwei.

* A 8 bytes transaction for 20,000 gas x 4 gwei/gas => 8 bytes would cost 80,000 gwei.
* So, talking about kB instead of B, it would cost 10,000,000 of gwei (or ,01 Ether).
* ,01 ETH/kB x 1,000 kB => 10 ETH para almacenar 1 Mb.
* Nowdays, an Ether is aprox. €164, so storing 1 Mb of information in a blockchain would cost €1,640.

With all this information, we can see clearly that, storing 1 GB of information (a very little amount nowadays) in a blockchain would cost **€1,640,000**!! (OMG). So, blockchain and IPFS are a very common couple in this ecosystem.

## More information

This project was presented on June 25, 2019 in the Escuela Superior de Ingeniería at Universidad de Cádiz, obtaining the highest score (10/10). If you are interested in knowing the details around this project, you can visit the following links:

* [Project documentation](https://drive.google.com/file/d/1_DnLsGQUuMttBdkgs425984ZnpjjX-s0/view?usp=sharing): a 129 page document explaining with all details all about this project.
* [GitHub repository](https://github.com/luisrozo/MedicalDataMarket): check how technologies such as blockchain, IPFS and ReactJS live together in a same system.

