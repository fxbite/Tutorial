<div align="center">
    <img src="./img/git2.png" alt="github">
    <h2>Vai trò của Git và Github đối với một developer.<br>Hướng dẫn cách sử dụng Git và Github.
    </h2>
    <p>
        <a href="https://www.facebook.com/HELLOGIT_UoG-Information-Technology-Club-102617695289423"><img src="https://img.shields.io/badge/Facebook-Join%20now-orange?style=flat&logo=facebook" alt="Facebook"></a>
        <a href="#"><img src="https://img.shields.io/badge/Copyright-Hello%20GIT-green?style=flat" alt="Discord"></a>
        <a href="#"><img src="https://img.shields.io/badge/Release-May%2015th%2C%202021-blue?style=flat"></a>
    </p>
</div>

<h2 id="content">Table of content</h2>
<ul>
<li><a href="#1">Git là gì?</a>
<li><a href="#2">Version Control System – VCS là gì?</a>
<li><a href="#3">Git có lợi ích gì?</a>
<li><a href="#a">Github là gì?</a>
<li><a href="#b">Tính năng của Github</a>
</ul>

<details>
<summary><a href="#c">Lợi ích chính của Github đối với lập trình viên</a></summary>
<ul>
<li><a href="#d">1. Quản lý source code dễ dàng</a>
<li><a href="#c">2. Tracking sự thay đổi qua các version</a>
<li><a href="#e">3. Markdown</a>
</details>

<details>
<summary><a href="#4">Các thuật ngữ Git quan trọng</a></summary>
<ul>
<li><a href="#5">1. Branch</a>
<li><a href="#6">2. Commit</a>
<li><a href="#7">3. Checkout</a>
<li><a href="#8">4. Fetch</a>
<li><a href="#9">5. Fork</a>
<li><a href="#10">6. Head</a>
<li><a href="#11">7. Index</a>
<li><a href="#12">8. Master</a>
<li><a href="#13">9. Merge</a>
<li><a href="#14">10. Origin</a>
<li><a href="#15">11. Pull</a>
<li><a href="#16">12. Push</a>
<li><a href="#17">13. Rebase</a>
<li><a href="#18">14. Remote</a>
<li><a href="#19">15. Repository</a>
<li><a href="#20">16. Stash</a>
<li><a href="#21">17. Tags</a>
<li><a href="#22">18. Upstream</a>
</ul>

</details>
<details>
<summary><a href="#23">Các lệnh git cơ bản</a></summary>
<ul>
<li><a href="#24">a. git config</a>
<li><a href="#25">b. git init</a>
<li><a href="#26">c. git clone</a>
<li><a href="#27">d. git status</a>
<li><a href="#28">e. git add</a>
<li><a href="#29">f. git remote</a>
<li><a href="#30">g. git commit</a>
<li><a href="#31">h. git push/git pull</a>
<li><a href="#32">i. git branch</a>
<li><a href="#33">k. git checkout</a>
<li><a href="#34">m. git stash</a>
<li><a href="#35">n. git merge</a>
<li><a href="#36">o. git reset</a>
<li><a href="#37">Note</a>
</ul>

</details>
<details>
<summary><a href="#38">Lời khuyên khi thao tác thường xuyên với Git trong công việc</a></summary> 
<ul>
<li><a href="#39">1. Git Cheet Sheets</a>
<li><a href="#40">2. Nên commit thương xuyên</a>
<li><a href="#41">3. Test rồi mới commit</a>
<li><a href="#42">4. Viết ghi chú khi commit</a>
<li><a href="#43">5. Thử nghiệm Branch khác</a>
<li><a href="#44">6. Theo một Git Workflow</a>
</ul>
</details>

<ul>
<li><a href="#45">Reference</a>
<li><a href="#46">Copyright</a>
</ul> 

