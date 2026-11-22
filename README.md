<div align="center">
  <img src="assets/saqta-icon.svg" alt="SAQTA" width="72" height="72" />
  <h1>SAQTA</h1>
  <p>Локальный криптографический пакет, CLI-утилита и 5-этапный анализатор шифров и уязвимостей.</p>
  <p><em>Local cryptographic suite, CLI tool, and 5-stage cipher & vulnerability analyzer.</em></p>
</div>

---

## Скачать / Download (Windows x64)

Перейдите в раздел **[Releases](https://github.com/moonshinelxv/saqta/releases/latest)**:

- **Графическое приложение (Desktop GUI):** скачайте `SAQTA-Desktop-v0.1.0-windows-x64.zip`, распакуйте архив в любую папку и запустите `saqta-desktop.exe` (рядом должен находиться `WebView2Loader.dll`).
- **Терминальная утилита (CLI):** скачайте `saqta-cli-v0.1.0-windows-x64.exe` (запуск из PowerShell/CMD: `saqta-cli-v0.1.0-windows-x64.exe --help`).
- **Проверка целостности:** сравните хэш-суммы SHA-256 с файлом `SHA256SUMS.txt` из того же релиза:
  ```powershell
  Get-FileHash SAQTA-Desktop-v0.1.0-windows-x64.zip -Algorithm SHA256
  ```

---

## Возможности / Features

- **Анализ и аудит (5 этапов):** проверка форматов и контейнеров (`PNG`, `PDF`, `ZIP`, `PEM`, `JWT`, `OpenSSL Salted__`, `PHC`-хэши), статистика энтропии и тесты NIST SP 800-22, поиск уязвимостей (утечки блоков `ECB`, `JWT alg:none`, слабые ключи `RSA`), вероятностная оценка и каскадная авто-расшифровка классических шифров и многослойных кодировок (`RU` + `EN`).
- **Шифрование и генерация ключей (107 алгоритмов):** `AES-GCM`, `ChaCha20-Poly1305`, `Ascon`, российский `ГОСТ` (`Кузнечик`, `Магма`, `Стрибог`), постквантовые алгоритмы `ML-KEM` / `ML-DSA`, асимметричные схемы (`RSA`, `ECIES`, `Ed25519`, `ElGamal`, `Paillier`), хэши, KDF и классические шифры.
- **Расшифровка:** выборочный режим (с точным ключом, маской или довычислением слабых параметров) и автоматический каскад для текстовых кодировок и классических шифров.
- **100% локально:** все операции выполняются офлайн на вашем устройстве, данные никуда не отправляются.

> **Важно:** SAQTA не является «магическим взломщиком» для корректно настроенных современных шифров (`AES-256`, `ChaCha20`, `ГОСТ`, `RSA-2048+`) без ключа — программа помогает определить тип данных, выявить ошибки реализации/слабые параметры, расшифровать классические шифры и надёжно защищать файлы.

---

## Примечание / Notice

Этот репозиторий предназначен исключительно для публикации официальных сборок и обновлений SAQTA. Исходный код проекта закрыт (`© 2026 moonshinelxv`, см. [LICENSE](LICENSE)).

This public repository distributes official compiled releases and updates for SAQTA only. Source code is proprietary and closed (`© 2026 moonshinelxv`, see [LICENSE](LICENSE)).
