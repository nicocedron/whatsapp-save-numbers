## Bienvenido / Welcome

Ver [documentación en español](https://nicocedron.github.io/whatsapp-save-numbers#español)

See [english docs](https://nicocedron.github.io/whatsapp-save-numbers#english)


### Español

Hola!

Para crear un archivo con los números no agendados en tu whatsapp solo debes ejecutar un código mágico en tu pestaña de [whatsapp web](https://web.whatsapp.com).

Pasos:

1. Abre whatsapp web.
2. Presiona **Control+Shift+J** en el caso de usar windows o linux, en el caso de mac **Command+Option+J**
3. Copia y pega el siguiente código en la parte blanca de la pestaña **Console**
4. Ve a [Contactos de google](https://contacts.google.com) e importa el archivo y lo tendrás guardado en tu teléfono.


```javascript
!function(){const e=(navigator.language||navigator.userLanguage).slice(0,2),n={es:{firstMessage:"Prefijo para sus contactos, Por ejemplo: Cliente",initialNumbers:function(e){return`Numero inicial de los contactos?\nPara los nombres, por ejemplo: ${e} 1000...1001...1002...etc`}},en:{firstMessage:"Prefix for your contacts, For example: Client",initialNumbers:function(e){return`Initial counter?\nPara los nombres, It is to list the names, for example: ${e} 1000...1001...1002...etc`}}}["es"!=e&&"en"==e?"es":e];var i=["Name,Given Name,Additional Name,Family Name,Yomi Name,Given Name Yomi,Additional Name Yomi,Family Name Yomi,Name Prefix,Name Suffix,Initials,Nickname,Short Name,Maiden Name,Birthday,Gender,Location,Billing Information,Directory Server,Mileage,Occupation,Hobby,Sensitivity,Priority,Subject,Notes,Language,Photo,Group Membership,Phone 1 - Type,Phone 1 - Value"],t=[],o=document.querySelector("#pane-side"),a=o.clientHeight,r=0,l=null,c=prompt(n.firstMessage),s=prompt(n.initialNumbers(c)),m=null;l=setInterval(function(){o.scrollTo(0,a*r),o.scrollHeight-a<=a*r?(clearInterval(l),setTimeout(function(){var e;clearInterval(m),e=s,t.forEach(function(n){var t;i.push(`${c} ${t=e,t.toString().padStart(5,"0")},,,,,,,,,,,,,,,,,,,,,,,,,,,,* myContacts,Mobile,${n}`),e++}),function(e,n){var i=new Blob([n],{type:"text/csv"});if(window.navigator.msSaveOrOpenBlob)window.navigator.msSaveBlob(i,e);else{var t=window.document.createElement("a");t.href=window.URL.createObjectURL(i),t.download=e,document.body.appendChild(t),t.click(),document.body.removeChild(t)}}("clients.csv",i.join("\n"))},1e3)):r++},500),m=setInterval(function(){document.querySelectorAll('[title^="+"]').forEach(function(e){var n=e.innerHTML;-1==t.indexOf(n)&&"+"==n[0]&&t.push(e.innerHTML)})},10)}();
```

### English

Hi!

To create a file with the numbers not saved in your whatsapp you just have to execute a magic code on [whatsapp web](https://web.whatsapp.com).

Steps:

1. Open whatsapp web.
2. Press **Control+Shift+J** in the case of using windows or linux, **Command+Option+J** for mac.
3. Copy and paste the following code into the white part of the ** Console ** tab
4. Go to [Google Contacts] (https://contacts.google.com) and import the file and you will have all the numbers saved on your phone.


```javascript
!function(){const e=(navigator.language||navigator.userLanguage).slice(0,2),n={es:{firstMessage:"Prefijo para sus contactos, Por ejemplo: Cliente",initialNumbers:function(e){return`Numero inicial de los contactos?\nPara los nombres, por ejemplo: ${e} 1000...1001...1002...etc`}},en:{firstMessage:"Prefix for your contacts, For example: Client",initialNumbers:function(e){return`Initial counter?\nPara los nombres, It is to list the names, for example: ${e} 1000...1001...1002...etc`}}}["es"!=e&&"en"==e?"es":e];var i=["Name,Given Name,Additional Name,Family Name,Yomi Name,Given Name Yomi,Additional Name Yomi,Family Name Yomi,Name Prefix,Name Suffix,Initials,Nickname,Short Name,Maiden Name,Birthday,Gender,Location,Billing Information,Directory Server,Mileage,Occupation,Hobby,Sensitivity,Priority,Subject,Notes,Language,Photo,Group Membership,Phone 1 - Type,Phone 1 - Value"],t=[],o=document.querySelector("#pane-side"),a=o.clientHeight,r=0,l=null,c=prompt(n.firstMessage),s=prompt(n.initialNumbers(c)),m=null;l=setInterval(function(){o.scrollTo(0,a*r),o.scrollHeight-a<=a*r?(clearInterval(l),setTimeout(function(){var e;clearInterval(m),e=s,t.forEach(function(n){var t;i.push(`${c} ${t=e,t.toString().padStart(5,"0")},,,,,,,,,,,,,,,,,,,,,,,,,,,,* myContacts,Mobile,${n}`),e++}),function(e,n){var i=new Blob([n],{type:"text/csv"});if(window.navigator.msSaveOrOpenBlob)window.navigator.msSaveBlob(i,e);else{var t=window.document.createElement("a");t.href=window.URL.createObjectURL(i),t.download=e,document.body.appendChild(t),t.click(),document.body.removeChild(t)}}("clients.csv",i.join("\n"))},1e3)):r++},500),m=setInterval(function(){document.querySelectorAll('[title^="+"]').forEach(function(e){var n=e.innerHTML;-1==t.indexOf(n)&&"+"==n[0]&&t.push(e.innerHTML)})},10)}();
```
