## Giới thiệu

a

## Kiến thức cơ bản

a

## Sơ đồ

<img width="880" height="372" alt="Lab Diagram drawio" src="https://github.com/user-attachments/assets/e085b50f-e566-47cb-89a6-f2c0b798d8a3" />

## Cài đặt và cấu hình

Lab sử dụng VMWare Workstation để chạy 3 máy ảo: 2 máy Ubuntu và 1 Windows 10.

### VM1 - Wazuh server

Cài đặt Wazuh manager, Wazuh Indexer, Wazuh dashboard.

Có thể tham khảo hướng dẫn cài đặt ở đây: https://documentation.wazuh.com/current/installation-guide/index.html

### VM2 - SOAR & Incident Response

Cài đặt TheHive và Shuffle.

### VM3 - Windows 10 Enpoint

Cài đặt Sysmon và Wazuh Agent.

### Cấu hình mạng
Tất cả các máy ảo được cấu hình sử dụng chung một mạng ảo NAT, cho phép chúng giao tiếp trực tiếp với nhau thông qua địa chỉ IP nội bộ. Cách cấu hình này giúp đảm bảo các luồng dữ liệu như log từ endpoint gửi về SIEM, hay cảnh báo từ Wazuh gửi sang hệ thống SOAR đều được thực hiện một cách ổn định. Đối với SOC Analyst, việc truy cập vào các giao diện quản trị như Wazuh Dashboard, Shuffle hay TheHive được thực hiện thông qua trình duyệt web trên máy host, không cần triển khai thêm máy ảo riêng.
