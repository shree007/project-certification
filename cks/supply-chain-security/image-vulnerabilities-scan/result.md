
python:3.4-alpine (alpine 3.9.2)
================================
Total: 13 (HIGH: 13)

┌──────────────┬────────────────┬──────────┬────────┬───────────────────┬───────────────┬──────────────────────────────────────────────────────────────┐
│   Library    │ Vulnerability  │ Severity │ Status │ Installed Version │ Fixed Version │                            Title                             │
├──────────────┼────────────────┼──────────┼────────┼───────────────────┼───────────────┼──────────────────────────────────────────────────────────────┤
│ expat        │ CVE-2018-20843 │ HIGH     │ fixed  │ 2.2.6-r0          │ 2.2.7-r0      │ expat: large number of colons in input makes parser consume  │
│              │                │          │        │                   │               │ high amount...                                               │
│              │                │          │        │                   │               │ https://avd.aquasec.com/nvd/cve-2018-20843                   │
│              ├────────────────┤          │        │                   ├───────────────┼──────────────────────────────────────────────────────────────┤
│              │ CVE-2019-15903 │          │        │                   │ 2.2.7-r1      │ expat: heap-based buffer over-read via crafted XML input     │
│              │                │          │        │                   │               │ https://avd.aquasec.com/nvd/cve-2019-15903                   │
├──────────────┼────────────────┤          │        ├───────────────────┼───────────────┼──────────────────────────────────────────────────────────────┤
│ libcrypto1.1 │ CVE-2019-1543  │          │        │ 1.1.1a-r1         │ 1.1.1b-r1     │ openssl: ChaCha20-Poly1305 with long nonces                  │
│              │                │          │        │                   │               │ https://avd.aquasec.com/nvd/cve-2019-1543                    │
│              ├────────────────┤          │        │                   ├───────────────┼──────────────────────────────────────────────────────────────┤
│              │ CVE-2020-1967  │          │        │                   │ 1.1.1g-r0     │ openssl: Segmentation fault in SSL_check_chain causes denial │
│              │                │          │        │                   │               │ of service                                                   │
│              │                │          │        │                   │               │ https://avd.aquasec.com/nvd/cve-2020-1967                    │
│              ├────────────────┤          │        │                   ├───────────────┼──────────────────────────────────────────────────────────────┤
│              │ CVE-2021-23840 │          │        │                   │ 1.1.1j-r0     │ openssl: integer overflow in CipherUpdate                    │
│              │                │          │        │                   │               │ https://avd.aquasec.com/nvd/cve-2021-23840                   │
│              ├────────────────┤          │        │                   ├───────────────┼──────────────────────────────────────────────────────────────┤
│              │ CVE-2021-3450  │          │        │                   │ 1.1.1k-r0     │ openssl: CA certificate check bypass with                    │
│              │                │          │        │                   │               │ X509_V_FLAG_X509_STRICT                                      │
│              │                │          │        │                   │               │ https://avd.aquasec.com/nvd/cve-2021-3450                    │
├──────────────┼────────────────┤          │        │                   ├───────────────┼──────────────────────────────────────────────────────────────┤
│ libssl1.1    │ CVE-2019-1543  │          │        │                   │ 1.1.1b-r1     │ openssl: ChaCha20-Poly1305 with long nonces                  │
│              │                │          │        │                   │               │ https://avd.aquasec.com/nvd/cve-2019-1543                    │
│              ├────────────────┤          │        │                   ├───────────────┼──────────────────────────────────────────────────────────────┤
│              │ CVE-2020-1967  │          │        │                   │ 1.1.1g-r0     │ openssl: Segmentation fault in SSL_check_chain causes denial │
│              │                │          │        │                   │               │ of service                                                   │
│              │                │          │        │                   │               │ https://avd.aquasec.com/nvd/cve-2020-1967                    │
│              ├────────────────┤          │        │                   ├───────────────┼──────────────────────────────────────────────────────────────┤
│              │ CVE-2021-23840 │          │        │                   │ 1.1.1j-r0     │ openssl: integer overflow in CipherUpdate                    │
│              │                │          │        │                   │               │ https://avd.aquasec.com/nvd/cve-2021-23840                   │
│              ├────────────────┤          │        │                   ├───────────────┼──────────────────────────────────────────────────────────────┤
│              │ CVE-2021-3450  │          │        │                   │ 1.1.1k-r0     │ openssl: CA certificate check bypass with                    │
│              │                │          │        │                   │               │ X509_V_FLAG_X509_STRICT                                      │
│              │                │          │        │                   │               │ https://avd.aquasec.com/nvd/cve-2021-3450                    │
├──────────────┼────────────────┤          │        ├───────────────────┼───────────────┼──────────────────────────────────────────────────────────────┤
│ sqlite-libs  │ CVE-2019-19244 │          │        │ 3.26.0-r3         │ 3.28.0-r2     │ sqlite: allows a crash if a sub-select uses both DISTINCT    │
│              │                │          │        │                   │               │ and window...                                                │
│              │                │          │        │                   │               │ https://avd.aquasec.com/nvd/cve-2019-19244                   │
│              ├────────────────┤          │        │                   ├───────────────┼──────────────────────────────────────────────────────────────┤
│              │ CVE-2019-5018  │          │        │                   │ 3.28.0-r0     │ sqlite: Use-after-free in window function leading to remote  │
│              │                │          │        │                   │               │ code execution                                               │
│              │                │          │        │                   │               │ https://avd.aquasec.com/nvd/cve-2019-5018                    │
│              ├────────────────┤          │        │                   ├───────────────┼──────────────────────────────────────────────────────────────┤
│              │ CVE-2020-11655 │          │        │                   │ 3.28.0-r3     │ sqlite: malformed window-function query leads to DoS         │
│              │                │          │        │                   │               │ https://avd.aquasec.com/nvd/cve-2020-11655                   │
└──────────────┴────────────────┴──────────┴────────┴───────────────────┴───────────────┴──────────────────────────────────────────────────────────────┘

