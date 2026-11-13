# Phân tích lỗi tính toán của LLM

## Phần 1. Hai nhận định sai

1. **Sai khi cho rằng AI trả lời sai là do máy chủ hỏng.** LLM tạo câu trả lời bằng cơ chế **Next Token Prediction** (dự đoán token tiếp theo). Vì vậy, LLM có thể tạo kết quả số học sai dù hệ thống vẫn hoạt động bình thường.
2. **Sai khi cho rằng nhiều tham số đồng nghĩa tính toán chính xác 100%.** Qua **Pre-training**, LLM học các mẫu và quan hệ từ dữ liệu, không mặc định thực hiện thuật toán cộng chính xác như máy tính bỏ túi. LLM có thể suy luận, nhưng vẫn có sai sót.

**Phép tính đúng:** 15.480 + 28.750 = **44.230** (dấu chấm ngăn cách hàng nghìn).

## Phần 2. Prompt sửa lỗi

> Hãy dùng công cụ Calculator hoặc Python để tính chính xác `15480 + 28750`. Hiển thị phép tính và kết quả, sau đó kiểm tra lại bằng một phép tính độc lập. Không tự đoán đáp án. Nếu không sử dụng được công cụ tính toán, hãy nói rõ giới hạn đó.

**Kết luận:** Với phép tính cần độ chính xác cao, ưu tiên công cụ tính toán và kiểm tra kết quả, không tin tuyệt đối vào câu trả lời LLM.
