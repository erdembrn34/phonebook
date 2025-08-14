# Phonebook Programı

Bu basit Python programı, kullanıcıdan isim ve telefon numarası bilgilerini alır, bunları saklar ve kullanıcıya isim arama imkanı verir.

## Özellikler
- Kullanıcıdan **3** kişi için ad ve telefon numarası alır.
- Girilen bilgileri ekranda listeler.
- Kullanıcıya bir isim arama imkanı sunar.
- Aranan isim bulunduğunda ilgili telefon numarasını gösterir, bulunmazsa "Name Not Found" mesajı verir.

## Kullanım
1. Program çalıştırıldığında, sırasıyla **Name** (isim) ve **Phone Number** (telefon numarası) bilgilerini girin.
2. Tüm girişler tamamlandığında, program girilen isim ve numaraları tablo şeklinde gösterir.
3. **Enter search term** yazısında aramak istediğiniz ismi girin.
4. Arama sonucu ekranda gösterilir.

## Kod Açıklaması
```python
names = []
phone_numbers = []
num = 3  # Kayıt sayısı

# Kullanıcıdan veri alma
for i in range(num):
    name = input("Name: ")
    phone_number = input("Phone Number: ")

    names.append(name)
    phone_numbers.append(phone_number)

# Tüm kayıtları ekrana yazdırma
print("\nName\t\t\tPhone Number\n")
for i in range(num):
    print("{}\t\t\t{}".format(names[i], phone_numbers[i]))

# İsim arama
search_term = input("\nEnter search term: ")
print("Search result:")

if search_term in names:
    index = names.index(search_term)
    phone_number = phone_numbers[index]
    print("Name: {}, Phone Number: {}".format(search_term, phone_number))
else:
    print("Name Not Found")
