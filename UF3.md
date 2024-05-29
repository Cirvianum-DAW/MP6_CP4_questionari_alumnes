## QÜESTIONS UF3

### 1. Què és el DOM (Document Object Model) en JavaScript?

- A) Una biblioteca de JavaScript per manipular gràfics.
- B) Una API per accedir i manipular el contingut, l'estructura i l'estil dels documents HTML.
- C) Un llenguatge de programació per crear pàgines web dinàmiques.
- D) Un gestor de bases de dades per a aplicacions web.

### 2. Quina és la diferència principal entre `getElementById` i `querySelector`?

- A) `getElementById` retorna un element amb un ID específic, mentre que `querySelector` retorna el primer element que coincideix amb un selector CSS.
- B) `getElementById` retorna una llista de tots els elements amb un ID específic, mentre que `querySelector` retorna tots els elements que coincideixen amb un selector CSS.
- C) `getElementById` és una funció obsoleta i `querySelector` és la seva versió més recent.
- D) `getElementById` retorna el primer element que coincideix amb un selector CSS, mentre que `querySelector` retorna un element amb un ID específic.

### 3. Quina propietat d'un node DOM utilitzaries per accedir al contingut text d'un element?

- A) `innerHTML`
- B) `textContent`
- C) `nodeValue`
- D) `outerHTML`

### 4. Com es pot canviar l'atribut `src` d'una imatge amb id "myImage" utilitzant JavaScript?

- A) `document.getElementById('myImage').src = 'nou_link.jpg';`
- B) `document.querySelector('myImage').src = 'nou_link.jpg';`
- C) `document.getElementById('myImage').setAttribute('src', 'nou_link.jpg');`
- D) A i C són correctes.

### 5. Quina és la manera <u>correcta o bona pràctica</u> si volem afegir un esdeveniment de clic a un botó amb id "myButton"?

- A)

```javascript
document.getElementById("myButton").onclick = function () {
  alert("Clicat!");
};
```

- B)

```javascript
document.getElementById("myButton").addEventListener("click", function () {
  alert("Clicat!");
});
```

- C)

```javascript
document.getElementById("myButton").addEventListener("onclick", function () {
  alert("Clicat!");
});
```

- D) Tant la A com la B es consideren bones pràctiques.

### 6. Quin és el resultat de la següent funció?

```javascript
const element = document.createElement("div");
element.textContent = "Hola, món!";
document.body.appendChild(element);
```

- A) Afegeix un nou element `div` amb el text "Hola, món!" al cos del document.
- B) Afegeix un nou element `div` buit al cos del document.
- C) Sobrescriu el cos del document amb un nou element `div` amb el text "Hola, món!".
- D) No fa res, perquè `element` no està afegit al DOM.

### 7. Com es pot seleccionar tots els elements amb la classe "item" i canviar el seu color de text a vermell?

```javascript
const elements = document.querySelectorAll(".item");
elements.forEach((element) => {
  element.style.color = "red";
});
```

- A) `document.querySelector('.item').style.color = 'red';`
- B) `document.querySelectorAll('.item').style.color = 'red';`
- C) `document.querySelectorAll('.item').forEach(element => { element.style.color = 'red'; });`
- D) `document.querySelector('.item').forEach(element => { element.style.color = 'red'; });`

### 8. Quin és el resultat de la següent manipulació del DOM?

```html
<ul id="list">
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
```

```javascript
const list = document.getElementById("list");
const newElement = document.createElement("li");
newElement.textContent = "Item 3";
list.insertBefore(newElement, list.firstChild);
```

- A) Afegeix un nou element `li` amb el text "Item 3" al final de la llista.
- B) Substitueix el primer element `li` amb el text "Item 3".
- C) Afegeix un nou element `li` amb el text "Item 3" al principi de la llista.
- D) No fa res, perquè `nouElement` no està afegit correctament.

### 9. Com es pot eliminar un element amb id "myElement" del DOM?

- A) `document.getElementById('myElement').remove();`
- B) `document.getElementById('myElement').parentNode.removeChild(myElement);`
- C) `document.querySelector('#myElement').remove();`
- D) Totes les anteriors són correctes.

### 10. Quin és el resultat de la següent manipulació del DOM?

```html
<div id="container">
  <p>Paràgraf 1</p>
  <p>Paràgraf 2</p>
</div>
```

```javascript
const container = document.getElementById("container");
const paragrafs = container.getElementsByTagName("p");
container.removeChild(paragrafs[0]);
```

