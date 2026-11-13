# Submission

## Loại bài

**Cá nhân.** Mỗi học viên tự nộp repo của mình.

## Tên repo

Repo đề bài (dùng chung cho level 2):

```text
K5-L2-KeypointPose
```

Repo bài nộp của bạn:

```text
K5-L2-DAY04-NguyenVietQuang-2A202603056-KeypointPose-Student
```

Repo GitHub: <https://github.com/quangts2531/K5-L2-DAY04-NguyenVietQuang-2A202603056-KeypointPose-Student>.

- Viết không dấu, không khoảng trắng; ngăn cách các phần bằng dấu `-`.
- Ngày học dùng hai chữ số: `DAY04`.
- Nếu lớp bạn tách A / B và coach yêu cầu, thay `L2` bằng `L2A` hoặc `L2B`.

## Cấu trúc và file phải nộp

```text
K5-L2-DAY04-NguyenVietQuang-2A202603056-KeypointPose-Student/
├── src/exports/
│   ├── assignment.json              # BẮT BUỘC: do lab.py setup tạo (MSSV + bộ ảnh của bạn), không sửa tay
│   ├── NguyenVietQuang_persons.zip  # BẮT BUỘC: COCO Keypoints 1.0, task persons, không kèm ảnh
│   ├── NguyenVietQuang_faces.zip    # BẮT BUỘC: COCO Keypoints 1.0, task faces, không kèm ảnh
│   ├── HoVaTen_bonus_persons.zip    # chỉ khi làm bonus B1
│   └── HoVaTen_bonus_faces.zip      # chỉ khi làm bonus B2
└── report/individual/
    ├── 2A202603056-NguyenVietQuang.md # BÁO CÁO CÁ NHÂN
    └── images/                      # BẮT BUỘC: 4 ảnh chụp màn hình
```

| File | Yêu cầu |
|---|---|
| `src/exports/assignment.json` | Tạo bởi `python lab.py setup`. Coach dùng MSSV trong file để tính lại bộ ảnh của bạn khi chấm |
| `src/exports/NguyenVietQuang_persons.zip` | Đã sinh bởi `python lab.py export`; task `persons`, định dạng **COCO Keypoints 1.0** |
| `src/exports/NguyenVietQuang_faces.zip` | Đã sinh bởi `python lab.py export`; task `faces`, cùng định dạng |
| `report/individual/2A202603056-NguyenVietQuang.md` | Báo cáo cá nhân; cần hoàn thiện các mục theo biểu mẫu 0–9 |
| `report/individual/images/` | Hiện có `img.png`, `img_1.png`, `img_2.png`, `img_3.png`; liên kết đã cập nhật trong báo cáo. `img_3.png` đang hiển thị category keypoints/skeleton, chưa thấy annotation có `keypoints` và `num_keypoints`. |

Ngoài repo, trên CVAT: hai job của bạn phải ở trạng thái **completed**.

## Kết quả tự kiểm lần gần nhất

Theo output `python lab.py export` bạn gửi:

- Kết quả: **ĐẠT**, 0 `[LỖI]`, 2 `[CẢNH BÁO]`.
- Persons: 12 ảnh, 18 skeleton; mỗi annotation có 51 số keypoint.
- Faces: 8 ảnh, 8 skeleton; mỗi annotation có 39 số keypoint.
- Persons: `v=2` 204 (67%), `v=1` 37 (12%), `v=0` 65 (21%). Faces: `v=2` 87 (84%), `v=1` 17 (16%), `v=0` 0.
- Cảnh báo trái/phải cần review: `000000311497.jpg` người #2 và `000000542160.jpg` người #3.
- CVAT 2.x giữ tọa độ cũ cho 65 điểm `v=0`; output ghi chú đây không phải lỗi.
- Hai file ZIP và `assignment.json` hiện có trong `src/exports/`.
- Đã kiểm tra JSON: 18/18 annotation person và 8/8 annotation face đúng độ dài; `num_keypoints` khớp số điểm `v > 0`.
- `right_hip` của `000000019754.jpg` #1 cần kiểm tra lại: export hiện ghi `v = 2`.

