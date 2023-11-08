# B-
B站取消关注，复制下面代码进到关注页面。


按下F12，控制台复制粘贴。

补充：

①建议使用手机热点，IP被x后，开关飞行模式即可。
②不急的话300设大点如500,1000等等。。

```
function unfollow() {
const btns = $(".be-dropdown-item:contains('取消关注')");

let num = 0;
const loop = setInterval(() => {
btns[num].click();
num++;
if (num >= btns.length) {
clearInterval(loop);

$(".be-pager-next:contains('下一页')").click();

setTimeout(() => {
unfollow();
}, 1200);
}
}, 300);
}
unfollow();
```
