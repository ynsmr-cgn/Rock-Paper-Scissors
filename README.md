# Rock-Paper-Scissors
En:I share with you the simple Rock-Paper-Scissors game I made in Python.
Below you can find the lines of code.

Tr:Python'da yapmış olduğum basit Taş-Kağıt-Makas oyununu sizlerle paylaşıyorum. 
Aşağıda kod satırlarını bulabilirsiniz. 
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

import random
import os


liste = ["Taş", "Kağıt", "Makas"]


bilgisayar_puan = 0
oyuncu_puan = 0


menu = """
    Taş-Kağıt-Makas
    
    1- Oyna
    2- Skoru Göster
    3- Çıkış
    
"""


while True:
    os.system("cls")
    print(menu)
    bilgisayar_secim = random.choice(liste)

    secim = int(input("Seçiminiz -> "))
    if secim == 3:
        quit()
    if secim == 1:
        oyna_secim = """
        
    1- Taş
    2- Kağıt
    3- Makas
        
        """
        print(oyna_secim)
        numara = int(input("Seçtiğiniz numarayı giriniz: "))
        if numara == 1:
            if bilgisayar_secim == "Taş":
                print("Bilgisayarın seçimi: ", bilgisayar_secim)
                print("Berabere!")
                input("Devam etmek için enter'ı tuşlayınız. ")
            elif bilgisayar_secim == "Kağıt":
                print("Bilgisayarın seçimi: ", bilgisayar_secim)
                print("Bilgisayar kazandı!")
                bilgisayar_puan = bilgisayar_puan + 10
                input("Devam etmek için enter'ı tuşlayınız. ")
            elif bilgisayar_secim == "Makas":
                print("Bilgisayarın seçimi: ", bilgisayar_secim)
                print("Oyuncu kazandı!")
                oyuncu_puan = oyuncu_puan + 10
                input("Devam etmek için enter'ı tuşlayınız. ")
        elif numara == 2:
            if bilgisayar_secim == "Taş":
                print("Bilgisayarın seçimi: ", bilgisayar_secim)
                print("Oyuncu kazandı!")
                oyuncu_puan = oyuncu_puan + 10
                input("Devam etmek için enter'ı tuşlayınız. ")
            elif bilgisayar_secim == "Kağıt":
                print("Bilgisayarın seçimi: ", bilgisayar_secim)
                print("Berabere!")
                input("Devam etmek için enter'ı tuşlayınız. ")
            elif bilgisayar_secim == "Makas":
                print("Bilgisayarın seçimi: ", bilgisayar_secim)
                print("Bilgisayar kazandı!")
                bilgisayar_puan = bilgisayar_puan + 10
                input("Devam etmek için enter'ı tuşlayınız. ")
        elif numara == 3:
            if bilgisayar_secim == "Taş":
                print("Bilgisayarın seçimi: ", bilgisayar_secim)
                print("Bilgisayar kazandı!")
                bilgisayar_puan = bilgisayar_puan + 10
                input("Devam etmek için enter'ı tuşlayınız. ")
            elif bilgisayar_secim == "Kağıt":
                print("Bilgisayarın seçimi: ", bilgisayar_secim)
                print("Oyuncu kazandı!")
                oyuncu_puan = oyuncu_puan + 10
                input("Devam etmek için enter'ı tuşlayınız. ")
            elif bilgisayar_secim == "Makas":
                print("Bilgisayarın seçimi: ", bilgisayar_secim)
                print("Berabere!")
                input("Devam etmek için enter'ı tuşlayınız. ")
    elif secim == 2:
        print("Oyunucunun skoru:", oyuncu_puan, " | Bilgisayarın skoru: ", bilgisayar_puan)
        input("Devam etmek için enter'ı tuşlayınız. ")
