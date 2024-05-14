# Opus OMP DOI Plugin

## Introduction

The Opus OMP DOI Plugin provides an infrastructure for assigning unique DOI identifiers to monographs and chapters within the OMP platform. A DOI is a numeric identifier that allows for pointing to an electronic item (like a monograph or chapter) permanently, even if its URL changes. This facilitates the tracking, referencing, and citation of content items over time, irrespective of their location on the web.

Developer: Original plugin developed by the PKP OMP team. The modifications were carried out by the University Paris Cité Open Access team.

## Features

- Automatic or manual DOI assignment.
- Integration with DOI registration agencies such as Crossref.
- Support for setting up DOI prefixes and suffixes.
- Customization option for DOI suffixes:
  - **Monographs:** The suffix is generated using the publication's submission ID, transformed using a CRC32 hash.
  - **Chapters:** The suffix is generated using a combination of the monograph's submission ID and the chapter's ID, transformed using a CRC32b hash.
- Customization option for an obfuscated form of DOIs, added by the University Paris Cité Open Access.

## Installation

```bash
OMP=/path/to/OMP_INSTALLATION
cd $OMP/plugins/importexport
git clone https://github.com/PAYS-upcite/Opus-OMP-DOI-Plugin
```

## Configuration

1. Navigate to the plugin management interface in your OMP installation:
   `{OMP_SERVER}/index.php/{MY_PRESS}/management/importexport/plugin/DOIPlugin`
2. Ensure the plugin is enabled and configured as per your requirements.

## Usage

- The plugin allows registering DOIs for monographs and chapters via the OMP management interface.
- DOI Suffix Generation:
  - **Monographs:** The suffix is based on the submission ID of the publication, hashed with CRC32 to ensure uniqueness and consistency.
  - **Chapters:** The suffix combines the submission ID of the monograph and the chapter ID, hashed with CRC32b, providing a unique identifier for each chapter.

## Credits

### Main Developer

- PKP OMP team

### Contributors

- University Paris Cité Open Access team

## Licensing

The Opus OMP DOI Plugin is licensed under GPLv3.
