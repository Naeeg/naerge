def toplama(x, y):
    return x + y

def cikarma(x, y):
    return x - y

def carpma(x, y):
    return x * y

def bolme(x, y):
    if y != 0:
        return x / y
    else:
        return "Hata: Sıfıra bölme!"

def hesap_makinesi():
    print("Hesap Makinesi")
    print("Yapmak istediğiniz işlemi seçin:")
    print("1. Toplama")
    print("2. Çıkarma")
    print("3. Çarpma")
    print("4. Bölme")

    while True:
        secim = input("Seçiminiz (1/2/3/4): ")

        if secim in ('1', '2', '3', '4'):
            try:
                sayi1 = float(input("Birinci sayıyı girin: "))
                sayi2 = float(input("İkinci sayıyı girin: "))
            except ValueError:
                print("Lütfen geçerli bir sayı girin.")
                continue

            if secim == '1':
                print(f"{sayi1} + {sayi2} = {toplama(sayi1, sayi2)}")
            elif secim == '2':
                print(f"{sayi1} - {sayi2} = {cikarma(sayi1, sayi2)}")
            elif secim == '3':
                print(f"{sayi1} * {sayi2} = {carpma(sayi1, sayi2)}")
            elif secim == '4':
                print(f"{sayi1} / {sayi2} = {bolme(sayi1, sayi2)}")

            # Başka bir işlem yapmak ister misiniz?
            devam = input("Başka bir işlem yapmak ister misiniz? (evet/hayır): ")
            if devam.lower() != 'evet':
                break
        else:
            print("Geçersiz seçim, lütfen 1, 2, 3 veya 4 girin.")

if __name__ == "__main__":
    hesap_makinesi()
