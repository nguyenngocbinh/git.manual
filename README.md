

# Giới thiệu Git

- Git dùng để quản lý phiên bản code (tương tự như __track changes__ trong MS word);
  
- Git có nhiều trang hỗ trợ như: github.com, bitbucket.com, ... không phải git là chỉ riêng trang github, git giống như là 1 chuẩn quản lý phiên bản, ngoài ra còn có SVN là 1 chuẩn khác để quản lý phiên bản.
        
# Các khái niệm trong git

- Repository (Kho): là thư mục. Thư mục trên github.com gọi là remote repository, còn ở máy tính là local repository.

- Branch (nhánh): ví dụ mình làm 1 phần trên 1 nhánh, mình rẽ sang nhánh khác làm chức năng khác, sau này hộp lại (merge)

- Remote (máy chủ): Nơi lưu tất cả các phiên bản
 
- add: sau khi làm gì đó thay đổi thì add (thêm) cái thay đổi đó vào
    
- commit: chốt thay đổi
    
- pull (kéo về): lấy code của thằng làm chung đã push (đẩy) lên.

  - Pull từ branch nào về branch hiện tại cũng được, nếu pull từ branch khác thì sẽ có "Merge" xảy ra, còn pull từ cùng branch thì là như update code base.
Khi mình làm thay đổi dưới local trùng với chỗ người nào đó đã sửa và push lên (nhưng mình chưa pull về trước đó), thì khi pull về sẽ có "conflict". 

  - "Conflict" nghĩa là "đụng độ". Khi code pull về bị conflict, cần phải "Resolve conflict" bằng cách chọn thay đổi nào được giữ lại và thay đổi nào sẽ xóa đi hoặc giữ lại cả 2 và chỉnh sữa cho tụi nó hoạt động.
    
- push: đưa code lên remote repository, nghĩa là đẩy lên cho người khác kéo về
    
- Collaborators: làm việc nhóm với git:

  + Ai tạo repos thì vào đây: https://github.com/<tên_tài_khoản>/<tên_repos>/settings/collaboration
 
  + gõ email github thành viên vào, thằng được mời làm chung đồng ý thì làm thôi.
      
# Ví dụ

+ Tải git về cài vào máy: https://git-scm.com/

+ Tiếp là phải tạo 1 remote repository (thư mục trên github.com) đó là chỗ lúc push code sẽ lên, repository đó có 1 đừng dẫn, đuôi là *.git.
ví du: https://github.com/nguyenngocbinh/git.manual.git. Việc tạo này phải tạo trên trang github.com, lên đó tìm nút tạo ("New repository").

+ Tạo 1 thư mục để chứa code dưới máy tính. Thư mục này sẽ liên kết với cái thư mục trên github sau này (làm theo các bước dưới)

+ Khởi tạo git trong thư mục mới tạo: Bấm chuột phải chọn "Git bash here" để mở màn hình console. Gõ: __git init__

+ Liên kết nó với thư mục ở github.com: cũng ở màn hình consolde mới mở lên, gõ: git remote add origin <đường dẫn tới thư mục trên github.com>
ví dụ: __git remote add origin__ https://github.com/nguyenngocbinh/git.manual

+ Sau khi liên kết 2 thư mục, lấy hết nội dung trên thư mục ở github về, trên console, gõ: __git pull origin master__

+ xong, đã lấy hết nội dung thư mục trên github về.

+ Khi làm gì đó thay đổi trên thư mục ở máy nhà, phải _ADD_ sau đó _COMMIT_ sau đó _PUSH_ lên github. Làm như sau:

  - ADD: mở git bash (màn hình console) lên, gõ: __git add__ *

  - COMMIT: cũng trên bash, gõ: git commit -m "nội dụng đã thực hiện" trong đó cái trong dấu ngoặc kép là ghi chú của việc commit, cái này bắt buộc nhập

  - PUSH: cũng trên bash, gõ: __git push origin master__
    
+ Khi ai đó push gì mới lên thì ở máy lấy về bằng cách: gõ trên bash tại thư mục đã khởi tạo git (git init): __git pull origin master__

+ Hết, luyện tập bằng cách tạo 1 repo trống trên github cá nhân.
    
# Git GUI
    
Git GUI cho phép dùng git với giao diện, trực quan, bấm nút khỏi gõ lệnh.

  + SourceTree: miễn phí và lợi hại: https://www.sourcetreeapp.com

  + ToroiseGit: cũng miễn phí, ai dùng svn quen thì TortoiseGit thôi: https://tortoisegit.org/
   
  + "Integrated Source Controll" của IDE: là trình quản lý git có sẵn trong mấy IDE ví dụ như VSCode, Visual Studio... cũng tiện và lợi hại không kém.
        
