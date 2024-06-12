# Apple Inc. (AAPL) Hisse Senedi Fiyat Tahmini

Bu proje, Apple Inc. (AAPL) hisse senedi fiyatlarını tahmin etmek amacıyla çeşitli makine öğrenimi modellerini kullanarak bir analiz ve tahmin çalışması yapmaktadır. Projenin temel amacı, geçmiş fiyat verilerini kullanarak gelecekteki fiyat hareketlerini tahmin etmek ve bu tahminlerin doğruluğunu değerlendirmektir. Bu bağlamda, Random Forest Regressor ve Gradient Boosting Regressor modelleri kullanılarak iki farklı tahmin yöntemi incelenmiştir.

## Kullanılan Kütüphaneler
- `yfinance`: Hisse senedi verilerini almak için kullanılır.
- `pandas`: Veri işleme ve analiz için kullanılır.
- `numpy`: Sayısal işlemler için kullanılır.
- `matplotlib`: Grafik çizimi için kullanılır.
- `seaborn`: Grafiklerin estetik görünümünü artırmak için kullanılır.
- `scikit-learn`: Makine öğrenimi modelleri ve veri bölme işlemleri için kullanılır.
- `vectorbt`: Portföy backtest ve performans analizi için kullanılır.

## Veri Toplama
Hisse senedi verileri `yfinance` kütüphanesi kullanılarak alınmıştır. AAPL hisse senedi verileri 12 Haziran 2020 ile 12 Haziran 2024 tarihleri arasında indirilmiştir.

```python
import yfinance as yf

ticker = 'AAPL'
stock_data = yf.download(ticker, start='2020-06-12', end='2024-06-12')

print(stock_data.head())
print(stock_data.tail())
