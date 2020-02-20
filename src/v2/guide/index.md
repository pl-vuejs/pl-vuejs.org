---
title: Introduction
type: guide
order: 2
---

## Co to jest Vue.js?

Vue (wymawiane /vjuː/, jak **view**) to **progresywny framework** do budowania interfejsów użytkownika. W przeciwieństwie do innych monolitycznych frameworków, Vue jest zaprojektowany od podstaw tak, aby można go było stopniowo adaptować. Biblioteka rdzeniowa jest skoncentrowana tylko na warstwie widoku i jest łatwa do pobrania i zintegrowania z innymi bibliotekami lub istniejącymi projektami. Z drugiej strony, Vue jest również doskonale zdolny do zasilania zaawansowanych jednostronicowych aplikacji, gdy jest używany w połączeniu z [nowoczesnym oprzyrządowaniem] (single-file-components.html) i [wspierającymi bibliotekami] (https://github.com/vuejs/awesome-vue#components--libraries).

Jeśli chciałbyś dowiedzieć się więcej o Vue'u przed nurkowaniem, to <a id="modal-player" href="#">created a video</a> walking through the core principles and a sample project.

Jeśli jesteś doświadczonym programistą frontendowym i chcesz wiedzieć jak Vue porównuje się z innymi bibliotekami/ramami, sprawdź [Comparison with Other Frameworks](comparison.html).

<div class="vue-mastery"><a href="https://www.vuemastery.com/courses/intro-to-vue-js/vue-instance/" target="_blank" rel="sponsorowany noopener" title="Free Vue.js Course">Watch a free video course on Vue Mastery</a></div>.

# Rozpoczynamy

<a class="button" href="installation.html">Installation</a>

<p class="tip">Oficjalny przewodnik zakłada znajomość HTML, CSS i JavaScript na poziomie średnio zaawansowanym. Jeśli jesteś zupełnie nowy w rozwoju front-end, może nie być najlepszym pomysłem, aby wskoczyć od razu do frameworka jako pierwszy krok - chwyć się podstaw, a potem wracaj! Wcześniejsze doświadczenie z innymi frameworkami pomaga, ale nie jest wymagane.</p>

Najprostszym sposobem na wypróbowanie Vue.js jest skorzystanie z [Przykładu Hello World](https://codesandbox.io/s/github/vuejs/vuejs.org/tree/master/src/v2/examples/vue-20-hello-world). Zachęcamy do otwarcia go w innej zakładce i podążania za kilkoma podstawowymi przykładami. Możesz też <a href="https://github.com/vuejs/vuejs.org/blob/master/src/v2/examples/vue-20-hello-world/index.html" target="_blank" download="index.html" rel="noopener noreferrer">create an <code>index.html</code> file</a> and include Vue z:

```html
<!-- wersja rozwojowa, zawiera pomocne ostrzeżenia konsoli -->
<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
```

albo:

```html
<!-- wersja produkcyjna, zoptymalizowana pod kątem wielkości i prędkości -->
<script src="https://cdn.jsdelivr.net/npm/vue"></script>
```

Strona [Instalacja](install.html) zawiera więcej opcji instalacji Vue. Uwaga: Nie**** zalecamy, aby początkujący zaczęli od `vue-cli`, szczególnie jeśli nie znasz jeszcze narzędzi budowania opartych na Node.js.

Jeśli wolisz coś bardziej interaktywnego, możesz również sprawdzić [tę serię samouczków na Scrimbie](https://scrimba.com/g/gvuedocs), która daje ci mieszankę screencastu i placu zabaw z kodem, z którym możesz się wstrzymać i bawić w dowolnym momencie.

## Rendering deklaratywny

<div class='scrimba"><a href="https://scrimba.com/p/pXKqta/cQ3QVcr" target="_blank" rel="noopener noreferrer">Try this lesson on Scrimba</a></div>

Rdzeniem Vue.js jest system, który pozwala na deklaratywne renderowanie danych do DOM przy użyciu prostej składni szablonów:

```html
<div id="app">
  {{\i1}
</div>
```
``` js
var app = nowy Vue({\i0}
  el: '#app',
  dane: {
    wiadomość: "Witaj Vue!
  }
})
```
{% surowy%}
<div id="app" class="demo">
  {{\i1}
</div>
<scriptum>
var app = nowy Vue({\i0}
  el: '#app',
  dane: {
    wiadomość: "Witaj Vue!
  }
})
</scriptum>
{% endraw %}

Stworzyliśmy już naszą pierwszą aplikację Vue! Wygląda to dość podobnie do renderowania szablonu łańcucha, ale Vue wykonał wiele pracy pod maską. Dane i DOM są teraz połączone, a wszystko jest teraz **reaktywne**. Skąd mamy wiedzieć? Otwórz konsolę JavaScript w twojej przeglądarce (teraz, na tej stronie) i ustaw `app.message` na inną wartość. Powinieneś zobaczyć renderowany przykład powyżej odpowiednio zaktualizować.

Oprócz interpolacji tekstu, możemy również powiązać atrybuty elementów w ten sposób:

```html
<div id="app-2">
  <span v-bind:title="message">
    Przesuń nade mną myszkę na kilka sekund.
    by zobaczyć mój dynamicznie związany tytuł!
  </span>
</div>
```
```js
var app2 = nowy Vue({\i0}
  el: "#app-2",
  dane: {
    wiadomość: Załadowałeś tę stronę na " + nowy Date().toLocaleString()
  }
})
```
{% surowy%}
<div id="app-2" class="demo">
  <span v-bind:title="message">
    Przesuń nade mną myszkę na kilka sekund, aby zobaczyć mój dynamicznie oprawiony tytuł!
  </span>
</div>
<scriptum>
var app2 = nowy Vue({\i0}
  el: "#app-2",
  dane: {
    wiadomość: Załadowałeś tę stronę na " + nowy Date().toLocaleString()
  }
})
</scriptum>
{% endraw %}

Tutaj spotykamy się z czymś nowym. Atrybut `v-bind`, który widzisz nazywa się **directive**. Dyrektywy są poprzedzone `v-` aby wskazać, że są to specjalne atrybuty dostarczone przez Vue'a, i jak można się było domyślać, stosują one specjalne reaktywne zachowanie do renderowanego DOM. Tutaj, w zasadzie jest napisane "trzymaj atrybut `tytuł` tego elementu na bieżąco z właściwością `komunikatu` na instancji Vue'a".

Jeśli ponownie otworzysz swoją konsolę JavaScript i wpiszesz `app2.message = 'jakaś nowa wiadomość'`, po raz kolejny zobaczysz, że powiązany HTML - w tym przypadku atrybut `tytuł` - został zaktualizowany.

## Wyrażenia warunkowe i pętle

<div class='scrimba"><a href="https://scrimba.com/p/pXKqta/cEQe4SJ" target="_blank" rel="noopener noreferrer">Try this lesson on Scrimba</a></div>

Łatwo jest też przełączyć obecność jakiegoś elementu:

```html
<div id="app-3">
  <span v-if="see">Teraz mnie widzisz</span>
</div>
```

```js
var app3 = nowy Vue({\i0}
  el: "#app-3",
  dane: {
    oglądany: prawdziwy
  }
})
```

{% surowy%}
<div id="app-3" class="demo">
  <span v-if="see">Teraz mnie widzisz</span>
</div>
<scriptum>
var app3 = nowy Vue({\i0}
  el: "#app-3",
  dane: {
    oglądany: prawdziwy
  }
})
</scriptum>
{% endraw %}

Idź i wpisz w konsoli `app3.seen = false`. Powinieneś zobaczyć, że wiadomość zniknęła.

Ten przykład pokazuje, że możemy powiązać dane nie tylko z tekstem i atrybutami, ale także z **strukturą** DOM. Ponadto, Vue dostarcza również potężny system efektów przejścia, który może automatycznie zastosować [efekty przejścia](transitions.html), gdy elementy są wstawiane/aktualizowane/usuwane przez Vue.

Istnieje jeszcze kilka innych dyrektyw, każda z nich posiada swoją własną, specjalną funkcjonalność. Na przykład, dyrektywa `v-for` może być używana do wyświetlania listy elementów przy użyciu danych z tablicy:

```html
<div id="app-4">
  <ol>
    <li v-for="todo in todos">
      (todo.text })
    </li>
  </ol>
</div>
```
```js
var app4 = nowy Vue({\i0}
  el: "#app-4",
  dane: {
    todos: [
      { tekst: "Naucz się JavaScript" },
      { tekst: "Learn Vue" {\i1}
      { tekst: "Zbuduj coś niesamowitego" { tekst: "Zbuduj coś niesamowitego"}
    ]
  }
})
```
{% surowy%}
<div id="app-4" class="demo">
  <ol>
    <li v-for="todo in todos">
      (todo.text })
    </li>
  </ol>
