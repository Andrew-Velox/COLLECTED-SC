###############################################
### *--> script dump ID <--* ###                                                           #
### *--> rekod boleh asal contact author <--* ###                             #
### *--> author by hikmat <--* ###                                                       #
### *--> coding python 3 <--* ###                                                        #
###############################################
import requests,bs4,os,sys,json,datetime,time,rich,re,random

from concurrent.futures import ThreadPoolExecutor as tren
from bs4 import BeautifulSoup as sop
from rich.table import Table as table
from rich.console import Console as console
from rich.console import Group as grup_rich
from rich.panel import Panel as panel
from rich.markdown import Markdown as mark
from rich.columns import Columns as columns
from rich.text import Text as text_rich
from rich import print as vprint

FR = {'1':'januari','2':'februari','3':'maret','4':'april','5':'mei','6':'juni','7':'juli','8':'agustus','9':'september','10':'oktober','11':'november','12':'desember'}
tgl = datetime.datetime.now().day
bln = FR[(str(datetime.datetime.now().month))]
thn = datetime.datetime.now().year
sekarang = str(tgl)+"-"+str(bln)+"-"+str(thn)
id = []
loop = 0
m_fb = 'm.facebook.com'
url_businness = "https://business.facebook.com"
ua_business = "Mozilla/5.0 (Linux; Android 8.1.0; MI 8 Build/OPM1.171019.011) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/69.0.3497.86 Mobile Safari/537.36"
web_fb = "https://www.facebook.com/"
head_grup = {"user-agent": "Mozilla/5.0 (Linux; Android 10; Mi 9T Pro Build/QKQ1.190825.002; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/88.0.4324.181 Mobile Safari/537.36 [FBAN/EMA;FBLC/id_ID;FBAV/239.0.0.10.109;]"}

def clear():
	os.system('clear')
def jalan(xnxx):
	for ewe in xnxx + '\n':
		sys.stdout.write(ewe);sys.stdout.flush();time.sleep(0.05)
		
## [ Warna² Random ] ##

P = "\x1b[0;97m" # Putih
M = "\x1b[0;91m" # Merah
H = "\x1b[0;92m" # Hijau
K = "\x1b[0;93m" # Kuning
B = "\x1b[0;94m" # Biru
U = "\x1b[0;95m" # Ungu
O = "\x1b[0;96m" # Biru Muda
N = "\033[0m"    # Warna Mati
o = '\033[1;36m'
###----------[ COLOR FOR RICH ]---------- ###
Z2 = "[#000000]" # HITAM
M2 = "[#FF0000]" # MERAH
M3 = "#FF0000" # MERAH
H2 = "[#00FF00]" # HIJAU
H3 = "#00FF00" # HIJAU
K2 = "[#FFFF00]" # KUNING
K3 = "#FFFF00" # KUNING
B2 = "[#00C8FF]" # BIRU
B3 = "#00C8FF" # BIRU
U2 = "[#AF00FF]" # UNGU
U3 = "#AF00FF" # UNGU
N2 = "[#FF00FF]" # PINK
N3 = "#FF00FF" # PINK
O2 = "[#00FFFF]" # BIRU MUDA
O3 = "#00FFFF" # BIRU MUDA
P2 = "[#FFFFFF]" # PUTIH
P3 = "#FFFFFF" # PUTIH
J2 = "[#FF8F00]" # JINGGA
J3 = "#FF8F00" # JINGGA
A2 = "[#AAAAAA]" # ABU-ABU
warna_warni_rich=random.choice([J3,K3,H3,P3,O3,N3,U3,B3,M3])
garis = f" {P}[{H}•{P}]"

def banner():
	os.system("clear")
	print(f"""
\t________      _____   ___________
\t\______ \    /     \  \_   _____/
 \t|    |   \  /  \ /  \  |    __)  
 \t|    `    \/    Y    \ |     \   
\t/_______  /\____|__  / \___  /   
        \t\/         \/      \/    • Dump Multi Fast •
\t{garis} author by : HikmatXD""")

def cek_cookie():
	try:
		token  = open('token.txt','r').read()
		cookie = {'cookie':open('cookie.txt','r').read()}
		try:
			token  = open('token.txt','r').read()
			cookie = {'cookie':open('cookie.txt','r').read()}
			kook = open('cookie.txt','r').read()
			get  = requests.Session().get('https://graph.facebook.com/me?fields=name,id&access_token=%s'%(token),cookies=cookie)
			gut = json.loads(get.text)
			xname = gut["name"]
			x=f"{P2}{kook}"
			vprint(panel(x,style=f"{H3}"))
			x=f"{P2}{token}"
			vprint(panel(x,style=f"{H3}"))
			print("")
			x=f"{P2}cookie {H2}{xname} {P2}belum invalid"
			vprint(panel(x,style=f"{H3}"))
			input(f"{garis} enter untuk ke menu ")
			menu()
		except (KeyError):
			x=f"{P2}cookie kadaluarsa"
			vprint(panel(x,style=f"{H3}"))
			os.system('rm -rf cookie.txt')
			os.system('rm -rf token.txt')
			login()
		except requests.exceptions.ConnectionError:
			x=f"{P2}koneksi internet bermasalah"
			vprint(panel(x,style=f"{H3}"))
			exit()
	except IOError:
		login()

