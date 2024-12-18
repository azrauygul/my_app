***MR. Bill***  
*******

**WHO ARE WE**
As Azra Uygul and Fırat Göçmen, we are working on a project that leverages blockchain technology to develop a legal and transparent invoice recording system. Azra, with her background in mathematics, brings an analytical perspective, while Fırat, with his computer engineering expertise, shapes our software development approach. As two dedicated developers, we are working hard to bring this project to life. By utilizing the security and transparency features of blockchain, we ensure that contracts are recorded accurately and securely.


*******
**DESCRIPTION**
This repository contains a blockchain-based invoice management system developed in Motoko. It allows users to securely manage invoices, ensuring transparency and accuracy. Users can add, update, delete, and retrieve invoices, as well as calculate total amounts for each user. The system uses blockchain to store invoices, ensuring data integrity and preventing manipulation  
******

**HOW TO USE**


## Features

- **Add Invoice**: Add a new invoice with details such as user name, invoice ID, total amount, and date.
- **Get All Invoices for a User**: Retrieve all invoices associated with a specific user.
- **Get Invoice by ID**: Retrieve a specific invoice by its unique ID.
- **Update Invoice**: Update an existing invoice by its ID.
- **Delete Invoice**: Delete an invoice by its ID.
- **Calculate Total Amount for a User**: Calculate the total amount of invoices for a specific user.

## Data Model

### Fatura (Invoice)
Each invoice consists of:
- `id`: Unique identifier for the invoice.
- `kullanici_adi`: The username of the person associated with the invoice.
- `toplamTutar`: The total amount of the invoice.
- `tarih`: The date when the invoice was created.

### FaturaData
A map that stores lists of invoices for each user, with the username as the key.

## Functions

### addFatura(user: Text, newFatura: Fatura)  
Adds a new invoice for a user.  
Returns the newly added invoice.

### getEntries(user: Text)  
Retrieves all invoices for a specified user.  
Returns a list of invoices or `null` if no invoices exist.

### getFaturaId(user: Text, targetId: Nat)  
Retrieves a specific invoice by its ID for a given user.  
Returns the invoice or `null` if the invoice doesn't exist.

### updateFatura(user: Text, targetId: Nat, updatedFatura: Fatura)  
Updates a specific invoice based on its ID.  
Returns `true` if the update was successful.

### deleteFatura(user: Text, targetId: Nat)  
Deletes a specific invoice based on its ID.  
Returns `true` if the deletion was successful.

### totalAmountForUser(user: Text)  
Calculates the total amount of all invoices for a specified user.  
Returns the total amount as a natural number.

## Usage

### Deployment
To interact with the system, deploy the Motoko actor on the Internet Computer platform. You can then call the available functions via the provided APIs.

### Example Usage

1. **Add an Invoice**
   ```motoko
   let newInvoice = {
       id = 1;
       kullanici_adi = "user123";
       toplamTutar = 100;
       tarih = "2024-12-18";
   };
   let addedInvoice = await addFatura("user123", newInvoice);
   ********
     
**VİSİON**  
Our project vision is to create a blockchain-based system that allows users to securely and transparently manage their invoices in the digital environment. This system ensures the entire process, from invoice creation to storage, is secure by recording and making user data immutable and accessible. Our goal is to simplify invoice management and provide a secure, efficient solution in the increasingly digital world. 
*********  
**LANGUAGE**  
*Motoko  
Footer
© 2024 GitHub, Inc.
