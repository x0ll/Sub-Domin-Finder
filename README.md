# Sub-Domin-Finder
Subdomain Finder is a simple open-source Python tool for discovering active subdomains of a target domain. It uses DNS resolution to identify valid subdomains, highlights results with color, supports file output, and helps in reconnaissance, security testing, and bug bounty research.

---

##  About

**Subdomain Finder** is a lightweight script that checks which subdomains of a target domain are active.  
It reads subdomains from a wordlist and tries to resolve their IPs using Python’s built-in `socket` module.  
Color-coded output (green = found, red = not found) makes results easy to read and analyze.

---

##  Tool Preview
<img width="493" height="232" alt="image" src="https://github.com/user-attachments/assets/b89043b0-6351-4e3d-a9f4-2f6ae2a9340b" />

---

##  How to Use

Run the tool from your terminal using:

```bash
python subdomain_finder.py -d example.com -l subs.txt -O results.txt -v
```

---

 ##  Help Menu

The following image shows the output of the help command for the tool: 

<img width="1043" height="392" alt="image" src="https://github.com/user-attachments/assets/d8a9d441-b7a8-4db4-afdf-8dbdf6b5c439" />

```bash
python subdomain_finder.py -h

```
---
##  Subdomain List File


<img width="615" height="502" alt="image" src="https://github.com/user-attachments/assets/8814d38a-8d0c-4c75-af01-158fb65d52fb" />

Before running the tool, create a simple text file that contains your subdomains list.  
Each subdomain should be written on a new line, like this 👇

``` txt
www
mail
ftp
blog
test
api
```
---
##   Example Output
<img width="617" height="514" alt="image" src="https://github.com/user-attachments/assets/f30e7b20-9dc7-4786-8fdc-69fc18ea0585" />




---

##  Conclusion

Thank you for using **Subdomain Finder Tool**!  
I hope it helps you in your security testing and reconnaissance projects.  
If you like this tool, consider giving it a ⭐ on GitHub — your support means a lot! 💪  

📸 Follow me on Instagram: [@rc.j5]