def login():
	banner()
	x=f"{P2}halo pengguna script dump multi fast :)\n{P2}silahkan pilih fitur login cookie untuk melanjutkan ke menu dump multi fast.. klo tidak mengerti apa² bisa ketik {M2}help {P2}untuk meminta bantuan !!"
	vprint(panel(x,style=f"{H3}"))
	print("")
	x=f"{P2}[01] login with cookie\n{P2}[02] report bug script\n{P2}[{M2}00{P2}] exit "
	vprint(panel(x,style=f"{H3}"))
	cukuf = input(f" {P}[{H}•{P}] pilih : {H}")
	if cukuf in ["help","Help","HELP"]:
		print("")
		x=f"{P2}whatsapp admin *--> {H2}082115413282 {P2}harap chat klo ada kepentingan yang mau disampaikan ke author dmf\nini klo gak bisa diarahin ke whastapp admin yakk"
		vprint(panel(x,style=f"{H3}"))
		print("")
		x=f"{P2}sedang diarahkan ke whastapp author"
		vprint(panel(x,style=f"{H3}"))
		os.system('xdg-open https://wa.me/+6282115413282?text=bang+cara+pake+script+abang+kek+mana?')
		input(f" {P}[{H}•{P}] kembali")
		login()
	elif cukuf in ["1","01"]:
		login_cookie()
	elif cukuf in ["2","02"]:
		print("")
		x=f"{P2}whatsapp admin *--> {H2}082115413282 {P2}harap chat klo memang ada yang error\nini klo gak bisa diarahin ke whastapp admin yakk"
		vprint(panel(x,style=f"{H3}"))
		print("")
		x=f"{P2}sedang diarahkan ke whastapp author"
		vprint(panel(x,style=f"{H3}"))
		os.system('xdg-open https://wa.me/+6282115413282?text=bang+script+mu+itu+ada+yang+error!!')
		input(f" {P}[{H}•{P}] kembali")
		login()
	elif cukuf in ["0","00"]:
		exit()
	else:
		print("")
		jalan(f"{garis} isi yang benar!! ")
		login()

def login_cookie():
	print("")
	#testi_ua()
	x = f"{P2}jangan pake akun pribadi!! harus pake akun tumbal untuk ambil cookie"
	vprint(panel(x,style=f"{H3}"))
	cookie = str(input(f"{garis} masukkan cookie :"+H+" "))
	with requests.Session() as xyz:
		try:
			jalan(f"{garis} sedang proses mohon tunggu ")
			get_tok = xyz.get(url_businness+'/business_locations',headers = {"user-agent":ua_business,"referer": web_fb,"host": "business.facebook.com","origin": url_businness,"upgrade-insecure-requests" : "1","accept-language": "id-ID,id;q=0.9,en-US;q=0.8,en;q=0.7","cache-control": "max-age=0","accept":"text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8","content-type":"text/html; charset=utf-8"},cookies = {"cookie":cookie})
			token = re.search("(EAAG\w+)", get_tok.text).group(1)
			open('cookie.txt','w').write(cookie) 
			open('token.txt','w').write(token)
			x=f"{P2}{token}"
			vprint(panel(x,style=f"{H3}"))
			input(f"{garis} enter untuk ke menu ")
			menu()
		except requests.exceptions.ConnectionError:
			x=f"{P2}koneksi internet bermasalah"
			vprint(panel(x,style=f"{H3}"))
		except (KeyError,IOError):
			x=f"{P2}{cookie} invalid"
			vprint(panel(x,style=f"{H3}"))
			os.system("rm -rf cookie.txt")
			os.system("rm -rf token.txt")
			login()
	