</div>
<scriptum>
var app4 = nowy Vue({\i0}
  el: "#app-4",
  dane: {
    todos: [
      { tekst: "Naucz się JavaScript" },
      { tekst: "Learn Vue" {\i1}
      { tekst: "Zbuduj coś niesamowitego" { tekst: "Zbuduj coś niesamowitego"}
    ]
  }
})
</scriptum>
{% endraw %}

W konsoli wpisz `app4.todos.push({tekst: 'Nowa pozycja' })`. Powinieneś zobaczyć nową pozycję dołączoną do listy.

## Obsługa formularzy użytkownika

<div class="scrimba"><a href="https://scrimba.com/p/pXKqta/czPNaUr" target="_blank" rel="noopener noreferrer">Try this lesson on Scrimba</a></div>

To let users interact with your app, we can use the `v-on` directive to attach event listeners that invoke methods on our Vue instances:

```html
<div id="app-5">
  <p>{{ message }}</p>
  <button v-on:click="reverseMessage">Reverse Message</button>
</div>
```
```js
var app5 = new Vue({
  el: '#app-5',
  data: {
    message: 'Hello Vue.js!'
  },
  methods: {
    reverseMessage: function () {
      this.message = this.message.split('').reverse().join('')
    }
  }
})
```
{% raw %}
<div id="app-5" class="demo">
  <p>{{ message }}</p>
  <button v-on:click="reverseMessage">Reverse Message</button>
</div>
<script>
var app5 = new Vue({
  el: '#app-5',
  data: {
    message: 'Hello Vue.js!'
  },
  methods: {
    reverseMessage: function () {
      this.message = this.message.split('').reverse().join('')
    }
  }
})
</script>
{% endraw %}

Note that in this method we update the state of our app without touching the DOM - all DOM manipulations are handled by Vue, and the code you write is focused on the underlying logic.

Vue also provides the `v-model` directive that makes two-way binding between form input and app state a breeze:

```html
<div id="app-6">
  <p>{{ message }}</p>
  <input v-model="message">
</div>
```
```js
var app6 = new Vue({
  el: '#app-6',
  data: {
    message: 'Hello Vue!'
  }
})
```
{% raw %}
<div id="app-6" class="demo">
  <p>{{ message }}</p>
  <input v-model="message">
</div>
<script>
var app6 = new Vue({
  el: '#app-6',
  data: {
    message: 'Hello Vue!'
  }
})
</script>
{% endraw %}

## Używanie komponentów

<div class='scrimba"><a href="https://scrimba.com/p/pXKqta/cEQVkA3" target="_blank" rel="noopener noreferrer">Try this lesson on Scrimba</a></div>

System komponentów jest kolejnym ważnym pojęciem w Vue, ponieważ jest to abstrakcja, która pozwala nam budować duże aplikacje składające się z małych, samodzielnych i często wielokrotnego użytku komponentów. Jeśli się nad tym zastanowimy, prawie każdy rodzaj interfejsu aplikacji może być abstrakcyjny w postaci drzewa komponentów:

!Component Tree](/images/components.png)

