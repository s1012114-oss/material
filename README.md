# material
教材設計
<!DOCTYPE html>
<html lang="zh-Hant">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>周老師教材作品集</title>

<style>
body{
    font-family: "Noto Sans TC", sans-serif;
    max-width: 1000px;
    margin: auto;
    padding: 30px;
    background:#f7f9fc;
}

h1{
    text-align:center;
    color:#2c3e50;
}

.filter{
    text-align:center;
    margin:30px 0;
}

select{
    padding:10px;
    font-size:16px;
    border-radius:8px;
}

.cards{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
    gap:20px;
}

.card{
    background:white;
    padding:20px;
    border-radius:15px;
    box-shadow:0 3px 10px rgba(0,0,0,.1);
    transition:.3s;
}

.card:hover{
    transform:translateY(-5px);
}

.card h3{
    margin-top:0;
    color:#34495e;
}

.card p{
    color:#666;
}

.btn{
    display:inline-block;
    margin-top:10px;
    padding:8px 15px;
    background:#3498db;
    color:white;
    text-decoration:none;
    border-radius:8px;
}

.btn:hover{
    background:#2980b9;
}
</style>

</head>
<body>

<h1>📚 周老師教材作品集</h1>

<div class="filter">
    <label>教材分類：</label>
    <select id="categoryFilter">
        <option value="all">全部教材</option>
        <option value="teaching">教學設計</option>
        <option value="strategy">學習策略</option>
        <option value="social">社會技巧</option>
        <option value="service">服務導論</option>
    </select>
</div>

<div class="cards">

    <div class="card" data-category="teaching">
        <h3>直接教學法教案</h3>
        <p>運用明確教學步驟與範例示範。</p>
        <a href="files/直接教學法.pdf" class="btn">查看教材</a>
    </div>

    <div class="card" data-category="strategy">
        <h3>組織策略教學</h3>
        <p>分類整理數學概念與公式。</p>
        <a href="files/組織策略.pdf" class="btn">查看教材</a>
    </div>

    <div class="card" data-category="social">
        <h3>善意提醒回應技巧</h3>
        <p>社會技巧直接教學教材。</p>
        <a href="files/社會技巧.pdf" class="btn">查看教材</a>
    </div>

    <div class="card" data-category="service">
        <h3>服務型態探索活動</h3>
        <p>高職服務導論教學活動。</p>
        <a href="files/服務導論.pdf" class="btn">查看教材</a>
    </div>

</div>

<script>
const filter = document.getElementById("categoryFilter");
const cards = document.querySelectorAll(".card");

filter.addEventListener("change", () => {
    const value = filter.value;

    cards.forEach(card => {

        if(value === "all"){
            card.style.display = "block";
        }else{
            card.style.display =
                card.dataset.category === value
                ? "block"
                : "none";
        }

    });
});
</script>

</body>
</html>
