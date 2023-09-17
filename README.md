<p align="center">
<img src="https://i.imgur.com/9Ab7VoK.png" height="80%" width="80%" alt="Patriot CTF"/>
<p/>
<h1>PatriotCTF2023: Multi-numeral (Cryptography)</h1>
PatriotCTF 2023 is a Jeopardy-style CTF competition organized by the MasonCC (Mason Competitive Cyber) club at George Mason University.
<br/>
<br/>
<h2>Challenge Description:</h2> 
<p align="center">
This challenge provides a file named 'Challenge.txt', as well as the prompt 'Much numbers, many wows.' 
<br/>
<br/>
Flag format: <strong>PCTF{}</strong>
<br/>
<br/>
<img src="https://i.imgur.com/e0r6rNd.png" height="80%" width="80%" alt="Challenge.txt"/>   
<br/>
<br/>
<h2>Solution:</h2> 
<p align="center">
The provided file, 'Challenge.txt', appears to be binary values. I navigated to https://cryptii.com/pipes/binary-decoder, which is an online platform used for cryptographic tools such as encoding and decoding data. I entered in the binary data and got the following output:  
<br />
<br />
<img src="https://i.imgur.com/bkjZqA8.png" height="80%" width="80%" alt="Decimal Output"/> 
<br />
<br />
This output appeared to be decimal values, so I entered in these values again and selected the seperator as 'Decimal'. The platform then returned the following output (right): 
<br />
<br />
<img src="https://i.imgur.com/ePeQQOF.png" height="90%" width="90%" alt="Hex Output"/> 
<br />
<br />
The outputted values appeared to be hex values, which I ran through the decoder once more to retrieve the following values (right): 
<br/>
<br/>
<img src="https://i.imgur.com/xzgfS92.png" height="90%" width="90%" alt="Base64 Output"/>
<br/>
<br/>
The decoded hex values then returned what appeared to be Base64 values. I then wrote a simple Python script to decode Base64 using the 'base64' module in Python. For more information on the 'base64' module in Python, refer to the following link: https://docs.python.org/3/library/base64.html. 
<br/>
<br/>
<img src="https://i.imgur.com/meQJzvC.png" height="70%" width="70%" alt="Python Decoder"/>
<br/>
<br/>
The script begins by importing the 'base64' module. It then uses the 'base64.b64decode()' built-in function in Python, as well as the retrieved Base64 string from the hex values to decode the string. The 'flag' variable converts the binary data into a string. The script then prints out the following result:
<br/>
<br/>
<img src="https://i.imgur.com/sAAAKLI.png" height="60%" width="60%" alt="Flag"/>
 <br/>
 <br/>
The flag has been retrieved! 
<h2>Key takeaways:</h2>
<p align="center">
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