<h2 id="1">Git là gì?</h2>
<p style="margin-bottom: 45px"><code>Git</code> là một hệ thống quản lý phiên bản phân tán <strong>(Distributed Version Control System – DVCS)</strong>, nó là một trong những hệ thống quản lý phiên bản phân tán phổ biến nhất hiện nay. <strong>Git</strong> cung cấp cho mỗi lập trình viên kho lưu trữ (<strong>repository</strong>) riêng chứa toàn bộ lịch sử thay đổi.
</p>

<p align="right">
<a href="#content" ><img src="https://img.shields.io/badge/Back%20to%20top-Click%20me-orange?style=flat-square" ></a>
</p>

<h2 id="2">Version Control System – VCS là gì?</h2>
<p>VCS là viết tắt của <strong>Version Control System</strong> là <strong>hệ thống kiểm soát các phiên bản phân tán mã nguồn mở</strong>. Các VCS sẽ lưu trữ tất cả các file trong toàn bộ dự án và ghi lại toàn bộ lịch sử thay đổi của file. Mỗi sự thay đổi được lưu lại sẽ được và thành một version (phiên bản).

VCS nghĩa là hệ thống giúp lập trình viên có thể lưu trữ nhiều phiên bản khác nhau của một mã nguồn được nhân bản (<strong>clone</strong>) từ một kho chứa mã nguồn (<strong>repository</strong>), mỗi thay đổi vào mã nguồn trên local sẽ có thể ủy thác (<strong>commit</strong>) rồi đưa lên server nơi đặt kho chứa chính.</p>
<div align="center">
    <img src="./img/git1.png" style="height: 400px">
</div>
<p>Và một máy tính khác nếu họ có quyền truy cập cũng có thể clone lại mã nguồn từ kho chứa hoặc clone lại một tập hợp các thay đổi mới nhất trên máy tính kia.

Lập trình viên có thể xem lại danh sách các sự thay đổi của file như xem một dòng thời gian của các phiên bản. Mỗi phiên bản bao gồm: nội dung file bị thay đổi, ngày giờ sửa đổi, người thay đổi là ai, lý do thay đổi hay tên phiên bản…
</p>

<p align="right">
<a href="#content" ><img src="https://img.shields.io/badge/Back%20to%20top-Click%20me-orange?style=flat-square" ></a>
</p>

<h2 id ="3" style="margin-top: 45px">Git có lợi ích gì?</h2>
<p>Các dự án thực tế thường có nhiều lập trình viên làm việc song song. Vì vậy, một hệ thống kiểm soát phiên bản như Git là cần thiết để đảm bảo không có xung đột code giữa các lập trình viên.

Ngoài ra, các yêu cầu trong các dự án như vậy thay đổi thường xuyên. Vì vậy, một hệ thống kiểm soát phiên bản cho phép các nhà phát triển revert và quay lại phiên bản cũ hơn của code.

Cuối cùng, đôi khi một số dự án đang được chạy song song liên quan đến cùng một cơ sở code. Trong trường hợp như vậy, khái niệm phân nhánh trong Git là rất quan trọng.
<ul>
<li>Dễ sử dụng, thao tác nhanh, gọn, lẹ và rất an toàn.
<li>Sẽ dàng kết hợp các phân nhánh (branch), có thể giúp quy trình làm việc code theo nhóm đơn giản hơn rất nhiều.
<li>Chỉ cần clone mã nguồn từ kho chứa hoặc clone một phiên bản thay đổi nào đó từ kho chứa, hoặc một nhánh nào đó từ kho chứa là bạn có thể làm việc ở mọi lúc mọi nơi.
<li>Deployment sản phẩm của bạn một cách không thể nào dễ dàng hơn.
</ul>
</p>

<p align="right">
<a href="#content" ><img src="https://img.shields.io/badge/Back%20to%20top-Click%20me-orange?style=flat-square" ></a>
</p>

<h2 id="a" style="margin-top: 45px">Github là gì?</h2>
<p> 
<a href="https://github.com/" style="color: red">GitHub</a> là một dịch vụ nổi tiếng cung cấp kho lưu trữ mã nguồn <a href="https://git-scm.com/" style="color:red">Git</a> cho các dự án phần mềm. <strong>Github có đầy đủ những tính năng của Git</strong>, ngoài ra nó còn bổ sung những tính năng về social để các developer tương tác với nhau.
</p>

