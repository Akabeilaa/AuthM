# ProVerif Verification Project

This repository contains ProVerif models and queries for analyzing the **AuthM protocol**, including both **authentication** and **registration** phases under different adversarial settings.

---

## 📁 Project Structure

AuthMVerif/
├── AuthM.pvl
├── Auth/
│ ├── ideal.pv
| └── auth_A3_A4.pv
│ ├── mal_onechannel/
│ ├── mal_twochannel/
│ ├── mal_threechannel/
│ └── mal_fourchannel/
│
└── Register/
├── ideal.pv
├── mal_onechannel/
├── mal_twochannel/
├── mal_threechannel/
└── mal_fourchannel/


---

## 📌 Description

- **AuthM.pvl**  
  Shared library file containing cryptographic primitives and common definitions.

- **Auth/**  
  Models and queries for the **authentication phase**.

- **Register/**  
  Models and queries for the **registration phase**.

- **ideal.pv**  
  Represents the protocol execution without attacker.

- **auth_A3_A4.pv**  
  Verify A3 and A4 objectives.

- **mal_*channel/**  
  Adversarial models where the attacker compromises different numbers of communication channels (from one to four).

---

## ⚙️ Usage

Run all commands from the `0309grap` directory.

### 🚀 Example Commands

```bash
# Authentication (ideal)
proverif -lib AuthM.pvl ./Auth/ideal.pv

# Authentication (one-channel attack)
proverif -lib AuthM.pvl ./Auth/mal_onechannel/xxx.pv

# Registration (ideal)
proverif -lib AuthM.pvl ./Register/ideal.pv

# Registration (two-channel attack)
proverif -lib AuthM.pvl ./Register/mal_twochannel/xxx.pv
```
