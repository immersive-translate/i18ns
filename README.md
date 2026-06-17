# Immersive Translate Localization Metadata

This repository maintains shared localization metadata for Immersive Translate.
It is read by AI-assisted localization workflows and reviewed by humans who
know specific languages, regions, or product terminology.

This repository is **not** the source of truth for released translation files.
Released strings live in each product repository. This repository stores the
context that helps humans and AI produce consistent, native-sounding product
copy.

## Metadata Contract

### Stores

- Product terminology and naming rules.
- Locale-specific style profiles.
- Preferred, discouraged, and ambiguous translations.
- Product wording rules for billing, quotas, errors, privacy, AI services, and
  other high-risk surfaces.
- Review schemas for AI and human localization suggestions.
- Good/bad examples that explain wording decisions.

### Does Not Store

- Bulk generated translation files.
- Complete released locale JSON files.
- Docusaurus build output or translated documentation mirrors.
- Unreviewed machine translation dumps.
- Product implementation details that belong in the extension, website, or
  service repositories.

### Product Usage Contract

Product repositories should use this README as shared localization context.
They should still:

1. Read product-specific source strings and UI context.
2. Apply relevant locale profiles and term policies from this repository.
3. Generate or review candidate translations in the product repository.
4. Run product-specific structure and quality checks.
5. Keep released translation files in the product repository.

This repository provides guidance and metadata. It does not replace
product-specific validation.

## For Weblate Contributors

We are moving away from using Weblate as the source of truth for released
translations. The old Weblate sync path is not the main contribution path
anymore.

This repository now accepts localization metadata: terminology, locale style
profiles, preferred wording, discouraged wording, and examples. These rules are
used by our AI-assisted i18n workflow when generating and reviewing product
translations.

If you want to help, contribute language knowledge instead of bulk translation
files:

- Tell us which term sounds better in your language.
- Explain regional wording differences.
- Add examples of awkward or preferred UI wording.
- Report translation issues with locale, current wording, suggested wording, and
  reason.

Released translation files are still maintained in each product repository. This
repository provides shared guidance for humans and AI reviewers.

## Contribution Rules

Contribute the language knowledge you are confident about. The most useful
changes are small, specific, and explain the reason behind the wording.

### Good Contributions

- Add or improve a locale profile for a language or region you know well.
- Suggest a better product term with examples.
- Mark wording as awkward, too literal, too long for UI, or misleading.
- Explain regional differences such as Taiwan vs. Hong Kong Traditional
  Chinese, European vs. Brazilian Portuguese, or formal vs. informal tone.
- Add good/bad example pairs so future AI reviews can learn the pattern.

### Avoid

- Submitting large batches of generated translations.
- Replacing product names or SKU names without explaining local market
  convention.
- Changing placeholder syntax such as `{count}`, `<1>...</1>`, Markdown links,
  HTML tags, or code-like text.
- Treating one locale's wording as automatically correct for another region.

## Canonical Workflow

Immersive Translate uses a native-localization-first workflow.

| Stage | Rule |
| --- | --- |
| Product intent | `zh-CN` expresses product intent and Chinese business context. |
| Structure bridge | `en` anchors placeholders, labels, tags, Markdown, HTML fragments, and cross-language semantic boundaries. |
| Target localization | Target languages should sound like native product UI, not word-for-word translations. |
| Rewrite freedom | Localized strings may reorder, shorten, or rewrite copy when product meaning stays the same. |
| External input | External suggestions are useful inputs, but they are not automatically merged into released translations. |
| Validation | AI output must pass structure checks, terminology checks, and high-risk human review when needed. |

## Term Policy

Use this table for product-wide terms. Add terms only when the rule has value
across more than one product surface.

| Term | Type | Default Policy | Allowed Local Variation | Notes |
| --- | --- | --- | --- | --- |
| `Immersive Translate` | Brand | Follow the product's established local operating name. Do not force English if a locale already has a reviewed local brand convention. | Yes | Keep consistency with existing reviewed product copy. |
| `OpenAI`, `Claude`, `Gemini`, `DeepL` | Third-party service names | Keep official service names in English unless the service has an official localized name used in that locale. | Limited | Applies to provider names, model setup, and service labels. |
| `API Key` | Technical term | Keep `API`; localize `Key` when that is natural. | Yes | Examples: `API-Schluessel`, `API キー`, `cle API`, `API 密钥`, `API 金鑰`. |
| `UserScript` | Channel / technical entry point | Keep in technical entry points, channel labels, and script titles. | Yes | May be localized in explanatory copy for general users. |
| `Pro`, `Max`, `PDF Pro`, `AI Pro Tokens` | SKU / entitlement | Treat as SKU or plan names when they name a product entitlement. | Limited | Localize surrounding explanations naturally. |
| `credits` / `tokens` | Quota / metering | Localize user entitlements as credits, points, quota, balance, or another local equivalent. | Yes | Keep token terminology for model/API metering when that is local convention. |

## Locale Profiles

Each locale profile should use this shape:

```md
### `locale-code`

- Tone:
- UI length:
- Preferred terms:
- Avoid:
- Product naming:
- Examples:
```

### `zh-TW`

- Tone: Natural Taiwan product UI, not mechanical
  Simplified-to-Traditional conversion.
- UI length: Prefer concise labels that still sound natural in Taiwan software
  products.
- Preferred terms: `擴充功能`, `選取文字翻譯`, `流量包`, `選單`.
- Avoid: Overly terse terms such as `倉庫` for general users when `GitHub 倉庫`
  or another clearer phrase is needed.
