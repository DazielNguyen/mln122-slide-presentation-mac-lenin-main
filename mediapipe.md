# Giải thích kịch bản tích hợp MediaPipe: Điều khiển Thuyết trình Tương tác

## 1. Mục đích của việc tích hợp MediaPipe
Việc nhúng module trí tuệ nhân tạo **MediaPipe (do Google phát triển)** vào trang Web trình chiếu (cụ thể ở file `flag-hands.html`) nhằm mục đích:
- **Tăng cường phần Trải nghiệm tương tác (Augmented Interaction):** Cho phép người thuyết trình điều khiển bài báo cáo, số liệu kinh tế và mô hình minh họa 3D bằng cử chỉ tay (Hand Tracking) hoàn toàn mà không cần tới chuột hay clicker. 
- **Minh họa trực quan lý luận Kinh tế chính trị:** Thay vì chỉ nói lý thuyết suông, hệ thống MediaPipe biến các khái niệm trừu tượng (như tỷ suất GTTD, tư bản bất biến, lao động) thành các chỉ số **sống động, nhảy số realtime** mô phỏng sự tương tác của nền kinh tế. Điều này làm bật lên tư tưởng "Thực tiễn là tiêu chuẩn của chân lý" của Mác.

---

## 2. Các Cử chỉ tay (Hand Gestures) & Ý nghĩa chi tiết

Kịch bản sử dụng 21 điểm mốc (landmarks) trên bàn tay để nhận diện 5 cử chỉ chính. Mỗi cử chỉ tương ứng với một thao tác điều hướng nội dung hoặc thay đổi 1 **Biến số Kinh tế học**.

### ✊ 1. Nắm đấm (Fist)
- **Hành vi thực hiện:** Nắm chặt cả 5 ngón tay lại (giấu các mốc ngón tay vào phía trong lòng).
- **Chức năng logic (`action = "form"`):**
  - Ra lệnh hệ thống tập hợp.
  - **Hiệu ứng đồ họa:** Hàng ngàn hạt phân tử (Particles 3D) đang bay lơ lửng, phân tán sẽ bị hút lại và nối thành hình **Biểu tượng Robot và Người Lao Động** kèm theo thông điệp "GIÁ TRỊ - LAO ĐỘNG - AI". Đại diện cho "Sự tập trung cường độ cao và gắn kết biện chứng giữa con người với máy móc".

### 🖐 2. Mở lòng bàn tay (Open Palm)
- **Hành vi thực hiện:** Duỗi thẳng mở rộng 5 ngón tay, lòng bàn tay hướng thẳng về Camera.
- **Chức năng logic (`action = "scatter"`):**
  - **Hiệu ứng đồ họa:** Đánh tan khối hình Robot ban gốc, các hạt lượng tử sẽ vỡ ra và bay lơ lửng tự do (Biểu hiện của sự giải phóng và phân tán).
  - **Công dụng thuyết trình:** Khi rơi vào trạng thái này, hệ thống sẽ triệu hồi **4 Thẻ lý thuyết tổng kết** mọc lên từ dưới đáy màn hình. Cổ tay của bạn lúc này biến thành "con trỏ chuột ảo" — hễ bạn di chuyển tay hướng về thẻ nào, thẻ đó sẽ tự động được phóng to lại gần camera để khán giả dễ đọc.

### 👌 3. Cử chỉ OK (Pinch / OK Pose)
- **Hành vi thực hiện:** Ngón trỏ và ngón cái chụm lại thành hình chữ o, 3 ngón còn lại duỗi thẳng ra.
- **Chức năng logic (`action = "training"`):**
  - **Ý nghĩa Kinh tế:** Hành động này đóng vai trò như lệnh **"Đầu tư / Đào tạo lại nguồn nhân lực" (Reskilling / Upskilling)** trong kỷ nguyên công nghệ số. 
  - **Minh họa bài học:** Duy trì cử chỉ này trước ống kính, màn hình chỉ số kinh tế trên góc sẽ chạy: (Chất lượng lao động tăng, chỉ số Công bằng tăng) đồng thời giảm sát thương của (Rủi ro thất nghiệp cấu trúc do AI). Đại biểu cho hàm ý sinh viên thích ứng công nghệ làm tăng chất xám (v).

