0. Előkészületek
	1. Sox telepítése:
	
		pi@raspberrypi:~$ sudo apt-get install python-pyaudio python3-pyaudio sox

	2. Pyaudio telepítés:
	
		pi@raspberrypi:~$ sudo pip install pyaudio
	
		Ha a pip nincs telepítve: https://pip.pypa.io/en/stable/installing/
	
	3. Ellenőrzés:
	
		pi@raspberrypi:~$ rec temp.wav
		
		Ha bármilyen error miatt nem működik a felvétel: http://docs.kitt.ai/snowboy/#running-on-pi
	
	
1. Letöltés:

	pi@raspberrypi:~$ git clone https://github.com/kmettyjanos/SnowBoyPythonTest.git
	
2. Hotword létrehozása:

	https://snowboy.kitt.ai/dashboard
	
	Pontosabb találati arányt lehet elérni, ha ugyanazzal a mikrofonnal vesszük fel a hangmintát mint amivel a felismerést fogjuk végezni.
	http://docs.kitt.ai/snowboy/#my-trained-model-works-well-on-laptops-but-not-on-pi-s
	
3. Hangminták másolása a Pi-re:

	pi@raspberrypi:~$ ~/SnowBoyPythonTest/resources mappába.
	
4. Indítás:

	pi@raspberrypi:~$ python SnowBoyPythonTest/demo2.py SnowBoyPythonTest/resources/model1.pmdl SnowBoyPythonTest/resources/model2.pmdl

	Az argumentumként megadott két hangminta közül
	
		- az elsőre BEKAPCSOLJA a monitort
		
		- a másodikra pedig KIKAPCSOLJA
		
	
	