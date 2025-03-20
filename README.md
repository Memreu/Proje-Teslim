# Metro Ağ Simülasyonu 🚅

Bu proje, metro istasyonları arasında en az aktarmalı veya en hızlı rotayı bulmak için geliştirilmiş bir Python uygulamasıdır.

***

## 📕 Kullanılan Teknolojiler ve Kütüphaneler

- **Python 3.x**: Proje, modern programlama dili Python kullanılarak geliştirilmiştir.
- **collections.deque**: BFS algoritmasında hızlı ve verimli kuyruk işlemleri için tercih edilmiştir.
- **collections.defaultdict**: Varsayılan değerler atanabilen sözlük yapısı, metro hatlarını kolayca organize etmek için kullanılmıştır.
- **heapq**: En hızlı rotayı belirlemek için kullanılan öncelikli kuyruk (min-heap) yapısını sağlar.
- **typing**: Tip kontrolü ve kod okunabilirliğini artırmak amacıyla tip açıklamaları için kullanılmıştır.

***

## 🦾 Algoritmaların Çalışma Mantığı

### 1. BFS Algoritması
BFS algoritması, en az aktarmalı rotayı bulmak için kullanılır. 
**Algoritmanın çalışma mantığı:**
- Başlangıç istasyonundan başlar
- Her seviyede tüm komşu istasyonları ziyaret eder
- Ziyaret edildi olarak işaretlenmiş istasyonlar tekrar ziyaret edilmez
- İstasyonlar işlenir
- İlk bulunan rota, en az aktarmalı rota olacak şekilde çıktı verecektir

### 2. A* Algoritması
A* algoritması, en hızlı rotayı bulmak için kullanılır. 
**Nasıl Çalışır:**
- Her adımda en düşük maliyetli yolu seçer
- Öncelikli kuyruk (pq) kullanarak en düşük maliyetli yolları önceliklendirir
- İstasyonlar arası tahmini süreyi hesaplar

***

### ❓ Neden Bu Algoritmalar?

- **BFS**: Aktarma sayısını minimize etmek için grafikte "seviyeye dayalı" tarama gereklidir ve BFS bunun için idealdir.
- **A***: En hızlı rotayı bulur. Heuristic fonksiyonu ile performansı artırır Dinamik rota optimizasyonuna sahiptir. Öncelikli pq yapısı ile verimli aramalar için idealdir.
  
***

