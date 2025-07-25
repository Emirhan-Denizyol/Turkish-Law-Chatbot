# 🇹🇷 Turkish Constitutional Law Chatbot (LLM + RAG)

Bu proje, Türkiye Cumhuriyeti Anayasası’na dayalı olarak doğru, tutarlı ve kaynak göstererek yanıt üretebilen bir Türkçe hukuk danışman chatbot sistemidir. Proje kapsamında açık kaynak büyük dil modeli (LLM) fine-tune edilerek hem hukuki içeriklere özel hale getirilmiş hem de RAG (Retrieval-Augmented Generation) yapısı ile desteklenmiştir.

## 🔍 Amaç

Anayasa hukukuna dair sorulara:
- **Anayasa maddelerine dayalı yanıtlar vermek**,
- **Halüsinatif (uydurma) cevapları azaltmak**,
- **Maddenin içeriğinden özetleyerek sade açıklamalar sunmak**.

## 🧠 Kullanılan Model

- Model: `unsloth/llama-3-8b-Instruct`
- Eğitim yöntemi: PEFT (LoRA) + Unsloth hızlandırması
- Eğitim verisi: 1982 Türkiye Cumhuriyeti Anayasası + soru-cevap çiftleri
- Eğitim donanımı: Google Colab / A100 GPU (40 GB)
- Maks sekans uzunluğu: 1024 token

## 📁 Proje İçeriği

| Dosya / Klasör                          | Açıklama |
|----------------------------------------|----------|
| `Turkish_Law_Chatbot.ipynb`            | Eğitim, LoRA birleştirme ve inference adımlarını içeren Jupyter notebook |
| `1982_anayasasi_maddeler.csv`          | Madde numarası ve içeriklerini içeren orijinal anayasa veri seti |
| `anayasa_maddeleri_iceriğe_gore_baslikli.csv` | Her maddeye içerik odaklı başlık eklenmiş sürüm |
| `llama-anayasa-chatbot-full/`          | Fine-tune edilmiş ve merge edilmiş tam model klasörü |
| `README.md`                            | Proje açıklaması ve kullanım talimatları |

## 🛠️ Kurulum

```bash
git clone https://github.com/kullanici_adiniz/turkish-law-chatbot.git
cd turkish-law-chatbot

# Ortamı kur
pip install -r requirements.txt