### ↔️ 4. Vuốt tay ngang (Swipe Trái / Phải)
- **Hành vi thực hiện:** Đưa bàn tay chuyển động ngang khung hình rất nhanh và dứt khoát về bên trái hoặc phải.
- **Chức năng logic (`action = "redistribute"`):**
  - **Ý nghĩa Kinh tế:** Cử chỉ này mô phỏng trạng thái **Điều tiết chính sách** / Can thiệp thời gian lao động.
  - **Minh họa bài học:** Khi ở chế độ GTTD:
    - **Vuốt tay sang một hướng (Ép lao động):** Kéo vạch thời gian lao động lên cao → Lượng GTTD bóc lột sinh ra (`m`) tăng mạnh để nhà đầu tư giàu lên nhưng *Cảnh báo Công bằng Xã hội bị tụt giảm báo động*.
    - **Vuốt tay hướng ngược lại:** Phân phối lại phúc lợi → Thời gian lao động giảm, mâu thuẫn xã hội được xoa dịu. Đây là minh chứng mâu thuẫn giữa tiến bộ công nghệ và lợi nhuận nhà tư bản.

### 🫶 5. Hai tay ghép trái tim (Two-hand Heart)
- **Hành vi thực hiện:** Đưa hai bàn tay lại sát nhau trước ngực, ghép thành hình vòng cung trái tim lớn.
- **Chức năng logic (`action = "heart"`):**
  - **Ý nghĩa đồ họa:** Tư tưởng trịnh trọng, nhân văn kết thúc bản lý luận.
  - **Hiệu ứng:** Dàn hạt phân tử 3D sẽ biến đổi hình hài (Morphing) mượt mà thành một **Trái tim khổng lồ màu hồng/cam rực rỡ** lơ lửng, kèm hiệu ứng phát sáng dập dìu. Dòng chữ *Thanks for your attentions* được bật lên làm Backdrop cho việc kết thúc buổi thuyết trình.

---

## 3. Lời khuyên Kịch bản nói khi Trình bày với Giảng Viên (Cách nói ăn điểm)

*Khi đến đoạn chiếu Web Demo Camera, bạn có thể giải thích theo mẫu diễn đạt sau nhằm ghi điểm về sự am hiểu lý thuyết:*

> *"Dạ thưa Giảng viên, điểm độc đáo nhất của dự án bên em là thay vì dùng biểu đồ Excel tĩnh, nhóm đã nhúng thẳng AI Computer Vision (Mediapipe của Google) để biến cơ thể người thuyết trình thành 'biến số kinh tế' tương tác Real-time.*
> 
> *Khi lên thuyết trình, nếu em làm cử chỉ tay **Vuốt ngang**, nó mô phỏng việc nhà Tư bản ép tăng cường độ lao động, thầy cô có thể thấy ngay trên màn hình lượng Giá trị thặng dư (m) nhảy vọt mạnh, nhưng lập tức chỉ số Công bằng phúc lợi bị báo động.*
> 
> *Ngược lại, nếu em giơ **cử chỉ OK**, nó đại diện cho việc nhà nước ra sắc lệnh 'Đầu tư đào tạo nâng cao kỹ năng (Upskilling)' cho gen Z. Ở trạng thái này, chất xám (v) tăng, hệ thống lập tức trung hòa đi tỷ lệ thất nghiệp do AI gây ra.*
> 
> *Và cuối cùng thao tác đổi **Tay Nắm đấm** hội tụ khối hạt 3D thành biểu tượng 'Robot và Người lao động' là thông điệp nhấn mạnh biện chứng cốt lõi của bài học: AI chỉ tác động như hằng số (c), nguồn gốc sinh lời đích thực vẫn là sinh lực của con người (v). Thông qua tương tác trực quan này, nhóm muốn bám sát khẩu quyết triết học: 'Thực tiễn là tiêu chuẩn cao nhất của chân lý'."*
