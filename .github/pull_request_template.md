Git, Github


Cheat sheet: https://quickref.me/git


B1: Tạo repo trên Github(có file Readme.md nội dung bất kỳ)


B2: Clone repo về máy
    git clone …


B3: Tạo folder `.github` bên trong có file `pull_request_template.md` lấy ở Guidelines 
    Và thay đổi nội dung file Readme.md
    Name: 
    Age:
    Position:


B4: Add các thay đổi vào staging 
    git add .


B5: Tạo commit
    git commit -m '...'


B6: Push code lên repo trên Github
    git push origin main

B7: Từ main tạo và checkout 2 nhánh mới có tên là `update/your-name/yyyymmdd/info-1` và `update/your-name/yyyymmdd/info-2`
    git branch update/your-name/yyyymmdd/info-1
    git branch update/your-name/yyyymmdd/info-2


B8: Checkout qua branch `update/your-name/yyyymmdd/info-1`
    git checkout update/your-name/yyyymmdd/info-1
    
    Thay đổi name push các thay đổi lên Github như B4,5,6 tạo PR theo template sẵn có title của PR là [Update] Info 1, để base branch là main
    Làm tương tự với `update/your-name/yyyymmdd/info-2` lưu ý name ở `info-2` phải khác `info-1`
    Check trạng thái của 2 PR lúc này sẽ là ko conflict và có thể merge và base branch


B9: Merge PR `[Update] Info 2`
    gVào PR `[Update] Info 1` trạng thái bây giờ sẽ là conflict và không thể merge(tiến hành fix conflict)


B10: Ở trên máy checkout qua `main` và pull code mới nhất về
     git checkout main
     git pull hoặc git pull origin main


B11: Checkout qua `update/your-name/yyyymmdd/info-1`
     git checkout update/your-name/yyyymmdd/info-1


     Tiến hành merge code từ main và fix conflict
     git merge main


     Vào file bị conflict chọn keep `current`,`incoming`,`both` changes tuỳ theo muốn giữ phần code nào
     Sau khi fix conflict làm tương tự B4, 5, 6
     Lên Github kiểm tra lại trạng thái PR `info-1` bây giờ chuyển thành ko conflict và có thể merge và base branch
     Merge PR


B12: Trên máy checkout về main và pull code mới nhất như B10



