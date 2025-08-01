
# Mô phỏng Matching Mạch L-match 100MHz (LTspice)

## 🎯 Mục tiêu

Thiết kế và mô phỏng mạch L-match khớp trở từ nguồn 50Ω đến tải 200Ω tại tần số 100 MHz.

## 🧪 Thông tin mô phỏng

- Công cụ: LTspice (MacOS / Windows đều dùng được)
- File sơ đồ nguyên lý: `Lmatch100MHz.asc`
- Loại mô phỏng: AC Sweep
- Tần số quét: 10 MHz đến 200 MHz (dạng log)

## ⚙️ Tham số mạch

| Linh kiện | Giá trị     | Ghi chú                  |
|-----------|-------------|---------------------------|
| L1        | 120 nH      | Cuộn cảm nối tiếp         |
| C1        | 39 pF       | Tụ nối đất (song song với tải) |
| R1        | 200 Ω       | Tải cần ghép trở          |
| V1        | AC 1V, Rser=50Ω | Nguồn tín hiệu RF có trở kháng 50Ω |

## 📈 Kết quả mong đợi

- S11 (phản xạ) đạt mức thấp nhất gần 100 MHz
- Độ lợi truyền đạt tốt tại 100 MHz
- Mức phản xạ đầu vào thấp (VSWR thấp)

## 📁 Danh sách file

- `Lmatch100MHz.asc`: sơ đồ mạch chính
- `Draft1.asc`: mạch thử nghiệm khác
- `Draft1.net`: netlist mô phỏng
- `.raw`: kết quả (nếu có)

## ✅ Cách sử dụng

1. Mở LTspice
2. File > Open > `Lmatch100MHz.asc`
3. Chạy `.ac` simulation (AC Analysis)
4. Quan sát tín hiệu tại node `Vin` hoặc vẽ biểu thức S11

## 👤 Tác giả

- Nguyễn Thiên Hoàng – [github.com/ThienHoangNguyen92](https://github.com/ThienHoangNguyen92)
