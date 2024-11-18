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

#*************************************************************************************************************************

# Manhattan Mesafesi Hesaplama

### Adımlar:
1. İki vektör arasındaki her elemanın farkının mutlak değerini alırız.
2. Bu mutlak farkların toplamı, Manhattan mesafesini verir.

Aşağıdaki R kodu, iki vektör arasındaki Manhattan mesafesini hesaplamak için kullanılabilir:

```r
# Manhattan mesafesini hesapla
manhattan_mesafe <- sum(abs(sayilar1 - sayilar2))

# Mesafeyi yazdır
print(manhattan_mesafe)

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



