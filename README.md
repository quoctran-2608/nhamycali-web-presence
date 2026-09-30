# NHÀ MỸ CALI — Web Presence & Entity Operations

Repository này là **source of truth** cho việc xây dựng, chuẩn hóa và duy trì hiện diện số của thương hiệu **NHÀ MỸ CALI** trên website, mạng xã hội, nền tảng xuất bản, RSS/distribution và các profile công khai.

> Core mission: **Giúp Người Việt An Tâm Mua Nhà Mỹ.**

## Mục tiêu

Repo phục vụ 4 mục tiêu chính:

1. Giữ thông tin thương hiệu nhất quán trên mọi nền tảng.
2. Cho Codex/AI biết chính xác dữ liệu nào được phép dùng khi tạo hoặc cập nhật account.
3. Theo dõi trạng thái từng tài khoản, URL profile, bước xác minh và việc cần làm thủ công.
4. Xây dựng web presence, content distribution và branded citations theo hướng bền vững, không spam backlink.

## Nguyên tắc

- **Brand consistency trước số lượng account.**
- **Verify first, create second — trừ khi owner đã xác nhận rõ account chưa tồn tại trên đúng platform đó.**
- **Không tạo account trùng nếu profile chính thức đã tồn tại.**
- **Không dùng automation để bypass CAPTCHA, anti-bot, phone verification, identity verification hoặc security controls.**
- **Không tạo nội dung/link chỉ để thao túng ranking.**
- **Không tự bịa dữ kiện thương hiệu, MLS, giá, license, social URL, review count hoặc thông tin pháp lý.**
- Dữ liệu động phải được kiểm tra lại trước khi xuất bản.
- Credential, password, recovery code, TOTP secret, ID document và payment information **không được commit vào repo**.

## Codex: đọc gì trước?

Codex phải bắt đầu từ:

1. `AGENTS.md`
2. `brand/BRAND_ENTITY.yaml`
3. `brand/OFFICIAL_LINKS.yaml`
4. `brand/BRAND_DNA.md`
5. `brand/COPY_LIBRARY.md`
6. `assets/ASSET_MANIFEST.yaml`
7. `assets/PLATFORM_ASSET_POLICY.yaml`
8. `docs/REGISTRATION_POLICY.md`
9. `docs/OWNER_AUTHORIZATIONS.md`
10. `campaign/ACCOUNT_CREATION_RULES.md`
11. `campaign/SEO_LINK_POLICY.md`
12. `campaign/PLATFORMS.yaml`
13. `research/WAVE_1_DECISIONS.yaml` when working on Wave 1
14. `playbooks/PILOT_SEQUENCE.yaml` + exact platform playbook
15. `state/`

## Cấu trúc hiện tại

```text
.
├── AGENTS.md
├── README.md
├── brand/
│   ├── BRAND_DNA.md
│   ├── BRAND_ENTITY.yaml
│   ├── OFFICIAL_LINKS.yaml
│   └── COPY_LIBRARY.md
├── assets/
│   ├── README.md
│   ├── ASSET_MANIFEST.yaml
│   ├── PLATFORM_ASSET_POLICY.yaml
│   ├── avatar/
│   │   └── nhamycali-avatar-square.png
│   ├── cover/
│   │   └── nhamycali-cover-official.png
│   ├── helen/
│   │   └── helen-ha-nguyen-headshot.png
│   └── logo/
│       └── nhamycali-logo-transparent.png
├── campaign/
│   ├── PLATFORMS.yaml
│   ├── ACCOUNT_CREATION_RULES.md
│   ├── SEO_LINK_POLICY.md
│   └── CONTENT_SEEDING_PLAN.md
├── docs/
│   ├── CODEX_BROWSER_PILOT.md
│   ├── EXECUTION_ROADMAP.md
│   ├── HUMAN_INPUTS_REQUIRED.md
│   ├── OWNER_AUTHORIZATIONS.md
│   └── REGISTRATION_POLICY.md
├── research/
│   ├── WAVE_1_DECISIONS.yaml
│   └── WAVE_1_LIVE_RESEARCH_2026-09-28.md
├── playbooks/
│   ├── README.md
│   ├── PILOT_SEQUENCE.yaml
│   ├── BLUESKY.md
│   ├── SUBSTACK.md
│   ├── BLOGGER.md
│   ├── GRAVATAR_AUDIT.md
│   ├── LINKTREE_AUDIT.md
│   └── MEDIUM_MANUAL.md
├── content/
│   └── seed/
│       ├── BLUESKY_SEED.md
│       ├── SUBSTACK_WELCOME.md
│       └── BLOGGER_FIRST_POST.md
├── secrets/
│   └── .env.example
├── state/
│   ├── accounts.csv
│   ├── failures.csv
│   └── manual_actions.md
├── templates/
│   ├── platform_report.md
│   └── account_audit.md
└── .gitignore
```

