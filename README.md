# SQL-Queries-Examples
Some important SQL queries to retrieve data from the database. Creating Tables, creating database, executing queries and finally drop commands.

// creating the database

--------------------------------------------------------
--  File created - Thursday-October-09-2014   
--------------------------------------------------------
--------------------------------------------------------
--  DDL for Table FEATURE
--------------------------------------------------------

  CREATE TABLE "FEATURE" 
   (	"FEATURE_ID" VARCHAR2(20 BYTE), 
    	"FEATURE_NAME" VARCHAR2(20 BYTE)
   ) SEGMENT CREATION IMMEDIATE 
  PCTFREE 10 PCTUSED 40 INITRANS 1 MAXTRANS 255 
  NOCOMPRESS LOGGING
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS" ;
  REM INSERTING into FEATURE
  SET DEFINE OFF;
  
  // Inserting data into feature table
  
Insert into FEATURE (FEATURE_ID,FEATURE_NAME) values ('Fea1','swimming pool');
Insert into FEATURE (FEATURE_ID,FEATURE_NAME) values ('Fea2','Jacuzzi');
Insert into FEATURE (FEATURE_ID,FEATURE_NAME) values ('Fea3','billiard table');
Insert into FEATURE (FEATURE_ID,FEATURE_NAME) values ('Fea4','Xbox 360');
Insert into FEATURE (FEATURE_ID,FEATURE_NAME) values ('Fea5','board games');
Insert into FEATURE (FEATURE_ID,FEATURE_NAME) values ('Fea6','pets allowed');
--------------------------------------------------------
--  DDL for Index FEATURE_PK
--------------------------------------------------------

  CREATE UNIQUE INDEX "FEATURE_PK" ON "FEATURE" ("FEATURE_ID") 
  PCTFREE 10 INITRANS 2 MAXTRANS 255 
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS" ;
--------------------------------------------------------
--  Constraints for Table FEATURE
--------------------------------------------------------

  ALTER TABLE "FEATURE" ADD CONSTRAINT "FEATURE_PK" PRIMARY KEY ("FEATURE_ID")
  USING INDEX PCTFREE 10 INITRANS 2 MAXTRANS 255 
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS"  ENABLE;
  ALTER TABLE "FEATURE" MODIFY ("FEATURE_ID" NOT NULL ENABLE);








--------------------------------------------------------
--  File created - Thursday-October-09-2014   
--------------------------------------------------------
--------------------------------------------------------
--  DDL for Table VILLAUSER
--------------------------------------------------------

  CREATE TABLE "VILLAUSER" 
   (	"USERID" CHAR(5 BYTE), 
	"USER_EMAIL" VARCHAR2(50 BYTE), 
	"USER_NAME_FIRSTNAME" VARCHAR2(20 BYTE), 
	"USER_NAME_LASTNAME" VARCHAR2(20 BYTE), 
	"USER_DOB" DATE, 
	"USER_FAV_VILLA" VARCHAR2(20 BYTE)
   ) SEGMENT CREATION IMMEDIATE 
  PCTFREE 10 PCTUSED 40 INITRANS 1 MAXTRANS 255 
  NOCOMPRESS LOGGING
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS" ;
  REM INSERTING into VILLAUSER
  SET DEFINE OFF;
  
  //Insert data into table Villa User
  
Insert into VILLAUSER (USERID,USER_EMAIL,USER_NAME_FIRSTNAME,USER_NAME_LASTNAME,USER_DOB,USER_FAV_VILLA) values ('U1   ','jack_killer@gmail.com','Jackie','Jones',to_date('28-FEB-83','DD-MON-RR'),'Vil2,Vil4');
Insert into VILLAUSER (USERID,USER_EMAIL,USER_NAME_FIRSTNAME,USER_NAME_LASTNAME,USER_DOB,USER_FAV_VILLA) values ('U2   ','Hello_macy@yahoo.com','Jessie','Jackson',to_date('04-MAR-86','DD-MON-RR'),'Vil8');
Insert into VILLAUSER (USERID,USER_EMAIL,USER_NAME_FIRSTNAME,USER_NAME_LASTNAME,USER_DOB,USER_FAV_VILLA) values ('U3   ','john_black@hotmail.com','Tommy','Trojan',to_date('22-APR-90','DD-MON-RR'),'Vil10,Vil3,Vil7');
Insert into VILLAUSER (USERID,USER_EMAIL,USER_NAME_FIRSTNAME,USER_NAME_LASTNAME,USER_DOB,USER_FAV_VILLA) values ('U4   ','ny_robert@usc.edu','Niki','Nanjan',to_date('10-JUN-80','DD-MON-RR'),'Vil10,Vil4');
Insert into VILLAUSER (USERID,USER_EMAIL,USER_NAME_FIRSTNAME,USER_NAME_LASTNAME,USER_DOB,USER_FAV_VILLA) values ('U5   ','cool_andrew@bbc.co.uk','Jalli','Shadan',to_date('27-NOV-84','DD-MON-RR'),'Vil1');
Insert into VILLAUSER (USERID,USER_EMAIL,USER_NAME_FIRSTNAME,USER_NAME_LASTNAME,USER_DOB,USER_FAV_VILLA) values ('U6   ','coryphillip@voa.gov','Houtan','Khandan',to_date('06-JUN-66','DD-MON-RR'),'Vil3');
Insert into VILLAUSER (USERID,USER_EMAIL,USER_NAME_FIRSTNAME,USER_NAME_LASTNAME,USER_DOB,USER_FAV_VILLA) values ('U7   ','DaneilJ@msnbc.com','Naz','Nazi',to_date('20-APR-00','DD-MON-RR'),'Vil2,Vil4,Vil12');
Insert into VILLAUSER (USERID,USER_EMAIL,USER_NAME_FIRSTNAME,USER_NAME_LASTNAME,USER_DOB,USER_FAV_VILLA) values ('U8   ','rohanau@cs.mit.edu','Ab','Bazi',to_date('12-DEC-56','DD-MON-RR'),'Vil1,Vil9');
Insert into VILLAUSER (USERID,USER_EMAIL,USER_NAME_FIRSTNAME,USER_NAME_LASTNAME,USER_DOB,USER_FAV_VILLA) values ('U9   ','edmorales@houti.com','Ben','Ghazi',to_date('10-NOV-73','DD-MON-RR'),'Vil6');
Insert into VILLAUSER (USERID,USER_EMAIL,USER_NAME_FIRSTNAME,USER_NAME_LASTNAME,USER_DOB,USER_FAV_VILLA) values ('U10  ','danamoon@louti.com','Carlos','Santana',to_date('07-JUL-77','DD-MON-RR'),'Vil11,Vil12');
Insert into VILLAUSER (USERID,USER_EMAIL,USER_NAME_FIRSTNAME,USER_NAME_LASTNAME,USER_DOB,USER_FAV_VILLA) values ('U11  ','owner1@villa.com','Roberto','Carlos',to_date('05-MAY-55','DD-MON-RR'),'null');
Insert into VILLAUSER (USERID,USER_EMAIL,USER_NAME_FIRSTNAME,USER_NAME_LASTNAME,USER_DOB,USER_FAV_VILLA) values ('U12  ','owner2@villa.com','De','Vilardo',to_date('04-APR-44','DD-MON-RR'),'null');
Insert into VILLAUSER (USERID,USER_EMAIL,USER_NAME_FIRSTNAME,USER_NAME_LASTNAME,USER_DOB,USER_FAV_VILLA) values ('U13  ','owner3@villa.com','villa','Blanka',to_date('11-NOV-74','DD-MON-RR'),'Vil1');
Insert into VILLAUSER (USERID,USER_EMAIL,USER_NAME_FIRSTNAME,USER_NAME_LASTNAME,USER_DOB,USER_FAV_VILLA) values ('U14  ','ceo@villa.com','nino','bino',to_date('01-JAN-91','DD-MON-RR'),'Vil2');
Insert into VILLAUSER (USERID,USER_EMAIL,USER_NAME_FIRSTNAME,USER_NAME_LASTNAME,USER_DOB,USER_FAV_VILLA) values ('U15  ','manager2@villa.com','Bookish','Morinio',to_date('17-APR-50','DD-MON-RR'),'null');
--------------------------------------------------------
--  DDL for Index VILLA_USER_PK
--------------------------------------------------------

  CREATE UNIQUE INDEX "VILLA_USER_PK" ON "VILLAUSER" ("USERID") 
  PCTFREE 10 INITRANS 2 MAXTRANS 255 
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS" ;
--------------------------------------------------------
--  Constraints for Table VILLAUSER
--------------------------------------------------------

  ALTER TABLE "VILLAUSER" ADD CONSTRAINT "VILLA_USER_PK" PRIMARY KEY ("USERID")
  USING INDEX PCTFREE 10 INITRANS 2 MAXTRANS 255 
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS"  ENABLE;
  ALTER TABLE "VILLAUSER" MODIFY ("USERID" NOT NULL ENABLE);