def menu():
	banner()
	try:EwePaksa = requests.get("http://ip-api.com/json/").json()
	except:EwePaksa = {'-'}
	try:IP = EwePaksa["query"]
	except:IP = {'-'}
	try:nibba = EwePaksa["country"]
	except:nibba = {'-'}
	try:rasis_Z_K_= EwePaksa["isp"]
	except:rasis_Z_K_ = {'-'}
	try:rasis_Z_K_X_= EwePaksa["city"]
	except:rasis_Z_K_X_ = {'-'}
	try:rasis_Z_K_X_R_= EwePaksa["timezone"]
	except:rasis_Z_K_X_R_ = {'-'}
	try:rasis_Z_K_X_R_H_= EwePaksa["countryCode"]
	except:rasis_Z_K_X_R_H_ = {'-'}
	try:rasis_Z_K_X_R_H_M_= EwePaksa["regionName"]
	except:rasis_Z_K_X_R_H_M_ = {'-'}
	try:rasis_Z_K_X_R_H_M_P_= EwePaksa["as"]
	except:rasis_Z_K_X_R_H_M_P_ = {'-'}
	token  = open('token.txt','r').read()
	cookie = {'cookie':open('cookie.txt','r').read()}
	get  = requests.Session().get('https://graph.facebook.com/me?fields=name,id&access_token=%s'%(token),cookies=cookie)
	jsx = json.loads(get.text)
	nama = jsx["name"]
	tumbal_id = jsx["id"]
	xn = requests.Session().get('https://graph.facebook.com/me?access_token=%s'%(token),cookies=cookie)
	x = json.loads(xn.text)
	lis = x["link"]
	try:co = x["email"]
	except (KeyError,IOError):
		co = M+"-"+P
	try:pko = x["birthday"]
	except (KeyError,IOError):
		pko = M+"-"+P
	try:no_kep = x["mobile_phone"]
	except (KeyError,IOError):
		no_kep = M+"-"+P
	try:lok = x["locale"]
	except (KeyError,IOError):
		lok = M+"-"+P
	print("")
	x=f"{P2}ini bukan script crack fb!!.. ini cuman dump id nya doang biar simple..\nnanti next crack fb dari file dump!!"
	vprint(panel(x,style=f"{H3}"))
	print("")
	x=f"{P2} ┌─ selamat datang {K2}{nama}\n{P2} │ └─ tanggal lahirmu : {H2}{pko}\n{P2} │ └─ ID kamu : {H2}{tumbal_id}\n{P2} │ └─ IP kamu : {H2}{IP}\n{P2} │ ┌─ negara kamu : {H2}{nibba}\n{P2} └─ tanggal sekarang : {H2}{sekarang}"
	vprint(panel(x,style=f"{H3}"))
	print("")
	x=f"{P2}[01] dump id public\n{P2}[02] dump id followers\n{P2}[03] dump id post likes\n{P2}[04] dump id public v2\n{P2}[05] dump id followers v2\n{P2}[06] check info akun target\n{P2}[07] beri tanggapan script ini\n{P2}[08] report bug script\n{P2}[09] tracked ip\n{P2}[{M2}00{P2}] exit/hapus cookie"
	vprint(panel(x,style=f"{H3}"))
	hikmat = input(f"{garis} pilih : {H}")
	if hikmat in ["1","01"]:
		dump_public()
	elif hikmat in ["2","02"]:
		dump_followers()
	elif hikmat in ["3","03"]:
		dump_post()
	elif hikmat in ["4","04"]:
		dump_publicv2() 
	elif hikmat in ["5","05"]:
		dump_followersv2()
	elif hikmat in ["6","06"]:
		check_ingfo_akun()
	elif hikmat in ["7","07"]:
		print("")
		f = input(f"{garis} berapa bintang untuk script dump multi fast kami : {H}")
		if f in ["1"]:
			print("")
			x=f"{P2}terimakasih telah memberi bintang {H2}1 {P2}untuk script kami >< semoga saja kamu sehat² selalu amin :) "
			vprint(panel(x,style=f"{H3}"))
			input(f"{garis} enter untuk kembali ")
			menu()
		elif f in ["2"]:
			print("")
			x=f"{P2}terimakasih telah memberi bintang {H2}2 {P2}untuk script kami >< semoga saja kamu sehat² selalu amin :) "
			vprint(panel(x,style=f"{H3}"))
			input(f"{garis} enter untuk kembali ")
			menu()
		elif f in ["3"]:
			print("")
			x=f"{P2}terimakasih telah memberi bintang {H2}3 {P2}untuk script kami >< semoga saja kamu sehat² selalu amin :) "
			vprint(panel(x,style=f"{H3}"))
			input(f"{garis} enter untuk kembali ")
			menu()
		elif f in ["4"]:
			print("")
			x=f"{P2}terimakasih telah memberi bintang {H2}4 {P2}untuk script kami >< semoga saja kamu sehat² selalu amin :) "
			vprint(panel(x,style=f"{H3}"))
			input(f"{garis} enter untuk kembali ") 
			menu()
		elif f in ["5"]:
			print("")
			x=f"{P2}terimakasih telah memberi bintang {H2}5 {P2}untuk script kami >< semoga saja kamu sehat² selalu amin :) "
			vprint(panel(x,style=f"{H3}"))
			input(f"{garis} enter untuk kembali ")
			menu()
		elif f in ["6"]:
			print("")
			x=f"{P2}terimakasih telah memberi bintang {H2}6 {P2}untuk script kami >< semoga saja kamu sehat² selalu amin :) "
			vprint(panel(x,style=f"{H3}"))
			input(f"{garis} enter untuk kembali ")
			menu()
		elif f in ["7"]:
			print("")
			x=f"{P2}terimakasih telah memberi bintang {H2}7 {P2}untuk script kami >< semoga saja kamu sehat² selalu amin :) "
			vprint(panel(x,style=f"{H3}"))
			input(f"{garis} enter untuk kembali ")
			menu()
		elif f in ["8"]:
			print("")
			x=f"{P2}terimakasih telah memberi bintang {H2}8 {P2}untuk script kami >< semoga saja kamu sehat² selalu amin :) "
			vprint(panel(x,style=f"{H3}"))
			input(f"{garis} enter untuk kembali ")
			menu()
		elif f in ["9"]:
			print("")
			x=f"{P2}terimakasih telah memberi bintang {H2}9 {P2}untuk script kami >< semoga saja kamu sehat² selalu amin :) "
			vprint(panel(x,style=f"{H3}"))
			input(f"{garis} enter untuk kembali ")
			menu()
		elif f in ["10"]:
			print("")
			x=f"{P2}terimakasih telah memberi bintang {H2}10 {P2}untuk script kami >< semoga saja kamu sehat² selalu amin :) "
			vprint(panel(x,style=f"{H3}"))
			input(f"{garis} enter untuk kembali ")
			menu()
		else:
			print("") 
			jalan(f"{garis} isi yang benar")
			menu()
	elif hikmat in ["8","08"]:
		print("")
		x=f"{P2}whatsapp admin *--> {H2}082115413282 {P2}harap chat klo memang ada yang error\nini klo gak bisa diarahin ke whastapp admin yakk"
		vprint(panel(x,style=f"{H3}"))
		print("")
		x=f"{P2}sedang diarahkan ke whastapp author"
		vprint(panel(x,style=f"{H3}"))
		os.system('xdg-open https://wa.me/+6282115413282?text=bang+script+mu+itu+ada+yang+error!!')
		input(f" {P}[{H}•{P}] kembali")
		menu()
	elif hikmat in ["9","09"]:
		print("")
		x=f"{P2}[01] tracked ip sendiri\n[02] tracked ip target\n{P2}[{M2}00{P2}] kembali"
		vprint(panel(x,style=f"{H3}"))
		pilpil()
	elif hikmat in ["0","00"]:
		print("")
		x=f"{P2}[01] hapus cookie\n{P2}[02] exit\n{P2}[{H2}00{P2}] kembali"
		vprint(panel(x,style=f"{H2}"))
		zk = input(f"{garis} pilih : {H}")
		if zk in ["1","01"]:
			print("")
			c = input(f"{garis} anda yakin ingin menghapus cookie ({M}y{P}/{H}t{P}) : {H}")
			if c in ["ya","y","Y"]:
				print("")
				os.system("rm -rf cookie.txt")
				os.system("rm -rf token.txt")
				jalan(f"{garis} sukses menghapus cookie bawaan ")
				cek_cookie()
			elif c in ["t","T","tidak"]:
				menu()
			else:
				print("")
				jalan(f"{garis} isi yang benar ")
				menu()
		elif zk in ["2","02"]:
			exit()
		elif zk in ["0","00"]:
			menu()
		else:
			print("")
			jalan(f"{garis} isi yang benar ")
			menu()
	else:
		print("")
		jalan(f"{garis} isi yang benar ")
		menu()
			