## Workflow chuẩn cho Codex

```text
Load rules
  ↓
Read brand source of truth
  ↓
Check whether official account already exists
  ↓
Research current platform/domain/signup requirements
  ↓
Classify platform purpose
  ↓
Create/update profile only when appropriate
  ↓
Complete public profile
  ↓
Verify public URL and website link
  ↓
Record result
  ↓
Capture manual blockers
  ↓
Continue to next platform
```

## Trạng thái

- [x] Khởi tạo repository.
- [x] Chặng 1 — Agent rules + brand source of truth.
- [x] Chặng 2 — Platform registry + SEO/link policy.
- [x] Chặng 3 — Account state + execution templates.
- [x] Chặng 4 — Nạp và duyệt brand assets thật.
- [x] Chặng 5A — Xác nhận registration mailbox + SMS verification policy ngoài Git.
- [x] Chặng 5B — Cho phép temporary bootstrap password trong local `secrets/.env` cho pilot; password manager/unique passwords là bước hardening trước khi scale.
- [x] Chặng 6 — Research live Wave 1 platforms trước khi signup.
- [x] Chặng 7A — Soạn pilot playbook + seed content + Codex entry point.
- [x] Chặng 7B — Bluesky pilot completed và public QA đạt.
- [x] Chặng 8A — Audit/close-out Bluesky completed.
- [x] Chặng 8B — Substack pilot completed và subdomain thương hiệu đã chốt.
- [ ] Chặng 8C — Chạy Blogger pilot.

## Registry hiện tại

- **52 platform IDs** đã được phân loại.
- `state/accounts.csv` có **52 state rows**, khớp 1:1 với platform registry.
- Linktree đã được ghi nhận là account hiện hữu.
- Pinterest: owner xác nhận đã có account nhưng **đã loại khỏi chiến dịch chủ động**; Codex không tạo, phát triển hay sửa profile này nếu chưa được tái kích hoạt.
- Những platform chưa xác minh chính xác như Writexo/All4webs/Justpast.it/Postach được khóa ở chế độ **research first**.

### Autonomous browser mode

Browser execution mặc định là **autonomous đối với thao tác bình thường**. Codex không cần hỏi lại trước mỗi nút Next/Continue/Save/Edit/Publish, không cần hỏi lại khi rút gọn bio theo giới hạn ký tự, và có thể retry/reload/navigate lại trang hợp lệ nếu UI không phản hồi.

Canonical facts vẫn là ranh giới cứng: Codex không được tự bịa hoặc thay đổi tên pháp lý, contact, địa chỉ, license, brokerage relationship, ownership claim hay verified URL.

### Standing owner authorization

Owner đã phê duyệt trước việc Codex tự tick/bấm **I agree / Accept / Continue** đối với Terms of Service, Privacy Policy, Community Guidelines và standard Publisher/Creator Agreements trong luồng tạo **free account/profile/publication** đã được repo phê duyệt.

