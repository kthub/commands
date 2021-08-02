## Commands

### Git
Alias for simplistic-push
```
alias gpush="git add --all; git commit -m 'commit'; git push origin master"
```

### SSH
Generate keys
```
ssh-keygen -t rsa -b 4096 -C "keiichi.tsuda@gmail.com" -f id_rsa_kt
```
If you unable to ssh, try followings.
```
ssh root@cicd01 -o PreferredAuthentications=password
# .ssh/config を変えてもOK
```

### Bookmarklet
You can use the bookmarklet below to add a copy button to the code section of GitHub README.md.
```
javascript:(function(){var copy = function(target) {    var textArea = document.createElement('textarea');    textArea.setAttribute('style','width:1px;border:0;opacity:0;');    document.body.appendChild(textArea);    textArea.value = target.innerHTML;    textArea.select();    document.execCommand('copy');    document.body.removeChild(textArea);};var codes = document.querySelectorAll("code");codes.forEach(function(code){  var button = document.createElement("button");  button.className = "btn btn-sm";  button.innerHTML = "copy";  console.log("code=" + code);  console.log("code.innerHTML=" + code.innerHTML);  code.parentNode.insertBefore(button, null);  button.addEventListener('click', function(e){    e.preventDefault();    copy(code);  });});})();
```