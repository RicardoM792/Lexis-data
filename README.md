# LEXIS PRO — Data Files

These JSON files power the **LEXIS PRO** English learning app (A1 → C2).

## 📁 Files

| File | Content | Level |
|------|---------|-------|
| `colors.json` | 20 colors with Spanish, hex codes, IPA, examples | A1 |
| `numbers.json` | Cardinal (0–1M) + ordinal numbers | A1 |
| `pronouns.json` | Subject, object, possessive, reflexive, demonstrative, interrogative | A1 |
| `seasons_time.json` | 4 seasons, 12 months, 7 days, 22 time expressions | A1 |
| `adjectives.json` | 50+ adjectives in groups: size, appearance, feelings, quality, advanced | A1–B2 |
| `nouns.json` | Family, body parts, food, places, abstract nouns | A1–B1 |
| `verbs.json` | 44 essential verbs with conjugations, patterns, Spanish | A1–C1 |
| `grammar.json` | 19 grammar rules with affirmative/negative/question forms | A1–C2 |
| `vocabulary_a1_a2.json` | 100+ core words for beginners with full Spanish translation | A1–A2 |

## 🚀 How to upload to GitHub

1. Create a new **public** repository (e.g., `lexis-data`)
2. Upload all `.json` files to the repository root
3. For each file, get the **Raw URL**:
   - Click the file in GitHub
   - Click the **Raw** button
   - Copy the URL (format: `https://raw.githubusercontent.com/YOUR_USERNAME/lexis-data/main/filename.json`)
4. Open `lexis.html` and update the `GITHUB_BASE_URL` variable:
   ```javascript
   const GITHUB_BASE_URL = 'https://raw.githubusercontent.com/YOUR_USERNAME/lexis-data/main/';
   ```

## 🔗 Oxford Word Lists (external, already public)

The app also loads Oxford 3000 & 5000 from:
- `https://raw.githubusercontent.com/ittuann/The-Oxford-5000-Word-Lists/main/The%20Oxford%203000.txt`
- `https://raw.githubusercontent.com/ittuann/The-Oxford-5000-Word-Lists/main/The%20Oxford%205000.txt`

## 📖 Classic Books (Project Gutenberg)

Books are loaded on-demand from `gutenberg.org` via CORS proxy when the user clicks "Extract vocabulary".

## ✅ Features powered by these files

- **Colors quiz**: match color → Spanish/hex
- **Numbers quiz**: cardinal & ordinal
- **Pronouns**: grouped by type with grammar notes
- **Seasons/Time**: months, days, expressions
- **Adjectives**: with opposites and categories
- **Smart quizzes**: multiple choice, fill-in-blank, negative forms
- **Spanish toggle**: all words have `es` field for translation
- **Offline cache**: all loaded data saved in `localStorage`