def pilpil():
	hikmatz = input(f"{garis} pilih : {H}")
	if hikmatz in ["1","01"]:
		tracked_sendiri()
	elif hikmatz in ["2","02"]:
		tracked_target()
	elif hikmatz in ["0","00"]:
		menu()
	else:
		jalan(f"{garis} isi yang benar")
		pilpil()
			
def tracked_sendiri():
	a = requests.get("http://ip-api.com/json/",headers={"Referer":"http://ip-api.com/","Content-Type":"application/json; charset=utf-8","User-Agent":"Mozilla/5.0 (Linux; Android 10; Mi 9T Pro Build/QKQ1.190825.002; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/88.0.4324.181 Mobile Safari/537.36[FBAN/EMA;FBLC/it_IT;FBAV/239.0.0.10.109;]"}).json()
	try:ip = a["query"]
	except KeyError:
		ip = " "
	try:bn = a["status"]
	except KeyError:
		bn = " "
	try:ng = a["country"]
	except KeyError:
		ng = " "
	try:cc = a["countryCode"]
	except KeyError:
		cc = " "
	try:pr = a["regionName"]
	except KeyError:
		pr = " "
	try:kt = a["city"]
	except KeyError:
		kt = " "
	try:kb = a["zip"]
	except KeyError:
		kb = " "
	try:tz = a["timezone"]
	except KeyError:
		tz = " "
	try:sp = a["isp"]
	except KeyError:
		sp = " "
	jalan(f"\n{garis} status : {bn}")
	jalan(f"{garis} IP kamu : {ip}")
	jalan(f"{garis} negara kamu : {ng}")
	jalan(f"{garis} kode negara : {cc}")
	jalan(f"{garis} provinsi : {pr}")
	jalan(f"{garis} kota  : {kt}")
	jalan(f"{garis} kode pos : {kb}")
	jalan(f"{garis} zona waktu : {tz}")
	jalan(f"{garis} provider : {sp}")
	jalan(f"{garis} ingfo full : http://ip-api.com/#{ip}")
	input(f"{garis} enter untuk kembali ")
	menu()
	
