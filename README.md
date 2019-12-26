## Một số config hữu ích cho git ở local
Đầu tiên mở file config git trên terminal:
```
git config -e --global
```
Thêm những phần sau vào file config:
- Thông tin cá nhân
```
[user]
      name    =
      email   =
```
- Lưu tài khoản(bỏ qua phần đăng nhập khi push)
```
[credential]
      helper  = store
```
- Đặt nhánh hiện tại làm nhánh push(không cần khai báo nhánh khi push)
```
[push]
      default = current
```
- Thêm một số lệnh cho git
  ```
  [alias]
  ```
  - Hiển thị trạng thái
  ```
      stt     =  status --short --branch
  ```
  - Thao tác với commit
  ```
      ci      =  commit
  ```
  - Chuyển nhánh
  ```
      co      =  checkout
  ```
  - Thao tác với nhánh
  ```
      br      =  branch
  ```
  - Bỏ đánh dấu file(stage)
  ```
      unstage =  reset HEAD --
  ```
  - Xem commit cuối cùng
  ```
      last    =  log -1 HEAD
  ```
  - So sánh khác nhau
  ```
      di      =  diff
  ```
  - Xem log
  ```
      ll      = log --pretty=format:"%C(yellow)%h%Cred%d\\ %Creset%s%Cblue\\ $
      ld      = log --pretty=format:"%C(yellow)%h\\ %C(green)%ad%Cred%d\\ %Cr$
      ls      = log --pretty=format:"%C(green)%h\\ %C(yellow)[%ad]%Cred%d\\ %$
  ```
  - *Xóa nhánh đã được merge vào nhánh hiện tại*
  ```
      cleanup = "!git branch --merged | grep  -v '\\*\\|master\\|develop' | x$
  ```
