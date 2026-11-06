---
applyTo: "data/**,scripts/**"
---

- Never edit `data/` by hand. Change `scripts/generate-data.ts` and run `npm run generate:data` instead.
- Keep all data synthetic, with no BSN, IBAN, email address, phone number or street address.
- Pin each new edge case in the generator and its test.
