
<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>VTC1 - Tuyển dụng nhân lực</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

body {
    background: #f4f7fb;
    color: #263445;
}

header {
    background: #102d50;
    color: white;
    padding: 20px 7%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 15px;
}

.logo {
    font-size: 30px;
    font-weight: bold;
    color: #ff4545;
}

.logo span {
    color: white;
}

nav a {
    color: white;
    text-decoration: none;
    margin-left: 22px;
}

nav a:hover {
    color: #ff4545;
}

.hero {
    background: linear-gradient(120deg,#102d50,#2464a0);
    color: white;
    padding: 75px 20px;
    text-align: center;
}

.hero h1 {
    font-size: 38px;
    margin-bottom: 15px;
}

.hero p {
    margin-bottom: 30px;
}

.search-box {
    max-width: 850px;
    margin: auto;
    background: white;
    padding: 15px;
    border-radius: 10px;
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
}

.search-box input,
.search-box select {
    flex: 1;
    min-width: 180px;
    padding: 14px;
    border: 1px solid #ddd;
    border-radius: 5px;
}

button {
    background: #ed3939;
    color: white;
    border: none;
    padding: 14px 22px;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background: #c82323;
}

.container {
    width: 86%;
    max-width: 1200px;
    margin: 45px auto;
}

.section-title {
    text-align: center;
    margin-bottom: 30px;
    color: #102d50;
}

.stats {
    display: grid;
    grid-template-columns: repeat(3,1fr);
    gap: 20px;
    margin-bottom: 50px;
}

.stat-card {
    background: white;
    padding: 25px;
    text-align: center;
    border-radius: 10px;
    box-shadow: 0 3px 12px #0000000c;
}

.stat-card h2 {
    color: #ed3939;
    font-size: 30px;
}

.jobs {
    display: grid;
    grid-template-columns: repeat(2,1fr);
    gap: 20px;
}

.job-card {
    background: white;
    padding: 24px;
    border-radius: 10px;
    box-shadow: 0 3px 12px #0000000c;
    border-left: 4px solid #ed3939;
}

.job-card h3 {
    color: #102d50;
    margin-bottom: 12px;
}

.job-card p {
    margin: 8px 0;
}

.job-card button {
    margin-top: 12px;
}

.form-section {
    background: white;
    padding: 30px;
    border-radius: 10px;
    max-width: 650px;
    margin: 50px auto;
}

.form-section input,
.form-section textarea,
.form-section select {
    width: 100%;
    padding: 13px;
    margin: 10px 0;
    border: 1px solid #ddd;
    border-radius: 5px;
}

footer {
    background: #102d50;
    color: white;
    padding: 35px;
    text-align: center;
    line-height: 2;
}

@media(max-width:700px) {
    .jobs, .stats {
        grid-template-columns: 1fr;
    }

    .hero h1 {
        font-size: 27px;
    }

    nav a {
        margin: 5px;
        display: inline-block;
    }
}
</style>
</head>

<body>

<header>
    <div class="logo">VTC1 <span>NHÂN LỰC</span></div>
    <nav>
        <a href="#home">Trang chủ</a>
        <a href="#jobs">Việc làm</a>
        <a href="#apply">Ứng tuyển</a>
        <a href="#contact">Liên hệ</a>
    </nav>
</header>

<section class="hero" id="home">
    <h1>KẾT NỐI NHÂN TÀI – KIẾN TẠO TƯƠNG LAI</h1>
    <p>VTC1 - Nền tảng tuyển dụng và phát triển nguồn nhân lực</p>

    <div class="search-box">
        <input type="text" id="keyword"
        placeholder="Nhập vị trí công việc...">

        <select id="location">
            <option value="">Tất cả địa điểm</option>
            <option>Hà Nội</option>
            <option>TP. Hồ Chí Minh</option>
            <option>Quảng Ninh</option>
            <option>Đà Nẵng</option>
        </select>

        <button onclick="searchJobs()">Tìm kiếm</button>
    </div>
</section>

<div class="container">

    <h2 class="section-title">VTC1 - CƠ HỘI NGHỀ NGHIỆP</h2>

    <div class="stats">
        <div class="stat-card">
            <h2>500+</h2>
            <p>Việc làm</p>
        </div>

        <div class="stat-card">
            <h2>200+</h2>
            <p>Doanh nghiệp</p>
        </div>

        <div class="stat-card">
            <h2>1000+</h2>
            <p>Ứng viên</p>
        </div>
    </div>

    <h2 class="section-title" id="jobs">
        DANH SÁCH VIỆC LÀM
    </h2>

    <div class="jobs" id="jobList">

        <div class="job-card" data-location="Hà Nội">
            <h3>Nhân viên kinh doanh</h3>
            <p>🏢 Công ty VTC1</p>
            <p>📍 quảng ninh</p>
            <p>💰 10 - 15 triệu/tháng</p>
            <button onclick="applyJob('Nhân viên kinh doanh')">
                Ứng tuyển ngay
            </button>
        </div>

        <div class="job-card" data-location="Quảng Ninh">
            <h3>Nhân viên hành chính</h3>
            <p>🏢 Công ty VTC1</p>
            <p>📍 Quảng Ninh</p>
            <p>💰 8 - 12 triệu/tháng</p>
            <button onclick="applyJob('Nhân viên hành chính')">
                Ứng tuyển ngay
            </button>
        </div>

        <div class="job-card" data-location="TP. Hồ Chí Minh">
            <h3>Chuyên viên Marketing</h3>
            <p>🏢 Công ty VTC1</p>
            <p>📍 TP. Hồ Chí Minh</p>
            <p>💰 12 - 18 triệu/tháng</p>
            <button onclick="applyJob('Chuyên viên Marketing')">
                Ứng tuyển ngay
            </button>
        </div>

        <div class="job-card" data-location="Đà Nẵng">
            <h3>Nhân viên IT</h3>
            <p>🏢 Công ty VTC1</p>
            <p>📍 Đà Nẵng</p>
            <p>💰 15 - 25 triệu/tháng</p>
            <button onclick="applyJob('Nhân viên IT')">
                Ứng tuyển ngay
            </button>
        </div>

    </div>

    <section class="form-section" id="apply">
        <h2 class="section-title">ĐĂNG KÝ ỨNG TUYỂN VTC1</h2>

        <form onsubmit="submitForm(event)">
            <input type="text" id="name"
            placeholder="Họ và tên" required>

            <input type="tel" id="phone"
            placeholder="Số điện thoại" required>

            <input type="email" id="email"
            placeholder="Email" required>

            <select id="position" required>
                <option value="">Chọn vị trí ứng tuyển</option>
                <option>Nhân viên kinh doanh</option>
                <option>Nhân viên hành chính</option>
                <option>Chuyên viên Marketing</option>
                <option>Nhân viên IT</option>
            </select>

            <textarea id="message"
            placeholder="Giới thiệu bản thân..."
            rows="4"></textarea>

            <button type="submit">GỬI HỒ SƠ</button>
        </form>
    </section>

</div>

<footer id="contact">
    <h2>VTC1 - HỆ THỐNG TUYỂN DỤNG NHÂN LỰC</h2>
    <p>Kết nối doanh nghiệp - Phát triển nhân tài</p>
    <p>Email: tuyendung@vtc1.vn</p>
    <p>Hotline: 0900 000 000</p>
    <p>© 2026 VTC1. All rights reserved.</p>
</footer>

<script>

function searchJobs() {
    let keyword = document.getElementById("keyword")
        .value.toLowerCase();

    let location = document.getElementById("location")
        .value;

    let jobs = document.querySelectorAll(".job-card");

    jobs.forEach(job => {
        let text = job.innerText.toLowerCase();
        let jobLocation = job.dataset.location;

        let matchKeyword = text.includes(keyword);
        let matchLocation = !location ||
            jobLocation === location;

        job.style.display =
            matchKeyword && matchLocation ? "block" : "none";
    });
}

function applyJob(position) {
    document.getElementById("position").value = position;

    document.getElementById("apply")
        .scrollIntoView({behavior: "smooth"});
}

function submitForm(event) {
    event.preventDefault();

    let name = document.getElementById("name").value;
    let phone = document.getElementById("phone").value;
    let email = document.getElementById("email").value;
    let position = document.getElementById("position").value;

    alert(
        "Cảm ơn " + name +
        "! Bạn đã đăng ký vị trí " + position +
        ". VTC1 sẽ liên hệ với bạn."
    );

    event.target.reset();
}

</script>

</body>
</html>
