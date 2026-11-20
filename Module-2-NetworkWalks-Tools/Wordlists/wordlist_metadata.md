# Wordlist Analysis & Metadata

## Overview
Password auditing tools rely on structured dictionaries to model real-world user password selection behaviors. During Week 3 practical exercises, dictionary attacks were evaluated using standard wordlists to demonstrate how predictable human patterns undermine authentication systems.

---

## Wordlist Characteristics

| Parameter | Specification |
|---|---|
| **Primary Wordlist** | `JTR_default_password.txt` (Standardized Security Dictionary) |
| **Total Candidate Entries** | 3,556 unique credential entries |
| **Origin & Methodology** | Compiled based on real-world breach telemetry, historical Unix account defaults, and high-frequency community credential dumps |
| **Target Coverage** | Common base phrases, repeated numeric sequences, default vendor passwords, and keyboard geometry walks |

---

## Defensive Implications
* **Low Computational Barrier:** A dictionary containing 3,556 entries can be fully traversed in under 4 minutes even in a single-threaded web browser (~16 pw/s), and in milliseconds within native multi-threaded C tools like John the Ripper.
* **Necessity of Long-Tail Passwords:** Passphrases exceeding 16 characters or generated randomly completely negate standard wordlist and hybrid rule-based attacks.
