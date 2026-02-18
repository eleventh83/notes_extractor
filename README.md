:::writing{variant=“standard” id=“45321”}

PowerPoint Speaker Notes Extractor

A small CLI tool to extract speaker notes from a .pptx file and save them as a plain text file with page (slide) markers.

Features
	•	Extracts speaker notes from each slide
	•	Adds markers like ===== Page N =====
	•	Writes (no notes) when a slide has no notes
	•	Simple CLI: -i for input, -o for output (optional)

Dependency
	•	Python 3.9+ (recommended)
	•	python-pptx￼

Install:

pip install python-pptx

Usage

Basic (output defaults to <input_stem>_notes.txt next to the input file):

python notes_extractor.py -i input.pptx

Custom output path:

python notes_extractor.py -i input.pptx -o /path/to/output.txt

Output format (example)

===== Page 1 =====
...notes...

===== Page 2 =====
(no notes)

Notes
	•	Only .pptx is supported (not .ppt / .pptm).
	•	Output is UTF-8 encoded plain text.
:::