Chi tiết và giới hạn nằm trong `docs/OWNER_AUTHORIZATIONS.md`.

Điều này không cho phép Codex bịa thông tin pháp lý/cá nhân, chấp nhận payment/paid trial/Stripe/card/bank, hoặc bypass CAPTCHA/OTP/security controls.

## Human input tiếp theo

Xem:

**`docs/HUMAN_INPUTS_REQUIRED.md`**

Bộ asset first-wave đã hoàn tất và được commit từ đúng các file người dùng cung cấp:

- `assets/logo/nhamycali-logo-transparent.png`
- `assets/avatar/nhamycali-avatar-square.png`
- `assets/helen/helen-ha-nguyen-headshot.png`
- `assets/cover/nhamycali-cover-official.png`

Banner hiện tại là asset chính thức 851×315, đủ làm reference/cover ở nơi phù hợp nhưng **không được coi là high-resolution master cho mọi nền tảng**.

Registration policy hiện đã xác nhận ở mức cần thiết để research/pilot:

- primary registration mailbox: đã chọn, giữ ngoài Git;
- temporary bootstrap password: owner đã phê duyệt, chỉ đọc từ local `secrets/.env`, không ghi literal vào repo;
- SMS verification: ưu tiên số Việt Nam do owner kiểm soát; dùng số business Mỹ làm fallback khi nền tảng không nhận số Việt Nam;
- exact values chỉ được nạp qua local `secrets/.env`;
- Pinterest đã có nhưng không còn nằm trong active campaign;
- Bluesky: owner xác nhận ngày 2026-09-30 rằng chưa có account, nên pilot được đi thẳng vào signup và bỏ qua duplicate-discovery.

Live Wave 1 research + Bluesky pilot hiện có trạng thái:

- **Completed:** Bluesky — https://bsky.app/profile/nhamycali.bsky.social
- **Completed:** Substack — https://nhamycali.substack.com/
- **Next pilot:** Blogger.
- **Existing — audit only:** Gravatar, Linktree.
- **Manual-only:** Medium.
- **Deferred:** Google Sites.
- **Removed from active signup:** About.me, Feedly, Inoreader, Pinterest.

Chi tiết:
- `research/WAVE_1_LIVE_RESEARCH_2026-09-28.md`
- `research/WAVE_1_DECISIONS.yaml`

Pilot package đã sẵn sàng:

- `docs/CODEX_BROWSER_PILOT.md`
- `playbooks/PILOT_SEQUENCE.yaml`
- `playbooks/BLUESKY.md`
- `playbooks/SUBSTACK.md`
- `playbooks/BLOGGER.md`
- seed content tương ứng trong `content/seed/`.

Ưu tiên tiếp theo:

- chạy **Blogger duy nhất** theo `docs/CODEX_BROWSER_PILOT.md`;
- Codex được phép chủ động với toàn bộ thao tác UI thông thường, chỉnh copy không-canonical, upload asset, save/publish nội dung đã duyệt và cập nhật repo;
- standard free signup Terms/Privacy/Community/Publisher Agreement đã được owner pre-authorize; không hỏi lại;
- chỉ dừng ở hard blocker: CAPTCHA/anti-bot, OTP/2FA/security challenge, giấy tờ định danh/thiếu factual attestation, payment, ownership conflict, Terms cấm workflow hoặc yêu cầu commitment ngoài authorization, hoặc destructive irreversible action;
- audit Blogger trước khi mở rộng Wave 1/2 tiếp theo.

Không gửi password, mã 2FA, recovery code hoặc giấy tờ định danh vào repo.

## Canonical website

**https://nhamycali.com/**

## Human trust anchor

**Helen Hà Nguyễn** — Realtor® tại Coldwell Banker Realty, CalRE #01256922.

Chi tiết authoritative nằm trong `brand/` và phải được đọc cùng `AGENTS.md` trước khi thực hiện bất kỳ automation nào.

---

Maintained for the NHÀ MỸ CALI web-presence program.
