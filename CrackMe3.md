**CrackMe 3**

- Đến vị trí có thông báo đầu tiên để tắt nó

![](images/CrackMe2.1.png)

- Ở dòng 00401029 có 1 lệnh jump dựa theo việc so sánh ở dòng 0040101D để hiện messagebox ở dòng 00401039.
Ta chỉ cần sửa jne thành je để bypass box đầu.

![](images/CrackMe2.2.png)
 
- Sau khi đổi thì sẽ bỏ qua thông báo đầu tiên như dưới

![](images/CrackMe2.3.png)

- Mở file vừa patch để tiếp tục loại bỏ bước tiếp
![](images/CrackMe2.4.png)
- Tìm đến vị trí giữa MessageBoxA và PostQuitMessage (là vùng để hiện dialog 2), ta cần jump đến vị trí đó, và ta cần tự tạo lệnh jump command(do không có sẵn). Ta cần sửa dòng 0040110D thành push 0x401121

![](images/CrackMe2.5.png)
 
patch file và ta đã pass được box 2.

![](images/CrackMe2.6.png)
  
- Tìm đến vị trí hiện REGISTERED ta thấy dòng 004010D8 có lệnh je dựa trên lệnh compare eax ngay trên. Ta sửa thành jne để nó không jump xuống dòng unregistered.
 
![](images/CrackMe2.7.png)
