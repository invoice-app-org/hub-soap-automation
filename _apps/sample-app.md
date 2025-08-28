---
title: Bilingual GST Invoicing
summary: Mobile + Web platform for Indic invoices, bilingual PDFs, batch GST filing, optional voice commands.
version: v2025.08.28
hero_svg: /assets/apps/sample-app/v2025.08.28/architecture.svg
assets:
  - {
      label: "SVG (source of truth)",
      url: "/assets/apps/sample-app/v2025.08.28/architecture.svg",
      note: "vector",
    }
  - {
      label: "PNG 2400w",
      url: "/assets/apps/sample-app/v2025.08.28/architecture@2400w.png",
      note: "high-DPI",
    }
  - {
      label: "SoaP PDF",
      url: "/assets/apps/sample-app/v2025.08.28/soap.pdf",
      note: "one-pager",
    }
history:
  - {
      version: "v2025.08.10",
      url: "/assets/apps/sample-app/v2025.08.10/architecture.svg",
      date: "2025-08-10",
    }
---

## Solution on a Page (SoaP)

- **Problem:** End-to-end invoicing (Indic+English) with GST batch filing.
- **Audience:** SMB retailers/wholesalers.
- **Architecture:** AWS (Cognito, APIGW, S3, SQS, RDS), Spring services, Node doc renderer.
- **Differentiators:** Bilingual fields, optional voice, HITL OCR for handwritten invoices (EN/HI/TE).

**Performance budgets:** LCP < 2s (mid-tier Android), p95 API < 300ms, render < 5s.
