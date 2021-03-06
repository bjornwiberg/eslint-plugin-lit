# Detects usages of legacy binding syntax (no-legacy-template-syntax)

Legacy lit-extended syntax is no longer supported so any uses of it
are likely to be mistakes.

## Rule Details

This rule disallows use of legacy lit-extended syntax in templates.

The following patterns are considered warnings:

```ts
html`<x-foo bar?=${x}>`;
html`<x-foo on-bar=${x}>`;
html`<x-foo bar$=${x}>`;
```

The following patterns are not warnings:

```ts
html`<x-foo ?bar=${x}>`;
html`<x-foo .bar=${x}>`;
html`<x-foo bar=${x}>`;
```

## When Not To Use It

If you use lit-extended syntax, then you will not need this rule.