def tracked_target():
	print("")
	x=f"{P2}contoh ip : {K2}193.34.56.125"
	vprint(panel(x,style=f"{H3}"))
	hm = input(f"{garis} ip target : {H}") 
	a = requests.get("http://ip-api.com/json/"+hm,headers={"Referer":"http://ip-api.com/","Content-Type":"application/json; charset=utf-8","User-Agent":"Mozilla/5.0 (Linux; Android 10; Mi 9T Pro Build/QKQ1.190825.002; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/88.0.4324.181 Mobile Safari/537.36[FBAN/EMA;FBLC/it_IT;FBAV/239.0.0.10.109;]"}).json()
	try:ip = a["query"]
	except KeyError:
		ip = " "
	try:bn = a["status"]
	except KeyError:
		bn = " "
	try:ng = a["country"]
	except KeyError:
		ng = " "
	try:cc = a["countryCode"]
	except KeyError:
		cc = " "
	try:pr = a["regionName"]
	except KeyError:
		pr = " "
	try:kt = a["city"]
	except KeyError:
		kt = " "
	try:kb = a["zip"]
	except KeyError:
		kb = " "
	try:tz = a["timezone"]
	except KeyError:
		tz = " "
	try:sp = a["isp"]
	except KeyError:
		sp = " "
	jalan(f"\n{garis} status : {bn}")
	jalan(f"{garis} IP target : {ip}")
	jalan(f"{garis} negara target : {ng}")
	jalan(f"{garis} kode negara : {cc}")
	jalan(f"{garis} provinsi : {pr}")
	jalan(f"{garis} kota  : {kt}")
	jalan(f"{garis} kode pos : {kb}")
	jalan(f"{garis} zona waktu : {tz}")
	jalan(f"{garis} provider : {sp}")
	jalan(f"{garis} ingfo full : http://ip-api.com/#{ip}")
	input(f"{garis} enter untuk kembali ")
	menu()
	

			
def dump_public():
	try:
		os.mkdir('dump')
	except:pass
	try:
		xaco = input(f"{garis} id public  :\x1b[38;5;46m ")
		cuy = input(f"{garis} nama file  :\x1b[38;5;46m ")
		print("")
		wkwk  = ('dump/' + cuy + '.json').replace(' ', '_')
		xxx = open(wkwk, 'w')
		token = open('token.txt','r').read()
		cookie = open('cookie.txt','r').read()
		coki = {"cookie":cookie}
		cyna = requests.get('https://graph.facebook.com/%s?fields=friends.limit(90000)&access_token=%s'%(xaco,token),cookies=coki).json()
		for fuck in cyna['friends']['data']:
			id.append(fuck['id']+'|'+fuck['name'])
			xxx.write(fuck['id']+'|'+fuck['name'] + '\n')
			fr = random.choice([O,B,H,P,K,M,U])
			sys.stdout.write(f'\r\033[0m *--> %s {fr}• \033[0m%s                  \r\n\x1b[38;5;231m [ \x1b[38;5;46m%s\x1b[38;5;231m ] [ \x1b[38;5;46m%s\x1b[38;5;231m ] \x1b[0;96mproses dump ID...'%(fuck['id'],fuck['name'],datetime.datetime.now().strftime('%H:%M:%S'), len(id)
			)); sys.stdout.flush()
			time.sleep(0.0050)
			
		xxx.close()
		jalan(f"\n{garis} berhasil dump id dari publik");print(f"{garis} salin output file *--> [ %s%s%s ]"%(H,wkwk,P))
		input(f"{garis} kembali ");menu()
	except (KeyError,IOError):
		os.remove(wkwk)
		jalan(f"{garis} gagal dump id, kemungkinan id tidak ada.\n")
		input(f"{garis} kembali ");menu()
		
def dump_followers():
	try:
		os.mkdir('dump')
	except:pass
	try:
		xaco = input(f"{garis} id followers  :\x1b[38;5;46m ")
		cuy = input(f"{garis} nama file  :\x1b[38;5;46m ")
		print("")
		wkwk  = ('dump/' + cuy + '.json').replace(' ', '_')
		xxx = open(wkwk, 'w')
		token = open('token.txt','r').read()
		cookie = open('cookie.txt','r').read()
		coki = {"cookie":cookie}
		cyna = requests.get('https://graph.facebook.com/%s?fields=subscribers.limit(90000)&access_token=%s'%(xaco,token),cookies=coki).json()
		for fuck in cyna['subscribers']['data']:
			id.append(fuck['id']+'|'+fuck['name'])
			xxx.write(fuck['id']+'|'+fuck['name'] + '\n')
			fr = random.choice([O,B,H,P,K,M,U])
			sys.stdout.write(f'\r\033[0m *--> %s {fr}• \033[0m%s                  \r\n\x1b[38;5;231m [ \x1b[38;5;46m%s\x1b[38;5;231m ] [ \x1b[38;5;46m%s\x1b[38;5;231m ] \x1b[0;96mproses dump ID...'%(fuck['id'],fuck['name'],datetime.datetime.now().strftime('%H:%M:%S'), len(id)
			)); sys.stdout.flush()
			time.sleep(0.0050)
			
		xxx.close()
		jalan(f"\n{garis} berhasil dump id followers ");print(f"{garis} salin output file *--> [ %s%s%s ]"%(H,ah,P))
		input(f"{garis} kembali ");menu()
	except (KeyError,IOError):
		os.remove(wkwk)
		jalan(f"{garis} gagal dump id, kemungkinan id tidak ada.\n")
		input(f"{garis} kembali ");menu()

