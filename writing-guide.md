# Vue Docs Writing Guide

Pisanie dokumentacji jest ćwiczeniem z empatii. Nie opisujemy obiektywnej rzeczywistości - kod źródłowy już to robi. Naszym zadaniem jest pomoc w kształtowaniu relacji między użytkownikami a ekosystemem Vue'a. Ten stale rozwijający się przewodnik zawiera pewne zasady i zalecenia, jak to zrobić w sposób spójny w ramach ekosystemu Vue.

## Zasady

- **Alement nie istnieje, dopóki nie jest dobrze udokumentowany.**
- **Chodzi o zdolności poznawcze użytkownika (tzn. moc mózgu).** Kiedy użytkownik zaczyna czytać, zaczyna od pewnej ilości ograniczonej mocy mózgu, a kiedy się kończy, przestaje się uczyć.**
  - Zdolności poznawcze są **szybciej zużywane** przez złożone zdania, konieczność uczenia się więcej niż jednego pojęcia na raz, oraz abstrakcyjne przykłady, które nie odnoszą się bezpośrednio do pracy użytkownika.
  - Zdolności poznawcze są **wolniej zużywane**, kiedy pomagamy im czuć się stale mądrymi, silnymi i ciekawymi. Rozbijanie rzeczy na strawialne kawałki i myślenie o przepływie dokumentu może pomóc w utrzymaniu ich w tym stanie.
- **Zawsze staramy się patrzeć z perspektywy użytkownika.** Kiedy coś dokładnie rozumiemy, staje się to dla nas oczywiste. Nazywa się to _klątwa wiedzy_. Aby napisać dobrą dokumentację, spróbuj zapamiętać, co najpierw musiałeś wiedzieć, ucząc się tego pojęcia. Jakiego żargonu musiałeś się nauczyć? Co źle zrozumiałeś? Co zajęło ci dużo czasu, aby naprawdę zrozumieć? Dobra dokumentacja spotyka użytkowników tam, gdzie są. Pomocne może być przećwiczenie wyjaśniania koncepcji ludziom osobiście, zanim
- **Opisz najpierw _problem_, potem rozwiązanie.** Zanim pokażesz jak działa funkcja, ważne jest, aby wyjaśnić dlaczego istnieje. W przeciwnym razie użytkownicy nie będą mieli kontekstu, aby wiedzieć, czy ta informacja jest dla nich ważna (czy jest to problem, którego doświadczają?) lub z jaką wcześniejszą wiedzą/doświadczeniem ją połączyć.
- **Pisząc, nie bój się zadawać pytań**, _szczególnie_ jeśli boisz się, że mogą być "głupi". Bycie bezbronnym jest trudne, ale tylko w ten sposób możemy pełniej zrozumieć, co musimy wyjaśnić.
- **Bądź zaangażowany w dyskusje o funkcjach.** Najlepsze API pochodzą z rozwoju opartego na dokumentacji, gdzie budujemy funkcje, które są łatwe do wyjaśnienia, zamiast próbować dowiedzieć się jak je później wyjaśnić. Wcześniejsze zadawanie pytań (szczególnie "głupich" pytań) często pomaga ujawnić zamieszanie, niespójności i problematyczne zachowanie, zanim złamana zmiana będzie konieczna do ich naprawienia.

## Organizacja

- **Instalacja/Integracja** Dostarczenie dokładnego przeglądu, jak zintegrować oprogramowanie do tak wielu różnych rodzajów projektów, jak to konieczne.
- **Instalacja/Integracja**: Daj dokładny przegląd, jak zintegrować oprogramowanie z tak wieloma różnymi rodzajami projektów, jak to konieczne:
  - Przedstawienie mniej niż 10-minutowego przeglądu problemów, które projekt rozwiązuje i dlaczego istnieje.
  - Przedstawienie mniej niż 30-minutowego przeglądu problemów rozwiązywanych przez projekt i sposobu ich rozwiązywania, w tym kiedy i dlaczego należy korzystać z projektu i kilku prostych przykładów kodu. Na końcu, link do strony instalacyjnej oraz do początku przewodnika Essentials Guide.
