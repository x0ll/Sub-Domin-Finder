import socket
from termcolor import colored
import colorama
import argparse

colorama.init()

banar = r"""
____        _         _                 _       
/ ___| _   _| |__   __| | ___  _ __ ___ (_)_ __  
\___ \| | | | '_ \ / _` |/ _ \| '_ ` _ \| | '_ \ 
 ___) | |_| | |_) | (_| | (_) | | | | | | | | | |
|____/ \__,_|_.__/ \__,_|\___/|_| |_| |_|_|_| |_|

 _____ _           _           
|  ___(_)_ __   __| | ___ _ __ 
| |_  | | '_ \ / _` |/ _ \ '__|
|  _| | | | | | (_| |  __/ |   
|_|   |_|_| |_|\__,_|\___|_|   
"""

print(colored(banar, 'yellow'))
print(colored('@rc.j5', 'yellow'))
print(colored('@rc.j5', 'yellow'))
print()

# seating
parser_s = argparse.ArgumentParser()
parser_s.add_argument("-d", "--domain", help="domain name to search (e.g. - google.com)", required=True)
parser_s.add_argument("-l", "--list", help="Subdomains list file path (e.g.- subdomainList.txt)", required=True)
parser_s.add_argument("-O", "--out", help="Output file to save results (e.g.- googleSubs.csv)")
parser_s.add_argument("-v", "--verbose", help="Show not found subdomains too", action="store_true")
args = parser_s.parse_args()

# the get the IP
def get_theIP_Addr(domain_name):
    try:
        IP = socket.gethostbyname(domain_name)
        return IP
    except socket.gaierror:
        return None

# Open the list file
with open(args.list, 'r') as the_subdomains_list:
    for sub in the_subdomains_list.readlines():
        sub = sub.strip()
        if not sub:
            continue
        domain = f"{sub}.{args.domain}"
        IP = get_theIP_Addr(domain)

        if IP is not None:
            print(f"{colored('[+] FOUND:', 'green')} {domain:<25}{IP}")
        else:
            if args.verbose:
                print(f"{colored('[-] NOT FOUND:', 'red')} {domain:<25}{IP}")

        # Save to file if selected
        if args.out:
            with open(args.out, 'a') as out_file:
                if IP is not None:
                    out_file.write(f"[+] FOUND: {domain:<25} {IP}\n")
                elif args.verbose:
                    out_file.write(f"[-] NOT FOUND: {domain:<25}\n")
