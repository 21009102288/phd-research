# Codex Notes for This Obsidian Vault

Scope: this file applies to the entire vault rooted at this directory.

## Obsidian Markdown Rules

- Use Obsidian wikilinks for internal notes: `[[Note Name]]`.
- Always leave one blank line before Markdown tables.
- Use Obsidian-compatible math syntax only:
  - Inline math: `$...$`
  - Display math:

    ```markdown
    $$
    ...
    $$
    ```

- Do not use LaTeX delimiters `\(...\)` or `\[...\]`; Obsidian may render them inconsistently.

## Markdown to PDF Formula Rules

- Before exporting Markdown to PDF, verify that no `\(...\)` or `\[...\]` delimiters remain.
- Every display formula block must have paired `$$` delimiters.
- Do not leave bare LaTeX formula lines outside `$$...$$` blocks.
- For matrix or multi-line equations, keep the entire equation inside a single display block; do not split rows into separate math blocks.
- When using Pandoc/XeLaTeX, prefer a Unicode-capable font and avoid Unicode subscript characters in normal text if the PDF engine reports missing glyphs.
  - Prefer `O2Hb`, `HHb`, `SO2`, `R^2` in normal text.
  - Use LaTeX syntax inside math, e.g. `$O_2Hb$`, `$SO_2$`, `$R^2$`.
- After PDF export, render key pages to PNG and visually check important formulas.

## Recommended Formula Check

Run a quick check before considering formula work complete:

```powershell
python -c "from pathlib import Path; files=list(Path('.').rglob('*.md')); bad=[]; unpaired=[]; [bad.append(str(p)) for p in files if ('\\\\(' in p.read_text(encoding='utf-8', errors='ignore') or '\\\\[' in p.read_text(encoding='utf-8', errors='ignore'))]; [unpaired.append(str(p)) for p in files if p.read_text(encoding='utf-8', errors='ignore').count('$$') % 2]; print('bad_delimiters', bad); print('unpaired_display_math', unpaired)"
```