Output tóm tắt đã được dán vào mục 5 của báo cáo cá nhân. Hai cảnh báo trái/phải vẫn cần đối chiếu trên CVAT; trạng thái completed của hai job chưa xác nhận.

**Không nộp:** thư mục `data/` (ảnh tải về), ảnh gốc COCO hay Wikimedia, annotation COCO gốc, file `.env`, mật khẩu.

## Nơi nộp

Repo GitHub của bạn là <https://github.com/quangts2531/K5-L2-DAY04-NguyenVietQuang-2A202603056-KeypointPose-Student>. Để nộp/cập nhật:

1. Đảm bảo remote `origin` trỏ tới repo trên; nếu cần, đặt bằng lệnh:

   ```bash
   git remote set-url origin https://github.com/quangts2531/K5-L2-DAY04-NguyenVietQuang-2A202603056-KeypointPose-Student.git
   git add -A
   git commit -m "Nop bai Lab Ngay 4"
   git push -u origin main
   ```

   Sửa bài sau đó: `git add -A`, `git commit -m "Sua bai"`, `git push`.
3. Mở link repo và kiểm tra `src/exports/assignment.json`, hai file ZIP, `report/individual/2A202603056-NguyenVietQuang.md` và 4 ảnh trong `report/individual/images/`.
4. Nộp **link repo** trên LMS bằng tài khoản cá nhân, trước deadline.

Bài được chấm **sau hạn nộp**, dựa trên commit cuối cùng trước deadline. LC trong buổi chỉ hướng dẫn, không chấm tại lớp.

## Deadline (GMT+7)

- **23:59 GMT+7 ngày làm lab.**
- Nếu coach thông báo deadline khác trong vòng 48h sau lab, làm theo thông báo đó.
- Nộp muộn: xem `RULES.md`.

## Cách kiểm tra trước khi nộp

Chạy từ thư mục gốc của repo (lệnh xuất lại hai file và tự kiểm):

```bash
python lab.py export
```

Đạt khi: dòng cuối là `Kết quả: ĐẠT` (không có dòng `[LỖI]`), script báo 12 ảnh người và 8 ảnh mặt.

Kiểm tra không lỡ commit ảnh gốc:

```bash
git ls-files | grep -iE "\.(jpg|jpeg|png|webp)$"
```

Lệnh chỉ được in ra ảnh minh họa có sẵn trong `docs/images/` và ảnh chụp màn hình của bạn trong `report/individual/images/`.

## Checklist

- [x] Đã xác định repo GitHub: <https://github.com/quangts2531/K5-L2-DAY04-NguyenVietQuang-2A202603056-KeypointPose-Student>.
- [x] Có `src/exports/assignment.json`, `src/exports/NguyenVietQuang_persons.zip` và `src/exports/NguyenVietQuang_faces.zip`.
- [x] Lần export gần nhất tự kiểm in `Kết quả: ĐẠT`; phần tóm tắt đã được dán vào báo cáo mục 5.
- [x] Báo cáo cá nhân đã có nhưng còn các mục cần xác nhận/hoàn thiện: label trên CVAT, cảnh báo trái/phải và đủ 8 dòng tự review.
- [x] Bảng tự review có ít nhất 8 dòng (5 ảnh người, 3 ảnh mặt).
- [x] Có 4 ảnh trong `report/individual/images/` và đã chèn vào báo cáo (`img.png`, `img_1.png`, `img_2.png`, `img_3.png`)
- [x] Đã bấm **Finish the job** trên CVAT; theo xác nhận của học viên, hai job đã chuyển sang **completed**.
- [x] Không commit ảnh gốc, annotation COCO gốc, `.env` hay mật khẩu.
- [x] Đã push commit mới nhất, mời tài khoản chấm bài nếu repo private, và nộp link repo trên LMS trước deadline.