--------------------------------------------------------
--  File created - Thursday-October-09-2014   
--------------------------------------------------------
--------------------------------------------------------
--  DDL for Table OWNER
--------------------------------------------------------

  CREATE TABLE "OWNER" 
   (	"OWNER_ID" CHAR(5 BYTE), 
	"CONTACT_NUMBER" VARCHAR2(20 BYTE), 
	"MAMAGED_BY" CHAR(5 BYTE)
   ) SEGMENT CREATION IMMEDIATE 
  PCTFREE 10 PCTUSED 40 INITRANS 1 MAXTRANS 255 
  NOCOMPRESS LOGGING
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS" ;
  REM INSERTING into OWNER
  SET DEFINE OFF;
  
  //Insert data into owner Table
  
  Insert into OWNER (OWNER_ID,CONTACT_NUMBER,MAMAGED_BY) values ('U11  ','111-111-1111','U15  ');
  Insert into OWNER (OWNER_ID,CONTACT_NUMBER,MAMAGED_BY) values ('U12  ','222-222-2222','U15  ');
  Insert into OWNER (OWNER_ID,CONTACT_NUMBER,MAMAGED_BY) values ('U13  ','333-333-3333','U15  ');
  Insert into OWNER (OWNER_ID,CONTACT_NUMBER,MAMAGED_BY) values ('U14  ','444-444-4444',null);
--------------------------------------------------------
--  DDL for Index OWNER_PK
--------------------------------------------------------

  CREATE UNIQUE INDEX "OWNER_PK" ON "OWNER" ("OWNER_ID") 
  PCTFREE 10 INITRANS 2 MAXTRANS 255 
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS" ;
--------------------------------------------------------
--  Constraints for Table OWNER
--------------------------------------------------------

  ALTER TABLE "OWNER" ADD CONSTRAINT "OWNER_PK" PRIMARY KEY ("OWNER_ID")
  USING INDEX PCTFREE 10 INITRANS 2 MAXTRANS 255 
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS"  ENABLE;
  ALTER TABLE "OWNER" MODIFY ("OWNER_ID" NOT NULL ENABLE);
--------------------------------------------------------
--  Ref Constraints for Table OWNER
--------------------------------------------------------

  ALTER TABLE "OWNER" ADD CONSTRAINT "OWNER_VILLAUSER_FK1" FOREIGN KEY ("OWNER_ID")
	  REFERENCES "VILLAUSER" ("USERID") ON DELETE CASCADE ENABLE;


--------------------------------------------------------
--  File created - Thursday-October-09-2014   
--------------------------------------------------------
--------------------------------------------------------
--  DDL for Table VILLA
--------------------------------------------------------

  CREATE TABLE "VILLA" 
   (	"VILLA_ID" VARCHAR2(20 BYTE), 
	"NAME" VARCHAR2(20 BYTE), 
	"OWNER" CHAR(5 BYTE)
   ) SEGMENT CREATION IMMEDIATE 
  PCTFREE 10 PCTUSED 40 INITRANS 1 MAXTRANS 255 
 NOCOMPRESS LOGGING
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS" ;
REM INSERTING into VILLA
SET DEFINE OFF;

// Insert data into Villa table

Insert into VILLA (VILLA_ID,NAME,OWNER) values ('Vil1','Fifi','U11  ');
Insert into VILLA (VILLA_ID,NAME,OWNER) values ('Vil2','Lulu','U12  ');
Insert into VILLA (VILLA_ID,NAME,OWNER) values ('Vil3','Penny','U13  ');
Insert into VILLA (VILLA_ID,NAME,OWNER) values ('Vil4','Kiki','U11  ');
Insert into VILLA (VILLA_ID,NAME,OWNER) values ('Vil5','Vivi','U11  ');
Insert into VILLA (VILLA_ID,NAME,OWNER) values ('Vil6','Gigi','U11  ');
Insert into VILLA (VILLA_ID,NAME,OWNER) values ('Vil7','Kitty','U12  ');
Insert into VILLA (VILLA_ID,NAME,OWNER) values ('Vil8','Ellie','U13  ');
Insert into VILLA (VILLA_ID,NAME,OWNER) values ('Vil9','Ali','U14  ');
Insert into VILLA (VILLA_ID,NAME,OWNER) values ('Vil10','Kelley','U12  ');
Insert into VILLA (VILLA_ID,NAME,OWNER) values ('Vil11','Dori','U12  ');
Insert into VILLA (VILLA_ID,NAME,OWNER) values ('Vil12','Houti','U13  ');
--------------------------------------------------------
--  DDL for Index VILLA_PK
--------------------------------------------------------

  CREATE UNIQUE INDEX "VILLA_PK" ON "VILLA" ("VILLA_ID") 
  PCTFREE 10 INITRANS 2 MAXTRANS 255 COMPUTE STATISTICS 
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS" ;
--------------------------------------------------------
--  Constraints for Table VILLA
--------------------------------------------------------

  ALTER TABLE "VILLA" ADD CONSTRAINT "VILLA_PK" PRIMARY KEY ("VILLA_ID")
  USING INDEX PCTFREE 10 INITRANS 2 MAXTRANS 255 COMPUTE STATISTICS 
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS"  ENABLE;
  ALTER TABLE "VILLA" MODIFY ("VILLA_ID" NOT NULL ENABLE);
