# Experiment 2: DDL Commands

## AIM
To study and implement DDL commands and different types of constraints.

## THEORY

### 1. CREATE
Used to create a new relation (table).

**Syntax:**
```sql
CREATE TABLE (
  field_1 data_type(size),
  field_2 data_type(size),
  ...
);
```
### 2. ALTER
Used to add, modify, drop, or rename fields in an existing relation.
(a) ADD
```sql
ALTER TABLE std ADD (Address CHAR(10));
```
(b) MODIFY
```sql
ALTER TABLE relation_name MODIFY (field_1 new_data_type(size));
```
(c) DROP
```sql
ALTER TABLE relation_name DROP COLUMN field_name;
```
(d) RENAME
```sql
ALTER TABLE relation_name RENAME COLUMN old_field_name TO new_field_name;
```
### 3. DROP TABLE
Used to permanently delete the structure and data of a table.
```sql
DROP TABLE relation_name;
```
### 4. RENAME
Used to rename an existing database object.
```sql
RENAME TABLE old_relation_name TO new_relation_name;
```
### CONSTRAINTS
Constraints are used to specify rules for the data in a table. If there is any violation between the constraint and the data action, the action is aborted by the constraint. It can be specified when the table is created (using CREATE TABLE) or after it is created (using ALTER TABLE).
### 1. NOT NULL
When a column is defined as NOT NULL, it becomes mandatory to enter a value in that column.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) NOT NULL
);
```
### 2. UNIQUE
Ensures that values in a column are unique.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) UNIQUE
);
```
### 3. CHECK
Specifies a condition that each row must satisfy.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) CHECK (logical_expression)
);
```
### 4. PRIMARY KEY
Used to uniquely identify each record in a table.
Properties:
Must contain unique values.
Cannot be null.
Should contain minimal fields.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) PRIMARY KEY
);
```
### 5. FOREIGN KEY
Used to reference the primary key of another table.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size),
  FOREIGN KEY (column_name) REFERENCES other_table(column)
);
```
### 6. DEFAULT
Used to insert a default value into a column if no value is specified.

Syntax:
```sql
CREATE TABLE Table_Name (
  col_name1 data_type,
  col_name2 data_type,
  col_name3 data_type DEFAULT 'default_value'
);
```

**Question 1**

<img width="879" height="438" alt="Screenshot 2025-10-16 103523" src="https://github.com/user-attachments/assets/5391983b-2752-49c4-95f8-327e729db5fe" />

**Output:**
<img width="904" height="194" alt="Screenshot 2025-10-16 103629" src="https://github.com/user-attachments/assets/2724d34a-80cc-42e7-a615-df26c3e1b31a" />

**Question 2**

<img width="773" height="577" alt="Screenshot 2025-10-16 103900" src="https://github.com/user-attachments/assets/d8554490-70fa-421e-9a33-1897605a19b6" />


**Output:**
<img width="905" height="308" alt="Screenshot 2025-10-16 103912" src="https://github.com/user-attachments/assets/b85cec0f-e6c7-45fd-949f-daee83f94080" />


**Question 3**

<img width="709" height="425" alt="Screenshot 2025-10-16 103925" src="https://github.com/user-attachments/assets/041a50ab-d9d0-4bd5-9eb3-70fb15378554" />


**Output:**
<img width="877" height="311" alt="Screenshot 2025-10-16 103937" src="https://github.com/user-attachments/assets/0122a267-a161-4b26-8d4a-239942a33076" />


**Question 4**

<img width="783" height="442" alt="Screenshot 2025-10-16 103957" src="https://github.com/user-attachments/assets/76995afd-6d5f-41f8-b888-7c67285e2d3f" />


**Output:**
<img width="859" height="270" alt="Screenshot 2025-10-16 104006" src="https://github.com/user-attachments/assets/920bef55-0b31-4bf1-a85d-3fd9499b9a2d" />


**Question 5**

<img width="856" height="441" alt="Screenshot 2025-10-16 104024" src="https://github.com/user-attachments/assets/877b44ae-3b87-4c6c-942c-a0ef0492512e" />


**Output:**
<img width="883" height="288" alt="Screenshot 2025-10-16 104034" src="https://github.com/user-attachments/assets/12e5dfcd-8bba-477e-96e0-14bdea608c71" />


**Question 6**

<img width="874" height="384" alt="Screenshot 2025-10-16 104049" src="https://github.com/user-attachments/assets/ff3ae24a-3135-49d7-a0d0-f629857dda94" />


**Output:**

<img width="875" height="303" alt="Screenshot 2025-10-16 104059" src="https://github.com/user-attachments/assets/22a8e0f2-e92d-456e-83b4-b944304fecc9" />


**Question 7**

<img width="757" height="436" alt="Screenshot 2025-10-16 104111" src="https://github.com/user-attachments/assets/a312bd01-1fb5-4300-a4bd-402de67bbf95" />


**Output:**
<img width="882" height="329" alt="Screenshot 2025-10-16 104120" src="https://github.com/user-attachments/assets/347538e6-58d9-4dea-a735-afb7b983ba4c" />



**Question 8**

<img width="713" height="505" alt="Screenshot 2025-10-16 104201" src="https://github.com/user-attachments/assets/b1cb0189-8598-4eb7-9280-00a3763eee6f" />


**Output:**
<img width="873" height="283" alt="Screenshot 2025-10-16 104222" src="https://github.com/user-attachments/assets/d8d82533-cf7f-49e1-ae30-34a1e3e507e7" />



**Question 9**

<img width="805" height="565" alt="Screenshot 2025-10-16 104241" src="https://github.com/user-attachments/assets/dd2b057d-a891-4105-8ded-50baa2fe31e1" />


**Output:**
<img width="861" height="341" alt="Screenshot 2025-10-16 104253" src="https://github.com/user-attachments/assets/494e2c0e-2a5e-4bb4-b283-12b74a81b1ff" />


**Question 10**

<img width="879" height="438" alt="Screenshot 2025-10-16 103523" src="https://github.com/user-attachments/assets/7e7f5872-801f-4dc4-b877-05c5e3148535" />

**Output:**
<img width="904" height="194" alt="Screenshot 2025-10-16 103629" src="https://github.com/user-attachments/assets/c59b68e4-6208-4027-9eeb-cb833a5ae593" />



## RESULT
Thus, the SQL queries to implement different types of constraints and DDL commands have been executed successfully.
