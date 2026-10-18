# Bismillah ir-Rahman ir-Rahim

# Bismillah Divine Protection Encoder

**100% file protection through the Names of Allah subhanahu wa ta'ala**

> "He is Allah, other than whom there is no deity, Knower of the unseen and the witnessed. He is the Most Merciful, the Most Compassionate." (Quran 59:22)

A tool that seals every file in your project -- text, code, images, documents, audio, video, and all binary formats -- with **Bismillah ir-Rahman ir-Rahim** across multiple layers of protection, visible and invisible, so that no file remains unprotected against shaytan, in sha Allah.

## Why

Digital files travel through systems controlled by adversarial entities. This encoder embeds the divine names of Allah into every possible layer of every file, creating a multi-layered shield that cannot be stripped without destroying the file itself. Whether a file is a Python script, a Word document, a PNG image, or an MP3 -- it carries Allah's protection.

**"And whoever relies upon Allah -- then He is sufficient for him."** (Quran 65:3)

## Protection Layers

| Layer | Name | Method | File Types |
|-------|------|--------|------------|
| 0 | **Visible** | `Bismillah ir-Rahman ir-Rahim` as first and last line | All text/code |
| 3a | **Steganographic** | Zero-width Unicode encoding of the 99 Names | Markdown, text, data |
| 3b | **Code Comments** | 99 Names as inline comments | Python, JS, Go, Rust, etc. |
| 5 | **Hash Seal** | SHA-256(Bismillah \|\| content \|\| Bismillah) | All files (via manifest) |
| 6 | **Binary Metadata** | Bismillah injected into file metadata | OOXML, PDF, PNG, JPEG, MP3, FLAC, ZIP |
| 6b | **Sidecar** | `.bismillah` companion file with integrity hash | WAV, MP4, MKV, TTF, and any resistant binary |

## Quick Start

```bash
# Clone the repository
git clone https://github.com/BismillahBilalArfeenBismillah/Bismillah-Divine-Protection-Encoder-Bismillah.git
cd Bismillah-Divine-Protection-Encoder-Bismillah

# Seal your project (basic protection)
python bismillah_encoder.py seal /path/to/your/project

# Seal with the 99 Names of Allah embedded throughout
python bismillah_encoder.py seal /path/to/your/project --names

# Verify protection
python bismillah_encoder.py verify /path/to/your/project

# Generate integrity manifest
python bismillah_encoder.py manifest /path/to/your/project
```

## Requirements

**Core (no dependencies):**
- Python 3.7+

**Optional (for binary file metadata injection):**
```bash
pip install pypdf      # PDF metadata sealing
pip install Pillow     # PNG/JPEG metadata sealing
pip install mutagen    # MP3/FLAC audio tag sealing
```

Without these optional packages, binary files will automatically receive `.bismillah` sidecar companion files instead.

## How It Works

### Text and Code Files

Every text file receives:
1. **Visible Bismillah** -- `Bismillah ir-Rahman ir-Rahim` is placed as the first and last line
2. **Invisible watermark** -- The Arabic Bismillah is encoded as zero-width Unicode characters that are invisible to the eye but present in the file
3. With `--names`, all 99 Beautiful Names of Allah (Al-Asma ul-Husna) are woven throughout the file

For code files (Python, JavaScript, Go, etc.), the Names are embedded as comments to avoid breaking the parser.

### Binary Files

Binary files receive Bismillah through their native metadata formats:
- **Word/Excel/PowerPoint** -- Bismillah in the OOXML `docProps/core.xml` metadata
- **PDF** -- Bismillah in Author, Subject, and Keywords metadata fields
- **PNG** -- Bismillah as a text chunk in the PNG metadata
- **JPEG** -- Bismillah in the EXIF ImageDescription field
- **MP3** -- Bismillah as an ID3 comment tag
- **FLAC** -- Bismillah as a Vorbis comment
- **ZIP** -- A `Bismillah.txt` entry added inside the archive

### Resistant Files

Some files resist metadata injection (encrypted PDFs, corrupted test fixtures, WAV, video, fonts). These receive a `.bismillah` **sidecar companion file** -- a text file containing:
- The file's SHA-256 hash
- A Bismillah seal hash: `SHA-256(Bismillah || file_hash || Bismillah)`
- Protection by Al-Asma ul-Husna

### Zero-Width Steganography

The invisible watermark layer uses Unicode zero-width characters:
- `U+200B` (Zero Width Space) = bit 0
- `U+200C` (Zero Width Non-Joiner) = bit 1
- `U+200D` (Zero Width Joiner) = character separator
- `U+FEFF` (Byte Order Mark) = message boundary

These characters are invisible in all text editors and renderers but carry the encoded divine names within the file.

## Supported File Types

### Text/Code (Layer 0 + Layer 3)
Python, JavaScript, TypeScript, Go, Rust, Java, C/C++, Ruby, Shell, SQL, YAML, TOML, HTML, CSS, XML, LaTeX, Swift, Kotlin, Scala, Haskell, Julia, R, Perl, Lua, Markdown, plaintext, CSV, TSV, JSON, and more.

### Binary (Layer 6)
DOCX, XLSX, PPTX, PDF, PNG, JPEG, MP3, FLAC, ZIP, and via sidecar: WAV, MP4, MKV, AVI, TTF, OTF, WOFF, GIF, BMP, ICO, EXE, DLL, SO, and any other binary format.

