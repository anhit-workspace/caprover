# Related basic information

- **Loki:** là hệ thống thu thập và tra cứu log tập trung được thiết kế từ Prometheus, có tính sẵn sàng cao (high-available) và có khả năng scale tốt. Loki được thiết kế để dễ dàng vận hành và hiệu quả về chi phí.
  - Tham khảo thêm: https://sdsrv.ai/blog/logging-system-cho-k8s-voi-loki/
- **Promtail:** là agent, có trách nhiệm đi thu gom log và gửi về cho Loki. Loki là thành phần chính, có trách nhiệm lưu trữ log và xử lý các câu query. Grafana là công cụ query và hiển thị log
- **cAdvisor:** tự động phát hiện tất cả các container trong máy và thu thập toàn bộ các thông tin thống kê như CPU, Memory, file system cũng như trạng thái sử dụng network. Nói tóm lại cAdvisor là một phần của kubelet.  
