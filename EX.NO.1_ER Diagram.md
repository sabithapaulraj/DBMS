# EXP NO 1: ER DIAGRAM CREATION, RELATIONAL MODEL AND SCHEMA GENERATION  
### DATE : 09/08/2023
## AIM:
<div align="justify">
   To create a ER Diagram for Bank management system or College management system using ERD Plus tool and generate the relational model with schema. 
</div>

## Algorithm
1. Create a login with https://erdplus.com.
2. Create a new ER Diagram with name
3. Create a strong entity, relation and attributes.
4. Create a weak entity, relation and attributes.
5. Specify attributes unique, multivalued and composite attributes.

### ER Diagram 
![image](https://github.com/sabithapaulraj/DBMS/assets/118343379/f75ee2fb-2112-446a-a37a-d32aa90cced1)




### Relational model
![image](https://github.com/sabithapaulraj/DBMS/assets/118343379/0e6760d7-442a-4d62-a088-d527b8eeee77)



### SQL DDL Schema 
```
CREATE TABLE PATIENT
(
PATIENT_ID INT NOT NULL,
NAME INT NOT NULL,
GENDER INT NOT NULL,
AGE INT NOT NULL,
DIAGNOSIS INT NOT NULL,
PRIMARY KEY (PATIENT_ID)
);
CREATE TABLE REGISTRATION
(
DATE INT NOT NULL,
TRANSACTIONID INT NOT NULL,
PERSONAL_DET INT NOT NULL,
ROOM_ASSIGN INT NOT NULL,
PRIMARY KEY (TRANSACTIONID)
);
CREATE TABLE DOCTOR
(
NAME INT NOT NULL,
SPECIALIZATION INT NOT NULL,
GENDER INT NOT NULL,
DOCTOR_ID INT NOT NULL,
PRIMARY KEY (DOCTOR_ID)
);
CREATE TABLE MEDICAL_RECORD
(
REPORT_ID INT NOT NULL,
DIAGNOSIS INT NOT NULL,
MEDICATIONS INT NOT NULL,
DISCHARGE INT NOT NULL,
PRIMARY KEY (REPORT_ID)
);
```

## RESULT 
<div align="justify">
Thus the ER diagram was drawn and relational diagram, SQL DDL staements are generated using ERD plus tool.
</div>
