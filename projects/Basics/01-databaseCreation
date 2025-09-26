create database CompanyDB
 use CompanyDB --shifts databases-- 
 create table Employee(
 id int primary key identity(1,1), --identity will generate numbers starting from 1 and incrementing by 1 automatically--
 first_name varchar(20) Default'Slim', -- default will assign a value when no value is given--
 middle_name varchar(20) not null, --the constraint 'not null' forced the record to have a value--
 last_name varchar(20),
 country varchar(10),
 fax_number varchar(12),
 salary decimal(10,2),
 birth_date date,
 age as Year(Current_timestamp) - Year(birth_date) --the Year() function extracts the year in a given date/time-date --
  --as allows age to be auto-calculated (derived attribute)--
 )
 insert into Employee values('Ahmed','Ali','Ahmed',null,null,10000,'9/11/1996')
 insert into Employee (first_name, middle_name,salary,birth_date) values('mohamed','Ali',35000,'9/11/1996')
 Set identity_insert Employee ON; -- forces a custom ID value with IDENTITY_INSERT--
 insert into Employee (id,first_name, middle_name,salary,birth_date) values(50,'mohamed','Ali',35000,'9/11/1996')
 Set identity_insert Employee OFF; --incrementing starts from the largest value after the identity-insert is disabled--
--insert into Employee values('AhmedAFCAGYWFAWYGUASGUYFASGFGSCFYHGEFYYGBEGFUYWEGFY','Ali','Ahmed',null,null,10000,'9/11/1996')   demonstrates the error given if the limit of  the varchar is exceeded--
  --strings above the set limit will not be allowed, however numbers will round up--
