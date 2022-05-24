<script> document.cookie = "session=test GDPR"; document.cookie =
"favorite_task=collect Data"; function alertCookie() { alert(document.cookie); }

// Exemplul 1
document.cookie = "name=oeschger; SameSite=None; Secure";
document.cookie = "favorite_food=tripe; SameSite=None; Secure";



function showCookies() {
const output = document.getElementById('cookies')
output.textContent = '> ' + document.cookie
}



function clearOutputCookies() {
const output = document.getElementById('cookies')
output.textContent = ''
}

// Exemplul 2
document.cookie = "test1=Hello; SameSite=None; Secure";
document.cookie = "test2=World; SameSite=None; Secure";



const cookieValue = document.cookie
.split('; ')
.find(row => row.startsWith('test2='))
.split('=')[1];



function showCookieValue() {
const output = document.getElementById('cookie-value')
output.textContent = '> ' + cookieValue
}



function clearOutputCookieValue() {
const output = document.getElementById('cookie-value')
output.textContent = ''
}



//Exemplul 3
function doOnce() {
if (!document.cookie.split('; ').find(row => row.startsWith('doSomethingOnlyOnce'))) {
document.cookie = "doSomethingOnlyOnce=true; expires=Fri, 31 Dec 9999 23:59:59 GMT; SameSite=None; Secure";
const output = document.getElementById('do-once')
output.textContent = '> Do something here!'
}
}



function clearOutputDoOnce() {
const output = document.getElementById('do-once')
output.textContent = ''
}

//Exemplul 5
document.cookie = "reader=1; SameSite=None; Secure";



function checkACookieExists() {
if (document.cookie.split(';').some((item) => item.trim().startsWith('reader='))) {
const output = document.getElementById('a-cookie-existence')
output.textContent = '> The cookie "reader" exists'
}
}



function clearOutputACookieExists() {
const output = document.getElementById('a-cookie-existence')
output.textContent = ''
}

//Exemplul 6
function checkCookieHasASpecificValue() {
if (document.cookie.split(';').some((item) => item.includes('reader=1'))) {
const output = document.getElementById('a-specific-value-of-the-cookie')
output.textContent = '> The cookie "reader" has a value of "1"'
}
}



function clearASpecificValueOfTheCookie() {
const output = document.getElementById('a-specific-value-of-the-cookie')
output.textContent = ''
}
</script>



<body> Bine ai venit la lab <button onclick="alertCookie()">Show cookies</button>



//Exemplul 1
<button onclick="showCookies()">Arata cookies</button>



<button onclick="clearOutputCookies()">
Clear
</button>



<div>
<code id="cookies"></code>
</div>



//Exemplul 2
<button onclick="showCookieValue()">Show cookie value</button>



<button onclick="clearOutputCookieValue()">
Clear
</button>



<div>
<code id="cookie-value"></code>
</div>

//Exemplul 3
<button onclick="doOnce()">Only do something once</button>



<button onclick="clearOutputDoOnce()">
Clear
</button>



<div>
<code id="do-once"></code>
</div>

//Exemplul 5
<button onclick="checkACookieExists()">
Check a cookie exists
</button>



<button onclick="clearOutputACookieExists()">
Clear
</button>



<div>
<code id="a-cookie-existence"></code>
</div>

//Exemplul 6
<button onclick="checkCookieHasASpecificValue()">
Check that a cookie has a specific value
</button>



<button onclick="clearASpecificValueOfTheCookie()">
Clear
</button>



<div>
<code id="a-specific-value-of-the-cookie"></code>
</div>
</body>
