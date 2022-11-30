Визначення стану застосунку можна розбити на 3 різних типи стану
  - Local state
    Належить окремому компоненту. Should be managed component-internal with useState()/ useReducer()
  - Cross-component state
    Стан, який впливає на декілька компонентів. Requires 'prop chains'/'prop drilling'
  - App-Wide state
    Стан, який стосується всього застосунку/всіх або майже всіх компонентів.
     Requires 'prop chains'/'prop drilling' OR React Context or Redux

За рахунок того, що компоненти встановлюють підписку на центральне сховище, реалізація якого надається *Redux* бібліотекою, вони знатимуть, коли дані в ньому змінюються і реагують на це, оновлюючи UI.
Також важливо розуміти, шо компоненти напряму не мають можливості впливати на дані в сховищі. Це відбувається за рахунок _reducer function_. Ця функція загалом є загальною концепцією, за якою такі функції отримують якісь дані на вхід і трансформуються їх певним чином, наприклад отримують масив чисел і повертають суму цих чисел.
