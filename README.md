<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript và CSS</title>
    <style>
        #NoiDung {
            width: 100%;
            height: 100px;
            border: 1px solid black;
            margin-top: 10px;
            font-size: 16px;
        }
    </style>
</head>
<body>
    <h1>JAVASCRIPT và CSS</h1>
    <button onclick="doiMau('green')">Xanh</button>
    <button onclick="doiMau('red')">Đỏ</button>
    <button onclick="doiMau('yellow')">Vàng</button>
    <button onclick="doiMau('')">Không màu</button>
    
    <select id="fontSizeSelect" onchange="thayDoiKichThuocChu()">
        <option value="20px">20px</option>
        <option value="25px">25px</option>
        <option value="30px">30px</option>
    </select>
    <button onclick="thayDoiKichThuocChu()">Đặt cỡ chữ</button>
    
    <select id="heightSelect" onchange="thayDoiChieuCao()">
        <option value="100px">100px</option>
        <option value="150px">150px</option>
        <option value="200px">200px</option>
    </select>
    <button onclick="thayDoiChieuCao()">Đặt chiều cao</button>
    <button onclick="tangChieuCao()">Tăng chiều cao</button>
    
    <button onclick="napCSSTieuDe()">Nạp css tiêu đề</button>
    <button onclick="napCSSNoiDung()">Nạp css nội dung</button>

    <textarea id="NoiDung">Xin chào các bạn!</textarea>

    <script>function doiMau(mau) {
        document.getElementById("NoiDung").style.backgroundColor = mau;
    }
    
    // Thay đổi kích thước chữ của text area
    function thayDoiKichThuocChu() {
        var size = document.getElementById("fontSizeSelect").value;
        document.getElementById("NoiDung").style.fontSize = size;
    }
    
    // Thay đổi chiều cao của text area
    function thayDoiChieuCao() {
        var height = document.getElementById("heightSelect").value;
        document.getElementById("NoiDung").style.height = height;
    }
    
    // Tăng chiều cao của text area
    function tangChieuCao() {
        var noiDung = document.getElementById("NoiDung");
        var currentHeight = window.getComputedStyle(noiDung).height;
        noiDung.style.height = (parseInt(currentHeight) + 20) + "px";
    }
    
    // Nạp CSS tiêu đề
    function napCSSTieuDe() {
        document.querySelector('h1').style.color = 'blue';
        document.querySelector('h1').style.fontSize = '30px';
    }
    
    // Nạp CSS nội dung
    function napCSSNoiDung() {
        var noiDung = document.getElementById("NoiDung");
        noiDung.style.color = 'green';
        noiDung.style.fontWeight = 'bold';
        noiDung.style.border = '2px solid blue';
    }</script>
</body>
</html>
