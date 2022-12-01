# flex-properties

```scss
// Flex properties

.flex-cont-header {
  @include width-auto;
  h1 {
    margin-top: 2rem;
  }
}
.basic-flex-box-container {
  background-color: #c2b2b2;
  //   padding: 2rem;
  margin: 2rem;
  // height: 30rem;// for testing

  // Flex properties
  display: flex;
  flex-direction: row;
  //   flex-direction: row-reverse;
  //   flex-direction: column;
  //   flex-direction: column-reverse;
  justify-content: center;
  align-items: flex-start;
  // align-items: flex-end;
  // align-items: stretch;
  // align-items: baseline;
  flex-wrap: wrap;
  .item {
    padding: 3rem;
    margin: 0 3rem;
    background-color: #f98e8e;
    font-size: 5rem;

    // grow an element
    // flex-grow: 1;
    // flex: 1;

    @include respond(phone600mx) {
      margin-bottom: 3rem;
    }
  }
  .i3 {
    font-size: 10rem;
    // flex-grow: 0;
    // flex-shrink: 1;
    // flex-basis: 20%;
    flex: 0 1 20%;
  }
  .i5 {
    align-self: flex-end;
    order: -1;
    flex-basis: 20%;
  }
  .i4 {
    order: -2;
    // flex-grow: 1;
    // or
    flex: 1;
  }
}
```