def dump_post():
	try:
		os.mkdir('dump')
	except:pass
	try:
		xaco = input(f"{garis} id likes  :\x1b[38;5;46m ")
		cuy = input(f"{garis} nama file  :\x1b[38;5;46m ")
		limit = input(f"{garis} limit likes : {H}")
		print("")
		wkwk  = ('dump/' + cuy + '.json').replace(' ', '_')
		xxx = open(wkwk, 'w')
		token = open('token.txt','r').read()
		cookie = open('cookie.txt','r').read()
		coki = {"cookie":cookie}
		cyna = requests.get('https://graph.facebook.com/%s?fields=likes.limit(%s)&access_token=%s'%(xaco,limit,token),cookies=coki).json()
		for fuck in cyna['likes']['data']:
			id.append(fuck['id']+'|'+fuck['name'])
			xxx.write(fuck['id']+'|'+fuck['name'] + '\n')
			fr = random.choice([O,B,H,P,K,M,U])
			sys.stdout.write(f'\r\033[0m *--> %s {fr}• \033[0m%s                  \r\n\x1b[38;5;231m [ \x1b[38;5;46m%s\x1b[38;5;231m ] [ \x1b[38;5;46m%s\x1b[38;5;231m ] \x1b[0;96mproses dump ID...'%(fuck['id'],fuck['name'],datetime.datetime.now().strftime('%H:%M:%S'), len(id)
			)); sys.stdout.flush()
			time.sleep(0.0050)
			
		xxx.close()
		jalan(f"\n{garis} berhasil dump id post likes ");print(f"{garis} salin output file *--> [ %s%s%s ]"%(H,wkwk,P))
		input(f"{garis} kembali ");menu()
	except (KeyError,IOError):
		os.remove(wkwk)
		jalan(f"{garis} gagal dump id, kemungkinan id tidak ada.\n")
		input(f"{garis} kembali ");menu()

def dump_publicv2():
	tutlu=[]
	it = input(f"{garis} id target :"+H+" ")
	try:
		token = open('token.txt','r').read()
		cookie = open('cookie.txt','r').read()
		coki = {"cookie":cookie}
		ka = requests.get('https://graph.facebook.com/%s?fields=friends.limit(90000)&access_token=%s'%(it,token),cookies=coki)
		oioo = json.loads(ka.text)
		for fuck in oioo['friends']['data']:
			tutlu.append(fuck['id'])
		token = open('token.txt','r').read()
		cookie = open('cookie.txt','r').read()
		coki = {"cookie":cookie}
		cyna = requests.get('https://graph.facebook.com/%s?access_token=%s'%(it,token),cookies=coki).json()
		print(f"{garis} name : %s%s"%(H,cyna['name']))
		print(f"{garis} total friends : {H}{len(tutlu)}")
	except (KeyError,IOError):
		jalan(f"{garis} cookie kadaluarsa")
		login()
	tl=[]
	to=[]
	ttl_tar=[]
	tlo=[]
	idl=[]
	lim = input(f"{garis} limit dump id :"+H+" ")
	token = open('token.txt','r').read()
	cookie = open('cookie.txt','r').read()
	coki = {"cookie":cookie}
	ka = requests.get('https://graph.facebook.com/%s?fields=friends.limit(%s)&access_token=%s'%(it,lim,token),cookies=coki)
	oioo = json.loads(ka.text)
	for fuck in oioo['friends']['data']:
		tl.append(fuck['id'])
	print("")
	x=f"{P2}[01] id urutan new\n{P2}[02] id urutan old\n{P2}[03] id urutan random"
	vprint(panel(x,style=f"{H3}"))
	GlukTzy = input(garis+" pilih : "+H)
	if GlukTzy in ['2','02']:
		for bacot in tl:
			idl.append(bacot)
	elif GlukTzy in ['1','01']:
		for bacot in tl:
			idl.insert(0,bacot)
	elif GlukTzy in ['3','03']:
		for bacot in tl:
			xx = random.randint(0,len(idl))
			idl.insert(xx,bacot)
	else:
		jalan(garis+" isi yang benar")
		exit()
	print("")
	#random_uidz()
	for uik in idl:
		try:
			token = open('token.txt','r').read()
			cookie = open('cookie.txt','r').read()
			coki = {"cookie":cookie}
			xn = requests.Session().get('https://graph.facebook.com/%s?access_token=%s'%(id,token),cookies=coki)
			x = json.loads(xn.text)
			try:lok = x["locale"]
			except (KeyError,IOError):
				lok = "-"
			coa = requests.get('https://graph.facebook.com/%s?access_token=%s'%(id,token),cookies=coki)
			el = json.loads(coa.text)
			try:lk = el["name"]
			except (KeyError,IOError):
				lk = "-"
			token = open('token.txt','r').read()
			cookie = open('cookie.txt','r').read()
			coki = {"cookie":cookie}
			ciner = requests.get('https://graph.facebook.com/%s?access_token=%s'%(uik,token),cookies=coki).json()
			token = open('token.txt','r').read()
			cookie = open('cookie.txt','r').read()
			coki = {"cookie":cookie}
			cyna = requests.get('https://graph.facebook.com/%s?fields=friends.limit(90000)&access_token=%s'%(uik,token),cookies=coki)
			eil = json.loads(cyna.text)
			try:
				for fuck in eil['friends']['data']:
					to.append(fuck['id']+'|'+fuck['name'])
			except KeyError:
				continue
			x=f"{P2}┌─ ID : {uik}\n{P2}│ └─ NAMA : {ciner['name']}\n│ └─ LOKASI : {ciner['locale']}\n│ ┌─ LINK : {ciner['link']}\n└─ FRIENDS : {len(to)}"
			vprint(panel(x,style=f"{warna_warni_rich}"))
			to.clear()
		except KeyError:
			print(K+'*--> '+M+'akun terspam')
	print("")
	x=f"{P2}salin hasil nya cokk biar gk ulang dump lagi!!"
	vprint(panel(x,style=f"{H3}"))
	input(f"{garis} enter untuk kembali")
	menu()