<p align="right">
<a href="#content" ><img src="https://img.shields.io/badge/Back%20to%20top-Click%20me-orange?style=flat-square" ></a>
</p>

<h2 id="b" style="margin-top: 45px">Tính năng của Github</h2>
<p><strong>GitHub</strong> được coi là một mạng xã hội dành cho lập trình viên lớn nhất và dễ dùng nhất với các tính năng cốt lõi như:

<ol>
<li>Wiki, issue, thống kê, đổi tên project, project được đặt vào namespace là user.
<li>Watch project: theo dõi hoạt động của project của người khác. Xem quá trình người ta phát triển phầm mềm thế nào, project phát triển ra sao.
<li>Follow user: theo dõi hoạt động của người khác.<br>
</ol>

Có 2 cách tiếp cận GitHub: Tạo project của riêng mình Contribute cho project có sẵn: fork project có sẵn của người khác, sửa đổi, sau đó đề nghị họ cập nhật sửa đổi của mình (tạo pull request).
</p>

<p align="right">
<a href="#content" ><img src="https://img.shields.io/badge/Back%20to%20top-Click%20me-orange?style=flat-square" ></a>
</p>

<h2 id="c" style="margin-top: 45px">Lợi ích chính của Github đối với lập trình viên</h2>
<h3 id="d" style="margin-top: 40px">1. Quản lý source code dễ dàng</h3>
<p>
Khi bạn tạo một repo, toàn bộ source code của repo đó được lưu trên GitHub. Tại đây, bạn có thể coi lại quá trình mình đã làm việc thông qua các comment sau mỗi lần commit. Và cái hay ở đây, là nhiều người có thể cùng làm một repo.

Lợi ích đầu tiên, chính là bạn biết được ai đã commit và commit cái gì. Tiếp theo, source của bạn có thể phát triển theo nhiều nhánh. Nguyên tắc làm việc với các nhánh như thế này: Bạn có thể rẽ nhiều nhánh để phát triển project. Nhưng cuối cùng, bạn phải merge lại vào nhánh MASTER để ra được project hoàn chỉnh.
</p>

<h3 id="e" style="margin-top: 40px">2. Tracking sự thay đổi qua các version</h3>
<p>
Khi có nhiều member cùng thực hiện một dự án thì khá là phức tạp để theo dõi revisons – ai thay đổi cái gì, lúc nào và mấy cái files đó được stored ở đâu. Đừng lo vì GitHub đã tính đến chuyện này giúp bạn, bằng cách luôn lưu lại những thay đổi bạn đã push lên repository. Cũng tương tự với Microsoft Word hay Google Drive, bạn có một lịch sử phiên bản để phòng trường hợp các phiên bản trước đó bị mất hay không được lưu.
</p>

<h3 id="f" style="margin-top: 40px">3. Markdown</h3>
<p>
Markdown là một cách định dạng text trên web. Bạn có thể chỉnh sửa cách hiển thị của document, format từ như định dạng in đậm hay in nghiêng, thêm hình và tạo list những thứ bạn có thể làm với Markdown. <br>
Hầu hết, Markdown chỉ là đoạn text đơn thuần với những ký tự đặc biệt chèn vào, như # hay *. Trong GitHub thì bạn có thể sử dụng Mardown ở những nơi: Git, Comments tại Issues và Pull Requests, các file có đuôi .md hay .markdown extension.
</p>
<div align="center">
<img src="./img/repo-browser.png">
</div>

<p align="right">
<a href="#content" ><img src="https://img.shields.io/badge/Back%20to%20top-Click%20me-orange?style=flat-square" ></a>
</p>

<h2 id="4" style="margin-top: 45px">Các thuật ngữ Git quan trọng</h2>
<h3 id="5">1. Branch</h3>
<p>Các <strong>Branch</strong> (nhánh) đại diện cho các <strong>phiên bản cụ thể</strong> của một kho lưu trữ tách ra từ project chính của bạn.

