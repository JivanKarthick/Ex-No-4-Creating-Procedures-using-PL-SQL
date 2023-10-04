# Ex. No: 4 Creating Procedures using PL/SQL

### AIM: To create a procedure using PL/SQL.

### Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create a procedure named as insert_employee data.
3. Inside the procdure block, write the query for inserting the values into the employee table.
4. End the procedure.
5. Call the insert_employee data procedure to insert the values into the employee table.
6. Display the employee table

### Program:
```
CREATE TABLE empq(
  2          empid NUMBER,
  3          empname VARCHAR(10),
  4          dept VARCHAR(10),
  5          salary NUMBER
  6          );

SQL> CREATE OR REPLACE PROCEDURE emp_data AS
        BEGIN      INSERT INTO empq(empid,empname,dept,salary)
        values(1,'dinesh','MD',10000000);
        INSERT INTO empq(empid,empname,dept,salary)
        values(2,'rathish','HR',500000);
        INSERT INTO empq(empid,empname,dept,salary)
        values(3,'faizal','IT',200000);
        COMMIT;
      FOR emp_rec IN (SELECT * FROM empq)LOOP
      DBMS_OUTPUT.PUT_LINE('EMPLOYEE ID:'||emp_rec.empid||',EMPLOYEE NAME:'|| emp_rec.empname||
      ',DEPARTMENT:'||emp_rec.dept||',SALARY:'||emp_rec.salary);
      END LOOP;
      END;
     /
 ```
### Output:
![image](https://github.com/JivanKarthick/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/121165867/765d065b-7cc8-40ec-8ce5-d5defb99b915)



### Result:
THE PROGRAM HAS BEEN IMPLEMENTED SUCCESSFULLY