- A) Elimina <p> Paràgraf 2 </p>
- B) Elimina <p> Paràgraf 1 </p>
- C) Elimina tots els paràgrafs dins del div amb id "container".
- D) No fa res, perquè `paragrafs` és una col·lecció buida.

### 11. Quin esdeveniment es dispara quan el cursor del ratolí entra dins d'un element?

- A) `click`
- B) `mouseover`
- C) `mousemove`
- D) `mouseenter`

### 12. Quin és el resultat del següent codi JavaScript?

```javascript
document.getElementById("myButton").addEventListener("click", function (event) {
  alert("Clic!");
});
document
  .getElementById("myButton")
  .addEventListener("mouseup", function (event) {
    alert("Botó soltat!");
  });
```

- A) Es mostra una alerta "Clic!" quan es fa clic amb qualsevol botó del ratolí.
- B) Es mostra una alerta "Clic!" quan es fa clic amb el botó esquerre del ratolí i una alerta "Botó soltat!" quan es deixa anar el botó del ratolí.
- C) Es mostra una alerta "Clic!" només quan es fa clic amb el botó esquerre del ratolí.
- D) Es mostra una alerta "Botó soltat!" només quan es fa clic amb el botó esquerre del ratolí.

### 13. Quina és la manera correcta de capturar l'enviament d'un formulari i prevenir l'acció predeterminada en JavaScript?

```html
<form id="myForm">
  <input type="text" name="username" />
  <button type="submit">Envia</button>
</form>
```

- A) `form

.onsubmit = function(event) { alert('Formulari enviat!'); }`

- B) `form.addEventListener('submit', function(event) { alert('Formulari enviat!'); });`
- C) `form.addEventListener('submit', function(event) { event.preventDefault(); alert('Formulari enviat!'); });`
- D) `form.onsubmit = function(event) { event.preventDefault(); alert('Formulari enviat!'); }`

### 14. Què passa quan es valida un formulari abans de ser enviat i l'usuari no ha omplert correctament el camp requerit?

```html
<form id="myForm" novalidate>
  <input type="text" id="username" name="username" required />
  <button type="submit">Envia</button>
</form>
```

```javascript
const form = document.getElementById("myForm");
form.addEventListener("submit", function (event) {
  const username = document.getElementById("username");
  if (!username.value) {
    alert("El camp username és obligatori!");
  }
});
```

- A) Es mostra una alerta dient "El camp username és obligatori!" però el formulari s'envia igualment.
- B) Es mostra una alerta dient "El camp username és obligatori!" i el formulari no s'envia.
- C) No passa res, perquè el camp requerit es valida automàticament pel navegador.
- D) El formulari s'envia sense cap validació.

### 15. Quin és el resultat del següent codi quan es selecciona una nova opció en un element `<select>` amb id "mySelect"?

```html
<select id="mySelect">
  <option value="1">Opció 1</option>
  <option value="2">Opció 2</option>
</select>
```

```javascript
document
  .getElementById("mySelect")
  .addEventListener("change", function (event) {
    alert("Nova selecció: " + event.target.value);
  });
```

- A) Es mostra una alerta amb el text "Nova selecció: " seguit del valor de l'opció seleccionada.
- B) Es mostra una alerta amb el text "Nova selecció: 1" o "Nova selecció: 2".
- C) Es mostra una alerta amb el text "Opció seleccionada: " seguit del valor de l'opció seleccionada.
- D) Es mostra una alerta amb el text "Opció seleccionada: Opció 1" o "Opció seleccionada: Opció 2".

### 16. Quina és la diferència principal entre els esdeveniments `input` i `change` en un element `<input>`?

- A) L'esdeveniment `input` es dispara quan es canvia el valor d'un element d'entrada i l'esdeveniment `change` es dispara immediatament després de qualsevol canvi en el valor d'un element d'entrada.
- B) L'esdeveniment `input` es dispara immediatament després de qualsevol canvi en el valor d'un element d'entrada, mentre que l'esdeveniment `change` es dispara quan l'element perd el focus després que s'ha canviat el seu valor.
- C) L'esdeveniment `input` es dispara quan l'element perd el focus després que s'ha canviat el seu valor, mentre que l'esdeveniment `change` es dispara immediatament després de qualsevol canvi en el valor d'un element d'entrada.
- D) No hi ha cap diferència entre `input` i `change`, ambdós esdeveniments es comporten de la mateixa manera.