Branch cho phép bạn theo dõi các thay đổi thử nghiệm bạn thực hiện đối với kho lưu trữ và có thể hoàn nguyên về các phiên bản cũ hơn.
</p>

<h3 id="6" style="margin-top: 40px">2. Commit</h3>
<p>Một commit đại diện cho một thời điểm cụ thể trong lịch sử dự án của bạn. Sử dụng lệnh commit kết hợp với lệnh <strong>git add</strong> để cho git biết những thay đổi bạn muốn lưu vào local repository.
</p>

<h3 id="7" style="margin-top: 40px">3. Checkout</h3>
<p>Sử dụng lệnh <code>git checkout</code> để chuyển giữa các branch. Chỉ cần nhập git checkout theo sau là tên của branch bạn muốn chuyển đến hoặc nhập git checkout master để trở về branch chính (master branch).
</p>

<h3 id="8" style="margin-top: 40px">4. Fetch</h3>
<p>Lệnh <code>git fetch</code> tìm nạp các bản sao và tải xuống tất cả các tệp branch vào máy tính của bạn. Sử dụng nó để lưu các thay đổi mới nhất vào kho lưu trữ của bạn. Nó có thể tìm nạp nhiều branch cùng một lúc.
</p>

<h3 id="9" style="margin-top: 40px">5. Fork</h3>
<p>Một fork là một bản sao của một kho lưu trữ (repository). Các lập trình viên thường tận dụng lợi ích của fork để thử nghiệm các thay đổi mà không ảnh hưởng đến dự án chính.
</p>

<h3 id="10"style="margin-top: 40px">6. Head</h3>
<p>Các commit ở đầu của một branch được gọi là head. Nó đại diện cho commit mới nhất của repository mà bạn hiện đang làm việc.
</p>

<h3 id="11" style="margin-top: 40px">7. Index</h3>
<p>Bất cứ khi nào bạn thêm, xóa hoặc thay đổi một file, nó vẫn nằm trong chỉ mục cho đến khi bạn sẵn sàng commit các thay đổi. Nó như là khu vực tổ chức (stagging area) cho Git. Sử dụng lệnh <code>git status</code> để xem nội dung của index của bạn.

Những thay đổi được tô sáng bằng màu xanh lá cây đã sẵn sàng để được commit trong khi những thay đổi màu đỏ thì chưa.
</p>

<h3 id="12"style="margin-top: 40px">8. Master</h3>
<p>Master là nhánh chính của tất cả các repository của bạn. Nó nên bao gồm những thay đổi và commit gần đây nhất.
</p>
<div align="center">
<img src="./img/branch.jpg" alt="branch">
</div>

<h3 id="13" style="margin-top: 40px">9. Merge</h3>
<p>Lệnh <code>git merge</code> kết hợp với các yêu cầu kéo (pull requests) để thêm các thay đổi từ nhánh này sang nhánh khác.
</p>

<h3 id="14" style="margin-top: 40px">10. Origin</h3>
<div align="center">
<img src="./img/origin-git.jpg">
</div>
<p>Origin là phiên bản mặc định của repository. Origin cũng đóng vai trò là bí danh hệ thống để liên lạc với nhánh chính.

Lệnh <code>git push origin master</code> để đẩy các thay đổi cục bộ đến nhánh chính.
</p>

<h3 id="15" style="margin-top: 40px">11. Pull</h3>
<p>Pull requests thể hiện các đề xuất thay đổi cho nhánh chính. Nếu bạn làm việc với một nhóm, bạn có thể tạo các pull request để yêu cầu người bảo trì kho lưu trữ xem xét các thay đổi và hợp nhất chúng.

Lệnh <code>git pull</code> được sử dụng để thêm các thay đổi vào nhánh chính.
</p>

<h3 id="16" style="margin-top: 40px">12. Push</h3>
<p>Lệnh <code>git push</code> được sử dụng để cập nhật các nhánh từ xa với những thay đổi mới nhất mà bạn đã <code>commit</code>.
</p>