--------------------------------------------------------
--  Ref Constraints for Table VILLA
--------------------------------------------------------

  ALTER TABLE "VILLA" ADD CONSTRAINT "VILLA_OWNER_FK1" FOREIGN KEY ("OWNER")
	  REFERENCES "OWNER" ("OWNER_ID") ON DELETE CASCADE ENABLE;


--------------------------------------------------------
--  File created - Thursday-October-09-2014   
--------------------------------------------------------
--------------------------------------------------------
--  DDL for Table FEATURE_VILLA
--------------------------------------------------------

  CREATE TABLE "FEATURE_VILLA" 
   (	"VILLA_ID" VARCHAR2(5 BYTE), 
	"FEATURE_ID" VARCHAR2(20 BYTE)
   ) SEGMENT CREATION IMMEDIATE 
  PCTFREE 10 PCTUSED 40 INITRANS 1 MAXTRANS 255 
 NOCOMPRESS LOGGING
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS" ;
  REM INSERTING into FEATURE_VILLA
  SET DEFINE OFF;
  
  // insert data into feature_villa table
  
Insert into FEATURE_VILLA (VILLA_ID,FEATURE_ID) values ('Vil1','Fea1');
Insert into FEATURE_VILLA (VILLA_ID,FEATURE_ID) values ('Vil1','Fea2');
Insert into FEATURE_VILLA (VILLA_ID,FEATURE_ID) values ('Vil10','Fea5');
Insert into FEATURE_VILLA (VILLA_ID,FEATURE_ID) values ('Vil11','Fea2');
Insert into FEATURE_VILLA (VILLA_ID,FEATURE_ID) values ('Vil12','Fea2');
Insert into FEATURE_VILLA (VILLA_ID,FEATURE_ID) values ('Vil2','Fea1');
Insert into FEATURE_VILLA (VILLA_ID,FEATURE_ID) values ('Vil3','Fea1');
Insert into FEATURE_VILLA (VILLA_ID,FEATURE_ID) values ('Vil3','Fea4');
Insert into FEATURE_VILLA (VILLA_ID,FEATURE_ID) values ('Vil3','Fea5');
Insert into FEATURE_VILLA (VILLA_ID,FEATURE_ID) values ('Vil4','Fea2');
Insert into FEATURE_VILLA (VILLA_ID,FEATURE_ID) values ('Vil5','Fea4');
Insert into FEATURE_VILLA (VILLA_ID,FEATURE_ID) values ('Vil6','Fea6');
Insert into FEATURE_VILLA (VILLA_ID,FEATURE_ID) values ('Vil7','Fea3');
Insert into FEATURE_VILLA (VILLA_ID,FEATURE_ID) values ('Vil7','Fea4');
Insert into FEATURE_VILLA (VILLA_ID,FEATURE_ID) values ('Vil7','Fea5');
Insert into FEATURE_VILLA (VILLA_ID,FEATURE_ID) values ('Vil7','Fea6');
Insert into FEATURE_VILLA (VILLA_ID,FEATURE_ID) values ('Vil8','Fea6');
Insert into FEATURE_VILLA (VILLA_ID,FEATURE_ID) values ('Vil9','Fea5');
--------------------------------------------------------
--  DDL for Index FEATURE_VILLA_PK
--------------------------------------------------------

  CREATE UNIQUE INDEX "FEATURE_VILLA_PK" ON "FEATURE_VILLA" ("VILLA_ID", "FEATURE_ID") 
  PCTFREE 10 INITRANS 2 MAXTRANS 255 COMPUTE STATISTICS 
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS" ;
--------------------------------------------------------
--  Constraints for Table FEATURE_VILLA
--------------------------------------------------------

  ALTER TABLE "FEATURE_VILLA" ADD CONSTRAINT "FEATURE_VILLA_PK" PRIMARY KEY ("VILLA_ID", "FEATURE_ID")
  USING INDEX PCTFREE 10 INITRANS 2 MAXTRANS 255 COMPUTE STATISTICS 
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS"  ENABLE;
  ALTER TABLE "FEATURE_VILLA" MODIFY ("FEATURE_ID" NOT NULL ENABLE);
  ALTER TABLE "FEATURE_VILLA" MODIFY ("VILLA_ID" NOT NULL ENABLE);
--------------------------------------------------------
--  Ref Constraints for Table FEATURE_VILLA
--------------------------------------------------------

  ALTER TABLE "FEATURE_VILLA" ADD CONSTRAINT "FEATURE_VILLA_FEATURE_FK1" FOREIGN KEY ("FEATURE_ID")
	  REFERENCES "FEATURE" ("FEATURE_ID") ON DELETE CASCADE ENABLE;
  ALTER TABLE "FEATURE_VILLA" ADD CONSTRAINT "FEATURE_VILLA_VILLA_FK1" FOREIGN KEY ("VILLA_ID")
	  REFERENCES "VILLA" ("VILLA_ID") ENABLE;



--------------------------------------------------------
--  File created - Thursday-October-09-2014   
--------------------------------------------------------
--------------------------------------------------------
--  DDL for Table REVIEW
--------------------------------------------------------

  CREATE TABLE "REVIEW" 
   (	"REVIEW_ID" VARCHAR2(20 BYTE), 
	"USER_ID" CHAR(5 BYTE), 
	"VILLA_ID" VARCHAR2(20 BYTE), 
	"TEXT" VARCHAR2(100 BYTE), 
	"RATING" NUMBER(2,0)
   ) SEGMENT CREATION IMMEDIATE 
  PCTFREE 10 PCTUSED 40 INITRANS 1 MAXTRANS 255 
 NOCOMPRESS LOGGING
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS" ;
REM INSERTING into REVIEW
SET DEFINE OFF;

// Insert data into Review Table

