## grid get started

```scss
.grid-container {
  @include width-auto;
  padding: 2rem;
  background-color: #c6bfc6;
  display: grid;

  // grid
  // grid-template-columns: 150px 200px 350px;
  grid-template-columns: 1fr 2fr 40%;
  // grid-template-columns: repeat(3, 20rem);
  // grid-template-columns: repeat(3, 20rem) 1fr;
  // grid-template-columns: repeat(3, 1fr);

  // grid-template-rows: 150px 150px;
  grid-template-rows: repeat(2, 10rem);

  //   grid gap***

  grid-row-gap: 4rem;
  grid-column-gap: 3rem;
  //   OR
  grid-gap: 3rem;

  .item {
    background-color: #fdacac;

    //display adjustments
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 4rem;
    font-weight: bold;
    color: #fff;
    text-transform: uppercase;

    // positionning elements

    &-1 {
      // grid-row-start: 1;
      // grid-row-end: 3;
      grid-row: 1/3;

      // grid-column-start: 2;
      // grid-column-end: 4;
      grid-column: 2/4;

      background-color: #b9f5f5;
      color: #000;
    }
    &-2 {
      // span till end
      // grid-column: 1 / span 3;
      grid-column: 1 / -1;
    }
    // positionning elements
    &-6 {
      grid-row: 1/3;
      grid-column: 1/2;
    }
  }
}
```

## grid-challange

```scss
.grid-challange {
  @include width-auto;
  // height: 95vh;
  display: grid;
  grid-template-columns: repeat(3, 1fr) 0.75fr;
  // grid-template-rows: 10rem 20rem 50rem 10rem;
  grid-template-rows: 0.75fr 1fr 3fr 0.75fr;

  grid-gap: 3rem;

  // all direct children
  & > * {
    background-color: #dcd5d5;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 2rem;
    font-weight: bold;
    text-transform: uppercase;
    color: #242323;
    padding: 3rem;
  }
  .header {
    grid-column: 1/-1;
  }
  .sidebar {
    grid-row: 2/4;
    grid-column: 4/5;
  }
  .main-content {
    grid-column: 1/4;
  }
  .footer {
    grid-column: 1/-1;
  }
}
```

## grid alignment

> Alignment with implicit vs explicit grid

```scss
.grid-implicit {
  @include width-auto;
  background-color: rgb(228, 220, 220);
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-template-rows: repeat(2, 15rem);
  grid-gap: 3rem;

  // grid auto => implicit
  // grid-auto-flow: row;
  // grid-auto-flow: row dense;
  // grid-auto-rows: 80px;
  // grid-auto-flow: column;
  // grid-auto-columns: 0.5fr;

  // align-items: center;
  // justify-items: center;

  grid-template-columns: repeat(2, 100px);
  grid-template-rows: repeat(2, 15rem);

  justify-content: space-between;
  align-items: center;

  .grid-allign {
    background-color: #f8c7c7;
    // display: grid;
    // align-items: center;
    // justify-content: center;

    font-size: 3rem;
    padding: 2rem;

    &-4 {
      background-color: #fff;
      grid-column: 1/2;
      grid-row: 2/4;

      // display: grid;
      // align-items: center;
      // justify-content: center;
    }
  }
}
```

## grid min-max content

// FUNCTION

```scss
.grid-max-min {
  @include width-auto;

  display: grid;

  // grid-template-columns: max-content 1fr 1fr 1fr;
  // grid-template-columns: max-content repeat(3, 1fr);
  grid-template-columns: min-content repeat(3, 1fr);

  // grid-template-rows: repeat(2, 100px);
  // grid-template-rows: repeat(2, min-content);
  grid-template-rows: min-content 10rem;

  // minmax function
  // grid-template-columns: minmax(200px, 300px) repeat(3, 1fr);

  // grid-template-rows: repeat(2, minmax(150px, min-content));

  grid-gap: 3rem;

  .minMax {
    background-color: #fff;
    display: grid;
    justify-content: center;
    align-items: center;
    font-size: large;
    text-transform: uppercase;

    &-1 {
      padding: 2rem;
      background-color: #efcccc;
    }
  }
}
```

## grid-auto-fit-fill

```scss
.grid-auto-fit-fill {
  @include width-auto;
  display: grid;
  grid-gap: 3rem;

  grid-template-rows: repeat(2, minmax(150px, min-content));

  // grid-template-columns: repeat(4, 1fr);
  // grid-template-columns: repeat(auto-fill, 100px);
  // grid-template-columns: repeat(auto-fit, 100px);
  // grid-template-columns: repeat(auto-fit, minmax(150px, min-content));
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));

  .gridAuto {
    padding: 2rem;
    background-color: #dedada;
    font-size: large;
    text-transform: uppercase;
    &-1 {
      background-color: #e4d4d4;
    }
  }
}
```
