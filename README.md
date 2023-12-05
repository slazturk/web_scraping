# Web Scraping
Projenin Amacı:
"https://turkishnetworktimes.com/kategori/gundem/" web sitesindeki veriler requests ve beautifulsoup kütüphaneleri kullanılarak çekilmiştir.
----------
İlk olarak projede istendiği üzere web sitesinin ilk 50 sayfasına ulaşılmıştır. Daha sonra her bir sayfadaki haberlere ulaşabilmek için sayfalar "getEachNews" isimli fonksiyona gönderilmiştir.

def getEachNews(soup):
Fonksiyon parametresi olarak alınan sayfada bulunan haberlere ulaşmak için haberlerin bulunduğu ilgili kolona ulaşılmıştır. Daha sonra bu kolon içindeki her bir haberin url linki, görüntülenen fotoğraf ve haber başlığı bilgileri bir "dictionary" içine kaydedilmiştir. 
Daha sonra her bir haber linkinde bulunan içeriğe erişilmesi için haberin url linki "extractData" isimli fonksiyona gönderilmiştir.

def extractData(get_url):
Bu fonksiyon her bir haber linkinde bulunan metin içeriğini, haberin yayınlanma ve son güncelleme tarihlerini çekmeyi sağlar. Bulunan her bir text içeriği birleşirilip en çok kullanılan 10 kelime bulunmak üzere "mostFrequentWords" isimli fonksiyona gönderilmiştir.

def mostFrequentWords(all_text):
Bu fonksiyonda her bir metinde en çok tekrarlanan 10 kelime bulunmuştur.

----------