W Vue komponent jest zasadniczo instancją Vue z wstępnie zdefiniowanymi opcjami. Rejestracja komponentu w Vue jest prosta:

```js
/Zdefiniuj nowy komponent zwany todo-item
Vue.component('todo-item', {\i0}
  szablon: "<li>To jest todo</li>
})

var app = nowy Vue(...)
```

Teraz możesz skomponować go w szablonie innego komponentu:

```html
<ol>
  <!-- Stwórzcie instancję komponentu todo-item -->
  <todo-item><</todo-item>>
</ol>
```

Ale to sprawiłoby, że ten sam tekst byłby dla każdego todo, co nie jest super interesujące. Powinniśmy być w stanie przekazywać dane z zakresu rodzicielskiego na komponenty dziecięce. Zmodyfikujmy definicję komponentu tak, aby akceptowała ona [prop](components.html#Props):

```js
Vue.component('todo-item', {\i0}
  /Teraz komponent "todo-item" akceptuje
  /"rekwizyt", który jest jak niestandardowy atrybut.
  /Ten rekwizyt nazywa się todo.
  rekwizyty: ["todo"]
  szablon: "<li>{{todo.text }}</li>
})
```

Teraz możemy przekazać todo do każdego powtórzonego komponentu używając `v-bind`:

```html
<div id="app-7">
  <ol>
    <!--
      Teraz dostarczamy każdemu obiektowi todo-item z todo
      jest reprezentacyjny, więc jego zawartość może być dynamiczna.
      Musimy również zapewnić każdemu komponentowi "klucz",
      co zostanie wyjaśnione później.
    -->
    <todo-item
      v-for="pozycja w spisie artykułów spożywczych"
      v-bind:todo="item"
      v-bind:key="item.id"
    ></todo-item>
  </ol>
</div>
```
```js
Vue.component('todo-item', {\i0}
  rekwizyty: ['todo']
  szablon: "<li>{{todo.text }}</li>
})

var app7 = nowy Vue({\i0}
  el: "#app-7",
  dane: {
    Lista zakupów: [
      { id: 0, tekst: "Warzywa" },
      { id: 1, tekst: "Cheese" },
      { id: 2, tekst: "Co jeszcze ludzie mają jeść"}
    ]
  }
})
```
{% surowy%}
<div id="app-7" class="demo">
  <ol>
    <todo-item v-for="item in groceryList" v-bind:todo="item" :key="item.id"></todo-item>
  </ol>
</div>
<scriptum>
Vue.component('todo-item', {\i0}
  rekwizyty: ['todo']
  szablon: "<li>{{todo.text }}</li>
})
var app7 = nowy Vue({\i0}
  el: "#app-7",
  dane: {
    Lista zakupów: [
      { id: 0, tekst: "Warzywa" },
      { id: 1, tekst: "Cheese" },
      { id: 2, tekst: "Co jeszcze ludzie mają jeść"}
    ]
  }
})
</scriptum>
{% endraw %}

