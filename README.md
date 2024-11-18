# data-mining-after-midterm

# Öklid Mesafesi Hesaplama

Bu örnekte, iki vektör arasındaki Öklid mesafesini hesaplamak için R dilinde bir kod bulunmaktadır. 

Öklid mesafesi, iki nokta arasındaki düz çizgi mesafesini hesaplamak için kullanılır ve genellikle şu şekilde tanımlanır:

\[
d(\mathbf{X}, \mathbf{Y}) = \sqrt{\sum_{i=1}^{n} (x_i - y_i)^2}
\]

Bu hesaplama için aşağıdaki R kodu kullanılabilir:

```r
# İki vektör
sayilar1 <- c(12, 15, 29, 40)
sayilar2 <- c(5, 14, 30, 50)

# İki vektör arasındaki Öklid mesafesini hesapla
mesafe <- sqrt(sum((sayilar1 - sayilar2)^2))

# Mesafeyi yazdır
print(mesafe)

#*********************************************************************************************************************


# Manhattan Mesafesi Hesaplama

Bu örnekte, iki vektör arasındaki **Manhattan mesafesini** hesaplamak için R dilinde bir kod bulunmaktadır.

Manhattan mesafesi (ya da L1 mesafesi), iki vektör arasındaki farkların mutlak değerlerinin toplamıdır ve şu şekilde hesaplanır:

\[
d(\mathbf{X}, \mathbf{Y}) = \sum_{i=1}^{n} |x_i - y_i|
\]

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