Python (python-pkg)
===================
Total: 5 (HIGH: 5)

┌───────────────────────┬────────────────┬──────────┬────────┬───────────────────┬───────────────┬─────────────────────────────────────────────────────────────┐
│        Library        │ Vulnerability  │ Severity │ Status │ Installed Version │ Fixed Version │                            Title                            │
├───────────────────────┼────────────────┼──────────┼────────┼───────────────────┼───────────────┼─────────────────────────────────────────────────────────────┤
│ pip (METADATA)        │ CVE-2019-20916 │ HIGH     │ fixed  │ 19.0.3            │ 19.2          │ python-pip: directory traversal in _download_http_url()     │
│                       │                │          │        │                   │               │ function in src/pip/_internal/download.py                   │
│                       │                │          │        │                   │               │ https://avd.aquasec.com/nvd/cve-2019-20916                  │
│                       ├────────────────┤          │        │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2021-3572  │          │        │                   │ 21.1          │ python-pip: Incorrect handling of unicode separators in git │
│                       │                │          │        │                   │               │ references                                                  │
│                       │                │          │        │                   │               │ https://avd.aquasec.com/nvd/cve-2021-3572                   │
├───────────────────────┼────────────────┤          │        ├───────────────────┼───────────────┼─────────────────────────────────────────────────────────────┤
│ setuptools (METADATA) │ CVE-2022-40897 │          │        │ 40.8.0            │ 65.5.1        │ pypa-setuptools: Regular Expression Denial of Service       │
│                       │                │          │        │                   │               │ (ReDoS) in package_index.py                                 │
│                       │                │          │        │                   │               │ https://avd.aquasec.com/nvd/cve-2022-40897                  │
│                       ├────────────────┤          │        │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2024-6345  │          │        │                   │ 70.0.0        │ pypa/setuptools: Remote code execution via download         │
│                       │                │          │        │                   │               │ functions in the package_index module in...                 │
│                       │                │          │        │                   │               │ https://avd.aquasec.com/nvd/cve-2024-6345                   │
├───────────────────────┼────────────────┤          │        ├───────────────────┼───────────────┼─────────────────────────────────────────────────────────────┤
│ wheel (METADATA)      │ CVE-2022-40898 │          │        │ 0.33.1            │ 0.38.1        │ python-wheel: remote attackers can cause denial of service  │
│                       │                │          │        │                   │               │ via attacker controlled input...                            │
│                       │                │          │        │                   │               │ https://avd.aquasec.com/nvd/cve-2022-40898                  │
└───────────────────────┴────────────────┴──────────┴────────┴───────────────────┴───────────────┴─────────────────────────────────────────────────────────────┘
