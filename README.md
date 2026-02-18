# PowerPoint Speaker Notes Extractor

A tiny CLI tool that extracts **speaker notes** from a `.pptx` file and saves them as a **plain text** `.txt` file with **page (slide) markers**.

## Features
- Extracts speaker notes per slide
- Adds markers like `===== Page N =====`
- Writes `(no notes)` when a slide has no notes
- Simple CLI: `-i` for input, `-o` for output (optional)

## Requirements
- Python 3.9+ (recommended)
- `python-pptx`

## Install
```bash
pip install python-pptx
```

## Usage

Default output: `<input_stem>_notes.txt` next to the input file.
```bash
python notes_extractor.py -i input.pptx
```

Custom output path:
```bash
python notes_extractor.py -i input.pptx -o /path/to/output.txt
```

## Output Format (Example)
```text
===== Page 1 =====
...notes...

===== Page 2 =====
(no notes)
```

## Notes
- Only `.pptx` is supported (not `.ppt` / `.pptm`).
- Output is UTF-8 encoded.
