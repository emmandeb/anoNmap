# anoNmap
anoNmap is a port scanner which utilizes Facebook's XSPA vulnerability to perform anonymous port scans.

<img src='https://i.imgur.com/yhSESMH.png' />

### How anoNmap works?
I found a XSPA vulnerability in Facebook developer API and I reported it to their security team. But for some reason, they said its a feature and not a vulnerability.
So I created anoNmap to perform anonymous port scans by using this vulnerability. I am planning to added live host detection functionality in future.

<b>What is a XSPA vulnerability?</b><br>
An application is vulnerable to Cross Site Port Attacks if the application processes user supplied URLs and does not verify/sanitize the backend response received from remote servers before sending it back to the client.
The responses, in certain cases, can be studied to identify service availability (port status, banners etc.) and even fetch data from remote services in unconventional ways.

## Installing and Using anoNmap
Open terminal and enter
```
git clone https://github.com/UltimateHackers/anoNmap/
```
Now navigate to the script by entering
```
cd anoNmap
```
Finally, run the script by entering
```
python port.py
```
You can enter an IP address, as well as a domain. URL is also supported but only if its in the form http://example.com and not http://example.com/extra.php
After entering the target, you will need to enter your facebook cooke and after that, scan will start
<p><img src='https://i.imgur.com/6fzxlHZ.png' /></p>

#### How to find my Facebook cookie?

Open your browser and navigate to <b>developers tools-->Network</b>. It is a feature that comes preinsalled in most of the modern browsers. In Firefox, you can open it by pressing <i>Ctrl + Shift + Q </i>.
After opening it, visit any page and facebook and you will see all the requests made by user in the developer panel.
Click on any request and find and copy the Cookie value from the Headers.
Note: If anoNmap shows all ports as closed then consider increasing the value of timeout.