- **Przewodnik**: Sprawić, by użytkownicy czuli się inteligentni, silni i ciekawi, a następnie utrzymać ten stan, tak by zachować motywację i zdolności poznawcze do dalszego uczenia się. Strony Przewodnika powinny być czytane kolejno, więc generalnie powinny być uporządkowane od najwyższego do najniższego stosunku mocy do wysiłku.
  - **Essentials**: Czytanie Essentials nie powinno trwać dłużej niż 5 godzin, choć krótsze jest lepsze. Jego celem jest dostarczenie 20% wiedzy, która pomoże użytkownikom obsługiwać 80% przypadków użycia. Essentials może zawierać linki do bardziej zaawansowanych przewodników i API, jednak w większości przypadków należy ich unikać. Kiedy są one udostępniane, należy również podać kontekst, aby użytkownicy wiedzieli, czy powinni skorzystać z tego linku przy pierwszym czytaniu. W przeciwnym razie wielu użytkowników kończy się na wyczerpaniu swoich możliwości poznawczych - podskakiwanie za linkami, starając się w pełni poznać każdy aspekt danej funkcji przed przejściem dalej, a w rezultacie nigdy nie kończy tego pierwszego czytania esejów. Pamiętaj, że płynne czytanie jest ważniejsze od bycia dokładnym. Chcemy dać ludziom informacje, których potrzebują, aby uniknąć frustrujących doświadczeń, ale zawsze mogą wrócić i poczytać dalej, lub Google'owi mniej powszechny problem, gdy go napotkają.
  - **Advanced** Podczas gdy Essentials pomaga ludziom radzić sobie z ~80% przypadków użycia, kolejne przewodniki pomagają dotrzeć do 95% przypadków użycia, plus bardziej szczegółowe informacje o innych niż istotne funkcjach (np. przejścia, animacje), bardziej złożone funkcje wygody (np. miksiny, dyrektywy niestandardowe), oraz ulepszenia doświadczenia dev (np. JSX, wtyczki). Ostatnie 5% przypadków użycia, które są bardziej niszowe, złożone i/lub podatne na nadużycia, zostanie pozostawione w książce kucharskiej i odnośniku API, do których można się odwołać z tych zaawansowanych przewodników.
- **Reference/API**: Podaj pełną listę funkcji, w tym informacje o typie, opis problemu, który każdy z nich rozwiązuje, przykłady każdej kombinacji opcji oraz linki do przewodników, przepisów kulinarnych i innych wewnętrznych zasobów, dostarczając więcej szczegółów. W odróżnieniu od innych stron, ta nie jest przeznaczona do czytania od góry do dołu, więc można podać wiele szczegółów. Odnośniki te muszą być również łatwiejsze do pominięcia niż przewodniki, więc format powinien być bliższy hasłom słownikowym niż formatowi opowiadania historii w przewodnikach.
- **Migracje**:
  - **Wersje**: Gdy wprowadzane są ważne zmiany, przydatne jest dołączenie pełnej listy zmian, w tym szczegółowe wyjaśnienie, dlaczego zmiana została wprowadzona i jak migrować swoje projekty.
  - **Z innych projektów**: Jak ten program porównuje się z podobnym oprogramowaniem? Jest to ważne, aby pomóc użytkownikom zrozumieć, jakie dodatkowe problemy możemy dla nich rozwiązać lub stworzyć, i w jakim stopniu mogą przekazać wiedzę, którą już posiadają.
- **Style Guide**: Istnieją z konieczności pewne kluczowe elementy w rozwoju, które wymagają decyzji, ale nie są rdzeniem API. Przewodnik stylów dostarcza wykształconych, opiniotwórczych rekomendacji, które pomogą w podjęciu tych decyzji. Nie powinny być one podejmowane na ślepo, ale mogą pomóc zespołom zaoszczędzić czas poprzez dostosowanie się do mniejszych szczegółów.
- **Książka kucharska**: Przepisy w książce kucharskiej są napisane z pewnym założeniem znajomości Vue'a i jego ekosystemu. Każdy z nich jest wysoce ustrukturyzowanym dokumentem, w którym omawia się pewne wspólne szczegóły dotyczące realizacji, z którymi może zetknąć się dev Vue.

