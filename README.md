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
6. `campaign/ACCOUNT_CREATION_RULES.md`
7. `campaign/SEO_LINK_POLICY.md`
8. `campaign/PLATFORMS.yaml`
9. `state/`

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
│   └── ASSET_MANIFEST.yaml
├── campaign/
│   ├── PLATFORMS.yaml
│   ├── ACCOUNT_CREATION_RULES.md
│   ├── SEO_LINK_POLICY.md
│   └── CONTENT_SEEDING_PLAN.md
├── docs/
│   ├── EXECUTION_ROADMAP.md
│   └── HUMAN_INPUTS_REQUIRED.md
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
- [ ] Chặng 4 — Nạp và duyệt brand assets thật.
- [ ] Chặng 5 — Xác nhận registration email / recovery workflow ngoài Git.
- [ ] Chặng 6 — Research live Wave 1 platforms trước khi signup.
- [ ] Chặng 7 — Pilot automation trên một nhóm nhỏ.
- [ ] Chặng 8 — Audit pilot rồi mới scale.

## Registry hiện tại

- **52 platform IDs** đã được phân loại.
- `state/accounts.csv` có **52 state rows**, khớp 1:1 với platform registry.
- Linktree đã được ghi nhận là account hiện hữu.
- Pinterest được đánh dấu **existing-account check needed**.
- Những platform chưa xác minh chính xác như Writexo/All4webs/Justpast.it/Postach được khóa ở chế độ **research first**.

## Human input tiếp theo

Xem:

**`docs/HUMAN_INPUTS_REQUIRED.md`**

Ưu tiên hiện tại là nạp asset chính thức:

- logo transparent;
- square avatar;
- Helen official headshot;
- generic brand cover/banner.

Không cần gửi password hoặc giấy tờ định danh vào repo.

## Canonical website

**https://nhamycali.com/**

## Human trust anchor

**Helen Hà Nguyễn** — Realtor® tại Coldwell Banker Realty, CalRE #01256922.

Chi tiết authoritative nằm trong `brand/` và phải được đọc cùng `AGENTS.md` trước khi thực hiện bất kỳ automation nào.

---

Maintained for the NHÀ MỸ CALI web-presence program.