Insert into REVIEW (REVIEW_ID,USER_ID,VILLA_ID,TEXT,RATING) values ('Rev1','U1   ','Vil1','Poor maintainance considering the price.',2);
Insert into REVIEW (REVIEW_ID,USER_ID,VILLA_ID,TEXT,RATING) values ('Rev2','U2   ','Vil3','Boring and Dull',1);
Insert into REVIEW (REVIEW_ID,USER_ID,VILLA_ID,TEXT,RATING) values ('Rev3','U4   ','Vil6','Love it!',4);
Insert into REVIEW (REVIEW_ID,USER_ID,VILLA_ID,TEXT,RATING) values ('Rev4','U2   ','Vil1','Best vila error',2);
Insert into REVIEW (REVIEW_ID,USER_ID,VILLA_ID,TEXT,RATING) values ('Rev5','U7   ','Vil1','Though not clean, has fantastic scenery around it',3);
Insert into REVIEW (REVIEW_ID,USER_ID,VILLA_ID,TEXT,RATING) values ('Rev6','U5   ','Vil2','not recommended',1);
Insert into REVIEW (REVIEW_ID,USER_ID,VILLA_ID,TEXT,RATING) values ('Rev7','U6   ','Vil1','Good one',4);
Insert into REVIEW (REVIEW_ID,USER_ID,VILLA_ID,TEXT,RATING) values ('Rev8','U4   ','Vil4','I gonna rent again and again',5);
Insert into REVIEW (REVIEW_ID,USER_ID,VILLA_ID,TEXT,RATING) values ('Rev9','U9   ','Vil3','Good work',5);
Insert into REVIEW (REVIEW_ID,USER_ID,VILLA_ID,TEXT,RATING) values ('Rev10','U3   ','Vil9','A must visit villa',5);
Insert into REVIEW (REVIEW_ID,USER_ID,VILLA_ID,TEXT,RATING) values ('Rev11','U10  ','Vil8','Nice',1);
Insert into REVIEW (REVIEW_ID,USER_ID,VILLA_ID,TEXT,RATING) values ('Rev13','U6   ','Vil7','poor one',1);
Insert into REVIEW (REVIEW_ID,USER_ID,VILLA_ID,TEXT,RATING) values ('Rev14','U1   ','Vil7','popular one',4);
Insert into REVIEW (REVIEW_ID,USER_ID,VILLA_ID,TEXT,RATING) values ('Rev15','U7   ','Vil3','wanna go back!',5);
--------------------------------------------------------
--  DDL for Index REVIEW_PK
--------------------------------------------------------

  CREATE UNIQUE INDEX "REVIEW_PK" ON "REVIEW" ("REVIEW_ID") 
  PCTFREE 10 INITRANS 2 MAXTRANS 255 
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS" ;
--------------------------------------------------------
--  Constraints for Table REVIEW
--------------------------------------------------------

  ALTER TABLE "REVIEW" MODIFY ("VILLA_ID" NOT NULL ENABLE);
  ALTER TABLE "REVIEW" MODIFY ("USER_ID" NOT NULL ENABLE);
  ALTER TABLE "REVIEW" ADD CONSTRAINT "REVIEW_PK" PRIMARY KEY ("REVIEW_ID")
  USING INDEX PCTFREE 10 INITRANS 2 MAXTRANS 255 
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS"  ENABLE;
  ALTER TABLE "REVIEW" MODIFY ("REVIEW_ID" NOT NULL ENABLE);
--------------------------------------------------------
--  Ref Constraints for Table REVIEW
--------------------------------------------------------

  ALTER TABLE "REVIEW" ADD CONSTRAINT "REVIEW_VILLAUSER_FK1" FOREIGN KEY ("USER_ID")
	  REFERENCES "VILLAUSER" ("USERID") ON DELETE CASCADE ENABLE;
  ALTER TABLE "REVIEW" ADD CONSTRAINT "REVIEW_VILLA_FK1" FOREIGN KEY ("VILLA_ID")
	  REFERENCES "VILLA" ("VILLA_ID") ON DELETE CASCADE ENABLE;



--------------------------------------------------------
--  File created - Thursday-October-09-2014   
--------------------------------------------------------
--------------------------------------------------------
--  DDL for Table LIKED_REVIEWS
--------------------------------------------------------

  CREATE TABLE "LIKED_REVIEWS" 
   (	"REVIEW_ID" VARCHAR2(5 BYTE), 
	"USER_ID" VARCHAR2(40 BYTE)
   ) SEGMENT CREATION IMMEDIATE 
  PCTFREE 10 PCTUSED 40 INITRANS 1 MAXTRANS 255 
 NOCOMPRESS LOGGING
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS" ;
REM INSERTING into LIKED_REVIEWS
SET DEFINE OFF;

// Insert data into Liked_Reviews table

Insert into LIKED_REVIEWS (REVIEW_ID,USER_ID) values ('Rev1','U4,U2,U3');
Insert into LIKED_REVIEWS (REVIEW_ID,USER_ID) values ('Rev2','U7,U4');
Insert into LIKED_REVIEWS (REVIEW_ID,USER_ID) values ('Rev3','U8');
Insert into LIKED_REVIEWS (REVIEW_ID,USER_ID) values ('Rev4','U9');
Insert into LIKED_REVIEWS (REVIEW_ID,USER_ID) values ('Rev5','U2,U4');
Insert into LIKED_REVIEWS (REVIEW_ID,USER_ID) values ('Rev14','U2,U4,U6');
Insert into LIKED_REVIEWS (REVIEW_ID,USER_ID) values ('Rev15','U3,U6,U7');
--------------------------------------------------------
--  Constraints for Table LIKED_REVIEWS
--------------------------------------------------------

  ALTER TABLE "LIKED_REVIEWS" MODIFY ("USER_ID" NOT NULL ENABLE);
  ALTER TABLE "LIKED_REVIEWS" MODIFY ("REVIEW_ID" NOT NULL ENABLE);
--------------------------------------------------------
--  Ref Constraints for Table LIKED_REVIEWS
--------------------------------------------------------

  ALTER TABLE "LIKED_REVIEWS" ADD CONSTRAINT "LIKED_REVIEWS_REVIEW_FK1" FOREIGN KEY ("REVIEW_ID")
	  REFERENCES "REVIEW" ("REVIEW_ID") ON DELETE CASCADE ENABLE;