- Product naming: Follow existing reviewed Traditional Chinese operating copy
  for product, billing, and quota wording when available.
- Examples:
  - Prefer `選單` over `菜單` for Taiwan UI menu wording.

### `zh-HK`

- Tone: Hong Kong Traditional Chinese conventions when they differ from Taiwan
  wording.
- UI length: Concise product UI labels; do not inherit `zh-TW` wording by
  default.
- Preferred terms: Use English technical names when they are common in Hong
  Kong software UI.
- Avoid: Treating Taiwan Traditional Chinese as the automatic source for Hong
  Kong.
- Product naming: Keep product and technical names when English is the local
  convention.
- Examples:
  - If `zh-TW` and `zh-HK` differ, record the reason instead of silently
    copying one region to the other.

### `ja`

- Tone: Natural Japanese product UI, not English word order.
- UI length: Short UI labels may be concise and noun-like.
- Preferred terms: Use polite form for user-facing messages where appropriate.
- Avoid: Over-translating product names or service names without an established
  Japanese form.
- Product naming: Keep product and service names unless there is an official or
  reviewed Japanese convention.
- Examples:
  - Preserve placeholder and tag order constraints even when Japanese sentence
    order changes.

### `ko`

- Tone: Natural Korean SaaS/product UI tone.
- UI length: Prefer concise but polite user-facing strings.
- Preferred terms: Use polite forms for messages where appropriate.
- Avoid: Translating technical/product names that Korean software UI normally
  keeps in English or transliteration.
- Product naming: Keep product and service names when local convention supports
  that.
- Examples:
  - Distinguish explanatory copy from compact settings labels.

### `de`

- Tone: Clear, concise, and moderately formal.
- UI length: Avoid long compounds in cramped UI when a natural shorter label is
  available.
- Preferred terms: Follow German capitalization and compound-word conventions.
- Avoid: Legalistic phrasing unless the string is legal or billing copy.
- Product naming: Preserve names such as `Immersive Translate`, `UserScript`,
  `OpenAI`, and `DeepL` unless a reviewed local convention says otherwise.
- Examples:
  - Use formal product UI tone without making simple actions sound like legal
    notices.

### `fr`

- Tone: Natural French product copy rather than English syntax.
- UI length: Avoid overlong button labels.
- Preferred terms: Use formal `vous` unless a product surface explicitly
  chooses another tone.
- Avoid: Literal English word order.
- Product naming: Keep product and service names when they function as names.
- Examples:
  - Prefer idiomatic French product phrasing over source-text mirroring.

## Key Families

Identify a key family before choosing the translation strategy.

| Key Family | Risk | Review Focus |
| --- | --- | --- |
| `error.*` | User confusion, support burden | Accuracy, calm tone, actionable recovery. |
| `translationServices.*` | Provider setup mistakes | Provider names, model names, API terminology, setup instructions. |
| `rewardCenter.*` | Billing or entitlement misunderstanding | Billing, entitlement, quota, conversion wording. |
| `fileTranslate.*` | File state or limit misunderstanding | File limits, document states, failure messages. |
| `aiAssistant.*` | Overclaiming AI behavior or privacy risk | AI capability claims, mode names, privacy-sensitive wording. |

## AI Review Schema

AI review should judge the issue before proposing a rewrite. It should not
blindly translate the string again.

```json
{
  "key": "aiAssistant.topBar",
  "locale": "de",
  "category": "tone",
  "verdict": "revise",
  "issues": [
    "The current wording sounds translated rather than native product UI.",
    "The placeholder structure is correct."
  ],
  "suggested": "..."
}
```

### Fields

| Field | Required | Meaning |
| --- | --- | --- |
| `key` | Yes | Product i18n key or stable identifier. |
| `locale` | Yes | Target locale. |
| `category` | Yes | Main issue type, such as `tone`, `terminology`, `ui-length`, `structure`, `billing`, or `privacy`. |
| `verdict` | Yes | `keep`, `revise`, or `reject`. |
| `issues` | Yes | Short reasons behind the verdict. |
| `suggested` | For `revise` / `reject` | Complete replacement that preserves source structure. |

### Verdicts

- `keep`: no change needed.
- `revise`: current wording is usable but should be improved.
- `reject`: current wording is misleading, broken, or violates product rules.

## External Suggestion Schema

Community input, Weblate comments, and issue reports can be normalized into a
small sidecar object before they enter the AI workflow.

```json
{
  "source": "github-issue",
  "locale": "zh-TW",
  "key": "sidePanel.menu",
  "commentType": "preferred-term",
  "recommendation": "Use 選單 instead of 菜單 for Taiwan UI.",
  "reason": "選單 is the more natural Taiwan software UI term."
}
```

### Fields

| Field | Required | Meaning |
| --- | --- | --- |
| `source` | Yes | Origin of the suggestion, such as `github-issue`, `weblate-comment`, `support-ticket`, or `manual-review`. |
| `locale` | Yes | Target locale. |
| `key` | Optional | Product key when the suggestion is tied to a specific string. |
| `commentType` | Yes | Suggestion type, such as `preferred-term`, `avoid-term`, `tone`, `regional-usage`, or `structure-risk`. |
| `recommendation` | Yes | Proposed rule or wording guidance. |
| `reason` | Yes | Why this guidance should be followed. |

Do not copy private context, raw browser traces, or unrelated user metadata
into this repository.
