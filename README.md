# Ses Transkript Uygulaması - Streamlit

Bu uygulama, ses kayıtlarını metne dönüştüren ve Word belgesi olarak indirmenize olanak sağlayan bir Streamlit web uygulamasıdır.

## Özellikler

- Farklı ses formatlarını destekler (WAV, MP3, OGG, M4A, MP4)
- Google Speech Recognition API kullanarak ses tanıma (ücretsiz)
- Transkriptleri Word (.docx) belgesi olarak indirme
- Kullanıcı dostu Streamlit arayüzü
- Uzun ses kayıtlarını otomatik bölümleme ile işleme
- İşlem ilerleme durumu gösterimi

## Demo

Bu uygulamanın canlı demosuna şu adresten erişebilirsiniz:

[Ses Transkript Uygulaması Demo](https://streamlit.io/) - *Streamlit Cloud'a deploy ettikten sonra buradaki URL'yi güncelleyin*

## Kurulum ve Yerel Çalıştırma

1. Gerekli bağımlılıkları yükleyin:
```bash
pip install -r requirements.txt
```

2. FFmpeg'i yükleyin:
   - Windows: [FFmpeg İndirme Sayfası](https://ffmpeg.org/download.html)
   - Linux: `sudo apt-get install ffmpeg`
   - MacOS: `brew install ffmpeg`

3. Uygulamayı başlatın:
```bash
streamlit run streamlit_app.py
```

## Streamlit Cloud'a Deploy Etme

1. Bu repoyu GitHub'a pushleyin.
2. [Streamlit Cloud](https://streamlit.io/cloud) hesabınıza giriş yapın.
3. "New app" butonuna tıklayın ve GitHub reponuzu seçin.
4. Main file olarak `streamlit_app.py` belirtin.
5. "Deploy" butonuna tıklayın.

## Kullanım

1. Uygulama sayfasını açın.
2. "Ses dosyası yükleyin" alanından bir ses dosyası seçin.
3. "Transkript Et" düğmesine tıklayın.
4. Transkript metin kutusunda görüntülenecek ve Word belgesini indirebileceksiniz.

## Özelleştirme Seçenekleri

- Farklı dil desteği için, `streamlit_app.py` dosyasında `recognize_google` fonksiyonundaki `language` parametresini değiştirebilirsiniz.
- Ses dosyası bölme uzunluğunu `split_audio` fonksiyonunda `chunk_length_ms` parametresini değiştirerek ayarlayabilirsiniz.

## Notlar

- Ses tanıma için internet bağlantısı gereklidir.
- Uygulama uzun ses kayıtlarını parçalayarak işler, bu sayede Google Speech Recognition API sınırlamalarını aşar.
- Türkçe dil desteği varsayılan olarak ayarlanmıştır. 