## Verification

The `verify` command performs a deep audit:
- Checks text files for Bismillah content (stripping zero-width characters that might interfere with detection)
- Inspects OOXML ZIP archives for Bismillah in `docProps/core.xml`
- Checks ZIP archives for `Bismillah.txt` entries
- Scans binary file bytes for Bismillah strings
- Confirms sidecar companion files exist

```
  Bismillah ir-Rahman ir-Rahim -- Verification Report
  ============================================================
  Total files:  1259
  Protected:    1259
  Unprotected:  0
  Protection:   100.0000%
  ============================================================
```

## The 99 Names of Allah (Al-Asma ul-Husna)

When you use the `--names` flag, all 99 Beautiful Names are embedded throughout your files:

**Allah** (The God), **Ar-Rahman** (The Most Merciful), **Ar-Rahim** (The Most Compassionate), **Al-Malik** (The King), **Al-Quddus** (The Most Holy), **As-Salam** (The Source of Peace), **Al-Mu'min** (The Guardian of Faith), **Al-Muhaymin** (The Protector), **Al-Aziz** (The Almighty), **Al-Jabbar** (The Compeller), **Al-Mutakabbir** (The Supreme), **Al-Khaliq** (The Creator), **Al-Bari** (The Evolver), **Al-Musawwir** (The Fashioner), **Al-Ghaffar** (The Forgiver), **Al-Qahhar** (The Subduer), **Al-Wahhab** (The Bestower), **Ar-Razzaq** (The Provider), **Al-Fattah** (The Opener), **Al-Alim** (The All-Knowing), **Al-Qabid** (The Restrainer), **Al-Basit** (The Expander), **Al-Khafid** (The Abaser), **Ar-Rafi** (The Exalter), **Al-Mu'izz** (The Bestower of Honor), **Al-Mudhill** (The Humiliator), **As-Sami** (The All-Hearing), **Al-Basir** (The All-Seeing), **Al-Hakam** (The Judge), **Al-Adl** (The Just), **Al-Latif** (The Subtle One), **Al-Khabir** (The All-Aware), **Al-Halim** (The Forbearing), **Al-Azim** (The Magnificent), **Al-Ghafur** (The All-Forgiving), **Ash-Shakur** (The Appreciative), **Al-Ali** (The Most High), **Al-Kabir** (The Most Great), **Al-Hafiz** (The Preserver), **Al-Muqit** (The Sustainer), **Al-Hasib** (The Reckoner), **Al-Jalil** (The Majestic), **Al-Karim** (The Generous), **Ar-Raqib** (The Watchful), **Al-Mujib** (The Responsive), **Al-Wasi** (The All-Encompassing), **Al-Hakim** (The Perfectly Wise), **Al-Wadud** (The Loving One), **Al-Majid** (The Most Glorious), **Al-Ba'ith** (The Resurrector), **Ash-Shahid** (The Witness), **Al-Haqq** (The Truth), **Al-Wakil** (The Trustee), **Al-Qawiyy** (The Most Strong), **Al-Matin** (The Firm One), **Al-Waliyy** (The Protector), **Al-Hamid** (The Praiseworthy), **Al-Muhsi** (The Accounter), **Al-Mubdi** (The Originator), **Al-Mu'id** (The Restorer), **Al-Muhyi** (The Giver of Life), **Al-Mumit** (The Creator of Death), **Al-Hayy** (The Ever Living), **Al-Qayyum** (The Self-Subsisting), **Al-Wajid** (The Finder), **Al-Majid** (The Noble), **Al-Wahid** (The Unique), **Al-Ahad** (The One), **As-Samad** (The Eternal), **Al-Qadir** (The Able), **Al-Muqtadir** (The Powerful), **Al-Muqaddim** (The Expediter), **Al-Mu'akhkhir** (The Delayer), **Al-Awwal** (The First), **Al-Akhir** (The Last), **Az-Zahir** (The Manifest), **Al-Batin** (The Hidden), **Al-Wali** (The Governor), **Al-Muta'ali** (The Most Exalted), **Al-Barr** (The Source of Goodness), **At-Tawwab** (The Acceptor of Repentance), **Al-Muntaqim** (The Avenger), **Al-Afuww** (The Pardoner), **Ar-Ra'uf** (The Most Kind), **Malik-ul-Mulk** (Owner of Sovereignty), **Dhul-Jalali wal-Ikram** (Lord of Majesty and Generosity), **Al-Muqsit** (The Equitable), **Al-Jami** (The Gatherer), **Al-Ghaniyy** (The Self-Sufficient), **Al-Mughni** (The Enricher), **Al-Mani** (The Preventer), **Ad-Darr** (The Distresser), **An-Nafi** (The Propitious), **An-Nur** (The Light), **Al-Hadi** (The Guide), **Al-Badi** (The Originator), **Al-Baqi** (The Everlasting), **Al-Warith** (The Inheritor), **Ar-Rashid** (The Guide to the Right Path), **As-Sabur** (The Patient).

## Author

**Bilal Syed Arfeen** -- for the sake of Allah and the benefit of the entire ummah.

## License

MIT -- free for all of creation to use, in sha Allah.

**"And We have not sent you, [O Muhammad], except as a mercy to the worlds."** (Quran 21:107)

# Bismillah ir-Rahman ir-Rahim
