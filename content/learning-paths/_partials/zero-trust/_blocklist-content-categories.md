---
_build:
  publishResources: false
  render: never
  list: never
inputParameters: blocklistPolicyType;;blockedContentCategories
---

Entries in the [security risk content subcategory](/cloudflare-one/policies/gateway/domain-categories/#security-risk-subcategories), such as **New Domains**, do not always pose a security threat. We recommend you first create an Allow policy to track policy matching and identify any false positives. You can add false positives to your **Trusted Domains** list used in **All-$1-Domain-Allowlist**.

After your test is complete, we recommend you change the action to Block to minimize risk to your organization.

| Selector           | Operator | Value | Action |
| ------------------ | -------- | ----- | ------ |
| Content Categories | in       | $2    | Allow  |