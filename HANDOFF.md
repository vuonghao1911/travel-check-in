# Wandr Pitch Deck — Session Handoff

Last session ended mid-deploy. Tiếp tục bằng cách paste link này hoặc nói "tiếp tục từ HANDOFF.md".

## Project state

- **File chính**: `index.html` (single-page, Tailwind CDN, dark theme)
- **Git**: đã init, branch `main`, có commit
- **Deploy target**: GitHub `vuonghao1911/travel-check-in` (public) + Vercel

## Pending steps (sắp xếp theo thứ tự)

### Bước 1 — Manual (user làm trong browser)
- [ ] Add SSH pub key vào https://github.com/settings/keys (login bằng `vuonghao1911`)
  - Pub key file: `~/.ssh/id_rsa_personal.pub`
  - Comment cuối key: `vuonghao14298@gmail.com`
- [ ] Tạo repo trống: https://github.com/new
  - Owner: `vuonghao1911`
  - Name: `travel-check-in`
  - Public, KHÔNG tick README/gitignore/license

### Bước 2 — Claude làm (sau khi user reply "done")
```bash
cd "D:/Entertainment/travel-check-in"
git remote set-url origin github-personal:vuonghao1911/travel-check-in.git
git push -u origin main
```

### Bước 3 — Deploy Vercel
- Install vercel CLI: `npm i -g vercel` (hoặc dùng `npx vercel`)
- `vercel login` (user tự auth, interactive)
- `vercel --prod` từ project dir
- Hoặc: import repo qua https://vercel.com/new → auto-deploy on push

## Pitch deck content summary

15 phone mockup CSS-only:
- 5 core screens: Map Feed, Camera, Post Detail, Place Detail, Profile
- 6 tab screens: Search, Saved, Home Feed list, Trip Timeline, Notifications, Onboarding
- 3 map detail: Place Bottom Sheet, Heatmap, Realtime Posts
- 1 featured large: Map Full View (extracted block, không nằm trong scroll row)

Sections:
- Hero + marquee
- Vấn đề (3 card) + Giải pháp (6 feature)
- Thị trường TAM/SAM/SOM + VN beachhead
- Bảng cạnh tranh
- Retention benchmark + 6 metric annotation + SVG curve chart
- Roadmap 4 phase (Phase 1+2 đã expand đầy đủ với monthly breakdown + budget + exit criteria)
- 5 rủi ro accordion
- Tech stack 8 card
- Ask pre-seed $300-500k

## User preferences (active)

- Caveman mode full — terse Vietnamese, no fluff
- Vietnamese output mặc định
- Iterative small edits — dùng Edit, không rewrite
- CSS-only mockup khi show UI
- Don't break layout — featured elements ra block riêng

## Email + brand

- Pitch email: `vuonghao14298@gmail.com` (đã thay khắp file)
- Brand: **Wandr**
- Tagline: "Bản đồ du lịch thật. Không filter. Không fake."
