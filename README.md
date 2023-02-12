# Wprowadzenie do Grid Layout w HTML i CSS
Grid Layout jest jednym z najbardziej potężnych narzędzi do projektowania stron internetowych. Pozwala on na precyzyjne kontrolowanie położenia i rozmiaru elementów na stronie, co pozwala na stworzenie bardziej zaawansowanych i responsywnych projektów. W tym artykule omówimy podstawy korzystania z Grid Layout w HTML i CSS.

# Utworzenie siatki za pomocą Grid Layout
Aby skorzystać z Grid Layout, należy najpierw ustawić właściwość display na grid dla kontenera, który będzie naszą siatką. Następnie, możemy określić ilość i szerokość kolumn i wierszy, korzystając z właściwości grid-template-columns i grid-template-rows. Wartość grid-template-columns może być wyrażona w pikselach, procentach lub jednostkach fr, które dzielą siatkę na równe części.

```
.container {
  display: grid;
  grid-template-columns: 2fr 1fr;
  grid-template-rows: auto;
}
```
W powyższym kodzie ustawiliśmy siatkę na dwa kolumny o szerokości 2 i 1 jednostek fr, oraz automatycznie dostosowującą się wysokość wierszy.

# Umieszczanie elementów w siatce
Po utworzeniu siatki, możemy umieścić elementy w konkretnych komórkach siatki, używając właściwości grid-column i grid-row. Wartości tych właściwości odpowiadają indeksom kolumn i wierszy w naszej siatce.

```
.item1 {
  grid-column: 1 / 2;
  grid-row: 1 / 2;
}

.item2 {
  grid-column: 2 / 3;
  grid-row: 1 / 2;
}
```

W powyższym kodzie .item1 zostanie umieszczony w pierwszej kolumnie i pierwszym wierszu siatki, a .item2 zostanie umieszczony w drugiej kolumnie i pierwszym wierszu siatki. To jest możliwe dzięki zastosowaniu grid-template-columns, który określa liczbę i szerokość kolumn w naszej siatce. W naszym przypadku ustawiliśmy dwie kolumny o szerokości 300px i auto, co oznacza, że pierwsza kolumna będzie mieć stałą szerokość 300px, a druga kolumna będzie automatycznie dostosowywać swoją szerokość do zawartości.

Kolejną ważną rzeczą jest ustawienie grid-template-rows na repeat(2, 1fr), co oznacza, że nasza siatka będzie składać się z dwóch rzędów o takiej samej wysokości (1fr oznacza proporcjonalną część dostępnego obszaru).

Zwróćmy uwagę na ustawienie display: grid na elemencie nadrzędnym, co oznacza, że wszystkie jego dzieci będą ułożone w siatce.

Na końcu ustawiliśmy styl dla naszych elementów .item1 i .item2, aby wyśrodkować tekst wewnątrz każdego z nich. Ponadto, dla mniejszych rozdzielczości (np. telefonów) zastosowaliśmy media query i ustawiliśmy text-align na center, aby tekst i obraz były wyśrodkowane na ekranie.

W ten prosty sposób możemy zbudować responsywną stronę z wykorzystaniem CSS Grid Layout. To tylko wierzchołek góry lodowej możliwości, jakie daje nam ten layout, ale już teraz możemy zauważyć jego wygodę i elastyczność. Spróbuj samodzielnie zbudować coś więcej i ciesz się możliwościami, jakie daje CSS Grid Layout!
