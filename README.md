![The drag itself with nothing named: furrowed silt, a grapnel mid drag, and a broken cable lying ahead of the prongs](intro-banner.png)

# artex-executablemetadatascanner

![A repair ship at night: the lit stern and winch, the cable dropping to the grapnel, and the project name painted on the stern board](banner.png)

![A repair grapnel head on holding a caught cable, the heading plate](logo.png)

![A grapnel dragging across silt, pausing as a prong crosses the broken cable, shell fragments drifting in the near band](scene.svg)


# artex-ExecutableMetadataScanner

> Fray box: if a YARA rules file named with -r cannot be compiled, the report carries a yara_error field describing the compile failure and the run exits 1.

> Fray box: a rules file that does not exist also exits 1.
Scans executable files (PE, ELF, Mach-O) to extract metadata such as compiler information, timestamps, imported libraries, and embedded resources.  Uses `pefile` (for PE), `lief` (for ELF/Mach-O), and `yara-python` to identify suspicious characteristics based on YARA rules. Outputs a report highlighting potential red flags. If a YARA rules file named with `-r` cannot be compiled, the report carries a `yara_error` field describing the compile failure and the run exits 1, because the YARA part of the scan was not performed. A rules file that does not exist also exits 1. - Focused on Automated extraction of indicators of compromise (IOCs) and metadata from document and binary files. Focus on speed and accuracy, allowing quick triage of potentially malicious artifacts.

![Section divider](sep-light.svg)

## Install
`git clone https://github.com/ShadowStrikeHQ/artex-executablemetadatascanner`

![Section divider](sep-light.svg)

## Usage
`./artex-executablemetadatascanner [params]`

![Section divider](sep-heavy.svg)

## Parameters
- `-h`: Show help message and exit
- `-r`: Path to YARA rules file (optional)
- `-o`: Path to save the JSON report (optional)
- `-v`: Enable verbose logging

![Section divider](sep-light.svg)

## License
Copyright (c) ShadowStrikeHQ
