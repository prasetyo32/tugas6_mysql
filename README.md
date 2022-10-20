# tugas6_mysql
SELECT customers.customerName, customers.phone AS tlp, customers.city, payments.paymentDate, payments.amount, 
employees.firstName, employees.email, employees.jobTitle, 
offices.addressLine1, offices.phone, offices.city AS kota 
FROM customers
INNER JOIN  payments ON payments.customerNumber = customers.customerNumber 
INNER JOIN employees ON employees.employeeNumber = customers.salesRepEmployeeNumber 
INNER JOIN offices ON offices.officeCode = employees.officeCode;
