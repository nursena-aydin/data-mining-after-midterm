# data-mining-after-midterm

# Öklid Mesafesi Hesaplama


```r
# İki vektör
sayilar1 <- c(12, 15, 29, 40)
sayilar2 <- c(5, 14, 30, 50)

# İki vektör arasındaki Öklid mesafesini hesapla
mesafe <- sqrt(sum((sayilar1 - sayilar2)^2))

# Mesafeyi yazdır
print(mesafe)


#ÇIKTILAR: 12.29

#*************************************************************************************************************************

# Manhattan Mesafesi Hesaplama

### Adımlar:
1. İki vektör arasındaki her elemanın farkının mutlak değerini alırız.
2. Bu mutlak farkların toplamı, Manhattan mesafesini verir.

Aşağıdaki R kodu, iki vektör arasındaki Manhattan mesafesini hesaplamak için kullanılabilir:

```r
# İki vektör
sayilar1 <- c(12, 15, 29, 40)
sayilar2 <- c(5, 14, 30, 50)

# Manhattan mesafesini hesapla
manhattan_mesafe <- sum(abs(sayilar1 - sayilar2))

# Mesafeyi yazdır
print(manhattan_mesafe)


#ÇIKTILAR: 19

#***************************************************************************************************************************

## Minkowski Mesafesi Hesaplama (p=3)


Burada \( p = 3 \) olduğunda, aşağıdaki R kodu kullanılabilir:

```r
# İki vektör
sayilar1 <- c(12, 15, 29, 40)
sayilar2 <- c(5, 14, 30, 50)

# p=3 için Minkowski mesafesini hesapla
p <- 3
minkowski_mesafe <- (sum(abs(sayilar1 - sayilar2)^p))^(1/p)

# Mesafeyi yazdır
print(minkowski_mesafe)

#ÇIKTILAR: 11.03
#***************************************************************************************************************************

# Öklid ve Manhattan Mesafesi Hesaplama

Bu örnekte, bir veri çerçevesindeki (data frame) sayısal sütunlar arasındaki **Öklid** ve **Manhattan mesafelerini** hesaplamak için R dilinde bir kod bulunmaktadır.

Öncelikle aşağıdaki veri çerçevesine sahibiz:

```r
data <- data.frame(
  Urun = c("A", "B", "C"),
  Fiyat = c(150, 100, 255),
  Kalite = c(3.4, 4.5, 5.3)
)


# Öklid mesafesini hesapla
oklid_mesafesi2 <- dist(data[,-1], method = "euclidean")
print(as.matrix(oklid_mesafesi2))

#ÇIKTI:
         1        2        3
1   0.0000  50.0121 105.0172
2  50.0121   0.0000 155.0021
3 105.0172 155.0021   0.0000


# Manhattan mesafesini hesapla
manhattan_mesafesi2 <- dist(data[,-1], method = "manhattan")
print(as.matrix(manhattan_mesafesi2))

#ÇIKTI:
      1     2     3
1   0.0  51.1 106.9
2  51.1   0.0 155.8
3 106.9 155.8   0.0

ÖDEV:
Bu veriseti için Minkovski mesafesini hesaplayınız

#ÇÖZÜM

# Minkowski mesafesini hesaplama (p=3)
p <- 3
minkowski_mesafe <- dist(data[,-1], method = "minkowski", p = p)
print(as.matrix(minkowski_mesafe))

#ÇIKTI:
          1         2        3
1   0.00000  50.00018 105.0002
2  50.00018   0.00000 155.0000
3 105.00021 155.00001   0.0000




