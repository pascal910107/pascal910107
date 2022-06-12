

<!--
**pascal910107/pascal910107** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

<!-- https://github.com/anuraghazra/github-readme-stats -->
[![Pascal's GitHub Stats](https://github-readme-stats.vercel.app/api?username=pascal910107&count_private=true&show_icons=true&include_all_commits=true)](https://github.com/pascal910107)  
[![Pascal's Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=pascal910107&layout=compact)](https://github.com/pascal910107)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
body {
background-color: #000;
/*防止出現向下滾動條*/
overflow: hidden;
}
</style>
</head>
<body>
<script>
function snow() {
//    1、定義一片雪花模板
var flake = document.createElement('div');
// 雪花字元 ❄❉❅❆✻✼❇❈❊✥✺
flake.innerHTML = '❆';
flake.style.cssText = 'position:absolute;color:#fff;';
//獲取頁面的高度 相當於雪花下落結束時Y軸的位置
var documentHieght = window.innerHeight;
//獲取頁面的寬度，利用這個數來算出，雪花開始時left的值
var documentWidth = window.innerWidth;
//定義生成一片雪花的毫秒數
var millisec = 100;
//2、設定第一個定時器，週期性定時器，每隔一段時間（millisec）生成一片雪花；
setInterval(function() { //頁面載入之後，定時器就開始工作
//隨機生成雪花下落 開始 時left的值，相當於開始時X軸的位置
var startLeft = Math.random() * documentWidth;
//隨機生成雪花下落 結束 時left的值，相當於結束時X軸的位置
var endLeft = Math.random() * documentWidth;
//隨機生成雪花大小
var flakeSize = 5   20 * Math.random();
//隨機生成雪花下落持續時間
var durationTime = 4000   7000 * Math.random();
//隨機生成雪花下落 開始 時的透明度
var startOpacity = 0.7   0.3 * Math.random();
//隨機生成雪花下落 結束 時的透明度
var endOpacity = 0.2   0.2 * Math.random();
//克隆一個雪花模板
var cloneFlake = flake.cloneNode(true);
//第一次修改樣式，定義克隆出來的雪花的樣式
cloneFlake.style.cssText  = `
left: ${startLeft}px;
opacity: ${startOpacity};
font-size:${flakeSize}px;
top:-25px;
transition:${durationTime}ms;
`;
//拼接到頁面中
document.body.appendChild(cloneFlake);
//設定第二個定時器，一次性定時器，
//當第一個定時器生成雪花，並在頁面上渲染出來後，修改雪花的樣式，讓雪花動起來；
setTimeout(function() {
//第二次修改樣式
cloneFlake.style.cssText  = `
left: ${endLeft}px;
top:${documentHieght}px;
opacity:${endOpacity};
`;
//4、設定第三個定時器，當雪花落下後，刪除雪花。
setTimeout(function() {
cloneFlake.remove();
}, durationTime);
}, 0);
}, millisec);
}
snow();
</script>
</body>
</html>
