<div align="center">
  <img src="assets/saqta-icon.svg" alt="SAQTA" width="72" height="72" />
  <h1>SAQTA</h1>
  <p>Local cryptographic suite, CLI utility, 0.00–10.00 strength evaluator, and offline attack &amp; audit lab.</p>
</div>

---

## Download (Windows x64)

Go to **[Releases](https://github.com/moonshinelxv/saqta/releases/latest)**:

- **Windows Installer (Recommended):** download `SAQTA-v0.2.0-setup.exe`. Installs **SAQTA** and **SAQTA CLI**, registers Start Menu and Windows Search shortcuts, optionally adds a Desktop icon and adds `SAQTA-CLI` to `PATH`, and supports clean uninstall via Windows Installed Apps.
- **Portable Desktop App:** download `SAQTA-v0.2.0-windows-x64.zip`, extract to any folder, and run `SAQTA.exe` (keep `WebView2Loader.dll` in the same folder).
- **Standalone CLI (`SAQTA CLI`):** download `SAQTA-CLI.exe` and run from PowerShell or CMD (`SAQTA-CLI.exe --help`).
- **Verify Integrity:** check SHA-256 hashes against `SHA256SUMS.txt` attached to the release:
  ```powershell
  Get-FileHash SAQTA-v0.2.0-setup.exe -Algorithm SHA256
  ```

> **Windows SmartScreen Notice:** Because SAQTA is an independent unsigned build without an EV code-signing certificate, Windows Defender SmartScreen may display *"Windows protected your PC"* on first launch. Click **More info** -> **Run anyway**, and verify your download's SHA-256 hash against `SHA256SUMS.txt`.

---

## Features

- **0.00–10.00 Strength Rating System:** every algorithm in the 107-cipher catalog carries a security rating and attack notes, while both the **Encrypt** and **Analyze** views compute live `0.00–10.00` scores based on mode safety (AEAD vs ECB/CBC), passphrase entropy, KDF (`Argon2id`/`scrypt`/`PBKDF2`/`HKDF`), nonce hygiene, and NIST SP 800-22 statistics.
- **Analyze & Audit (5 Stages):** container and format inspection (`PNG`, `PDF`, `ZIP`, `PEM`, `JWT`, `OpenSSL Salted__`, `PHC` password hashes), Shannon/min-entropy &amp; NIST SP 800-22 statistics, vulnerability checks (`ECB` block leaks, `JWT alg:none` &amp; `kid`, static zero IV, `Sweet32` 64-bit risk, weak KDF cost, weak `RSA`), probabilistic classification, and cascade recovery.
- **Offline Cryptographic Attack &amp; Audit Lab:** GOST Kuznyechik S-box linear/differential (`LAT`/`DDT`) audit vs AES, Birthday Paradox &amp; Sweet32 calculator, Merkle–Damgård length-extension attack (`SHA-256`, `SHA-1`, `MD5`) with `HMAC` `ipad`/`opad` defense, local Vaudenay CBC Padding Oracle simulator, CBC bit-flipping, AES-GCM nonce-reuse Joux attack (`GF(2^128)`), ECDSA repeated-nonce / malleability / HNP bias &amp; RSA parameter/Hastad/common-modulus/forgery audits, Two-Time Pad crib-dragging, and LCG predictor.
- **Encrypt &amp; Keygen (107 Algorithms):** `AES-GCM`, `AES-GCM-SIV`, `ChaCha20-Poly1305`, `XChaCha20-Poly1305`, `Ascon`, `GOST` (`Kuznyechik`, `Magma`, `Streebog`), post-quantum `ML-KEM` / `ML-DSA`, hybrid `X25519 + ML-KEM-768`, asymmetric (`RSA`, `ECIES`, `Ed25519`, `ElGamal`, `Paillier`), hashes, KDFs, classical ciphers, and encodings.
- **English Default + EN/RU Switcher:** launches in English by default across both the app and Windows installer, with one-click EN/RU localization inside the app.
- **100% Local Execution:** runs completely offline via the native Rust engine with zero network uploads or telemetry.

> **Honest Scope:** SAQTA cannot magically crack properly configured modern encryption (`AES-256`, `ChaCha20`, `GOST`, `RSA-2048+`) without a key or implementation flaw. It identifies formats and weaknesses, executes real mathematical audits offline, recovers weak classical ciphers/encodings, and protects your data with strong modern cryptography.

---

## Distribution

This public repository distributes official compiled releases and updates for SAQTA only. Source code is proprietary and closed (`© 2026 moonshinelxv`, see [LICENSE](LICENSE)).
