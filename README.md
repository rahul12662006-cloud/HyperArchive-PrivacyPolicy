# Privacy Policy for HyperArchive

**Effective Date:** October 15, 2026  
**Last Updated:** October 15, 2026

HyperArchive ("we", "our", or "the App") is developed and maintained as a privacy-first, local-first file manager, archive extractor, cloud storage client, and peer-to-peer file bridge. We are strongly committed to respecting and protecting your privacy.

This Privacy Policy explains what information the App accesses, how it is handled, and why specific device permissions are required.

---

## 1. Zero Personal Data Collection Policy
- **No Analytics / No Tracking:** HyperArchive does not collect, track, profile, or sell your personal information, device identifiers, or browsing habits.
- **No Third-Party Advertising:** The App contains no advertising SDKs or third-party behavioral tracking libraries.
- **Local-First Architecture:** All file operations (compression, extraction, encryption, decryption, indexing, and viewing) happen locally on your device or directly between your device and your chosen storage endpoints.

---

## 2. Permissions and How They Are Used

HyperArchive requests only the permissions strictly required to perform core file management, archiving, and transfer tasks:

### A. All Files Access (`MANAGE_EXTERNAL_STORAGE`, `READ_EXTERNAL_STORAGE`, `WRITE_EXTERNAL_STORAGE`)
- **Purpose:** HyperArchive is a full-featured file manager and archive utility (7Z, ZIP, RAR, TAR, GZ, BZ2, XZ). Full file access is essential to browse files, extract archives to any chosen directory, compress documents/media, install user-selected APKs, and manage your storage.
- **Data Handling:** File data never leaves your device unless you explicitly initiate an upload to your own cloud account or transfer files via HyperBridge.

### B. Camera (`CAMERA`)
- **Purpose:** Used exclusively to scan QR codes for pairing devices over HyperBridge (local Wi-Fi transfer).
- **Data Handling:** No photos, video recordings, or facial data are ever saved, stored, or transmitted. The camera stream is processed strictly in-memory solely for barcode recognition.

### C. Local Network & Wi-Fi (`INTERNET`, `ACCESS_NETWORK_STATE`, `ACCESS_WIFI_STATE`, `CHANGE_WIFI_MULTICAST_STATE`)
- **Purpose:** 
  1. **HyperBridge:** Facilitates direct peer-to-peer file transfer between devices connected to the same local Wi-Fi or hotspot network.
  2. **Network Storage:** Connects to local SMB (Windows Share/NAS), SFTP, or WebDAV servers per your explicit configuration.
  3. **Cloud Storage (Google Drive):** Authenticates and syncs files directly with your authorized cloud account using official OAuth 2.0 PKCE protocols.
- **Data Handling:** Data is only transmitted to endpoints you explicitly configure. No intermediary proxy server intercepts your traffic.

### D. Biometrics (`USE_BIOMETRIC`, `USE_FINGERPRINT`)
- **Purpose:** Optional app lock feature to protect access to HyperArchive and your sensitive files using your device's fingerprint or face unlock.
- **Data Handling:** Biometric authentication is handled entirely by the Android operating system. The App never accesses or stores your raw biometric data.

### E. Foreground Service & Notifications (`FOREGROUND_SERVICE`, `FOREGROUND_SERVICE_DATA_SYNC`, `POST_NOTIFICATIONS`)
- **Purpose:** Keeps long-running compression, extraction, or network file transfers active when the app is minimized, preventing Android from killing the operation, and displays real-time progress notifications.

### F. Install Unknown Apps (`REQUEST_INSTALL_PACKAGES`)
- **Purpose:** Allows users to open and install `.apk` and package files directly from the archive viewer or file explorer when initiated by the user.

---

## 3. Cloud Storage & Third-Party Services
When you connect third-party cloud storage (such as Google Drive):
- Authentication uses secure OAuth 2.0 PKCE.
- Access tokens and credentials are encrypted on your device using AES-256 encryption.
- The App only accesses the files and folders you navigate to or select.
- HyperArchive does not operate any backend server; all requests communicate directly between your device and Google's official API servers.
- The App complies with Google API Services User Data Policy, including the Limited Use requirements.

---

## 4. Data Security
- Encrypted vaults on device protect cloud tokens and sensitive preferences using standard cryptographic primitives.
- Password-protected archives (ZIP, 7z) are encrypted and decrypted locally using standard AES-256 or ZipCrypto algorithms without transmitting passwords over the internet.

---

## 5. Children's Privacy
HyperArchive does not knowingly collect or solicit any personal information from children under the age of 13.

---

## 6. Changes to This Privacy Policy
We may update this Privacy Policy from time to time. Any updates will be reflected in the app release notes and this document.

---

## 7. Contact Us
If you have any questions or concerns regarding this Privacy Policy or HyperArchive, please contact:
- **Developer:** Rahul
- **Email:** support@hyperarchive.app (or contact via your GitHub repository)
- **GitHub:** https://github.com/rahul/HyperArchive
