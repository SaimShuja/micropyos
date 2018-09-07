# micropyosSmall os for micropythonThis small os i made to work out how to use the micropython commands for wifi network ect.you can copy files to and from a remote computer using scp and cal also get files from the internet with the wget command.How to run micropyos<br /> edit settings.py <br /> edit ssid and wifipassword for wifi connection<br /> retmoteIP remotePath uname and upass are for scp copying of files.<br /> import uos<br /> remoteIP='192.168.0.3'<br /> remotePath='/Users/thecodeman/Projects/micropyos/'<br /> uname='username'<br /> upass='password'<br /> wifiSSID = 'ssid'<br /> wifiPass = 'wifipassword'<br /> sdCardCLK = 4<br /> sdCardMOSI = 12<br /> sdCardMiso = 2<br /> sdCardCS =15<br /> timeZone= 'PST8PDT'<br /> autostartWiFi = True<br /> autoMountSD = True<br /> def initSDCard():<br /> #	uos.sdconfig(uos.SDMODE_4LINE, sdCardCLK , sdCardMOSI, sdCardMiso, sdCardCS)<br /> 	uos.sdconfig(uos.SDMODE_4LINE)<br /> 	try:<br /> 	    uos.mountsd()<br /> 	except Exception as e:<br /> 	    print(e)<br /> Once you get the settings file done just import micropyos.<br /> Commands:<br /> ls      - list files current directory<br /> lr      - list files on remote server (optional directory)<br /> cat     - display contents file<br /> rm      - remove file<br /> df      - display drive space<br /> time    - display time and date<br /> get     - scp from server<br /> put     - scp to server<br /> md      - make directory<br /> rmdir   - remove directory<br /> run     - run python script<br /> edit    - edit file using pye<br /> modules - list installed modules<br /> reset   - reset board<br /> wget    - get file over http and save to file<br /> cp 		- copy files local <br /> <br /> 