--------------------------------------------------------
--  File created - Thursday-October-09-2014   
--------------------------------------------------------
--------------------------------------------------------
--  DDL for Table MANAGER
--------------------------------------------------------

  CREATE TABLE "MANAGER" 
   (	"MANAGER_ID" CHAR(5 BYTE), 
	"MANAGED_BY" CHAR(5 BYTE)
   ) SEGMENT CREATION IMMEDIATE 
  PCTFREE 10 PCTUSED 40 INITRANS 1 MAXTRANS 255 
 NOCOMPRESS LOGGING
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS" ;
REM INSERTING into MANAGER
SET DEFINE OFF;
Insert into MANAGER (MANAGER_ID,MANAGED_BY) values ('U14  ','null ');
Insert into MANAGER (MANAGER_ID,MANAGED_BY) values ('U15  ','U14  ');
--------------------------------------------------------
--  DDL for Index MANAGER_PK
--------------------------------------------------------

  CREATE UNIQUE INDEX "MANAGER_PK" ON "MANAGER" ("MANAGER_ID") 
  PCTFREE 10 INITRANS 2 MAXTRANS 255 
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS" ;
--------------------------------------------------------
--  Constraints for Table MANAGER
--------------------------------------------------------

  ALTER TABLE "MANAGER" ADD CONSTRAINT "MANAGER_PK" PRIMARY KEY ("MANAGER_ID")
  USING INDEX PCTFREE 10 INITRANS 2 MAXTRANS 255 
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS"  ENABLE;
  ALTER TABLE "MANAGER" MODIFY ("MANAGER_ID" NOT NULL ENABLE);
--------------------------------------------------------
--  Ref Constraints for Table MANAGER
--------------------------------------------------------

  ALTER TABLE "MANAGER" ADD CONSTRAINT "MANAGER_VILLAUSER_FK1" FOREIGN KEY ("MANAGER_ID")
	  REFERENCES "VILLAUSER" ("USERID") ON DELETE CASCADE ENABLE;



--------------------------------------------------------
--  File created - Thursday-October-09-2014   
--------------------------------------------------------
--------------------------------------------------------
--  DDL for Table RATE
--------------------------------------------------------

  CREATE TABLE "RATE" 
   (	"RATE_ID" VARCHAR2(20 BYTE), 
	"VILLA_ID" VARCHAR2(20 BYTE), 
	"STARTDATE" DATE, 
	"ENDDATE" DATE, 
	"RATE" NUMBER
   ) SEGMENT CREATION IMMEDIATE 
  PCTFREE 10 PCTUSED 40 INITRANS 1 MAXTRANS 255 
 NOCOMPRESS LOGGING
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS" ;
REM INSERTING into RATE
SET DEFINE OFF;

// Insert data into Rate table

Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat1','Vil1',to_date('01-JAN-13','DD-MON-RR'),to_date('31-AUG-13','DD-MON-RR'),150);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat2','Vil2',to_date('01-JAN-13','DD-MON-RR'),to_date('31-AUG-13','DD-MON-RR'),100);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat3','Vil3',to_date('01-JAN-13','DD-MON-RR'),to_date('31-AUG-13','DD-MON-RR'),200);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat4','Vil4',to_date('01-JAN-13','DD-MON-RR'),to_date('31-AUG-13','DD-MON-RR'),130);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat5','Vil5',to_date('01-JAN-13','DD-MON-RR'),to_date('31-AUG-13','DD-MON-RR'),120);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat6','Vil6',to_date('01-JAN-13','DD-MON-RR'),to_date('31-AUG-13','DD-MON-RR'),140);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat7','Vil7',to_date('01-JAN-13','DD-MON-RR'),to_date('31-AUG-13','DD-MON-RR'),180);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat8','Vil8',to_date('01-JAN-13','DD-MON-RR'),to_date('31-AUG-13','DD-MON-RR'),300);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat9','Vil9',to_date('01-JAN-13','DD-MON-RR'),to_date('31-AUG-13','DD-MON-RR'),80);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat10','Vil10',to_date('01-JAN-13','DD-MON-RR'),to_date('31-AUG-13','DD-MON-RR'),250);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat11','Vil11',to_date('01-JAN-13','DD-MON-RR'),to_date('31-AUG-13','DD-MON-RR'),170);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat12','Vil12',to_date('01-JAN-13','DD-MON-RR'),to_date('31-AUG-13','DD-MON-RR'),110);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat13','Vil1',to_date('01-SEP-13','DD-MON-RR'),to_date('31-DEC-13','DD-MON-RR'),120);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat14','Vil2',to_date('01-SEP-13','DD-MON-RR'),to_date('31-DEC-13','DD-MON-RR'),75);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat15','Vil3',to_date('01-SEP-13','DD-MON-RR'),to_date('31-DEC-13','DD-MON-RR'),160);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat16','Vil4',to_date('01-SEP-13','DD-MON-RR'),to_date('31-DEC-13','DD-MON-RR'),90);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat17','Vil5',to_date('01-SEP-13','DD-MON-RR'),to_date('31-DEC-13','DD-MON-RR'),80);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat18','Vil6',to_date('01-SEP-13','DD-MON-RR'),to_date('31-DEC-13','DD-MON-RR'),100);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat19','Vil7',to_date('01-SEP-13','DD-MON-RR'),to_date('31-DEC-13','DD-MON-RR'),150);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat20','Vil8',to_date('01-SEP-13','DD-MON-RR'),to_date('31-DEC-13','DD-MON-RR'),200);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat21','Vil9',to_date('01-SEP-13','DD-MON-RR'),to_date('31-DEC-13','DD-MON-RR'),50);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat22','Vil10',to_date('01-SEP-13','DD-MON-RR'),to_date('31-DEC-13','DD-MON-RR'),200);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat23','Vil11',to_date('01-SEP-13','DD-MON-RR'),to_date('31-DEC-13','DD-MON-RR'),120);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat24','Vil12',to_date('01-SEP-13','DD-MON-RR'),to_date('31-DEC-13','DD-MON-RR'),90);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat25','Vil1',to_date('01-JAN-14','DD-MON-RR'),to_date('31-AUG-14','DD-MON-RR'),180);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat26','Vil2',to_date('01-JAN-14','DD-MON-RR'),to_date('31-AUG-14','DD-MON-RR'),120);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat27','Vil3',to_date('01-JAN-14','DD-MON-RR'),to_date('31-AUG-14','DD-MON-RR'),240);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat28','Vil4',to_date('01-JAN-14','DD-MON-RR'),to_date('31-AUG-14','DD-MON-RR'),150);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat29','Vil5',to_date('01-JAN-14','DD-MON-RR'),to_date('31-AUG-14','DD-MON-RR'),150);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat30','Vil6',to_date('01-JAN-14','DD-MON-RR'),to_date('31-AUG-14','DD-MON-RR'),180);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat31','Vil7',to_date('01-JAN-14','DD-MON-RR'),to_date('31-AUG-14','DD-MON-RR'),250);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat32','Vil8',to_date('01-JAN-14','DD-MON-RR'),to_date('31-AUG-14','DD-MON-RR'),400);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat33','Vil9',to_date('01-JAN-14','DD-MON-RR'),to_date('31-AUG-14','DD-MON-RR'),110);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat34','Vil10',to_date('01-JAN-14','DD-MON-RR'),to_date('31-AUG-14','DD-MON-RR'),320);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat35','Vil11',to_date('01-JAN-14','DD-MON-RR'),to_date('31-AUG-14','DD-MON-RR'),210);
Insert into RATE (RATE_ID,VILLA_ID,STARTDATE,ENDDATE,RATE) values ('Rat36','Vil12',to_date('01-JAN-14','DD-MON-RR'),to_date('31-AUG-14','DD-MON-RR'),140);
--------------------------------------------------------
--  DDL for Index RATE_PK
--------------------------------------------------------

  CREATE UNIQUE INDEX "RATE_PK" ON "RATE" ("RATE_ID") 
  PCTFREE 10 INITRANS 2 MAXTRANS 255 
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS" ;
--------------------------------------------------------
--  Constraints for Table RATE
--------------------------------------------------------

  ALTER TABLE "RATE" ADD CONSTRAINT "RATE_PK" PRIMARY KEY ("RATE_ID")
  USING INDEX PCTFREE 10 INITRANS 2 MAXTRANS 255 
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS"  ENABLE;
  ALTER TABLE "RATE" MODIFY ("VILLA_ID" NOT NULL ENABLE);
  ALTER TABLE "RATE" MODIFY ("RATE_ID" NOT NULL ENABLE);
