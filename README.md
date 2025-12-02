# thuc-nghiem-110-cau-hoi
Kiểm tra độ chính xác của Chabot
# Thực nghiệm đo độ chính xác của Chatbot trong hỗ trợ học tập

Repo này lưu trữ dữ liệu và kết quả thực nghiệm đo **độ chính xác của Chatbot** trong việc trả lời các câu hỏi trắc nghiệm môn Tin học 10, phục vụ cho đề tài luận văn:

> **“Ứng dụng Chatbot thông minh hỗ trợ học tập cho học sinh”**

---

## 1. Mục tiêu thực nghiệm

- Đánh giá **khả năng trả lời đúng** các câu hỏi kiến thức cơ bản Tin học 10 của Chatbot.
- So sánh giữa:
  - **Đáp án chuẩn** (do giáo viên / tài liệu chính thống cung cấp)  
  - **Đáp án do Chatbot sinh ra** trong cùng điều kiện.
- Làm cơ sở minh chứng cho **tính khả thi** khi sử dụng Chatbot như một công cụ hỗ trợ học tập cho học sinh THPT/THCS.

---

## 2. Mô tả bộ dữ liệu

- Tổng số câu hỏi: **110 câu trắc nghiệm**.
- Lĩnh vực: **Tin học 10**, bám sát sách giáo khoa/bộ đề đang sử dụng.
- Mỗi câu gồm:
  - Câu hỏi
  - 4 phương án A, B, C, D
  - Một **đáp án đúng** do giáo viên xác định.

Trong repo có các tệp:

- `110_cau_hoi_tin_hoc10.md` hoặc `110_cau_hoi_tin_hoc10.docx`  
  → Toàn bộ câu hỏi và đáp án đúng.
- `ket_qua_110_cau.xlsx`  
  → Bảng so sánh **Đáp án đúng** vs **Câu trả lời của Chatbot** theo từng câu.
- (Tuỳ chọn) `ket_qua_110_cau.csv`  
  → Phiên bản dữ liệu dạng bảng để xử lý bằng Python/R/Excel.

---

## 3. Quy trình thực nghiệm

1. **Chuẩn bị câu hỏi**
   - Chọn và chuẩn hoá **110 câu trắc nghiệm** Tin học 10.
   - Ghi nhận **đáp án đúng** cho từng câu (cột `Đáp án đúng`).

2. **Thiết lập kịch bản hỏi Chatbot**
   - Mỗi câu hỏi được gửi cho Chatbot ở **dạng độc lập**, không cung cấp trước đáp án đúng.
   - Chatbot được yêu cầu trả lời theo **định dạng: A / B / C / D**.
   - Mỗi câu chỉ hỏi **một lần**, không gợi ý lại hoặc “chữa bài”.

3. **Lưu kết quả**
   - Ghi lại câu trả lời của Chatbot cho từng câu (cột `Câu trả lời của Chatbot`).
   - So sánh với cột `Đáp án đúng` để xác định **Đúng/Sai**.

4. **Tính toán độ chính xác**
   - Độ chính xác được tính theo công thức:

     \[
     \text{Accuracy} = \frac{\text{Số câu trả lời đúng}}{\text{Tổng số câu}} \times 100\%
     \]

---

## 4. Kết quả chính

- **Tổng số câu hỏi:** 110  
- **Số câu Chatbot trả lời đúng:** 95  
- **Số câu trả lời sai:** 15  

→ **Độ chính xác (Accuracy):**

\[
Accuracy = \frac{95}{110} \approx 86{,}36\%
\]

Kết quả chi tiết theo từng câu được lưu trong:

- `ket_qua_110_cau.xlsx`  
  - Mỗi nhóm 11 câu được trình bày dưới dạng:
    - Dòng 1: `Câu` (số thứ tự 1–11, 12–22, …)  
    - Dòng 2: `Đáp án đúng`  
    - Dòng 3: `Câu trả lời của Chatbot`

---

## 5. Ý nghĩa sư phạm

- Độ chính xác **~86%** cho thấy Chatbot có khả năng:
  - Trả lời đúng phần lớn các câu hỏi kiến thức cơ bản Tin học 10.
  - Có tiềm năng trở thành **trợ giảng ảo** hỗ trợ học sinh trong quá trình ôn tập.
- Tuy nhiên vẫn tồn tại khoảng **14% câu sai**, do đó:
  - Chatbot **không thể thay thế hoàn toàn** giáo viên.
  - Cần được sử dụng như **công cụ hỗ trợ**, kết hợp với sự kiểm tra, định hướng của giáo viên.
