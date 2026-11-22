<div align="center">
  <img src="assets/saqta-icon.svg" alt="SAQTA" width="72" height="72" />
  <h1>SAQTA</h1>
  <p>Local cryptographic suite, CLI utility, and 5-stage cipher & vulnerability analyzer.</p>
</div>

---

## Download (Windows x64)

Go to **[Releases](https://github.com/moonshinelxv/saqta/releases/latest)**:

- **Desktop App (GUI):** download `SAQTA-Desktop-v0.1.0-windows-x64.zip`, extract it to any folder, and run `saqta-desktop.exe` (keep `WebView2Loader.dll` in the same folder).
- **Command-Line Tool (CLI):** download `saqta-cli-v0.1.0-windows-x64.exe` and run from PowerShell or CMD (`saqta-cli-v0.1.0-windows-x64.exe --help`).
- **Verify Integrity:** check SHA-256 hashes against `SHA256SUMS.txt` attached to the release:
  ```powershell
  Get-FileHash SAQTA-Desktop-v0.1.0-windows-x64.zip -Algorithm SHA256
  ```

---

## Features

- **Analyze & Audit (5 Stages):** container and format inspection (`PNG`, `PDF`, `ZIP`, `PEM`, `JWT`, `OpenSSL Salted__`, `PHC` password hashes), Shannon/min-entropy & NIST SP 800-22 statistics, vulnerability checks (`ECB` block leaks, `JWT alg:none`, weak `RSA` parameters), probabilistic classification, and cascade recovery for classical ciphers and multi-layer encodings.
- **Encrypt & Keygen (107 Algorithms):** `AES-GCM`, `ChaCha20-Poly1305`, `Ascon`, `GOST` (`Kuznyechik`, `Magma`, `Streebog`), post-quantum `ML-KEM` / `ML-DSA`, asymmetric cryptography (`RSA`, `ECIES`, `Ed25519`, `ElGamal`, `Paillier`), hashes, KDFs, classical ciphers, and encodings.
- **Decrypt (Selective & Auto-Cascade):** decrypt with an exact key, partial key mask, or weak-parameter computation, or run automated cascade unwrapping across nested encodings and classical ciphers.
- **Bilingual Inside the App:** full English and Russian UI and text-analysis oracle.
- **100% Local Execution:** everything runs offline on your machine via the native Rust engine with zero telemetry or network uploads.

> **Honest Scope:** SAQTA cannot magically crack properly configured modern encryption (`AES-256`, `ChaCha20`, `GOST`, `RSA-2048+`) without a key. It is designed to identify formats/ciphers, uncover implementation weaknesses, recover classical ciphers and encodings, and protect files with modern cryptography.

---

## Distribution

This public repository distributes official compiled releases and updates for SAQTA only. Source code is proprietary and closed (`© 2026 moonshinelxv`, see [LICENSE](LICENSE)).
