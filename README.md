# Test
Test

## Getting started
Easy setup! [Installing section](#installing)

### Installing
Firstly you need to install PostgreSQL that is the database manager that Ash Server uses:

`sudo apt install postgresql`

After that you need to switch to the Postgres user:

`sudo su postgres`

Then you need to create the user of the database that will owns the database (**you need to put the name you want instead of** `userName`):

`createuser userName -P --interactive`

It will ask you a password that you will use in the future to access to the user (**so make a strong password**) and if the user will be a superuser or not (**put yes**)

The last thing that needs to be done is creating the Database. To create the database, write:

`psql`

`create database ashdb;`

`psql` is needed to access to the default user, while `create database <name>` creates your database (<name> is the name of the database that you will need in the future)
  
  **Finish!**
  
  ## Access the database from command line
  To access the database from a terminal, switch to postgres user, than connect to the database:
  
`sudo su postgres`

  Than connect to it (giving the right parameters):

`psql ashdb -h localhost -p 5432 -U userName`

`ashdb` is the database name (must coincides with the one that you gave when you created the database), `-h` is the host (`localhost` for hosting the database on your machine), `-p` is the port (for Ash I chose `5432`) and `-U` rappresents the user you want to connect to (must coincide with the `userName` given when you created the user)
