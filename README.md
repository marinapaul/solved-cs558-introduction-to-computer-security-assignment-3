Download Link: https://assignmentchef.com/product/solved-cs558-introduction-to-computer-security-assignment-3
<br>
<strong><u>Choice 1 (SSL, 10 points extra credits):</u></strong>

<strong> </strong>

<strong>This assignment can be done using C/C++/Java/Python. </strong>




You will implement a client and a server using <strong>Secure Socket Layer (SSL)</strong>.  SSL enables to establish a secure connection between the server and the client.  Upon connection, the client prompts the user to enter his/her ID and password.  After the user enters the ID and the password, the client sends the ID and the password to the server through SSL connection.  <strong> </strong>




The server maintains a file <strong><em>password</em> </strong>which has the following format:

<strong>alice 12345 </strong>

<strong>       bob   67890  </strong>

<strong> </strong>

Where alice and bob are IDs, and 12345 and 67890 are the corresponding passwords.

<strong> </strong>

After the server receives the ID and the password, the server verifies the ID and the password.  If the ID and the password are correct, then the server sends “correct ID and password” to the client and terminates. Otherwise, the server sends “incorrect ID and password” to the client and terminates.

In order to establish a connection between the client and the server. The client needs to specify the server’s domain name (e.g. remote.cs.binghamton.edu) and port number.  The port number is used to identify the server process, and is specified as a number between 1024 and 65535. In this assignment, you will hard-code the server’s port number in both the client and the server.

The client has at least one argument &lt;server_domain&gt;, which specifies the domain of the server. You can add other arguments to the client and the server if needed.

In addition, you need to generate a public key certificate in order to establish the ssh connection.  For example, in C, you can use the following command to generate certificate.

openssl req -x509 -newkey rsa:4096 -keyout key.pem -out cert.pem -days 365

If you use java, you can use keytool to generate the certificate.

<strong>Note:  </strong>




You can use any code available on the web for SSL socket programming. However, you must write your own code for the rest part of the assignment (e.g. enter and verify ID and password, open/read files).   You should also generate the certificate by yourself.  Please use your name to generate the certificate (other information can be forged).

<strong> </strong>

If you use C, please use remote.cs.binghamton.edu.  The openssl installed on bingsuns may not work. To compile your C program, please use the following command:

<strong> </strong>

gcc -Wall -w -o sslcli sslcli.c -I/usr/local/ssl/include/ -L/usr/local/ssl/lib -lssl -lcrypto gcc -Wall -w -o sslserv sslserv.c -I/usr/local/ssl/include/ -L/usr/local/ssl/lib -lssl -lcrypto




<strong><em><u>Submission guideline</u></em></strong>




<ul>

 <li>Create a directory with a unique name (e.g. p3-[userid]), which contains the source code, the certificate, and a README file.</li>

 <li><strong>README </strong>file (text file, please do not submit a .doc file) contains Ø Your name and email address.

  <ul>

   <li>Whether your code was tested on bingsuns or remote.cs.</li>

   <li>How to compile and execute your program.</li>

   <li>(Optional) Briefly describe your algorithm or anything special about your submission.</li>

  </ul></li>

</ul>

-Tar the contents of this directory using the following command.

<strong>tar –cvf p3-[userid].tar p3-[userid]</strong>

E.g. tar -cvf p3-pyang.tar p3-pyang/

<ul>

 <li>Upload the tared file you create above to mycourses.</li>

</ul>

<strong> </strong>

<h1>Choice II: (RSA Implementation)</h1>

<strong><em> </em></strong>

<strong>The assignment can be done using C/C++/Java/Python. </strong>

<strong><em> </em></strong>

In this assignment, you will write a program to generate public/private key using the RSA algorithm, given below.  Your program has two arguments p and q, which are two prime numbers.




1.Compute n=p*q and ø(n)=(p-1)(q-1), print the value of n and ø(n) using the following format:

n= &lt;value of n&gt; phi(n)= &lt;value of ø(n)&gt;




<ol start="2">

 <li>Select at random the encryption key e such that 1&lt;e&lt;ø(n) and gcd(e,ø(n)) = 1, print the value of e using the following format e= &lt;value of e&gt;</li>

</ol>




<ol start="3">

 <li>Solve the following equation to find decryption key d (0&lt;=d&lt;=n): e*d mod ø(n) = 1, and print the value of d using the following format d= &lt;value of d&gt;</li>

</ol>




Execution (e.g. C):




./rsa 11 13

<strong> </strong>

<u>Submission guideline:</u>




<ul>

 <li>Create a directory with a unique name (e.g. p3-[userid]), which contains the source code and a README file.</li>

 <li><strong>README </strong>file (text file, please do not submit a .doc file) contains Ø Your name and email address.

  <ul>

   <li>Whether your code was tested on bingsuns or remote.cs.</li>

   <li>How to compile and execute your program.</li>

   <li>(Optional) Briefly describe your algorithm or anything special about your submission that the TA should take note of.</li>

  </ul></li>

</ul>

-Tar the contents of this directory using the following command.

<strong>tar –cvf p3-[userid].tar p3-[userid]</strong>

E.g. tar -cvf p3-pyang.tar p3-pyang/

<ul>

 <li>Upload the tared file you create above to mycourses.</li>

</ul>

<strong> </strong>

<h1>Choice III: PGP</h1>

<strong> </strong>

Download a PGP software that supports <strong>confidentiality</strong> AND <strong>digital signature</strong>, and show how to use PGP to provide confidentiality and digital signature.  You can choose any email client and any PGP software.


