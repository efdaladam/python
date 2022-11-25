# python #BANKAMATİK UYGULAMASI
efdalHesap = {
    'ad' :'efdal adam',
    'hesapNo' : '55555555',
    'bakiye' : 3000,
    'ekHesap' : 2000 
}

ozgeHesap = {
    'ad' :'özge uyğun',
    'hesapNo': '777777777',
    'bakiye' : 2000,
    'ekHesap': 1000
}

def paraCek(hesap, miktar):
    print(f"merhaba {hesap['ad']}")

    if (hesap['bakiye'] >= miktar):
        print('paranızı alabilirsiniz')
    else:
        toplam = hesap['bakiye'] + hesap['ekHesap']
        
        if(toplam >= miktar):
            ekHesapKullanımı = input('ek hesap kullanılsın mı e/h')
            if ekHesapKullanımı == 'e':
                print('paranızı alabilirsiniz')
            else:
                print(f"{hesap['hesapNo']} nolu hesabınızda {hesap['bakiye'] + hesap['ekHesap']} bulunmaktadır")

        else:
            print('üzgünüz bakiye yetersiz') 

paraCek(efdalHesap, 4000)
paraCek(ozgeHesap, 1500)

