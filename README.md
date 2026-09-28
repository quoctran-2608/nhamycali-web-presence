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
- **Verify first, create second.**
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
9. `campaign/ACCOUNT_CREATION_RULES.md`
10. `campaign/SEO_LINK_POLICY.md`
11. `campaign/PLATFORMS.yaml`
12. `research/WAVE_1_DECISIONS.yaml` when working on Wave 1
13. `state/`

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
│   ├── EXECUTION_ROADMAP.md
│   ├── HUMAN_INPUTS_REQUIRED.md
│   └── REGISTRATION_POLICY.md
├── research/
│   ├── WAVE_1_DECISIONS.yaml
│   └── WAVE_1_LIVE_RESEARCH_2026-09-28.md
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
- [ ] Chặng 5B — Chọn password-management workflow; recovery email là tùy chọn.
- [x] Chặng 6 — Research live Wave 1 platforms trước khi signup.
- [ ] Chặng 7 — Pilot browser-assisted trên Bluesky → Substack → Blogger, từng nền tảng một.
- [ ] Chặng 8 — Audit pilot rồi mới scale.

## Registry hiện tại

- **52 platform IDs** đã được phân loại.
- `state/accounts.csv` có **52 state rows**, khớp 1:1 với platform registry.
- Linktree đã được ghi nhận là account hiện hữu.
- Pinterest: owner xác nhận đã có account nhưng **đã loại khỏi chiến dịch chủ động**; Codex không tạo, phát triển hay sửa profile này nếu chưa được tái kích hoạt.
- Những platform chưa xác minh chính xác như Writexo/All4webs/Justpast.it/Postach được khóa ở chế độ **research first**.

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
- SMS verification: ưu tiên số Việt Nam do owner kiểm soát; dùng số business Mỹ làm fallback khi nền tảng không nhận số Việt Nam;
- exact values chỉ được nạp qua local `secrets/.env`;
- Pinterest đã có nhưng không còn nằm trong active campaign.

Live Wave 1 research đã hoàn tất. Kết quả chính:

- **Ready for pilot:** Bluesky, Substack, Blogger.
- **Existing — audit only:** Gravatar, Linktree.
- **Manual-only:** Medium.
- **Deferred:** Google Sites.
- **Removed from active signup:** About.me, Feedly, Inoreader, Pinterest.

Chi tiết:
- `research/WAVE_1_LIVE_RESEARCH_2026-09-28.md`
- `research/WAVE_1_DECISIONS.yaml`

Ưu tiên tiếp theo:

- chọn cách quản lý password ngoài Git;
- recovery email nếu muốn;
- bắt đầu pilot **Bluesky trước**, sau đó audit kết quả rồi mới đi Substack/Blogger;
- xác nhận thêm các account cũ nếu owner nhớ ra.

Không gửi password, mã 2FA, recovery code hoặc giấy tờ định danh vào repo.

## Canonical website

**https://nhamycali.com/**

## Human trust anchor

**Helen Hà Nguyễn** — Realtor® tại Coldwell Banker Realty, CalRE #01256922.

Chi tiết authoritative nằm trong `brand/` và phải được đọc cùng `AGENTS.md` trước khi thực hiện bất kỳ automation nào.

---

Maintained for the NHÀ MỸ CALI web-presence program.
