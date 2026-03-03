# Shopee Review Plugin for Claude Code

A Claude Code plugin that reviews draft Shopee Thailand product listings for Thai language naturalness, industry terminology accuracy, and SEO optimization.

## What it does

When you invoke `/shopee-review`, Claude reviews your draft product titles and descriptions across 3 axes:

1. **Thai Native Expression Check** - Detects unnatural phrasing, overly formal language, and machine-translation artifacts
2. **Industry Terminology Check** - Validates category-specific terms, brand names, and unit conventions
3. **SEO Optimization Check** - Evaluates keyword placement, title length, hashtag usage, and search algorithm alignment

## Installation

```bash
claude plugin install <github-user>/claude-shopee-review-plugin
```

Or install from a local directory:

```bash
claude plugin install --path /path/to/claude-shopee-review-plugin
```

## Usage

In Claude Code, invoke the skill:

```
/shopee-review
```

Then provide your draft product title and/or description in Thai. Claude will:

- Review the draft against all 3 axes
- Provide specific feedback with corrections and reasons (in Japanese)
- Output a finalized version in both Thai and Japanese

### Example

```
/shopee-review

Title draft:
[OKATSUNE] กรรไกรตัดกิ่ง รุ่น 103 คมกริบ ทนทาน ผลิตในญี่ปุ่น ของแท้ 100%

Description draft:
กรรไกรตัดกิ่งคุณภาพสูงจากแบรนด์ OKATSUNE ประเทศญี่ปุ่น...
```

## Supported Categories

- Gardening tools
- Hobbies & toys
- Beauty & cosmetics
- Electronics
- Food & supplements
- Fashion

## Output Format

The review provides structured feedback:

- Per-axis ratings with specific line-by-line corrections
- A/B pattern comparison (when multiple drafts are provided)
- Final polished version in Thai + Japanese translation

## License

MIT
