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
- **Không tạo account trùng nếu profile chính thức đã tồn tại.**
- **Không dùng automation để bypass CAPTCHA, anti-bot, phone verification, identity verification hoặc security controls.**
- **Không tạo nội dung/link chỉ để thao túng ranking.**
- **Không tự bịa dữ kiện thương hiệu, MLS, giá, license, social URL, review count hoặc thông tin pháp lý.**
- Dữ liệu động phải được kiểm tra lại trước khi xuất bản.
- Credential, password, recovery code, TOTP secret, ID document và payment information **không được commit vào repo**.

## Cấu trúc dự kiến

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
│   └── README.md
├── campaign/
│   ├── PLATFORMS.yaml
│   ├── ACCOUNT_CREATION_RULES.md
│   ├── SEO_LINK_POLICY.md
│   └── CONTENT_SEEDING_PLAN.md
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

Repo đang được xây dựng theo từng chặng:

- [x] Khởi tạo repository.
- [ ] Chặng 1 — Agent rules + brand source of truth.
- [ ] Chặng 2 — Platform registry + SEO/link policy.
- [ ] Chặng 3 — Account state + execution templates.
- [ ] Chặng 4 — Brand assets.
- [ ] Chặng 5 — Pilot automation trên một nhóm nhỏ platform.
- [ ] Chặng 6 — Audit rồi mới scale.

## Canonical website

**https://nhamycali.com/**

## Human trust anchor

**Helen Hà Nguyễn** — Realtor® tại Coldwell Banker Realty, CalRE #01256922.

Chi tiết authoritative nằm trong `brand/` và phải được đọc cùng `AGENTS.md` trước khi thực hiện bất kỳ automation nào.

---

Maintained for the NHÀ MỸ CALI web-presence program.
