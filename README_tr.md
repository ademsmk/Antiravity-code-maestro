# Maestro: Yapay Zeka Geliştirme Orkestratörü

Antigravity platformu için elit seviye orkestrasyon çerçevesi. Özelleşmiş ajanlar, modüler beceriler, akıllı hook sistemi ve kalıcı bellek sistemleri aracılığıyla yapay zeka geliştirmeyi güçlendirir.

> **Versiyon:** 1.0.0  
> **Yazar:** [ademsmk](https://github.com/ademsmk/Antiravity-code-maestro) • [GitHub](https://github.com/ademsmk/Antiravity-code-maestro)  
> **Felsefe:** "Nasıl'dan önce Neden. Mimari, uygulamadan önce gelir."

## Hızlı Başlangıç

### Kurulum

Antigravity Agent Entegrasyonu:
1. Proje kök dizinine `.agent` klasörünü ekleyin.
2. `.agent/agent.json` dosyasını [Antigravity Agent Dokümantasyonu](https://antigravity.google/docs/agent) doğrultusunda yapılandırın.
3. Maestro Agent'ı Antigravity platformunda yönetin ve çalıştırın.

### Önkoşullar

- **Node.js 18+** (hook sistemi için gereklidir)
- Antigravity platform hesabı

### Kullanım

Antigravity üzerinde Agent paneli veya komut arayüzü ile Maestro ile etkileşime geçebilirsiniz.

```bash
# Basic orchestration
/maestro your task description

# With Ralph Wiggum (autonomous iterations)
/maestro fix bugs and improve code. ralph 5 iterations

# Design mode
/maestro design new authentication system

# Plan mode
/maestro plan implement user dashboard

# Use the Grandmaster agent directly
/agent:grandmaster
```

## Mimari

```
┌─────────────────────────────────────────────────────────────────────┐
│                         MAESTRO SİSTEMİ                              │
├─────────────────────────────────────────────────────────────────────┤
│  ┌──────────┐    ┌──────────────┐    ┌─────────────────────────┐   │
│  │ /maestro │───▶│ grandmaster  │───▶│       BECERİLER         │   │
│  │  komutu  │    │    ajanı      │    │ (frontend, backend,     │   │
│  └──────────┘    └──────────────┘    │  tdd, debug, vb.)       │   │
│                         │            └─────────────────────────┘   │
│                         ▼                                           │
│  ┌─────────────────────────────────────────────────────────────┐   │
│  │                    HOOK SİSTEMİ                              │   │
│  │  SessionStart │ PostToolUse │ Stop │ PreCompact │ vb.       │   │
│  └─────────────────────────────────────────────────────────────┘   │
│                         │                                           │
│                         ▼                                           │
│  ┌──────────────────────────────────────────────────────────────┐   │
│  │                   UZUN SÜRELİ BELLEK (LTM)                    │   │
│  │                      (brain.jsonl)                            │   │
│  └──────────────────────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────────────────────┘
```

## Proje Yapısı

maestro/
├── .agent/
│   ├── agents/              # Ajanlar (grandmaster.md)
│   ├── commands/            # Özel komutlar (/maestro)
│   ├── skills/              # Uzmanlık becerileri
│   └── workflows/           # Otomasyon scriptleri (hook'lar)
│       ├── hooks.json       # Hook yapılandırması
│       └── lib/             # Ortak araçlar
│   ├── agent.json           # Agent yapılandırması
│   └── README.md            # Agent dokümantasyonu
├── package.json             # Node.js meta verileri
├── LICENSE                  # MIT Lisansı
├── README.md                # İngilizce Dokümantasyon
├── README_tr.md             # Türkçe Dokümantasyon
└── SKILL.md                 # Yönetişim Protokolü

## Bellek Sistemleri

### Uzun Süreli Bellek (brain.jsonl)
Oturumlar arası kalıcı proje bağlamı:
- **Tech Stack:** Framework'ler, bağımlılıklar, mimari kalıplar
- **Kararlar:** Alınan önemli mimari kararlar
- **Hedefler:** Proje amaçları
- **Hatalar:** Bilinen sorunlar ve engelleyiciler
- **Compact Geçmişi:** Context sıkıştırması sonrası oturum özetleri
- **Dosya Değişiklikleri:** Edit ve Create işlemlerinin kaydı

## Ralph Wiggum: Otonom QA

Dört Sütunlu Elit QA Sistemi:

| Sütun | Amaç |
|-------|------|
| **Proactive Gate** | Kodlamadan ÖNCE kenar durum tespiti |
| **Reflection Loop** | Öz-eleştiri ve iyileştirme |
| **Verification Matrix** | Test kapsama takibi (minimum %80) |
| **Circuit Breaker** | Duraksama tespiti ve pivot stratejileri |

Aktifleştirme: `ralph N iterasyon` veya "Ralph Wiggum modu"

## Becerilere Genel Bakış

| Beceri | Açıklama |
|--------|----------|
| `clean-code` | 2025 standartları, SOLID, güvenlik öncelikli |
| `frontend-design` | Atomic Design 2.0, Lovable/v0 standardı |
| `backend-design` | Zero-trust, API sözleşmeleri |
| `tdd-mastery` | Demir Yasa: Koddan önce test |
| `debug-mastery` | 4 fazlı sistematik hata ayıklama |
| `verification-mastery` | Tamamlamadan önce kanıt |
| `brainstorming` | Tasarım öncelikli metodoloji |
| `planning-mastery` | Küçük parçalı görev kırılımı |
| `git-worktrees` | İzole özellik geliştirme |
| `ralph-wiggum` | Otonom QA orkestrasyonu |
| `optimization-mastery` | Performans, INP, kısmi hidrasyon |
| `context7` | Upstash üzerinden otomatik kütüphane dokümantasyonu |
| `browser-extension` | Manifest v3, servis çalışanları |

## Platform Uyumluluğu

| Platform | Puan | Notlar |
|----------|------|--------|
| **Antigravity** | ⭐⭐⭐⭐⭐ | Doğal ortam, tam işlevsellik |
| **Windows** | ⭐⭐⭐⭐⭐ | Tam platformlar arası destek |
| **macOS** | ⭐⭐⭐⭐⭐ | Tam platformlar arası destek |
| **Linux** | ⭐⭐⭐⭐⭐ | Tam platformlar arası destek |

## Çekirdek Protokoller

1. **Sokratik Geçit:** Varsaymadan önce netleştirici sorular sor
2. **Önce Düşün:** Karmaşık eylemlerden önce `<think>` kullan
3. **TDD Demir Yasası:** Başarısız test olmadan üretim kodu yok
4. **Doğrulama:** Tamamlama iddialarından önce kanıt
5. **Temiz Kod:** TODO/FIXME yok, tembel placeholder yok

## Teşekkür

Birçok beceri [obra/superpowers](https://github.com/obra/superpowers) projesinden ilham alınarak adapte edilmiş ve Maestro orkestrasyon ortamı için ağır bir şekilde optimize edilmiştir:

| Özellik | Kaynak | Maestro Becerisi |
|---------|--------|------------------|
| TDD Demir Yasası | superpowers/tdd | `tdd-mastery` |
| Sistematik Hata Ayıklama | superpowers/debugging | `debug-mastery` |
| Doğrulama Protokolü | superpowers/verification | `verification-mastery` |
| Beyin Fırtınası Metodu | superpowers/brainstorming | `brainstorming` |
| Uygulama Planlama | superpowers/planning | `planning-mastery` |
| Git Worktrees | superpowers/worktrees | `git-worktrees` |

## Yıldız Geçmişi



## Yazar

**[ademsmk](https://github.com/ademsmk/Antiravity-code-maestro)** tarafından oluşturuldu ve sürdürülüyor.

- GitHub: [github.com/ademsmk/Antiravity-code-maestro](https://github.com/ademsmk/Antiravity-code-maestro)
- X/Twitter: [x.com/smk_adem](https://x.com/smk_adem)

## Lisans

MIT Lisansı - Detaylar için [LICENSE](LICENSE) dosyasına bakınız.

---

*Otonom geliştirmenin geleceğini Antigravity için orkestre ediyoruz.*
