# QlikSense Concatenate - NoConcatenate Load

QlikSense scripting language is very similar to SQL language.

**Concatenation**

If you want to merge physically two tables as one, than you need to use
concatenate table of data.
Where
1. Fields name are the same between tables
2. Number of fields are the same between tables
QlikSense default loading is a concatenate one.

Some notes:
- The order of the fields doesn't matter.
- Where the fields name are different, it fills missing rows with `Null` value.
*If you come from a SQL background: concatenate load is equal to UNION ALL in SQL.*

Let's see an example.
The following code..
```
[EmployeeMatch]:
Load * Inline 
[EmployeeCode, Rate
WETQA0, 100
WETQA1, 80
WETQA2, 20
];

[Employee2]:
Concatenate Load * Inline 
[EmployeeCode, Rate
WETQA3, 120
WETQA4, 40
WETQA5, 50
];
```
.. will upload `EmployeeMatch` table:
|EmployeeCode|Rate|
|---|---|
|WETQA0|100|
|WETQA1|80|
|WETQA2|20|
|WETQA3| 120|
|WETQA4| 40|
|WETQA5| 50|


If you don't specify `Concatenate Load` in the code above, QlikSense will perform
a *Join* between the two tables. The Join is done on the fields that have the same
name.


If you don't want QlikSense to Concatenate two tables even if they have the same structure
(same number of fields and same field names), you have to specify `NoConcatenate Load`

