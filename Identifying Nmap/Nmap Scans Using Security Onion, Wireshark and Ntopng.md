So the purpose of this project was to identify nmap and hydra scans and attacks using security tools like Security Onion, Wireshark, and NetFlow (ntopng). The first thing I did was make sure I was in my own local sandbox environment. The next thing I did was get these different tools up and running. Once everything was operational, nmap scans commenced. The first scan that was used was a simple port scan; the command was "sudo nmap -p 1-10000," followed by the IP address of the machine I was targeting. This command basically scans for any open ports from 1 to 10,000. Upping the antee, the hydra tool was let loose like a mad dog on the target machine! Hydra is basically a tool to crack or guess logins and passwords. The command used for this was "hydra -l <login_name> -P" followed by the path to the file containing the list of passwords, the protocol you want to test (ssh in this case), and the target IP address.



So did we get something juicy? First, let's check Security Onion.

![Security Onion](https://github.com/oaotwinn/Cybersecurity-Projects/blob/0189172cb7e24c2c4910a0faddaaaeb0c9eae182/Identifying%20Nmap/SecurityOnion1.png)

As you can see, we had a lot of failed authentication and user login attempts, followed by some dope stiff arms by the firewall. Tools like Security Onion and Kibana use automation to sniff out anomolies and indicators of attack like these. They compile data from all different types of logs including syslog, DHCP, DNS, and proxies. Let's head over to Wireshark!

![Wireshark](https://github.com/oaotwinn/Cybersecurity-Projects/blob/a17270ee9c69b9d9e14559fbd9e9d21aacbc6373/Identifying%20Nmap/Wireshark1.png)

Now we're talking! This thing lit up like a Christmas tree! The first sign of trouble was all that RED. Now, red is not necessarily a sign that something is wrong, but it is definitely something worth paying attention to. Let's dive a little deeper. We also notice that we have a lot of SYN packets without any ACK packets responding. Our knowledge of the TCP handshake tells us that the order of operation should be SYN, SYN/ACK, ACK. In this case, we just got a whole bunch of SYN and RST packets without any acknowledgements. HUGE RED FLAG!!! Another thing to notice is the high frequency in a short amount of time, very very sus. Let's move on to NetFlow.

![Ntopng](https://github.com/oaotwinn/Cybersecurity-Projects/blob/6e7dad314ee8082fc5020d3e8583896dfbb7f85d/Identifying%20Nmap/ntopng1.png)

I kind of struggled with this part ngl. I think it was a combination of me not having the best grasp when it comes to ntopng (if you are a hiring manager reading this, just pretend I never said that please) and that NetFlow is not as detailed when it comes to reviewing data like Wireshark. Normally, a high amount of flows is definitely something to look out for, and I will say that when looking through Ntopng, I did see a lot of attempts to communicate with a huge number of destination ports. Which is, as we know by now, is a port scan.



This concludes the cybersecurity recon mission. It looks like there will be no "Hail Hydra" today, not on my watch!
