# AWS-Certified-Solutions-Architect---Associate

Overview
Validate your AWS skills. 

This is your opportunity to take the next step in your career by expanding and validating your skills on the AWS cloud.  
AWS has been the frontrunner in cloud computing products and services, and the AWS Certified Solutions Architect 
Official Study Guide for the Associate exam will get you fully prepared through expert content, and real-world 
knowledge, key exam essentials, chapter review questions, access to Sybex�s interactive online learning environment, 
and much more. This official study guide, written by AWS experts, covers exam concepts, and provides key review on exam 
topics, including:

Mapping Multi-Tier Architectures to AWS Services, such as web/app servers, firewalls, caches and load balancers
Understanding managed RDBMS through AWS RDS (MySQL, Oracle, SQL Server, Postgres, Aurora)
Understanding Loose Coupling and Stateless Systems
Comparing Different Consistency Models in AWS Services
Understanding how AWS CloudFront can make your application more cost efficient, faster and secure
Implementing Route tables, Access Control Lists, Firewalls, NAT, and DNS
Applying AWS Security Features along with traditional Information and Application Security
Using Compute, Networking, Storage, and Database AWS services
Architecting Large Scale Distributed Systems
Understanding of Elasticity and Scalability Concepts
Understanding of Network Technologies Relating to AWS
Deploying and Managing Services with tools such as CloudFormation, OpsWorks and Elastic Beanstalk.
Learn from the AWS subject-matter experts, review with proven study tools, and apply real-world scenarios. 
If you are looking to take the AWS Certified Solutions Architect Associate exam, 
this guide is what you need for comprehensive content and robust study tools that will help you gain the edge on exam 
day and throughout your career. 

Create a Quiz or Flashcard Set to help you prepare for taking exams or to study. 
If you need more in-depth information and review, refer to the concepts and objectives that are covered in the 
accompanying products.

Please note the Resources link which may include information such as additional information about the product, 
test or learning objective, site or product FAQs and other resources available for this product.

CREATE TABLESPACE "AWS-Certified-Solutions-Architect---Associate"
  LOCATION 'D:\dev\src\workspaces\spring\AWS-Certified-Solutions-Architect---Associate';

-- Database: "AWS-Certified-Solutions-Architect---Associate"

-- DROP DATABASE "AWS-Certified-Solutions-Architect---Associate";

CREATE DATABASE "AWS-Certified-Solutions-Architect---Associate"
  WITH OWNER = dba
       ENCODING = 'UTF8'
       TABLESPACE = "AWS-Certified-Solutions-Architect---Associate"
       LC_COLLATE = 'Russian_Russia.1251'
       LC_CTYPE = 'Russian_Russia.1251'
       CONNECTION LIMIT = -1;

-- Schema: public

-- DROP SCHEMA public;

CREATE SCHEMA public
  AUTHORIZATION postgres;

GRANT ALL ON SCHEMA public TO postgres;
GRANT ALL ON SCHEMA public TO public;
COMMENT ON SCHEMA public
  IS 'standard public schema';

ALTER TABLE public."FlashCard" ADD id int4 NOT NULL ;
ALTER TABLE public."FlashCard" ADD question varchar NULL ;

-- DROP SEQUENCE public.flash_card_id_seq;

CREATE SEQUENCE public.flash_card_id_seq
INCREMENT BY 1
MINVALUE 1
MAXVALUE 9223372036854775807
START 1616349;

ALTER TABLE public."FlashCard" ALTER COLUMN id SET DEFAULT nextval('flash_card_id_seq'::regclass) ;

