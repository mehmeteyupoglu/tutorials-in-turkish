#Temel Hooklar

Hooklar React uygulamaları içerisinde class bileşenleri kullanmak zorunda olmadan state oluşturmayı ve bunları değiştirmeyi sağlayan yapılardır. Hooklar ile birlikte React, fonksiyonel programlama prensiplerini daha fazla kullanmaya başladı. Ayrıca, hooklar `props`, `context`, `refs`, `lifecycle` gibi kavramlara doğrudan ulaşabilmeyi sağlar.

Temel olarak hook kullanımını `useState` hooku ile göstermeye başlayabiliriz:

`useState`, class bileşenine ihtiyaç duymadan bir fonksiyon açarak veri(state) tanımlamamızı sağlayan yapıdır.

Örnek: `useState`

```
import React, { useState } from 'react';

function Example() {
  // "count" adında yeni bir state değişkeni tanımlayın.
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
```

`useState` ile birden fazla hook tanımlanabilir:

Örnek: `useState` birden fazla hook.

`useEffect` hooku ile birlikte `componentDidMount`, `componentDidUpdate` ve `componentWillUnmount` lifecycle metotlarıyla aynı işi yapar fakat bunlar `useEffect` altında birleştirilmiştir.

##Temel kurallar:

- Hooklar class bileşenler altında kullanılmaz
- Hooklar yalnız react fonksiyonları ile kullanılabilir
- Hookların kendisi de bir fonksiyon olduğu için ancak bunları çağırarak kullanabiliriz. Fakat hookları react bileşenlerinde en üstte çağırmak gerekir. Döngüler, koşullar ve iç içe fonksiyonlar içinde hooklarınızı çağırmayın