--------------------------------------------------------
--  Ref Constraints for Table RATE
--------------------------------------------------------

  ALTER TABLE "RATE" ADD CONSTRAINT "RATE_VILLA_FK1" FOREIGN KEY ("VILLA_ID")
	  REFERENCES "VILLA" ("VILLA_ID") ON DELETE CASCADE ENABLE;


--------------------------------------------------------
--  File created - Thursday-October-09-2014   
--------------------------------------------------------
--------------------------------------------------------
--  DDL for Table REERVATION
--------------------------------------------------------

  CREATE TABLE "REERVATION" 
   (	"RESERVATION_ID" VARCHAR2(20 BYTE), 
	"USER_ID" CHAR(5 BYTE), 
	"VILLA_ID" VARCHAR2(20 BYTE), 
	"STARTDATE" DATE, 
	"ENDDATE" DATE, 
	"COUPON_ID" VARCHAR2(20 BYTE), 
	"DEPOSIT" NUMBER
   ) SEGMENT CREATION IMMEDIATE 
  PCTFREE 10 PCTUSED 40 INITRANS 1 MAXTRANS 255 
 NOCOMPRESS LOGGING
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS" ;
REM INSERTING into REERVATION
SET DEFINE OFF;

// Insert data into Reservation table; wrongly named as Reervation

Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res1','U1   ','Vil1',to_date('02-JAN-13','DD-MON-RR'),to_date('04-JAN-13','DD-MON-RR'),'null',50);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res2','U7   ','Vil2',to_date('05-JAN-13','DD-MON-RR'),to_date('06-JAN-13','DD-MON-RR'),'null',30);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res3','U2   ','Vil3',to_date('03-FEB-13','DD-MON-RR'),to_date('07-FEB-13','DD-MON-RR'),'null',60);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res4','U4   ','Vil4',to_date('04-FEB-13','DD-MON-RR'),to_date('05-FEB-13','DD-MON-RR'),'null',39);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res5','U4   ','Vil5',to_date('06-MAR-13','DD-MON-RR'),to_date('12-MAR-13','DD-MON-RR'),'null',40);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res6','U4   ','Vil6',to_date('23-APR-13','DD-MON-RR'),to_date('25-APR-13','DD-MON-RR'),'null',42);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res7','U6   ','Vil7',to_date('29-MAY-13','DD-MON-RR'),to_date('01-JUN-13','DD-MON-RR'),'null',60);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res8','U10  ','Vil8',to_date('30-JUL-13','DD-MON-RR'),to_date('02-AUG-13','DD-MON-RR'),'null',100);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res9','U3   ','Vil9',to_date('11-AUG-13','DD-MON-RR'),to_date('12-AUG-13','DD-MON-RR'),'null',24);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res10','U2   ','Vil10',to_date('19-AUG-13','DD-MON-RR'),to_date('21-AUG-13','DD-MON-RR'),'null',75);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res11','U5   ','Vil11',to_date('15-AUG-13','DD-MON-RR'),to_date('17-AUG-13','DD-MON-RR'),'null',51);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res12','U6   ','Vil12',to_date('27-AUG-13','DD-MON-RR'),to_date('28-AUG-13','DD-MON-RR'),'null',33);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res13','U2   ','Vil1',to_date('01-SEP-13','DD-MON-RR'),to_date('03-SEP-13','DD-MON-RR'),'null',40);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res14','U5   ','Vil2',to_date('02-SEP-13','DD-MON-RR'),to_date('03-SEP-13','DD-MON-RR'),'null',25);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res15','U9   ','Vil3',to_date('15-SEP-13','DD-MON-RR'),to_date('20-SEP-13','DD-MON-RR'),'Coup3',36);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res16','U5   ','Vil4',to_date('01-OCT-13','DD-MON-RR'),to_date('03-OCT-13','DD-MON-RR'),'Coup4',27);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res17','U4   ','Vil5',to_date('15-OCT-13','DD-MON-RR'),to_date('16-OCT-13','DD-MON-RR'),'null',24);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res18','U5   ','Vil6',to_date('02-NOV-13','DD-MON-RR'),to_date('04-NOV-13','DD-MON-RR'),'null',30);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res19','U10  ','Vil7',to_date('06-NOV-13','DD-MON-RR'),to_date('07-NOV-13','DD-MON-RR'),'null',50);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res20','U9   ','Vil8',to_date('06-NOV-13','DD-MON-RR'),to_date('10-NOV-13','DD-MON-RR'),'null',60);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res21','U4   ','Vil9',to_date('10-NOV-13','DD-MON-RR'),to_date('13-NOV-13','DD-MON-RR'),'null',15);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res22','U4   ','Vil10',to_date('11-NOV-13','DD-MON-RR'),to_date('13-NOV-13','DD-MON-RR'),'null',60);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res23','U6   ','Vil11',to_date('01-DEC-13','DD-MON-RR'),to_date('04-DEC-13','DD-MON-RR'),'null',40);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res24','U5   ','Vil12',to_date('23-DEC-13','DD-MON-RR'),to_date('26-DEC-13','DD-MON-RR'),'null',30);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res25','U7   ','Vil1',to_date('12-JAN-14','DD-MON-RR'),to_date('15-JAN-14','DD-MON-RR'),'Coup1',48);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res26','U9   ','Vil2',to_date('06-JAN-14','DD-MON-RR'),to_date('07-JAN-14','DD-MON-RR'),'Coup2',34);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res27','U6   ','Vil2',to_date('05-FEB-14','DD-MON-RR'),to_date('09-FEB-14','DD-MON-RR'),'null',40);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res28','U5   ','Vil5',to_date('09-FEB-14','DD-MON-RR'),to_date('15-FEB-14','DD-MON-RR'),'null',50);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res29','U4   ','Vil8',to_date('18-MAR-14','DD-MON-RR'),to_date('19-MAR-14','DD-MON-RR'),'null',120);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res30','U2   ','Vil4',to_date('27-APR-14','DD-MON-RR'),to_date('30-APR-14','DD-MON-RR'),'null',50);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res31','U4   ','Vil10',to_date('29-MAY-14','DD-MON-RR'),to_date('01-JUN-14','DD-MON-RR'),'null',96);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res32','U9   ','Vil12',to_date('28-JUL-14','DD-MON-RR'),to_date('02-AUG-14','DD-MON-RR'),'null',42);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res33','U9   ','Vil7',to_date('11-AUG-14','DD-MON-RR'),to_date('12-AUG-14','DD-MON-RR'),'null',75);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res34','U7   ','Vil4',to_date('15-AUG-14','DD-MON-RR'),to_date('21-AUG-14','DD-MON-RR'),'null',50);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res35','U8   ','Vil8',to_date('13-AUG-14','DD-MON-RR'),to_date('17-AUG-14','DD-MON-RR'),'null',120);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res36','U3   ','Vil2',to_date('27-AUG-14','DD-MON-RR'),to_date('28-AUG-14','DD-MON-RR'),'null',40);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res37','U2   ','Vil11',to_date('20-JUN-14','DD-MON-RR'),to_date('23-JUN-14','DD-MON-RR'),'null',70);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res38','U1   ','Vil2',to_date('28-AUG-14','DD-MON-RR'),to_date('30-AUG-14','DD-MON-RR'),'null',40);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res39','U9   ','Vil1',to_date('10-APR-14','DD-MON-RR'),to_date('15-APR-14','DD-MON-RR'),'null',60);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res40','U9   ','Vil7',to_date('05-FEB-14','DD-MON-RR'),to_date('09-FEB-14','DD-MON-RR'),'null',75);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res41','U8   ','Vil7',to_date('09-FEB-14','DD-MON-RR'),to_date('15-FEB-14','DD-MON-RR'),'null',75);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res42','U5   ','Vil7',to_date('18-MAR-14','DD-MON-RR'),to_date('19-MAR-14','DD-MON-RR'),'null',75);
Insert into REERVATION (RESERVATION_ID,USER_ID,VILLA_ID,STARTDATE,ENDDATE,COUPON_ID,DEPOSIT) values ('Res43','U6   ','Vil1',to_date('12-MAY-14','DD-MON-RR'),to_date('13-MAY-14','DD-MON-RR'),'Coup5',51);
--------------------------------------------------------
--  DDL for Index REERVATION_PK
--------------------------------------------------------

  CREATE UNIQUE INDEX "REERVATION_PK" ON "REERVATION" ("RESERVATION_ID") 
  PCTFREE 10 INITRANS 2 MAXTRANS 255 
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS" ;
--------------------------------------------------------
--  Constraints for Table REERVATION
--------------------------------------------------------

  ALTER TABLE "REERVATION" ADD CONSTRAINT "REERVATION_PK" PRIMARY KEY ("RESERVATION_ID")
  USING INDEX PCTFREE 10 INITRANS 2 MAXTRANS 255 
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS"  ENABLE;
  ALTER TABLE "REERVATION" MODIFY ("COUPON_ID" NOT NULL ENABLE);
  ALTER TABLE "REERVATION" MODIFY ("VILLA_ID" NOT NULL ENABLE);
  ALTER TABLE "REERVATION" MODIFY ("USER_ID" NOT NULL ENABLE);
  ALTER TABLE "REERVATION" MODIFY ("RESERVATION_ID" NOT NULL ENABLE);
