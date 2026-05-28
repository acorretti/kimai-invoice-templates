# Clean business invoice

A generic PDF invoice template with a quieter editorial style. It keeps the issuer visually anchored in the header and footer, places the recipient in the main address block, and avoids explicit "to", "from", and "contact" labels.

The template does not render `invoice['template.title']` or `invoice['customer.number']`.

## Customization

You can customize this template by overriding variables or blocks from another invoice template.

```twig
{% extends '@invoice/clean-business-invoice.pdf.twig' %}

{% set accentColor = '#111111' %}
{% set mutedColor = '#666666' %}
{% set logoUrl = 'https://example.com/logo.svg' %}
```

### Variables

#### `logoUrl`
Sets the header logo. Defaults to `config('theme.branding.logo')`.

#### `accentColor`
Sets the primary text and rule color.

#### `mutedColor`
Sets secondary text color.

#### `ruleColor`
Sets separator line color.

#### `softColor`
Sets the background color for the invoice metadata and notes.

#### `fontFamily`
Sets the body font family. Make sure custom fonts are available to mPDF.

#### `headingFontFamily`
Sets the heading font family used for the invoice number.

#### `showFoldHoleMarks`
Set to `true` to print fold and hole marks.
