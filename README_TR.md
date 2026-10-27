# Bebektepe Garden — Android uygulama başlangıç paketi

Bu klasör, Android Chrome'da ana ekrana eklenebilen bir PWA başlangıç arayüzüdür. Aynı yayımlanmış adres daha sonra masaüstünde de açılabilir.

## Neler var?
- Rezervasyon ve müşteri/çift bilgileri
- Sözleşme, kapora/alınan ödeme ve kalan tutar görünümü
- Organizasyon ayrıntıları: seans, başlangıç saati, davetli/personel sayısı, menü, müzik, masa düzeni, fotoğraf-video, görev dağılımı, ek hizmet, saatli akış, özel istek/prova notları
- Organizasyon/personel formunu yazdırma veya PDF kaydetme
- Gelir-gider hareketleri
- PWA manifest ve servis çalışanı dosyaları
- Supabase için örnek tablo ve RLS SQL dosyası

## Dürüst durum bilgisi
Bu paket henüz internette yayımlanmadı. Uygulama arayüzü başlangıç aşamasında; bu HTML sürümünde gerçek Supabase oturum açma/veri kaydetme bağlantısı henüz tamamlanmamıştır. Ekrandaki örnek mod verileri kalıcı değildir. Gerçek müşteri/finans bilgisi girmeyin.

## Sonraki kurulum aşamaları
1. Supabase'de proje oluşturun.
2. `supabase/schema.sql` içeriğini Supabase Dashboard > SQL Editor'da çalıştırın ve RLS izinlerini test edin.
3. Bu klasörü HTTPS destekleyen bir hostinge (ör. Vercel) yayımlayın.
4. Android Chrome ile yayımlanan adresi açıp menüden **Ana ekrana ekle / Uygulamayı yükle** seçin.
5. Gerçek veri kaydetme ve giriş/rol yönetimi entegrasyonunu tamamlayıp test etmeden canlı kullanıma geçmeyin.
6. İlk kullanıcıyı oluşturduktan sonra yönetici rolü için SQL'deki örnek komutu kendi e-postanızla çalıştırın. Yeni hesaplar varsayılan olarak personel rolü alır.

## Güvenlik
- `service_role` veya secret key'i hiçbir zaman tarayıcıya ya da bu pakete koymayın.
- Gerçek kullanıma geçmeden önce RLS kurallarını yönetici/personel hesaplarıyla test edin.
- Yedekleme, kayıt geçmişi ve finans işlemi denetim izi ayrıca tamamlanmalıdır.

Resmî belgeler:
- https://supabase.com/docs/guides/auth
- https://supabase.com/docs/guides/database/postgres/row-level-security
- https://vercel.com/docs