## Pisanie i gramatyka

### Styl

- **Nagłówki powinny opisywać problemy**, a nie rozwiązania. Na przykład, mniej efektywnym nagłówkiem może być "Użycie rekwizytów", ponieważ opisuje on rozwiązanie. Lepszym nagłówkiem może być "Przekazywanie danych do komponentów dziecięcych z rekwizytami", ponieważ podaje kontekst rozwiązania problemu z rekwizytami. Użytkownicy nie zaczną zwracać uwagi na wyjaśnienie danej funkcji, dopóki nie dowiedzą się, dlaczego i kiedy by jej użyli.
- **Kiedy zakładasz wiedzę, zgłoś ją** na początku i połącz się z zasobami dla mniej powszechnej wiedzy, której oczekujesz.
- **W miarę możliwości wprowadzaj tylko jedną nową koncepcję na raz** (włączając w to zarówno tekst, jak i przykłady kodu). Nawet jeśli wielu ludzi jest w stanie zrozumieć, gdy wprowadzisz więcej niż jedno, jest też wielu, którzy staną się zagubieni - i nawet ci, którzy się nie zgubią, wyczerpią więcej swoich zdolności poznawczych.
- **Unikaj specjalnych bloków z treściami zawierającymi wskazówki i zastrzeżenia, jeśli to możliwe.** Ogólnie rzecz biorąc, lepiej jest połączyć je w bardziej naturalny sposób z główną treścią, np. opierając się na przykładach, aby pokazać skrajny przypadek.
- **Nie należy umieszczać więcej niż dwóch przeplatających się końcówek i zastrzeżeń na stronie.** Jeśli okaże się, że na jednej stronie potrzebne są więcej niż dwie końcówki, należy rozważyć dodanie sekcji z zastrzeżeniami, aby rozwiązać te problemy. Przewodnik jest przeznaczony do przeczytania od razu, a wskazówki i zastrzeżenia mogą być przytłaczające lub rozpraszające dla kogoś, kto próbuje zrozumieć podstawowe pojęcia.
- **Unikaj odwołań do autorytetu** (np. "powinieneś zrobić X, bo to jest najlepsza praktyka" lub "X jest najlepsze, bo daje Ci pełną separację obaw"). Zamiast tego pokaż na przykładach konkretne ludzkie problemy spowodowane i/lub rozwiązane za pomocą wzorca.
- **Podejmując decyzję o tym, czego uczyć w pierwszej kolejności, zastanów się, jaka wiedza zapewni najlepszy stosunek siły do wysiłku.** Oznacza to nauczanie tego, co pomoże użytkownikom rozwiązać największe bóle lub największą liczbę problemów, przy stosunkowo najmniejszym wysiłku do nauki. Dzięki temu uczący się czują się inteligentni, silni i ciekawi, więc ich zdolności poznawcze będą wolniej odpływać.
- **Bez względu na to, że kontekst zakłada szablon łańcucha lub system budowania, piszemy tylko kod, który działa w dowolnym środowisku przez oprogramowanie (np. Vue, Vuex, itp.).**
- **Pokaż, nie mów.** Na przykład, "Aby użyć Vue na stronie, możesz dodać to do swojego kodu HTML" (następnie pokaż tag skryptu), zamiast "Aby użyć Vue na stronie, możesz dodać element skryptu z atrybutem src, którego wartość powinna być linkiem do skompilowanego źródła Vue".
- **Zawsze unikaj humoru (dla angielskich docs)**, zwłaszcza sarkazmu i odniesień do popkultury, ponieważ nie przekłada się on dobrze na inne kultury.
- **Nigdy nie zakładaj bardziej zaawansowanego kontekstu niż trzeba.**
- **Większość przypadków preferuje linki pomiędzy sekcjami dokumentów niż powtarzanie tej samej treści w wielu sekcjach.** Niektóre powtórzenia treści są nieuniknione, a nawet niezbędne do nauki. Jednak zbyt duża ilość powtórzeń utrudnia również utrzymanie dokumentacji, ponieważ zmiana API będzie wymagała zmian w wielu miejscach i łatwo coś przeoczyć. Jest to trudna do osiągnięcia równowaga.
- **Specyficzny jest lepszy niż ogólny.** Na przykład, `<BlogPost>` przykład komponentu jest lepszy niż `<ComponentA>`.
- Na przykład, przykład komponentu `<BlogPost>` jest lepszy niż `<ComponentA>`.
- **Bądź istotny emocjonalnie.** Wyjaśnienia i przykłady, które odnoszą się do czegoś, z czym ludzie mają doświadczenie i o co się troszczą będą zawsze bardziej skuteczne.
- **Zawsze wolą prostszy, prosty język od skomplikowanego lub żargonowego.** Na przykład:
  - "możesz użyć Vue z elementem skryptu" zamiast "aby zainicjować użycie Vue, jedną z możliwych opcji jest rzeczywiste wstrzyknięcie go za pomocą skryptowego elementu HTML".
  - "funkcja, która zwraca funkcję" zamiast "funkcja wyższego rzędu".
