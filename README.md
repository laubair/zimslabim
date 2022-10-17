# DEPRICTED and NO MAINTAINED!

zimslabim
=========

Zimbra to Sql Ldap Address Book Importer

__zimslabimp__ is PHP script to download one or more address books from your [zimbra collaboration server](http://www.zimbra.com) and automatically import them into a SQL database and/or a LDAP Directory.
The idea is to reuse your zimbra addresses for other purpose like PBX using LDAP, Wordprocessors using SQL/ODBC ...

Features
--------
### General
* Imports multiple address books to SQL and/or LDAP keeps address boom information
* Uses zimbra REST Url to get autmatically XML export file of the zimbra address books
* Fully configurable using config.ini file
* Commandline args for maintianance like listing exiting address books and deleting specific address books
* Updates exsting addresses accoring address entry revision
* Different log levels using -v,-vv,-vvv switches
* Suitable for regularly importing using cron job

### LDAP Specific
* Default mapping to inetOrgPerson schema (default, others are possible).
* Attribute mapping is configurable in config.ini
* Different address books are kept separately below one 'ou' per address book
* Updates existing addresses according to last modification time

### SQL Specific
* Uses PHP PDO so at least mysql and sqllite are supported
* SQL tables are automactically created when needed
* Address book information kept in seperate table with reference to address entry
