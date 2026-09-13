# 📊 BÁO CÁO THU HOẠCH NGHIỆM THU BÀI LAB 3 (BƯỚC 3 — SUBMISSION ARTIFACT)

> **Họ và Tên Học viên:** Nguyễn Anh Dũng
> **Mã Sinh Viên / Mã Học viên:** 2A202602554
> **Chủ đề Lựa chọn:** Trợ lý Học vụ & Tra cứu Lịch thi cho sinh viên VinUni

---

## 1. BẢNG CHẤM ĐIỂM AGENTIC FIT SCORING MATRIX (ĐÁNH GIÁ CHỦ ĐỀ)

| Tiêu chí Đánh giá | Mức độ (1 - 5) | Giải trình chi tiết lý do chọn điểm |
| :--- | :---: | :--- |
| **1. Multi-step Reasoning** | 5 / 5 | Trợ lý cần hiểu câu hỏi của sinh viên, xác định học phần/lớp/kỳ học, đối chiếu lịch thi, kiểm tra điều kiện hoặc thông tin liên quan, rồi tổng hợp câu trả lời rõ ràng. Đây là chuỗi suy luận nhiều bước liên kết với nhau. |
| **2. Tool Interaction** | 5 / 5 | Hệ thống cần kết nối MCP Server hoặc cơ sở dữ liệu học vụ để truy xuất lịch thi, thông tin môn học, phòng thi, ca thi và các thông báo cập nhật từ nhà trường. |
| **3. Dynamic Decision** | 5 / 5 | Bước xử lý tiếp theo phụ thuộc vào dữ liệu tra cứu. Ví dụ, nếu sinh viên chưa cung cấp mã môn học hoặc có nhiều lớp học phần trùng tên, Agent phải hỏi lại hoặc đưa ra các lựa chọn phù hợp. |
| **4. Long Horizon Goal** | 4 / 5 | Agent cần duy trì ngữ cảnh trong suốt hội thoại, chẳng hạn thông tin sinh viên, học kỳ, môn học đang tra cứu và các câu hỏi tiếp theo. Tuy nhiên, phạm vi tác vụ chủ yếu vẫn tập trung vào hỗ trợ học vụ và lịch thi nên chưa cần quản lý mục tiêu dài hạn quá phức tạp. |
| **TỔNG ĐIỂM AGENTIC FIT** | **/ 20** | *Nếu tổng điểm > 12/20: Bài toán rất phù hợp triển khai Agentic System.* |

---

## 2. TRÍCH XUẤT KẾT QUẢ WATERFALL TRACE LOG (SAU KHI CHẠY TEST SUITE TRÊN API THẬT)

> ⚠️ **YÊU CẦU NGHIỆM THU:** Mở tệp `.env` điền `GEMINI_API_KEY` (hoặc `OPENAI_API_KEY`) để kết nối LLM thật trước khi thực thi `python src/app.py --all`. Bài nộp chỉ dùng Mock Offline Provider sẽ không đạt điểm nghiệm thực tế.

Dán 1 đoạn trích xuất log tiêu biểu từ file `docs/trace_waterfall.json` sinh ra từ phản hồi LLM API thật:

```json
[
  {
    "step": 1,
    "action_type": "TOOL_EXECUTION",
    "tool_name": "academic_query",
    "arguments": {
      "student_id": "SV2026001"
    },
    "observation": {
      "status": "SUCCESS",
      "student_id": "SV2026001",
      "data": {
        "full_name": "Nguyễn Văn An",
        "gpa": 3.85
      }
    },
    "latency_ms": 120.5
  }
]
```

---

## 3. TỔNG KẾT KẾT QUẢ NGHIỆM THU & NỘP BÀI

- [ ] Đã điền API Key thật trong `.env` và xác nhận Agent chạy mượt mà trên LLM API thật (Gemini/OpenAI).
- **Tổng số Test Cases đã chạy thành công:** ___ / 5 test cases.
- **Số lượt gọi Tool qua MCP Server chính xác:** ___ lượt.
- **Kết quả đẩy Repo nộp bài:** [ ] Đã Commit và Push mã nguồn thành công lên GitHub cá nhân.

---

> ✅ **HOÀN TẤT NỘP BÀI:** Sao chép đường link GitHub Repository cá nhân của bạn và dán vào ô nộp bài trên hệ thống LMS VLearn để hoàn tất Bài Lab 3!