<h3 id="17" style="margin-top: 40px">13. Rebase</h3>
<p>Lệnh <code>git rebase</code> cho phép bạn phân tách, di chuyển hoặc thoát khỏi các commit. Nó cũng có thể được sử dụng để kết hợp hai nhánh khác nhau.
</p>

<h3 id="18" style="margin-top: 40px">14. Remote</h3>
<p>Một Remote (kho lưu trữ từ xa) là một bản sao của một chi nhánh. Remote giao tiếp ngược dòng với nhánh gốc (origin branch) của chúng và các Remote khác trong kho lưu trữ.
</p>

<h3 id="19" style="margin-top: 40px">15. Repository</h3>
<p>Kho lưu trữ Git chứa tất cả các tệp dự án của bạn bao gồm các branch, tags và commit.
</p>

<h3 id="20" style="margin-top: 40px">16. Stash</h3>
<p>Lệnh git stash sẽ loại bỏ các thay đổi khỏi chỉ mục của bạn và xóa stashes chúng đi sau.

Nó có ích nếu bạn muốn tạm dừng những gì bạn đang làm và làm việc khác trong một khoảng thời gian. Bạn không thể đặt stash nhiều hơn một bộ thay đổi ở cùng một thời điểm.
</p>

<h3 id="21" style="margin-top: 40px">17. Tags</h3>
<p>Tags cung cấp cho bạn một cách để theo dõi các commit quan trọng. Các tags nhẹ chỉ đơn giản đóng vai trò là con trỏ trong khi các tags chú thích được lưu trữ dưới dạng các đối tượng đầy đủ.
</p>

<h3 id="22" style="margin-top: 40px">18. Upstream</h3>
<p>Trong ngữ cảnh của Git, upstream đề cập đến nơi bạn push các thay đổi của mình, thường là nhánh chính (master branch).

Xem <a href="https://git-scm.com/docs" style="color: red">Git docs reference</a> để biết thêm chi tiết về thuật ngữ liên quan đến Git.
</p>

<p align="right">
<a href="#content" ><img src="https://img.shields.io/badge/Back%20to%20top-Click%20me-orange?style=flat-square" ></a>
</p>

<h2 id="23" style="margin-top: 45px">* Các lệnh git cơ bản</h2>
<h3 id="24">a. git config</h3>
Tác dụng : Để set user name và email của bạn trong main configuration file.

Cách xài : Để kiểm tra tên và kiểu email trong cấu hình dùng.<br>
`$ git config -- global user.name`<br>
`$ git config -- global user.email`

Để set email hoặc tên mới.<br>
`$ git config -- global user.name = "Merlin"`<br>
`$ git config --global user.email merlin@example.com`

<h3 id="25" style="margin-top: 40px">b. git init</h3>
Tác dụng : Khởi tạo 1 git repository 1 project mới hoặc đã có.

Cách xài: Trong thư mục gốc của dự án, bạn có thể dùng terminal trong editor hoặc cmd tại thư mục gốc và gõ lệnh `$ git init`.

<h3 id="26" style="margin-top: 40px">c. git clone</h3>
Tác dụng: Copy 1 git repository từ remote source.

Cách xài: Bạn copy url một repository từ github (nhiều nền tảng khác) và dùng lệnh.<br> 
<div align="center">
<img src="./img/git-clone2.png">
</div>

`$ git clone <url>`<br>
`$ git clone https://github.com/fxbite/Tutorial.git`

<h3 id="27" style="margin-top: 40px">d. git status</h3>
Tác dụng: Để check trạng thái của những file bạn đã thay đổi trong thư mục làm việc. VD: Tất cả các thay đổi cuối cùng từ lần commit cuối cùng.

Cách xài : Dùng lệnh <code>$ git status</code> trong thư mục làm việc.

<h3 id="28" style="margin-top: 40px">e. git add</h3>
Tác dụng: Thêm thay đổi đến stage/index trong thư mục làm việc.

Cách xài: Mình sẽ dùng lệnh <code>git add</code> để <strong>add</strong> những tập tin (source code) <br>
`$ git add .` <br>
- Lệnh <code>git add .</code> trên thường xuyên được dùng. <br>
- Dấu " . " ở đây là "chọn tất cả tập tin" hoặc bạn có thể add "<strong>single file</strong>".