- **Unikaj języka, który unieważnia walkę** Więcej informacji na ten temat można znaleźć w książce [Słowa, których należy unikać w pisaniu edukacyjnym] (https://css-tricks.com/words-avoid-educational-writing/).
  
### Gramatyka

- **Unikaj skrótów** w pisaniu i przykładach kodu (np. `attribute` jest lepszy niż `attr`, `message` jest lepszy niż `msg`), chyba że specjalnie odnosisz się do skrótu w API (np. `$attrs`). Symbole skrótów zawarte na standardowych klawiaturach (np. `@`, `#`, `&`) są OK.
- **Odwołując się do bezpośrednio następującego przykładu, użyj dwukropka (`:`), aby zakończyć zdanie**, a nie kropki (`.`).
- **Użyj przecinka Oxford** (np. "a, b, i c" zamiast "a, b i c"). ![Dlaczego przecinek Oxford jest ważny](https://raw.githubusercontent.com/vuejs/vuejs.org/master/src/images/oxford-comma.jpg)
- **Odwołując się do nazwy projektu, pierwszeństwo mają szersze konwencje języka angielskiego przed wewnętrznymi konwencjami brandingowymi tego projektu.** Na przykład, "webpack" i "npm" nie uwzględniają konwencji takich jak "zawsze zaczynać słowo na początku zdania dużą literą", "nazwy projektów zawsze używają tytułu Case", a "akronimy są zawsze pisane wielką literą". Zamiast tego, zawsze pisz "Webpack i NPM", aby zapewnić bardziej spójne doświadczenie w dokumentach i uniknąć zdań takich jak "Jeśli nie chcesz używać Vue CLI, możesz użyć webpack lub Rollup bezpośrednio, instalując je przez npm lub Yarn".
- **Użyj tytułu Case dla nagłówków** - przynajmniej na razie, ponieważ jest to to to, czego używamy przez resztę docs. Istnieją badania sugerujące, że przypadek zdania (tylko pierwsze słowo nagłówka zaczyna się od dużej litery) jest w rzeczywistości lepszy pod względem czytelności, a także zmniejsza koszty poznawcze dla autorów dokumentacji, ponieważ nie muszą oni starać się zapamiętywać, czy kapitalizować słowa takie jak "i", "z" i "o".
- **Nie używaj emojis (z wyjątkiem dyskusji).** Emojis są słodkie i przyjazne, ale mogą rozpraszać uwagę w dokumentacji, a niektóre emojis przekazują nawet różne znaczenia w różnych kulturach.

## Iteracja i komunikacja

- **Wspaniale pochodzi z iteracji.** Pierwsze szkice są zawsze złe, ale pisanie ich jest bardzo ważne. Bardzo trudno jest uniknąć powolnego postępu Złego -> OK -> Dobrego -> Wielkiego -> Inspirującego -> Transcendentnego.
- **Poczekaj tylko, aż coś będzie "Dobre" przed publikacją.** Społeczność pomoże ci zepchnąć to dalej w dół łańcucha.
- **Spróbuj nie bronić się przed otrzymywaniem informacji zwrotnych.** Nasze pisanie może być dla nas bardzo osobiste, ale jeśli zdenerwujemy się ludźmi, którzy pomagają nam to poprawić, albo przestaną udzielać informacji zwrotnych, albo zaczną ograniczać ich rodzaj.
- Jeśli pokażesz komuś pracę z dużą ilością błędów ortograficznych/gramatycznych, dostaniesz informację zwrotną o gramatyce/błędach w pisowni, a nie bardziej wartościowe notatki o tym, czy pisanie osiąga Twoje cele.
- **Kiedy prosisz ludzi o informację zwrotną, powiedz recenzentom co:**
  - **próbujesz zrobić**
  - **Twoje obawy są**
  - **równowaga, którą próbujesz osiągnąć**
- **Kiedy ktoś zgłasza problem, prawie zawsze jest problem**, nawet jeśli rozwiązanie, które zaproponował, nie jest do końca właściwe. Zadawaj kolejne pytania, aby dowiedzieć się więcej.
- Ludzie muszą czuć się bezpiecznie, zadając pytania podczas tworzenia i przeglądania treści. Oto jak można to zrobić:
  - **Podziękuj ludziom za ich wkład/recenzje, nawet jeśli czujesz się zrzędliwy.** Na przykład:
    - "Wspaniałe pytanie!"
    - "Dzięki za poświęcenie czasu na wyjaśnienie. 🙂"
    - "To jest rzeczywiście celowe, ale dziękuję za poświęcenie czasu na wniesienie wkładu. 😊"
  - Posłuchaj, co ludzie mówią i odzwierciedlaj, jeśli nie jesteś pewien, czy dobrze rozumiesz.** To może pomóc w potwierdzeniu uczuć i doświadczeń ludzi, a także w zrozumieniu, czy *you're* rozumiesz *them* poprawnie.
  - **Używaj dużo pozytywnego i empatycznego emojis.** Zawsze lepiej wydawać się trochę dziwnym niż złym czy niecierpliwym.**
  - *Przejmij zasady/ograniczenia.** Jeśli ktoś zachowuje się w sposób obraźliwy/nieodpowiedni, zareaguj tylko życzliwie i dojrzale, ale również daj jasno do zrozumienia, że takie zachowanie jest niedopuszczalne i co się stanie (zgodnie z kodeksem postępowania), jeśli nadal będzie zachowywał się źle.

## Zasoby

### Software

- [Grammarly](https://www.grammarly.com/): Pulpitowa aplikacja i rozszerzenie przeglądarki do sprawdzania pisowni i gramatyki (chociaż sprawdzanie gramatyki nie wychwytuje wszystkiego i czasami pokazuje fałszywy wynik pozytywny).
- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker): Rozszerzenie dla VS Code pomagające sprawdzać pisownię w ramach przykładów z markdown i kodu.

### Książki

- [O studni pisarskiej](https://www.amazon.com/Writing-Well-30th-Anniversary-Nonfiction-ebook/dp/B0090RVGW0) (patrz [popularne cytaty](https://www.goodreads.com/work/quotes/1139032-on-writing-well-the-classic-guide-to-writing-nonfiction))
- [Bird by Bird](https://www.amazon.com/Bird-Some-Instructions-Writing-Life/dp/0385480016) (patrz [popularne cytaty](https://www.goodreads.com/work/quotes/841198-bird-by-bird-some-instructions-on-writing-and-life))
- [Teoria Obciążenia Poznawczego](https://www.amazon.com/Cognitive-Explorations-Instructional-Performance-Technologies/dp/144198125X/)
