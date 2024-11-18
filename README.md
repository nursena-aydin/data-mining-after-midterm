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


