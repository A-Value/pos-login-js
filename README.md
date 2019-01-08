<p align="center"><img width="10%"  src="https://github.com/A-Value/pos-login-js/blob/master/resources/images/pos-logo-128.png"></p>

### [Demos](https://demo-pos.avalue.co.th)

Working demos of H-POS Login

-----

### Quick example

Render the component on the parent page:

```javascript

<button id="popupLogin">Login with H-POS</button>
<div id="result"></div>

<script src="./h-pos.min.js"></script>
<script>
    document.querySelector('#popupLogin').addEventListener('click', function () {
            // Hide the button
            document.querySelector('#popupLogin').style.display = 'none';
            // Render the component
            HPOSLogin.render({
                onLogin: function (email, token) {
                    console.log('User logged in with email:', email);
                    document.querySelector('#result').innerText = email + ' logged in!' + ' Token: ' + token;
                }
            });
        });
</script>

```

### API

```javascript

onLogin: function (email, token) { }

```

`email`: user email

`token`: user token 

Get called after user complete authentication in popup window.
Both values can be `null` if authentication failed.

----

### Browser Support

- Internet Explorer 9+
- Chrome 27+
- Firefox 30+
- Safari 5.1+
- Opera 23+
