# Game Analytics — dashboard tĩnh cho Nam

Một file duy nhất `index.html`, không cần server, không cần đăng ký.

## Xài ngay trên máy (khuyên dùng — giữ doanh thu kín)
Mở `index.html` bằng trình duyệt là chạy. Up file CSV, dữ liệu lưu trong localStorage của trình duyệt đó.

## Deploy free (chỉ khi muốn có link)
Kéo `index.html` thả vào https://app.netlify.com/drop → được link `xxx.netlify.app`.
Tên miền phụ free khác: `xxx.vercel.app`, `xxx.pages.dev`, `xxx.github.io`.
**Cảnh báo:** các host free này đều công khai — đừng up dữ liệu doanh thu thật lên link công khai.

## File CSV nhận được
- AdMob: Reports → Download CSV (cột Date, Estimated earnings, Impressions, Ad requests, Clicks, eCPM)
- Play Console: Statistics → Export report (Install events, Uninstall events, First opens)
- LevelPlay / Unity Ads: export CSV của từng mạng, chỉ cần có cột ngày + số.
- Up nhiều file được; cùng ngày thì cộng dồn. Đổi game ở menu trên cùng để xem riêng Chess 3D Online / Block Legend.

## Đã kiểm chứng 2026-11-11
- `node --check` JS: OK.
- Parser thử với CSV mẫu kiểu AdMob (`Date,Install events,Impressions,Estimated earnings`): đọc đúng 2 dòng dữ liệu, số `$1,234.50` parse đúng 1234.5.
- Chưa thử với file CSV thật của Nam — lần đầu up file thật, kiểm tra xem tổng số ngày / doanh thu có khớp với AdMob không rồi hãy tin hẳn.
