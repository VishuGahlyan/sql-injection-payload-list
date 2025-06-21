# sql-injection-payload-list
**SQL Injection**

Is section mein, hum batayenge ki SQL injection kya hota hai, kuch common examples discuss karenge, samjhayenge ki alag-alag types ki SQL injection vulnerabilities kaise find aur exploit ki ja sakti hain, aur akhir mein SQL injection ko kaise prevent kiya ja sakta hai, iska summary denge.

**SQL Injection (SQLi) kya hai?**

SQL injection ek web security vulnerability hai jo attacker ko application ke database ko query karne wale commands mein interfere karne ka moka deti hai. Isse attacker aisi data dekh sakta hai jo normally uske liye accessible nahi hoti. Jaise ki doosre users ka data, ya koi bhi aisa data jo application access kar sakti hai. Kai cases mein attacker is data ko modify ya delete bhi kar sakta hai, jisse application ke content ya behavior mein permanent changes aa sakte hain.

Kuch situations mein, attacker SQL injection attack ko escalate karke underlying server ya back-end infrastructure ko compromise bhi kar sakta hai, ya denial-of-service attack bhi perform kar sakta hai.

https://github.com/payloadbox/sql-injection-payload-list/blob/master/Image/sql-injection.svg

# SQL Injection Types aur Unka Description:
*1. In-band SQLi (Classic SQLi)*

Yeh sabse common aur aasaan SQL Injection attack hai. Isme attacker ek hi communication channel ka use karta hai attack karne aur result lene ke liye. Iske do main types hote hain:

 *Error-based SQLi: Is technique mein attacker database server ke error messages ka faida uthata hai, jisse database ka structure samajh sakta hai. Kabhi-kabhi sirf errors se poora database bhi pata chal sakta hai.*

  *Union-based SQLi: Yeh technique UNION SQL operator ka use karti hai, jisse do ya zyada SELECT statements ke results ko combine karke ek hi response mein bheja jaata hai.*

*2. Inferential SQLi (Blind SQLi)*

Is type mein attacker directly data nahi dekhta. Isme data web application ke through transfer nahi hota, isliye ise "blind SQL Injection" bhi kehte hain. Attack karne mein zyada time lag sakta hai, lekin yeh 
utna hi dangerous hai. Attacker payload bhej ke, web application ke response aur database ke behavior ko observe karta hai, aur database ka structure reconstruct karta hai. Iske do types hain:

*Boolean-based (content-based) Blind SQLi: Isme attacker aise queries bhejta hai jo TRUE ya FALSE return karti hain. Web page ka content change hota hai ya nahi, usse attacker pata lagata hai ki query ka result kya tha.*

  *Time-based Blind SQLi: Isme attacker aisi query bhejta hai jo database ko kuch seconds ke liye rukne par majboor karti hai. Response delay dekh ke attacker TRUE ya FALSE ka andaza lagata hai.*

*3. Out-of-band SQLi*

Yeh common nahi hota kyunki yeh depend karta hai ki database server par kuch specific features enabled hain ya nahi. Isme attacker attack aur response lene ke liye alag channels ka use karta hai. Yeh especially useful hota hai jab time-based inferential attacks reliable nahi hote.

*4. Voice Based SQL Injection*
Yeh ek naya attack method hai jo un applications mein use hota hai jahan voice commands se database access hota hai. Attacker sound ke through SQL queries bhej ke database se information nikal sakta hai.

**SQL Injection Vulnerability Scanner Tools:**
*SQLMap – Automatic SQL Injection And Database Takeover Tool*

Description: Ek bahut powerful open-source tool jo SQL injection vulnerabilities detect karne aur database takeover karne ke liye use hota hai.

**Link: https://sqlmap.org/**

*jSQL Injection – Java Tool For Automatic SQL Database Injection*

Description: Java based automatic SQL injection tool jo easy to use GUI ke saath aata hai.

**Link: https://github.com/ron190/jsql-injection**

*BBQSQL – A Blind SQL-Injection Exploitation Tool*

Description: Blind SQL Injection ke liye specially bana ek tool, jo timing based attacks support karta hai.

**Link: https://github.com/Neohapsis/bbqsql**

*NoSQLMap – Automated NoSQL Database Pwnage*

Description: NoSQL injection vulnerabilities scan aur exploit karne ke liye automation tool.

**Link: https://github.com/codingo/NoSQLMap**

*Whitewidow – SQL Vulnerability Scanner*

Description: Automated SQL injection scanner jo web applications ko scan karta hai.

**Link: https://github.com/WhitewidowScanner/whitewidow**

*DSSS – Damn Small SQLi Scanner*

Description: Lightweight aur chhota SQL injection scanner jo quick scans karta hai.

**Link: https://github.com/epinna/dsss**

*explo – Human And Machine Readable Web Vulnerability Testing Format*

Description: Web vulnerability scanning ke liye ek format aur tool, jisme SQLi bhi include hai.

**Link: https://github.com/sensepost/explo**

*Blind-Sql-Bitshifting – Blind SQL-Injection via Bitshifting*

Description: Ek specific blind SQL injection technique ke liye tool.

**Link: (Ye tool publicly limited available hai, specific repos dhoondhna padega)**

*Leviathan – Wide Range Mass Audit Toolkit*

Description: Multiple vulnerabilities scan karne ke liye toolkit, jisme SQLi scanning bhi hota hai.

**Link: https://github.com/dreadlocked/leviathan**

Blisqy – Exploit Time-based blind-SQL-injection in HTTP-Headers (MySQL/MariaDB)

Description: HTTP headers mein time-based blind SQLi exploit karne ka tool.

Link: https://github.com/epinna/blisqy