def dump_followersv2():
	tutlu=[]
	it = input(f"{garis} id target :"+H+" ")
	try:
		token = open('token.txt','r').read()
		cookie = open('cookie.txt','r').read()
		coki = {"cookie":cookie}
		ka = requests.get('https://graph.facebook.com/%s?fields=subscribers.limit(90000)&access_token=%s'%(it,token),cookies=coki)
		oioo = json.loads(ka.text)
		for fuck in oioo['subscribers']['data']:
			tutlu.append(fuck['id'])
		token = open('token.txt','r').read()
		cookie = open('cookie.txt','r').read()
		coki = {"cookie":cookie}
		cyna = requests.get('https://graph.facebook.com/%s?access_token=%s'%(it,token),cookies=coki).json()
		print(f"{garis} name : %s%s"%(H,cyna['name']))
		print(f"{garis} total followers : {H}{len(tutlu)}")
	except (KeyError,IOError):
		jalan(f"{garis} cookie kadaluarsa")
		login()
	tl=[]
	to=[]
	ttl_tar=[]
	tlo=[]
	idl=[]
	lim = input(f"{garis} limit dump :"+H+" ")
	token = open('token.txt','r').read()
	cookie = open('cookie.txt','r').read()
	coki = {"cookie":cookie}
	ka = requests.get('https://graph.facebook.com/%s?fields=subscribers.limit(%s)&access_token=%s'%(it,lim,token),cookies=coki)
	oioo = json.loads(ka.text)
	for fuck in oioo['subscribers']['data']:
		tl.append(fuck['id'])
	x=f"{P2}[01] id urutan old\n{P2}[02] id urutan new\n{P2}[03] id urutan random"
	vprint(panel(x,style=f"{H3}"))
	GlukTzy = input(garis+" pilih : "+H)
	if GlukTzy in ['2','02']:
		for bacot in tl:
			idl.append(bacot)
	elif GlukTzy in ['1','01']:
		for bacot in tl:
			idl.insert(0,bacot)
	elif GlukTzy in ['3','03']:
		for bacot in tl:
			xx = random.randint(0,len(idl))
			idl.insert(xx,bacot)
	else:
		jalan(garis+" isi yang benar")
		exit()
	print("")
	#random_uidz()
	for uik in idl:
		try:
			token = open('token.txt','r').read()
			cookie = open('cookie.txt','r').read()
			coki = {"cookie":cookie}
			xn = requests.Session().get('https://graph.facebook.com/%s?access_token=%s'%(id,token),cookies=coki)
			x = json.loads(xn.text)
			try:lok = x["locale"]
			except (KeyError,IOError):
				lok = "-"
			coa = requests.get('https://graph.facebook.com/%s?access_token=%s'%(id,token),cookies=coki)
			el = json.loads(coa.text)
			try:lk = el["name"]
			except (KeyError,IOError):
				lk = "-"
			token = open('token.txt','r').read()
			cookie = open('cookie.txt','r').read()
			coki = {"cookie":cookie}
			ciner = requests.get('https://graph.facebook.com/%s?access_token=%s'%(uik,token),cookies=coki).json()
			token = open('token.txt','r').read()
			cookie = open('cookie.txt','r').read()
			coki = {"cookie":cookie}
			cyna = requests.get('https://graph.facebook.com/%s?fields=subscribers.limit(90000)&access_token=%s'%(uik,token),cookies=coki)
			eil = json.loads(cyna.text)
			try:
				for fuck in eil['subscribers']['data']:
					to.append(fuck['id']+'|'+fuck['name'])
			except KeyError:
				continue
			x=f"{P2}┌─ ID : {uik}\n{P2}│ └─ NAMA : {ciner['name']}\n│ └─ LOKASI : {ciner['locale']}\n│ ┌─ LINK : {ciner['link']}\n└─ FOLLOWERS : {len(to)}"
			vprint(panel(x,style=f"{warna_warni_rich}"))
			to.clear()
		except KeyError:
			print(K+'*--> '+M+'akun terspam')
	print("")
	x=f"{P2}salin hasil nya cokk biar gk ulang dump lagi!!"
	vprint(panel(x,style=f"{H3}"))
	input(f"{garis} enter untuk kembali")
	menu()

