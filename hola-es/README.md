# Hola ES

A creative Spanish-only PDF invoice template inspired by bold studio invoices: a large "FACTURA" heading, a light gray work band, a prominent "GRACIAS", and simple contact/payment sections.

This template intentionally hard-codes Spanish editorial text. It lists work as description, hours, and cost, without showing the hourly rate.

It uses Kimai's structured issuer and customer fields when available, falls back to the invoice template address/contact fields, and sets the generated PDF filename and A4 portrait format via `pdfContext.setOption()`.

## Customization

```twig
{% extends '@invoice/hola-es.pdf.twig' %}

{% set panelColor = '#f8f8f8' %}
{% set inkColor = '#1f1f1f' %}
{% set logoUrl = 'https://example.com/logo.svg' %}
```

### Variables

#### `logoUrl`
Sets the header logo. Defaults to `config('theme.branding.logo')`.

#### `inkColor`
Sets the primary text color.

#### `mutedColor`
Sets secondary text color.

#### `panelColor`
Sets the main work-band background.

#### `paperColor`
Sets the page background.

#### `ruleColor`
Sets separator line color.

#### `accentColor`
Sets stronger separators inside the work band.

#### `fontFamily`
Sets the body font family.

#### `displayFontFamily`
Sets the large display heading font.

#### `logoOffsetTop`
Adjusts the logo vertical offset. Defaults to `0`.