--------------------------------------------------------
--  Ref Constraints for Table REERVATION
--------------------------------------------------------

  ALTER TABLE "REERVATION" ADD CONSTRAINT "REERVATION_VILLAUSER_FK1" FOREIGN KEY ("USER_ID")
	  REFERENCES "VILLAUSER" ("USERID") ON DELETE CASCADE ENABLE;
  ALTER TABLE "REERVATION" ADD CONSTRAINT "REERVATION_VILLA_FK1" FOREIGN KEY ("VILLA_ID")
	  REFERENCES "VILLA" ("VILLA_ID") ON DELETE CASCADE ENABLE;


--------------------------------------------------------
--  File created - Thursday-October-09-2014   
--------------------------------------------------------
--------------------------------------------------------
--  DDL for Table COUPON
--------------------------------------------------------

  CREATE TABLE "COUPON" 
   (	"COUPON_ID" VARCHAR2(20 BYTE), 
	"VILLA_ID" VARCHAR2(20 BYTE), 
	"STARTDATE" DATE, 
	"ENDDATE" DATE, 
	"DISCOUNTPERCENT" NUMBER
   ) SEGMENT CREATION IMMEDIATE 
  PCTFREE 10 PCTUSED 40 INITRANS 1 MAXTRANS 255 
 NOCOMPRESS LOGGING
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS" ;
REM INSERTING into COUPON
SET DEFINE OFF;

// Insert data into coupon table

Insert into COUPON (COUPON_ID,VILLA_ID,STARTDATE,ENDDATE,DISCOUNTPERCENT) values ('Coup1','Vil1',to_date('01-SEP-13','DD-MON-RR'),to_date('31-JAN-14','DD-MON-RR'),20);
Insert into COUPON (COUPON_ID,VILLA_ID,STARTDATE,ENDDATE,DISCOUNTPERCENT) values ('Coup2','Vil2',to_date('01-SEP-13','DD-MON-RR'),to_date('31-DEC-13','DD-MON-RR'),15);
Insert into COUPON (COUPON_ID,VILLA_ID,STARTDATE,ENDDATE,DISCOUNTPERCENT) values ('Coup3','Vil3',to_date('01-SEP-13','DD-MON-RR'),to_date('31-DEC-13','DD-MON-RR'),25);
Insert into COUPON (COUPON_ID,VILLA_ID,STARTDATE,ENDDATE,DISCOUNTPERCENT) values ('Coup4','Vil4',to_date('01-SEP-13','DD-MON-RR'),to_date('31-DEC-13','DD-MON-RR'),10);
Insert into COUPON (COUPON_ID,VILLA_ID,STARTDATE,ENDDATE,DISCOUNTPERCENT) values ('Coup5','Vil1',to_date('01-JAN-14','DD-MON-RR'),to_date('31-AUG-14','DD-MON-RR'),15);
--------------------------------------------------------
--  DDL for Index COUPON_PK
--------------------------------------------------------

  CREATE UNIQUE INDEX "COUPON_PK" ON "COUPON" ("COUPON_ID") 
  PCTFREE 10 INITRANS 2 MAXTRANS 255 
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS" ;
--------------------------------------------------------
--  Constraints for Table COUPON
--------------------------------------------------------

  ALTER TABLE "COUPON" ADD CONSTRAINT "COUPON_PK" PRIMARY KEY ("COUPON_ID")
  USING INDEX PCTFREE 10 INITRANS 2 MAXTRANS 255 
  STORAGE(INITIAL 65536 NEXT 1048576 MINEXTENTS 1 MAXEXTENTS 2147483645
  PCTINCREASE 0 FREELISTS 1 FREELIST GROUPS 1
  BUFFER_POOL DEFAULT FLASH_CACHE DEFAULT CELL_FLASH_CACHE DEFAULT)
  TABLESPACE "USERS"  ENABLE;
  ALTER TABLE "COUPON" MODIFY ("VILLA_ID" NOT NULL ENABLE);
  ALTER TABLE "COUPON" MODIFY ("COUPON_ID" NOT NULL ENABLE);
