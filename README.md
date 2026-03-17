# empty

---

## architecture

3 components:

1. **SMTP Gateway (Postfix)**  
   install this.

2. **mail filter (mail_filter.py)**  
   - analys text of letter (ML)
   - dont incnlude im lazy (VirusTotal)
   - decision-making (delivery / quarantine)

3. **ML API (Flask)**  
   Provides REST API for classification of letters:
   - spam
   - phishing
   - ham

4. **Quarantine Web Interface**  
   Cringe web interface (pls edit this part @altynai):
   - here u see blocked letters
   - unlock it manually (release) like fortimail (never mind)

---

## Основной функционал

- SMTP-прокси на базе Postfix
- Классификация писем с использованием MultiOutput ML модели:
  - ham
  - spam
  - phishing
- Интеграция с VirusTotal (по SHA256 вложений)
- Карантин писем
- Веб-интерфейс управления карантином
- Логирование событий (audit log)
- Добавление заголовков анализа в письмо:
  - X-ML-Spam
  - X-ML-Phishing
  - X-ML-Decision
  - X-VT-Malicious-Attachment

---

## Структура проекта