`$ git add index.html`

<h3 id="29" style="margin-top: 40px">f. git remote</h3>
Tác dụng: Để check remote/source bạn có hoặc add thêm remote

Cách dùng: `$ git remote` để kiểm tra và liệt kê. Và `git remote add <: remote_url:>` để thêm.<br>

VD: `$ git remote add github git@github.com:fxbite/Tutorial.git`
- **github** là tên đặt cho remote. (đặt tên gì cũng được, để dễ thao tác và dễ nhớ)
- **github git@github.com:fxbite/Tutorial.git** là url theo dạng SSH. (Trong các nền tảng, github hay gitlab...sẽ có 2 dạng url cho 1 repo là **HTTPS** và **SSH**). <br>
Trong lập việc thực tế, thì dùng SSH sẽ tiện lợi nhất, chỉ cần configue 1 lần là dùng lệnh `$ git pull` hoặc `$ git push` dễ dàng. <br>
=> **URL SSH chuyên dùng để tải code lên github**.<br>
Còn HTTPS, nếu dùng tải source code lên github bằng `$ git push` hay `$ git pull` thì phải đăng nhập rất mất thời gian. <br>
=> **URL HTTPS dùng để chia sẻ public repository cho người khác**.

<h3 id="30" style="margin-top: 40px">g. git commit</h3>
Tác dụng: commit nghĩa là một action để Git lưu lại một snapshot của các sự thay đổi trong thư mục làm việc. Và các tập tin, thư mục được thay đổi đã phải nằm trong Staging Area. Mỗi lần commit nó sẽ được lưu lại lịch sử chỉnh sửa của code kèm theo tên và địa chỉ email của người commit. Ngoài ra trong Git bạn cũng có thể khôi phục lại tập tin trong lịch sử commit của nó để chia cho một branch khác, vì vậy bạn sẽ dễ dàng khôi phục lại các thay đổi trước đó.

Cách dùng : <code>git commit -m "Đây là message, bạn dùng để note những thay đổi để sau này dễ dò lại"</code>

<h3 id="31" style="margin-top: 40px">h. git push/git pull</h3>
Tác dụng: Push hoặc Pull các thay đổi đến remote. Nếu bạn đã added và committed các thay đổi và bạn muốn đẩy nó lên hoặc remote của bạn đã update và bạn apply tất cả thay đổi đó trên code của mình.

Cách dùng : <code>git pull <:remote:> <:branch:></code> và <code>git push <:remote:> <:branch:></code> <br>

VD: `$ git pull github main` <br>
- **github** là tên remote đã đặt bằng `$ git remote`. <br>
- **main** là tên branch.

`$ git push -u github main` <br>

<h3 id="32" style="margin-top: 40px">i. git branch</h3>
Tác dụng: liệt kê tất cả các branch (nhánh).

Cách dùng: `$ git branch` hoặc `$ git branch -a` <br>

Ngoài ra, có thể dùng để đặt tạo một branch mới.
VD: `$ git branch version 1` 

<h3 id="33" style="margin-top: 40px">k. git checkout</h3>
Tác dụng: Chuyển sang branch khác

Cách dùng: `$ git checkout <: branch:>` hoặc `$ git checkout -b <: branch:>` nếu bạn muốn tạo và chuyển sang một chi nhánh mới.

VD: `$ git checkout version1`

<h3 id="34" style="margin-top: 40px">m. git stash</h3>
Tác dụng: Lưu thay đổi mà bạn không muốn commit ngay lập tức.

Cách dùng: `$ git stash` trong thư mục làm việc của bạn. 

<h3 id="35" style="margin-top: 40px">n. git merge</h3>
Tác dụng: Merge 2 branch lại với nahu.

Cách dùng: Chuyển tới branch bạn muốn merge rồi  dùng `$ git merge <:branch_ban_muon_merge:>`

