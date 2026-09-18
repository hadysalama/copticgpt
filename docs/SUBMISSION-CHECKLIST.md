# CopticGPT — OpenAI Plugin Submission Checklist

Portal: **https://platform.openai.com/plugins** → create a **Skills only** submission.

## Bundle (ready to upload)

- [x] Plugin bundle: `.codex-plugin/plugin.json` + `skills/copticgpt/` + `skills/coptic-agent/`
- [x] All reference documents converted to plain text (`.txt`) in `references/` — every entry verified extractable and readable (the old PDFs were removed; the bundle dropped from 38MB to ~5MB)
- [x] `CopticGPT Master System Instructions.docx` preserved (SKILL.md explicitly overrides its identity-concealment instructions)
- [x] Logo + composer icon: `assets/coptic-cross.png` (1024×1024 PNG, square)
- [x] Listing metadata in `plugin.json`: name, displayName, short/long descriptions, category, capabilities, 3 starter prompts (`defaultPrompt`)
- [x] Author fields updated: `"Hady Sameh Adib Salama"` (was `"Local developer"`)
- [ ] `psalmody.txt` — the old Psalmody PDF was mostly scanned images with no readable text, so the Psalmody is being pulled fresh from CopticReader.org's open liturgical texts; it will be added to the bundle and the ZIP rebuilt when it lands

## Portal form fields (drafted for you)

- [x] Starter prompts — in `plugin.json` `defaultPrompt` (3 included; portal accepts these)
- [x] 5 positive + 3 negative test cases — see `TEST-CASES.md` (paste into the portal)
- [x] Privacy policy text — see `PRIVACY.md`
- [x] Terms of service text — see `TERMS.md`
- [ ] **Host PRIVACY.md and TERMS.md** somewhere public (e.g., a GitHub repo) and paste the URLs into the portal's Privacy Policy URL / Terms URL fields. The portal requires URLs, not files.
- [ ] **Support URL** — add a support link (e.g., a GitHub Issues page or an email page) to the portal form.

## Only you can do these

1. **Verified publisher identity** — the portal requires a verified developer or business identity on your OpenAI organization.
2. **Apps Management write access** — the submitting organization needs this permission.
3. **Upload the bundle** — upload `copticgpt-plugin-submission.zip` (in this folder) as a Skills-only submission.
4. **Paste the metadata** — listing info, starter prompts, test cases, privacy/terms/support URLs.
5. **Submit for review, then hit Publish** — public listing begins only after OpenAI's review *and* your separate Publish action.

## Suggested before upload

- Consider changing `category` from `"Productivity"` to `"Education"` in `plugin.json` if the portal offers it — this plugin is faith education, not productivity tooling.
- Optional: add per-skill `agents/openai.yaml` files for UI polish (display name, icon, invocation policy). Not required by the portal; the plugin works without them.
