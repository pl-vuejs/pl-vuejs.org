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

### Style

- **Headings should describe problems**, not solutions. For example, a less effective heading might be "Using props", because it describes a solution. A better heading might be "Passing Data to Child Components with Props", because it provides the context of the problem props solve. Users won't really start paying attention to the explanation of a feature until they have some idea of why/when they'd use it.
- **When you assume knowledge, declare it** at the beginning and link to resources for less common knowledge that you're expecting.
- **Introduce only one new concept at a time whenever possible** (including both text and code examples). Even if many people are able to understand when you introduce more than one, there are also many who will become lost - and even those who don't become lost will have depleted more of their cognitive capacity.
- **Avoid special content blocks for tips and caveats when possible.** It's generally preferable to blend these more naturally into the main content, e.g. by building on examples to demonstrate an edge case.
- **Don't include more than two interwoven tips and caveats per page.** If you find that more than two tips are needed in a page, consider adding a caveats section to address these issues. The guide is meant to be read straight through, and tips and caveats can be overwhelming or distracting to someone trying to understand the base concepts.
- **Avoid appeals to authority** (e.g. "you should do X, because that's a best practice" or "X is best because it gives you full separation of concerns"). Instead, demonstrate with examples the specific human problems caused and/or solved by a pattern.
- **When deciding what to teach first, think of what knowledge will provide the best power/effort ratio.** That means teaching whatever will help users solve the greatest pains or greatest number of problems, with the relatively least effort to learn. This helps learners feel smart, powerful, and curious, so their cognitive capacity will drain more slowly.
- **Unless the context assumes a string template or build system, only write code that works in any environment by the software (e.g. Vue, Vuex, etc).**
- **Show, don't tell.** For example, "To use Vue on a page, you can add this to your HTML" (then show the script tag), instead of "To use Vue on a page, you can add a script element with a src attribute, the value of which should be a link to Vue's compiled source".
- **Almost always avoid humor (for English docs)**, especially sarcasm and pop culture references, as it doesn't translate well across cultures.
- **Never assume a more advanced context than you have to.**
- **In most cases, prefer links between sections of the docs over repeating the same content in multiple sections.** Some repetition in content is unavoidable and even essential for learning. However, too much repetition also makes the docs more difficult to maintain, because a change in the API will require changes in many places and it's easy to miss something. This is a difficult balance to strike.
- **Specific is better than generic.** For example, a `<BlogPost>` component example is better than `<ComponentA>`.
- **Relatable is better than obscure.** For example, a `<BlogPost>` component example is better than `<CurrencyExchangeSettings>`.
- **Be emotionally relevant.** Explanations and examples that relate to something people have experience with and care about will always be more effective.
- **Always prefer simpler, plainer language over complex or jargony language.** For example:
  - "you can use Vue with a script element" instead of "in order to initiate the usage of Vue, one possible option is to actually inject it via a script HTML element"
  - "function that returns a function" instead of "higher order function"
- **Avoid language that invalidate struggle**, such as "easy", "just", "obviously", etc. For reference, see [Words To Avoid in Educational Writing](https://css-tricks.com/words-avoid-educational-writing/).

### Grammar

- **Avoid abbreviations** in writing and code examples (e.g. `attribute` is better than `attr`, `message` is better than `msg`), unless you are specifically referencing an abbreviation in an API (e.g. `$attrs`). Abbreviation symbols included on standard keyboards (e.g. `@`, `#`, `&`) are OK.
- **When referencing a directly following example, use a colon (`:`) to end a sentence**, rather than a period (`.`).
- **Use the Oxford comma** (e.g. "a, b, and c" instead of "a, b and c"). ![Why the Oxford comma is important](https://raw.githubusercontent.com/vuejs/vuejs.org/master/src/images/oxford-comma.jpg)
- **When referencing the name of a project, prioritize the broader conventions of English over internal branding conventions of that project.** For example, "webpack" and "npm" both disregard conventions such as "always start a word at the beginning of a sentence with a capital letter", "project names always use Title Case", and "acronyms are always capitalized". Instead, always write "Webpack and NPM" to provide a more consistent experience in the docs and avoid sentences like "If you don't want to use Vue CLI, you can use webpack or Rollup directly by installing them via npm or Yarn".
- **Use Title Case for headings** - at least for now, since it's what we use through the rest of the docs. There's research suggesting that sentence case (only first word of the heading starts with a capital) is actually superior for legibility and also reduces the cognitive overhead for documentation writers, since they don't have to try to remember whether to capitalize words like "and", "with", and "about".
- **Don't use emojis (except in discussions).** Emojis are cute and friendly, but they can be a distraction in documentation and some emoji even convey  different meanings in different cultures.

## Iteration & Communication

- **Excellence comes from iteration.** First drafts are always bad, but writing them is a vital part of the process. It's extremely difficult to avoid the slow progression of Bad -> OK -> Good -> Great -> Inspiring -> Transcendent.
- **Only wait until something is "Good" before publishing.** The community will help you push it further down the chain.
- **Try not to get defensive when receiving feedback.** Our writing can be very personal to us, but if we get upset with the people who help us make it better, they will either stop giving feedback or start limiting the kind of feedback they give.
- **Proof-read your own work before showing it to others.** If you show someone work with a lot of spelling/grammar mistakes, you'll get feedback about spelling grammar/mistakes instead of more valuable notes about whether the writing is achieving your goals.
- **When you ask people for feedback, tell reviewers what:**
  - **you're trying to do**
  - **your fears are**
  - **balances you're trying to strike**
- **When someone reports a problem, there is almost always a problem**, even if the solution they proposed isn't quite right. Keep asking follow-up questions to learn more.
- People need to feel safe asking questions when contributing/reviewing content. Here's how you can do that:
  - **Thank people for their contributions/reviews, even if you're feeling grumpy.** For example:
    - "Great question!"
    - "Thanks for taking the time to explain. 🙂"
    - "This is actually intentional, but thanks for taking the time to contribute. 😊"
  - **Listen to what people are saying and mirror if you're not sure you're understanding correctly.** This can help validate people's feelings and experiences, while also understanding if *you're* understanding *them* correctly.
  - **Use a lot of positive and empathetic emojis.** It's always better to seem a little strange than mean or impatient.
  - **Kindly communicate rules/boundaries.** If someone behaves in a way that's abusive/inappropriate, respond only with kindness and maturity, but also make it clear that this behavior is not acceptable and what will happen (according to the code of conduct) if they continue behaving poorly.

## Resources

### Software

- [Grammarly](https://www.grammarly.com/): Desktop app and browser extension for checking spelling and grammar (though grammar checking doesn't catch everything and occasionally shows a false positive).
- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker): An extension for VS Code to help you check spelling within markdown and code examples.

### Books

- [On Writing Well](https://www.amazon.com/Writing-Well-30th-Anniversary-Nonfiction-ebook/dp/B0090RVGW0) (see [popular quotes](https://www.goodreads.com/work/quotes/1139032-on-writing-well-the-classic-guide-to-writing-nonfiction))
- [Bird by Bird](https://www.amazon.com/Bird-Some-Instructions-Writing-Life/dp/0385480016) (see [popular quotes](https://www.goodreads.com/work/quotes/841198-bird-by-bird-some-instructions-on-writing-and-life))
- [Cognitive Load Theory](https://www.amazon.com/Cognitive-Explorations-Instructional-Performance-Technologies/dp/144198125X/)
