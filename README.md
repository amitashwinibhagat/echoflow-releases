# Echo Flow — Downloads & Releases

**Private, AI-polished dictation for Mac. Hold ⌥ Space, speak, release — polished text lands where your cursor is.**

[![macOS 15+](https://img.shields.io/badge/macOS-15%2B-black?logo=apple)](https://echoflow.one/download.html)
[![Apple Silicon](https://img.shields.io/badge/Apple_Silicon-arm64-black)](https://echoflow.one/download.html)
[![Latest release](https://img.shields.io/github/v/release/amitashwinibhagat/echoflow-releases?label=latest)](https://github.com/amitashwinibhagat/echoflow-releases/releases/latest)
[![Website](https://img.shields.io/badge/echoflow.one-visit-4a3728)](https://echoflow.one)

> **New here? Start at [echoflow.one](https://echoflow.one)** — features, use-cases, comparisons, and the email-gated one-click download at [echoflow.one/download.html](https://echoflow.one/download.html). This repo is the public distribution backbone behind that page: versioned, checksummed DMGs served over HTTPS for Sparkle in-app updates and direct downloads.

---

## ⬇️ Download

**Latest stable (recommended for everyone):**

👉 **[Download Echo Flow 1.5.0 (build 160) — EchoFlow-1.5.0-160.dmg](https://github.com/amitashwinibhagat/echoflow-releases/releases/download/v1.5.0/EchoFlow-1.5.0-160.dmg)**
`142 MB · macOS 15+ · Apple Silicon · notarized Developer ID DMG`

Or always get latest without checking the version number:

👉 **[Download latest (auto-updates to newest release)](https://github.com/amitashwinibhagat/echoflow-releases/releases/latest/download/EchoFlow-1.5.0-160.dmg)**

Prefer email-gated download with product tips? Use the [official download page](https://echoflow.one/download.html) — same binary, plus optional MailerLite updates.

Browse every version with notes and hashes: **[All releases →](https://github.com/amitashwinibhagat/echoflow-releases/releases)**

---

## ✨ Why Echo Flow

| | |
|---|---|
| 🎙️ **Speak anywhere** | Hold **⌥ Space** in any app — Mail, Slack, Docs, Xcode — release, and text appears at your cursor. No window switching. |
| 🧠 **Rewrite anything** | Floating palette (`⌥⇧Space`): Fix Writing, Make It Shorter, Sound Pro, Sound Friendly, Bullet Points, Key Takeaways, and more. Stays available even after the dictation trial ends. |
| 🔒 **Private by design** | Dictated audio, transcripts, and rewritten text stay on your Mac. No cloud STT, no account required. (Setup downloads, updates, licensing, and optional email signup contact servers — see [privacy architecture](https://echoflow.one/privacy-architecture.html).) |
| ⚡ **On-device AI** | Apple Intelligence on macOS 26+, local Echo Flow AI fallback, instant rule-based fallback — works offline. |
| 💳 **One-time purchase** | No subscription. **14-day dictation trial, no credit card.** One license covers up to three Macs you personally use, all 1.x updates included. |

---

## 🖥️ System requirements

- macOS 15 Sequoia or later (best on macOS 26 Tahoe with Liquid Glass)
- Apple Silicon (arm64)
- ~150 MB disk for the app · ~400 MB extra on first Echo Flow AI model setup
- Microphone + Accessibility permission (standard for dictation)

---

## 🔄 Updates

Echo Flow updates itself via [Sparkle](https://sparkle-project.org):

- Feed: [`https://echoflow.one/appcast.xml`](https://echoflow.one/appcast.xml)
- Each release entry carries a versioned DMG URL, byte `length`, and EdDSA `edSignature` — Sparkle verifies the signature before installing.
- Version scheme: `MAJOR.MINOR.PATCH build N` (e.g. `1.5.0 build 160`). Builds increase monotonically; licenses cover all `1.x`.

> **Coming from `releases.echoflow.one`?** That Netlify host is legacy. All new releases ship here. Old `/updates/*` and `/echoflow.dmg` URLs keep redirecting so no installed app is left behind.

---

## 📋 Version history

| Version | Build | Date | Highlights |
|---|---|---|---|
| [1.5.0](https://github.com/amitashwinibhagat/echoflow-releases/releases/tag/v1.5.0) | 160 | Aug 22, 2026 | Liquid Glass on macOS 26, real Mac menu bar, resizable window, native system colors |
| earlier | ≤158 | — | See [changelog](https://echoflow.one/changelog.html) for the full launch-cycle history |

Full product changelog (user-facing): [echoflow.one/changelog.html](https://echoflow.one/changelog.html)

---

## ✅ Verify your download

```bash
# size must be exactly 142207333 bytes
stat -f "%z" EchoFlow-1.5.0-160.dmg

# SHA-256 must match
shasum -a 256 EchoFlow-1.5.0-160.dmg
# e5d21df2754b75e60eefa17807f87787ef6b0a455d3dc8052e354e2a057cfe17
```

Sparkle verifies the EdDSA signature automatically on update. The DMG is Developer ID-signed and notarized by Apple — Gatekeeper shows a clean open, no warnings.

---

## 🔗 Links

- 🏠 [echoflow.one](https://echoflow.one) — homepage
- ⬇️ [Download](https://echoflow.one/download.html) · [Features](https://echoflow.one/features.html) · [Use cases](https://echoflow.one/use-cases.html) · [How to use](https://echoflow.one/how-to-use.html)
- 📰 [Changelog](https://echoflow.one/changelog.html) · [Blog](https://echoflow.one/blog/) · [Press kit](https://echoflow.one/press-kit.html) · [Launch kit](https://echoflow.one/launch-kit.html)
- 🔒 [Privacy](https://echoflow.one/privacy.html) · [Privacy architecture](https://echoflow.one/privacy-architecture.html) · [Terms](https://echoflow.one/terms.html)
- ✉️ [Contact](https://echoflow.one/contact.html)

Found an issue with a download? [Contact support](https://echoflow.one/contact.html) with the version, build number, SHA-256, and macOS version.

---

## 🛠️ Maintainer notes

This repo holds **release artifacts only** — no source. App source and the marketing site live in private repos.

```bash
# ship a new version (example: 1.6.0 build 165)
gh release create v1.6.0 EchoFlow-1.6.0-165.dmg \
  --repo amitashwinibhagat/echoflow-releases \
  --title "Echo Flow 1.6.0 (165)" \
  --notes-file notes.md

# asset naming: EchoFlow-<marketing-version>-<build>.dmg (no spaces)
# then update appcast.xml + /api/download in the website repo
```

<sub>© Echo Flow · Direct DMG is the only channel — no Mac App Store build planned · [echoflow.one](https://echoflow.one)</sub>
