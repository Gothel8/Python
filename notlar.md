# Python Giriş Notları 

Bu notlar Python’un temel taşlarını öğrenmek için hazırlandı.
Daha ileri aşamada pandas, numpy gibi kütüphaneler gelecek.

---

## 2. Değişkenler ve Veri Tipleri
Python’da veriler değişkenlere atanır. Temel veri tipleri: integer, float, string, boolean.

```python
age = 21           # integer
name = "Nurdan"    # string
gpa = 3.45         # float
is_student = True  # boolean
```

## 3. Stringlerle Çalışmak
Stringler (metinler) üzerinde işlem yapabiliriz.

````python
text = "Python"
print(text.upper())      # BÜYÜK HARF
print(text.lower())      # küçük harf
print(len(text))         # uzunluk
print(text[0])           # ilk karakter
print(text[1:4])         # alt string
````
Önemli fonksiyonlar: .strip(), .replace(), .find(), .split(), .join()


## 4. Sayılarla Çalışmak
Matematiksel işlemler, üs alma, yuvarlama vb.

```python
print(3 + 2)    # 5
print(3 ** 2)   # 9 (üs alma)
print(abs(-7))  # 7
print(round(3.7))  # 4
```
Önemli fonksiyonlar: max(), min(), sum(), round(), abs()


## 5. Kullanıcıdan Girdi Almak
```python
name = input("Adınızı girin: ")
print("Merhaba " + name)
```

## 6. Basit Hesap Makinesi
```python
num1 = float(input("Bir sayı girin: "))
num2 = float(input("Bir sayı daha girin: "))
print("Toplam:", num1 + num2)
```

## 7. Listeler
Listeler, birden fazla öğeyi saklamak için kullanılır.

```python
friends = ["Ali", "Ayşe", "Mehmet"]
friends.append("Zeynep")  # sona ekler
friends.insert(1, "Ece")  # 1. indexe ekler
friends.remove("Ali")     # siler
friends.pop()             # son öğeyi siler
print(friends)
```
Önemli fonksiyonlar: append(), insert(), remove(), pop(), sort(), reverse()


## 8. Tuple’lar
Tuple’lar, listeler gibi ama değiştirilemez (immutable).

```python
coordinates = (4, 5)
print(coordinates[0])
```

## 9. Fonksiyonlar
Kendi işlevlerimizi tanımlamak için kullanılır.

```python
def say_hi(name):
    print("Merhaba " + name)

say_hi("Nurdan")
```
Return ifadesi:

```python
def cube(num):
    return num ** 3

print(cube(3))  # 27
```

## 10. If – Else
Koşullu ifadeler ile karar yapıları oluşturulur.

```python
age = 20
if age >= 18:
    print("Reşit")
else:
    print("Reşit değil")
```
Karşılaştırmalar:

```python
print(5 == 5)  # True
print(5 != 3)  # True
print(3 > 1)   # True
print(2 <= 2)  # True
```

## 11. Dictionary
Anahtar-değer çiftlerini saklamak için kullanılır.

```python
aylar = {"Ocak": "January", "Şubat": "February"}
print(aylar["Ocak"])
aylar["Mart"] = "March"  # yeni ekleme
```
Önemli fonksiyonlar: keys(), values(), items(), get()


## 12. Döngüler
While Döngüsü:

```python
i = 1
while i <= 5:
    print(i)
    i += 1
```
For Döngüsü:

```python
for letter in "Python":
    print(letter)
```
Liste üzerinden:

```python
for friend in ["Ali", "Ayşe", "Mehmet"]:
    print(friend)
```

## 13. 2D List & Nested Loops
İç içe listeler ve döngüler.

```python
number_grid = [
    [1, 2, 3],
    [4, 5, 6]
]

for row in number_grid:
    for col in row:
        print(col)
```

## 14. Try / Except
Hata yönetimi için kullanılır.

```python
try:
    num = int(input("Bir sayı girin: "))
    print(10 / num)
except ZeroDivisionError:
    print("Sıfıra bölünemez")
except ValueError:
    print("Geçerli bir sayı girin")
```

## 15. Dosya Okuma
```python
file = open("data.txt", "r", encoding="utf-8")
print(file.read())
file.close()
```
Alternatif (otomatik kapatma):

```python
with open("data.txt", "r", encoding="utf-8") as file:
    print(file.read())
```
    
## 16. Yorum Satırları
```python
# Bu tek satırlık yorum
"""
Bu da çok
satırlı
yorum
"""
```




