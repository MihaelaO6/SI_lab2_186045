#**Втора лабораториска вежба по Софтверско Инженерство**

##**Михаела Обадиќ индекс: 186045**

### Група на код: 4

### Control flow graph:

![graph1](https://user-images.githubusercontent.com/61661727/83976211-f096ec80-a8f8-11ea-8ebe-a08cff025587.png)

![function_silab2](https://user-images.githubusercontent.com/61661727/83976222-00163580-a8f9-11ea-8192-fa7da2069f24.png)


### Цикломатска комплексност
Цикломатската комплексност е 7 и ја добив со Е-V+2,ребра Е = 23 и бројот на јазли V = 18 додадов 2. Односно 23-18+2=7. Истиот број може да се добие со броење на регионите на графот.

### Тест случаи според критериумот Multiple condtition

Ги разгледуваме деловите каде што има  if statement и логички оператори. <br/>
Во функцијата има 3 if-а со логички оператори. Најпрво го разгледуваме првиот услов и тој е : <br/>
***if (user.getUsername()!=null && user.getPassword()!=null)** (кај мене обележан //3) <br/>
Тој содржи логички оператор and &&. <br/>
Можни сценарија за првиот if се: <br/>
1.true && true -целиот израз е точен  <br/>
2.true && false- изразот е неточен бидејќи вториот дел е неточен <br/>
3. false && true/false -тука е исто дали вториот дел ке биде true или  false бидејќи првиот дел е false па целиот израз ќе биде false.  <br/>
Ако овој if  е точен ќе дојде да се разгледа и вториот if. <br/>
Случај 1: Ако user.getUsername() има вредност "obMi@c", а  user.getPassword() има вредносѕ null изразот ќе има вредност false односно ова е второто сценарио.  <br/>
Случај 2:Ако user.getUsername() е null, user.getPassword() ќе биде исто дали е true или false односно ова е третото сценарио. <br/>
Случај 3:Ако user.getUsername() е "obMi@c" и user.getPassword() е "mmmo1" значи името и лозинката се различни од null односно ова е првото сценарио.Бидејќи првиот if е true може да преминеме на вториот if кој што е :  <br/>
***if (!passwordLower.contains(user.getUsername().toLowerCase()) && password.length()>=8)*** (кај мене обележан //6) <br/>
За овој if имаме исто така 3 можни сценарија:  <br/>
1.true && true -целиот израз е точен  <br/>
2.true && false- изразот е неточен бидејќи вториот дел е неточен <br/>
3. false && true/false -тука е исто дали вториот дел ке биде true или  false бидејќи првиот дел е false па целиот израз ќе биде false. <br/>
Во третиот случај е опфатено второто сценарио т.е. лозинката не го содржи името, но има помалку од 8 карактери. <br/>
Случај 4:Ако user.getUsername() е "obMi@c", а user.getPassword() е "obMi@cik" значи лозинката го содржи името и според тоа целиот израз е неточен, тука е опфатено третото сценарио. <br/>
Случај5: Ако user.getUsername() е "obMi@c" а user.getPassword() е "mihaeМihaelala" значи лозинката не го содржи името и е подолга од 7 карактери. Ова е првото сценарио и изразот е точен, значи може да се оди на третиот if.Тој е: <br/>
***if (digit && upper && special)*** (кај мене обележан //15)  <br/>
Тука се можни 4 сценарија: <br/>
1.true && true && true -целиот израз е точен <br/>
2.true && false && false/true- изразот е неточен бидејќи вториот дел е неточен а после него не е важно каков е третиот дел(односно лозинката има бројки,но не големи букви и специјални знаци)  <br/>
3.false && false/true && false/true -тука е исто дали вториот дел и третиот дел ке бидат true или  false бидејќи првиот дел е false па целиот израз ќе биде false. <br/>
4.true && true && false значи лозинката има бројки, големи букви и специјални знаци.  <br/>
Случај 6: Ако user.getUsername() е "obMi@c" а user.getPassword() е "k@1408200mi" значи лозинката има бројки а нема големи букви и тука е опфатено второто сценарио. <br/>
Во случајот 5 е опишано третото сценарио.  <br/>
Случај 7: Ако user.getUsername е "obMi@S" а user.getPassword() е "MIh182jak91" и тука е опфатено првото сценарио. <br/>