def random_uidz():
	x=f"{P2}[01] id urutan old\n{P2}[02] id urutan new\n{P2}[03] id urutan random"
	vprint(panel(x,style=f"{H3}"))
	GlukTzy = input(garis+" pilih : "+H)
	if GlukTzy in ['2','02']:
		for bacot in tl:
			idl.append(bacot)
	elif GlukTzy in ['1','01']:
		for bacot in tl:
			idl.insert(0,bacot)
	elif GlukTzy in ['3','03']:
		for bacot in tl:
			xx = random.randint(0,len(idl))
			idl.insert(xx,bacot)
	else:
		jalan(garis+" isi yang benar")
		random_uidz()

def check_ingfo_akun():
	idt=[]
	try:
		token = open('token.txt','r').read()
		cookie = open('cookie.txt','r').read()
		coki = {"cookie":cookie}
	except (KeyError,IOError):
		jalan(garis+" cookie kadaluarsa");cek_cookie()
	idt = input(garis+" id target :%s "%(H))
	try:
		zx = requests.get("https://graph.facebook.com/"+idt+"?access_token=%s"%(token),cookies=coki);zy = json.loads(zx.text)
	except (KeyError,IOError):jalan(garis+" id tidak ditemukan");menu()
	try:nm = zy["name"]
	except (KeyError,IOError):nm = (M+"-")
	try:nd = zy["first_name"]
	except (KeyError,IOError):nd = (M+"-")
	try:nt = zy["middle_name"]
	except (KeyError,IOError):nt = (M+"-")
	try:nb = zy["last_name"]
	except (KeyError,IOError):nb = (M+"-")
	try:ut = zy["birthday"]
	except (KeyError,IOError):ut = (M+"-")
	try:gd = zy["gender"]
	except (KeyError,IOError):gd = (M+"-")
	try:em = zy["email"]
	except (KeyError,IOError):em = (M+"-")
	try:lk = zy["link"]
	except (KeyError,IOError):lk = (M+"-")
	try:us = zy["username"]
	except (KeyError,IOError):us = (M+"-")
	try:rg = zy["religion"]
	except (KeyError,IOError):rg = (M+"-")
	try:rl = zy["relationship_status"]
	except (KeyError,IOError):rl = (M+"-")
	try:rls = zy["significant_other"]["name"]
	except (KeyError,IOError):rls = (M+"-")
	try:lc = zy["location"]["name"]
	except (KeyError,IOError):lc = (M+"-")
	try:ht = zy["hometown"]["name"]
	except (KeyError,IOError):ht = (M+"-")
	try:ab = zy["about"]
	except (KeyError,IOError):ab = (M+"-")
	try:lo = zy["locale"]
	except (KeyError,IOError):lo = (M+"-")
	#try:ppk = zy["education"]["id"]
	#except (KeyError,IOError):ppk = (M+"-")
	print("")
	jalan(garis+" nama : %s%s"%(H,nm))
	jalan(garis+" nama depan : %s%s"%(H,nd))
	jalan(garis+" nama tengah : %s%s"%(H,nt))
	jalan(garis+" nama belakang : %s%s"%(H,nb))
	jalan(garis+" TTL : %s%s"%(H,ut))
	jalan(garis+" gender : %s%s"%(H,gd))
	try:
		token = open('token.txt','r').read()
		cookie = open('cookie.txt','r').read()
		coki = {"cookie":cookie}
		cy = requests.get('https://graph.facebook.com/%s?fields=friends.limit(99999)&access_token=%s'%(idt,token),cookies=coki)
		z = json.loads(cy.text)
		for i in z['friends']['data']:
			id.append(i['id'])
	except:pass
	jalan(garis+" total friends : "+H+"%s"%str(len(id)));time.sleep(0.03)
	lao=[]
	try:
		token = open('token.txt','r').read()
		cookie = open('cookie.txt','r').read()
		coki = {"cookie":cookie}
		cyna = requests.get('https://graph.facebook.com/%s?fields=subscribers.limit(90000)&access_token=%s'%(idt,token),cookies=coki)
		eil = json.loads(cyna.text)
		for fuck in eil['subscribers']['data']:
			lao.append(fuck['id'])
	except:pass
	jalan(garis+" total followers : "+H+"%s"%(len(lao)));time.sleep(0.03)
	jalan(garis+" email : %s%s"%(H,em))
	jalan(garis+" link : %s%s"%(H,lk))
	jalan(garis+" username : %s%s"%(H,us))
	jalan(garis+" agama : %s%s"%(H,rg))
	#asow(idt)
	#jalan(maling_pangsit+" Pendidikan : %s%s"%(H,ppk))
	jalan(garis+" status hubungan : %s%s"%(H,rl))
	jalan(garis+" hubungan dengan : %s%s"%(H,rls))
	jalan(garis+" tempat tinggal : %s%s"%(H,lc))
	jalan(garis+" tempat asal : %s%s"%(H,ht))
	jalan(garis+" tentang : %s%s"%(H,ab))
	jalan(garis+" locale : %s%s"%(H,lo))
	input(garis+" enter untuk kembali");menu()

cek_cookie()
