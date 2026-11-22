<div align="center">
  <img src="assets/saqta-icon.svg" alt="SAQTA" width="72" height="72" />
  <h1>SAQTA</h1>
  <p>Local cryptographic suite, CLI utility, and 5-stage cipher &amp; vulnerability analyzer.</p>
</div>

---

## Download (Windows x64)

Go to **[Releases](https://github.com/moonshinelxv/saqta/releases/latest)**:

- **Windows Installer (Recommended):** download `SAQTA-v0.1.0-setup.exe`. Installs **SAQTA** and **SAQTA CLI**, registers Start Menu and Windows Search shortcuts, optionally adds a Desktop shortcut and adds `SAQTA-CLI` to `PATH`, and supports clean uninstall via Windows Installed Apps.
- **Portable Desktop App:** download `SAQTA-v0.1.0-windows-x64.zip`, extract to any folder, and run `SAQTA.exe` (keep `WebView2Loader.dll` in the same folder). Standalone `SAQTA.exe` is also attached for portable updates.
- **Standalone CLI (`SAQTA CLI`):** download `SAQTA-CLI.exe` and run from PowerShell or CMD (`SAQTA-CLI.exe --help`).
- **Verify Integrity:** check SHA-256 hashes against `SHA256SUMS.txt` attached to the release:
  ```powershell
  Get-FileHash SAQTA-v0.1.0-setup.exe -Algorithm SHA256
  ```

> **Windows SmartScreen Notice:** Because SAQTA is an independent unsigned build without an EV code-signing certificate, Windows Defender SmartScreen may display *"Windows protected your PC"* on first launch. Click **More info** -> **Run anyway**, and verify your download's SHA-256 hash against `SHA256SUMS.txt`.

---

## Features

- **Analyze & Audit (5 Stages):** container and format inspection (`PNG`, `PDF`, `ZIP`, `PEM`, `JWT`, `OpenSSL Salted__`, `PHC` password hashes), Shannon/min-entropy &amp; NIST SP 800-22 statistics, vulnerability checks (`ECB` block leaks, `JWT alg:none`, weak `RSA` parameters), probabilistic classification, and cascade recovery for classical ciphers and multi-layer encodings.
- **Encrypt & Keygen (107 Algorithms):** `AES-GCM`, `ChaCha20-Poly1305`, `Ascon`, `GOST` (`Kuznyechik`, `Magma`, `Streebog`), post-quantum `ML-KEM` / `ML-DSA`, asymmetric cryptography (`RSA`, `ECIES`, `Ed25519`, `ElGamal`, `Paillier`), hashes, KDFs, classical ciphers, and encodings.
- **Decrypt (Selective & Auto-Cascade):** decrypt with an exact key, partial key mask, or weak-parameter computation, or run automated cascade unwrapping across nested encodings and classical ciphers.
- **Bilingual Inside the App:** full English and Russian UI and text-analysis oracle.
- **100% Local Execution:** everything runs offline on your machine via the native Rust engine with zero telemetry or network uploads.

> **Honest Scope:** SAQTA cannot magically crack properly configured modern encryption (`AES-256`, `ChaCha20`, `GOST`, `RSA-2048+`) without a key. It is designed to identify formats/ciphers, uncover implementation weaknesses, recover classical ciphers and encodings, and protect files with modern cryptography.

---

## Distribution

This public repository distributes official compiled releases and updates for SAQTA only. Source code is proprietary and closed (`© 2026 moonshinelxv`, see [LICENSE](LICENSE)).
