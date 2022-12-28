# Understanding the Cloud PaaS layer

![iaaspaas](https://user-images.githubusercontent.com/121013439/209799712-e971c157-c137-4ac4-a239-94899505294c.jpg)

The main benefit of PaaS offerings to most businesses is the systematic elimination of hardware and software managerial concerns, thus allowing companies concentrate on their business data, and applications. From the diagram above we see how various components in the chain of management narrows down from the On-Premises model unto the PaaS model. Hardware components, like networking, storage, servers up to OS, middleware, runtime etc are managed by the cloud provider.

## AZURE SQL's PaaS Offerings

Microsoft's SQL Server taps into this relatively new PaaS services and is offered as Azure SQL. In this offering the database all aspects of hardware and software management related to the database is 100% managed by Microsoft. In the PaaS model interacting with the Azure databases is done using network endpoints withing Azure.

# PaaS Databases Subscriptions

New orders for PaaS Databases can be done via two model:

**Managed Subscriptions** : This uses Volvo acquired Azure subscriptions and its database resources are created and managed by Volvocars.

Subscriptions are maintained based on the environments:

- Non-Production
- Production

![SQLPaaS_HLD (1)](https://user-images.githubusercontent.com/121013439/209799896-67f602eb-f3cf-4eb5-aa77-5fee0bcdb73f.jpg)


**Self-Managed Subscriptions** : The customer manages the Azure subscriptions while volvocars manages resources groups and the underlined databases.

![SQLPaaS_HLD2](https://user-images.githubusercontent.com/121013439/209800003-81ce9ceb-2e59-414d-87d2-281d02a0bd47.jpg)

Azure SQL Database offers the following deployment options in the PaaS:

Single database:

![singlesqldatabase](https://user-images.githubusercontent.com/121013439/209800516-84fc0e3b-e761-40e6-a2d9-d9fe91817527.jpg)

As a single database with its own set of resources managed via a logical SQL server. A single database is similar to a contained database in SQL Server. This option is optimized for modern application development of new cloud-born applications. Hyperscale and serverless options are available.

Elastic pool:

![elasticpool](https://user-images.githubusercontent.com/121013439/209801140-15e24ddc-3095-4341-9b7e-2393078a5bb5.jpg)

An elastic pool, which is a collection of databases with a shared set of resources managed via a logical server. Single databases can be moved into and out of an elastic pool. Elastic pools provide a cost-effective solution for managing the performance of multiple databases that have variable usage patterns.

Azure SQL Managed Instance:

This option provides all the PaaS benefits of Azure SQL Database but adds capabilities that were previously only available in SQL Server VMs. This includes a native virtual network and near 100% compatibility with on-premises SQL Server.

![managedinstance](https://user-images.githubusercontent.com/121013439/209801459-c50b93ff-78e4-4b54-b5d5-fa370b8de88a.jpg)

# Azure Purchase Models

Azure gives two purchasing models for its Databases, they are

DTU / eDTU and the vCore Model:

![purchase model](https://user-images.githubusercontent.com/121013439/209802455-7817ec05-be7a-437d-ab57-9c1d18b8ab53.jpg)


### DTU / eDTU Model:

This model supports only the Azure SQL Database offering. This model is based on a bundled measure of compute, storage, and I/O resources. Compute sizes are expressed in DTUs for single databases and in elastic database transaction units (eDTUs) for elastic pools. This option is suited for customers who want simple, preconfigured resource options.

### vCore Model (Preferred model):

This model supports both Azure SQL Database and SQL Managed instances. It is Microsoft's recommended model for its clients. This model allows you to independently choose compute and storage resources. This option is suited for customers who value flexibility, control, and transparency.

Use Case for the various tiers under the vCore model

![vCore](https://user-images.githubusercontent.com/121013439/209802794-03b134e2-d781-49e4-a0a5-fcaac76e9e13.jpg)