Jest to wymyślony przykład, ale udało nam się rozdzielić naszą aplikację na dwie mniejsze jednostki, a dziecko jest w miarę dobrze oddzielone od rodzica za pomocą interfejsu rekwizytowego. Teraz możemy jeszcze bardziej ulepszyć nasz `<todo-item>` komponent z bardziej złożonym szablonem i logiką bez wpływu na aplikację rodzicielską.

W dużej aplikacji, konieczne jest podzielenie całej aplikacji na komponenty, aby uczynić rozwój łatwym do zarządzania. Porozmawiamy dużo więcej o komponentach [w dalszej części przewodnika](components.html), ale oto (wyimaginowany) przykład, jak może wyglądać szablon aplikacji z komponentami:

```html
<div id="app">
  <app-nav></app-nav>
  <app-view>
    <app-sidebar></app-sidebar>
    <app-content></app-content>
  </app-view>
</div>
```

### Relacja do elementów niestandardowych

Być może zauważyłeś, że elementy Vue są bardzo podobne do **Custom Elements**, które są częścią [Web Components Spec](https://www.w3.org/wiki/WebComponents/). To dlatego, że składnia komponentów Vue'a jest luźno modelowana po specyfikacji. Na przykład, komponenty Vue implementują [Slot API](https://github.com/w3c/webcomponents/blob/gh-pages/proposals/Slots-Proposal.md) i `jest` specjalny atrybut. Jednakże, istnieje kilka kluczowych różnic:

1. Web Components Spec został sfinalizowany, ale nie jest natywnie zaimplementowany w każdej przeglądarce. Safari 10.1+, Chrome 54+ i Firefox 63+ natywnie wspierają komponenty WWW. Dla porównania, komponenty Vue nie wymagają żadnych polifiletów i działają konsekwentnie we wszystkich obsługiwanych przeglądarkach (IE9 i wyższych). W razie potrzeby komponenty Vue mogą być również owinięte w natywny niestandardowy element.

2. Komponenty Vue zapewniają ważne funkcje, które nie są dostępne w zwykłych niestandardowych elementach, a w szczególności przepływ danych pomiędzy komponentami, niestandardową komunikację zdarzeń i budowanie integracji narzędzi.

Chociaż Vue nie używa wewnętrznie elementów niestandardowych, ma [wielką interoperacyjność] (https://custom-elements-everywhere.com/#vue), jeśli chodzi o konsumpcję lub dystrybucję jako elementy niestandardowe. Vue CLI wspiera również budowanie komponentów Vue, które rejestrują się jako natywne elementy niestandardowe.

## Gotowy na więcej?

Pokrótce przedstawiliśmy najbardziej podstawowe funkcje rdzenia Vue.js - reszta tego przewodnika obejmie je i inne zaawansowane funkcje z dużo drobniejszymi szczegółami, więc upewnij się, że przeczytasz to wszystko!

<div id="video-modal" class="modal"><div class="video-space" style="padding": 56.25% 0 0 0; pozycja: względna;"><frame src="https://player.vimeo.com/video/247494684?dnt=1" style="height: 100%; left: 0; pozycja: absolute; top: 0; szerokość: 100%; margines: 0" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></div><script src="https://player.vimeo.com/api/player.js"></script><p class="modal-text">Video by <a href="https://www.vuemastery.com" target="_blank" rel="sponsorowany noopener" title="Vue.js Kursy na Vue Mastery">Vue Mastery</a>. Watch Vue Mastery's free <a href="https://www.vuemastery.com/courses/intro-to-vue-js/vue-instance/" target="_blank" rel="sponsorowany noopener" title="Vue.js Kursy na Vue Mastery">Intro do Vue course</a>.</div>.