--------------------------------------------------------
--  Ref Constraints for Table COUPON
--------------------------------------------------------

  ALTER TABLE "COUPON" ADD CONSTRAINT "COUPON_VILLA_FK1" FOREIGN KEY ("VILLA_ID")
	  REFERENCES "VILLA" ("VILLA_ID") ON DELETE CASCADE ENABLE;





-----------------------------------------------------------------------------------------------------------------

// DIFFERENT QUERIES TO RETRIEVE DATA//

------------------------------------------------------------------------------------------------------------------
// Query to select name of those villas that have Jacuzzi but do not allow pets.
SELECT DISTINCT NAME FROM C##ritika.VILLA VILLA
INNER JOIN C##ritika.FEATURE_VILLA  ON
VILLA.VILLA_ID = FEATURE_VILLA.VILLA_ID
INNER JOIN  C##ritika.FEATURE  ON
FEATURE_VILLA.FEATURE_ID =  FEATURE.FEATURE_ID
AND FEATURE.FEATURE_NAME='Jacuzzi'
MINUS
SELECT DISTINCT NAME FROM C##ritika.VILLA VILLA
INNER JOIN C##ritika.FEATURE_VILLA  ON
VILLA.VILLA_ID = FEATURE_VILLA.VILLA_ID
INNER JOIN  C##ritika.FEATURE  ON
FEATURE_VILLA.FEATURE_ID =  FEATURE.FEATURE_ID
AND FEATURE.FEATURE_NAME='pets allowed';
    
//Query to select users who have booked the maximum number of Villas
select u.user_name_firstname ,count(v.villa_id)
from villa v
inner join villauser u
on v.owner = u.userid
group by u.user_name_firstname
order by count(v.villa_id);

//Query to select Users who have got more than 10% of discount on rservation
select distinct(u.user_name_firstname), u.user_name_lastname
from villauser u
inner join reervation r
on u.userid = r.user_id
inner join coupon c
on r.coupon_id = c.coupon_id
where c.discountpercent > '10';
          
          
//Query to select top 3 users who booked the villas between 1st Jan to 31st December      
select * from
(select sum(r.deposit) total, u.user_name_firstname
from villauser u 
inner join reervation r
on u.userid = r.user_id
where r.startdate between to_date('01/01/2013','mm/dd/yyyy') AND to_date('12/31/2013','mm/dd/yyyy')
group by u.user_name_firstname
order by total desc)
where rownum <= 3;
         
         
         
select avg(extract(year from r.startdate) - extract(year from u.user_dob)) as age 
from villauser u
inner join reervation r
on u.userid = r.user_id
where r.startdate BETWEEN to_date('09/01/2013','mm/dd/yyyy') AND to_date('12/31/2013','mm/dd/yyyy')


select * from 
(select v.villa_id, u.userid, u.user_name_firstname, u.user_name_lastname, r.rating
from review r
inner join villa v
on r.villa_id = v.villa_id
inner join villauser u
on r.user_id = u.userid
where r.rating > (select avg(r.rating) from C##ritika.review r) 
order by r.rating desc)
where rownum <=3;


select * from (
select distinct v.villa_id, sum(r.enddate - r.startdate) as reserved_nights
from villa v
inner join reervation r
on v.villa_id = r.villa_id
where extract (year from r.startdate) > '2013'
group by v.villa_id
order by reserved_nights desc)
where rownum <= 1;


select review.user_id, count(villa_id) as number_review
from review, liked_reviews, villauser
where review.review_id = liked_reviews.review_id 
and review.user_id = villauser.userid
and rownum <=1
group by review.user_id 
order by number_review desc;

SELECT user_name_firstname, user_name_lastname, VACANCYRATIO FROM villauser U,
(SELECT T2.OWNER AS OWN_ID, (OWNED-COALESCE(RESERVED,0))/OWNED AS
VACANCYRATIO FROM
(select owner, COUNT(V2.VILLA_ID) AS RESERVED from reervation R, villa V2
where R.startdate <= to_date('08/15/2014', 'mm/dd/yyyy') and
R.enddate >=to_date('08/15/2014', 'mm/dd/yyyy') and V2.VILLA_ID LIKE
R.VILLA_ID
GROUP BY owner) T1
RIGHT JOIN
(select villa.owner,  count(villa.VILLA_ID) as owned from villa, villauser
where villauser.USERID LIKE villa.owner
group by villa.owner) T2 on T1.OWNER LIKE T2.OWNER) T3;


select u.user_name_firstname, 
u.user_name_lastname 
FROM villauser u, reervation r
where u.userid in 
(select r1.user_id 
from villauser u1, reervation r1
where r.user_id LIKE r1.user_id 
AND r.villa_id <> r1.villa_id 
AND r.startdate >= r1.startdate 
AND r.startdate <= r1.enddate);


select  villauser.user_name_firstname,villauser.user_name_lastname
from    C##ritika.villauser,
  (
 select distinct reservation1.OWNER
  from
     (select villa_id, owner, sum(enddate-startdate+1) AS RESERVATION1
    from (
   select owner , villa_id, startdate, enddate
    from  REERVATION JOIN VILLA USING(VILLA_ID)
   where STARTDATE>='1-JAN-2013' AND STARTDATE<='31-AUG-2013')
    group by VILLA_ID,OWNER) reservation1
    ,
    
    (select OWNER,VILLA_ID ,SUM(ENDDATE-STARTDATE+1) AS RESERVATION2 
    from (select OWNER,VILLA_ID,STARTDATE,ENDDATE 
    from  REERVATION JOIN VILLA USING(VILLA_ID)
    where STARTDATE>='1-JAN-2014' AND STARTDATE<='31-AUG-2014')
    group by VILLA_ID,OWNER) reservation2
  
  where (reservation1.RESERVATION1/reservation2.RESERVATION2)>=0.10 AND (reservation1.VILLA_ID=reservation2.VILLA_ID)
  
  ) OWNERIDS

where OWNERIDS.OWNER =  villauser.userid;