### 17. Quin és el resultat del següent codi quan l'usuari escriu text en un camp `<input>` amb id "myInput"?

```html
<input type="text" id="myInput" />
<p id="output"></p>
```

```javascript
document.getElementById("myInput").addEventListener("input", function (event) {
  document.getElementById("output").textContent = event.target.value;
});
```

- A) Es mostra el text introduït a l'element `<input>` en l'element `<p>` amb id "output" en temps real.
- B) Es mostra una alerta amb el text introduït a l'element `<input>` cada vegada que l'usuari escriu una lletra.
- C) Es canvia el valor de l'element `<input>` amb el text de l'element `<p>` amb id "output".
- D) No passa res, perquè l'esdeveniment `input` no està suportat.

### 18. Quina és la diferència entre afegir un esdeveniment a HTML i afegir-lo amb JavaScript?

```html
<!-- HTML -->
<button id="myButton" onclick="alert('Clic HTML!')">Fes clic HTML</button>

<!-- JavaScript -->
<button id="myButtonJS">Fes clic JS</button>
<script>
  document.getElementById("myButtonJS").addEventListener("click", function () {
    alert("Clic JS!");
  });
</script>
```

- A) No hi ha cap diferència entre ambdós mètodes.
- B) Afegir un esdeveniment amb HTML permet afegir múltiples esdeveniments al mateix element, mentre que amb JavaScript només es pot afegir un sol esdeveniment.
- C) Afegir un esdeveniment amb JavaScript permet afegir múltiples esdeveniments al mateix element, mentre que amb HTML només es pot afegir un sol esdeveniment.
- D) Ambdós mètodes permeten afegir múltiples esdeveniments al mateix element.

### 19. Quina és la diferència entre `innerHTML` i `textContent`?

```html
<div id="myDiv">Hola, <span>Món</span>!</div>
```

```javascript
const element = document.getElementById("myDiv");

console.log(element.innerHTML); // Què retorna això?
console.log(element.textContent); // Què retorna això?
```

- A) `innerHTML` retorna el text dins de l'element, mentre que `textContent` retorna el contingut HTML dins de l'element.
- B) `innerHTML` retorna el contingut HTML dins de l'element, mentre que `textContent` retorna el text dins de l'element, sense etiquetes HTML.
- C) `innerHTML` i `textContent` retornen el mateix contingut.
- D) `innerHTML` retorna el text dins de l'element, sense etiquetes HTML, mentre que `textContent` retorna el contingut HTML dins de l'element.

### 20. Què passa quan la propietat `hidden` d'un element està establerta a `true`?

```html
<div id="myDiv">Això és visible?</div>
```

```javascript
const element = document.getElementById("myDiv");
element.hidden = true;
```

- A) L'element es veu però no es pot interactuar amb ell.
- B) L'element no es veu i no es pot interactuar amb ell.
- C) L'element es veu i es pot interactuar amb ell.
- D) L'element no es veu però es pot interactuar amb ell.

### 21. Quin és l'avantatge d'utilitzar classes CSS en lloc d'utilitzar directament l'atribut `style` en un element?

- A) Les classes CSS permeten afegir estils dinàmics mentre que l'atribut `style` no.
- B) Utilitzar classes CSS fa que el codi sigui més net, més fàcil de mantenir i permet reutilitzar els estils.
- C) L'atribut `style` només es pot utilitzar per a canvis de color, mentre que les classes CSS es poden utilitzar per a qualsevol estil.
- D) No hi ha cap avantatge, és millor util

itzar sempre l'atribut `style`.

### 22. Quina és la millor manera de substituir completament totes les classes d'un element amb una nova classe?

```html
<div id="myDiv" class="oldClass anotherClass">Hola, món!</div>
<button id="setClass">Defineix Classe</button>
```

- A) `document.getElementById('myDiv').className = 'newClass';`
- B) `document.getElementById('myDiv').classList = 'newClass';`
- C) `document.getElementById('myDiv').classList.add('newClass');`
- D) `document.getElementById('myDiv').classList.replace('oldClass', 'newClass');`

### 23. Quan és preferible utilitzar l'atribut `style` directament en lloc de classes CSS?

- A) Quan es necessita aplicar estils estàtics que no canviaran mai.
- B) Quan podem necessitar aplicar estils dinàmics en temps d'execució amb JavaScript.
- C) Quan es vol assegurar que els estils no es poden sobreescriure amb altres classes CSS.
- D) Sempre és preferible utilitzar l'atribut `style` en lloc de classes CSS.
