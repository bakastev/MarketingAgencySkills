# Schema snippets (baseline templates)

Adjust values to the page; keep visible content and schema aligned.

## 1) Article + Author + Organization

```json
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "Page headline",
  "description": "Concise page summary",
  "author": {
    "@type": "Person",
    "name": "Author Name"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Organization Name",
    "url": "https://example.com"
  },
  "mainEntityOfPage": "https://example.com/page",
  "datePublished": "2026-01-26",
  "dateModified": "2026-02-17"
}
```

## 2) FAQPage (only when visible Q&A exists)

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Question text",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Direct answer text"
      }
    }
  ]
}
```

## 3) Organization Entity Block

```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "Organization Name",
  "url": "https://example.com",
  "sameAs": [
    "https://www.linkedin.com/company/example",
    "https://www.wikidata.org/wiki/Q12345"
  ]
}
```

## Validation Steps

1. Validate JSON syntax.
2. Validate schema type relevance to page intent.
3. Confirm all key values are visible in rendered page content.
4. Re-check after any copy edits.