<h3 id="36" style="margin-top: 40px">o. git reset</h3>
Tác dụng: Bạn đã đưa một tập tin nào đó vào Staging Area nhưng bây giờ bạn muốn loại bỏ nó ra khỏi đây để không phải bị commit theo.

Cách dùng: `$ git reset HEAD tên_file`

<h3 id="37" style="margin-top: 40px">* Note:</h3>
- Các lệnh git hay gặp trong project (từ a. đến k. trong các lệnh git cơ bản) <br>
- Các lệnh git khác có thể nghiên cứu thêm ở bên ngoài. (thông qua <strong>google</strong> hoặc <strong>youtube</strong>) <br>
- Ngoài ra, nghiên cứu các các nền tảng như <a href="https://github.com/"><strong>github</strong></a> hoặc <a href="https://about.gitlab.com/"><strong>gitlab</strong></a>...

<p style="margin-top: 40px" align="right">
<a href="#content" ><img src="https://img.shields.io/badge/Back%20to%20top-Click%20me-orange?style=flat-square" ></a>
</p>

<h2 id="38" style="margin-top: 45px">Lời khuyên khi thao tác thường xuyên với Git trong công việc</h2>
<h3 id="39">1. Git Cheet Sheets</h3>
Bạn không thể nào nhớ được hết các lệnh, lúc này bạn nên sử dụng các Git Cheet Sheets để dễ dàng tìm được lệnh Git bạn cần: <br><br>

- https://rogerdudler.github.io/git-guide/
- https://git-scm.com/docs/gittutorial
- https://gitsheet.wtf/
- http://ndpsoftware.com/git-cheatsheet.html
- https://gitexplorer.com/

<h3 id="40" style="margin-top: 40px">2. Nên commit thương xuyên</h3>
<p>Tách nhỏ commit của bạn và commit thường xuyên nhất có thể. Điều này giúp các thành viên trong nhóm dễ dàng tích hợp công việc của họ hơn mà không gặp phải xung đột hợp nhất.
</p>

<h3 id="41" style="margin-top: 40px">3. Test rồi mới commit</h3>
<p>Không bao giờ commit nếu chưa hoàn tất process. Cần phải test các thay đổi của bạn trước khi chia sẻ chúng với người khác.
</p>

<h3 id="42" style="margin-top: 40px">4. Viết ghi chú khi commit</h3>
<p>Viết ghi chú khi commit để cho các thành viên khác trong nhóm biết loại thay đổi bạn đã thực hiện. Hãy mô tả càng nhiều càng tốt.
</p>

<h3 id="43" style="margin-top: 40px">5. Thử nghiệm Branch khác</h3>
<p>Tận dụng lợi thế của các branch để giúp bạn theo dõi các dòng phát triển khác nhau.
</p>

<h3 id="44" style="margin-top: 40px">6. Theo một Git Workflow</h3>
<p>Bạn nên chọn theo một Git Workflow để đảm bảo cả nhóm của bạn đều cùng thực hiện như nhau.
</p>
<div align="center">
<img src="./img/git-workflow.jpg">
</div>

<p align="right">
<a href="#content" ><img src="https://img.shields.io/badge/Back%20to%20top-Click%20me-orange?style=flat-square" ></a>
</p>

<h2 id="45" style="margin-top: 45px">Reference</h2>
<p><ul>
<li> topdev.vn, 2021. Git là gì? Các lệnh git cơ bản mà mọi lập trình viên nên biết | TopDev. [online] TopDev. Available at: 
<a href="https://topdev.vn/blog/git-la-gi/">https://topdev.vn/blog/git-la-gi/</a> [Accessed 17 May 2021].

<li>topdev.vn, 2021. GitHub là gì? Những lợi ích GitHub mang lại cho lập trình viên | TopDev. [online] TopDev. Available at: <a href="https://topdev.vn/blog/github-la-gi/">https://topdev.vn/blog/github-la-gi/</a> [Accessed 17 May 2021].
</ul>
</p>

<h2 id="46" style="margin-top: 45px">Copyright</h2>

© 2021 Hello GIT, Team
