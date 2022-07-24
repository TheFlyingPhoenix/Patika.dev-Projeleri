# Merge Sort Projesi
## [16,21,11,8,12,22] Dizisinin Merge Sort türüne göre aşamaları
1. `[16,21,11]` - `[8,12,22]`
2. `[16,21]` - `[11]`  -  `[8,12]` - `[22]`
3. `[16,21]` - `[11]`  -  `[8,12]` - `[22]`
4. `[16]` - `[21]` - `[11]`  -  `[8]` - `[12]` - `[22]`
5. `[16,21]` - `[11]`  -  `[8,12]` - `[22]`
6. `[11,16,21]`  -  `[8,12,22]`
7. `[16,21,11,8,12,22]`

| Diziyi orta indeksinden ikiye bölüyoruz.                                                                    |    |    |    | 16 | 21 | 11 |  8 | 12 | 22 |    |    |    |
|-------------------------------------------------------------------------------------------------------------|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| Bölünmüş bütün dizileri tekrar ortadan ikiye bölüyoruz.                                                     |    |    | 16 | 21 | 11 |    |    |  8 | 12 | 22 |    |    |
| Bütün diziler tek bir elemana kadar parçalandığında sıradaki işleme geçiyoruz.                              |    | 16 | 21 |    | 11 |    |    |  8 | 12 |    | 22 |    |
| Tek elemanlı dizileri aynı indekslerle **sıralayarak** birleştiriyoruz.                                     | 16 |    | 21 |    | 11 |    |    |  8 |    | 12 |    | 22 |
| Ardından **sıralanmış** hale gelen dizilerin ilk elemanlarından başlayarak, yanındaki diziyle kıyaslıyoruz. |    | 16 | 21 |    | 11 |    |    |  8 | 12 |    | 22 |    |
| Eğer herhangi bir dizinin bütün elemanları sıralanır ve o dizi biterse                                      |    |    | 11 | 16 | 21 |    |    |  8 | 12 | 22 |    |    |
| Kalan diziyi olduğu gibi sıralı diziye kopyalayabiliriz. Çünkü kendi içinde zaten sıralı.                   |    |    |    |  8 | 11 | 12 | 16 | 21 | 22 |    |    |    |
|                                                                                                             |    |    |    |    |    |    |    |    |    |    |    |    |

## Big O Notation 
n boyutundaki bir dizinin maksimum parçaya bölünmesi **O(logn)**, tüm alt dizilerin birleştirilmesi ise **O(n)** zaman alır. Worst Case ve Average Case durumunda ise **O(n \* log2(n))**.\
Bu dizi için **Big O Notation: O(6 \* (log2(6))) = 15.50977500**