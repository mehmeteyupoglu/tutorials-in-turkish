# Styled Components

Styled components React uygulamalarında hızlıca stillendirme işlemleri yapabileceğiniz bir kütüphanedir.
Projenize dahil etmek için aşağıdaki komut satırını eklemelesiniz:

`npm install --save styled-components`

Styled components stillendirme yapabilmeniz için react bileşeni oluşturur ve bu bileşeni stillendirmek istediğiniz bileşene sararak stil işlemini yapabilirsiniz.

```
    // Title adında bir bileşen oluşturup bir <h1> etiketi stillendirelim
    const Title = styled.h1`
      font-size: 1.5em;
      text-align: center;
      color: palevioletred;
    `;

    // Wrapper adında bir bileşen oluşturarak bir section etiketi stillendirelim
    const Wrapper = styled.section`
      padding: 4em;
      background: papayawhip;
    `;

    // Oluşturduğumuz bu bileşenleri React dosyasında herhangi bir bileşen gibi kullanabiliriz.
    render(
      <Wrapper>
        <Title>
          Hello World!
        </Title>
      </Wrapper>
    );
```

![styled-header](tutorials-in-turkish/styled-component.png)
