# Faal UI WordPress Widget – Tasarım Notları

Bu tasarım çıktısı, istenen iki skillin kurulumu denenerek başlatıldı:

- `frontend-design`
- `web-design-guidelines`

> Kurulum denemesi ağ/proxy kısıtı nedeniyle başarısız oldu (`CONNECT tunnel failed, 403 Forbidden`).
> Bu yüzden aynı hedefe uygun şekilde erişilebilirlik, mobil öncelik, görsel hiyerarşi ve tema izolasyonu prensipleriyle fallback tasarım üretildi.

## Üretilen çıktılar

- `faal-ui-widget-prototype.html`: Mobil-first prototip markup
- `faal-ui-widget-prototype.css`: Style sistemi (renk, spacing, focus states, responsive kırılımlar)

## WordPress'e taşıma önerisi

1. Prototipi bir shortcode içinde render edin (`[faalui_tool]`).
2. CSS'i namespace'li sınıf köküyle (`.faalui-widget`) izole edin.
3. API işlemlerini frontend'den değil WP REST proxy üzerinden yapın.
4. Gutenberg block varyantını ikinci adımda ekleyin.

## UX kararları

- Tek kart üzerinde adım adım ilerleme (maaş günü -> masraflar -> hesapla)
- Birincil CTA (`Hesapla`) için yüksek kontrastlı aksan rengi
- Form alanlarında net etiket + odak durumu
- Dar ekranda tek sütuna düşen responsive form yapısı
