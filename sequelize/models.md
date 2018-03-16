# Model Validation
It takes in Promise and waits until it resolves.

```
sequelize.define(
  'model',
  {},
  {
    validate: {
      isUnique(value, next) {
        return Promise.resolve()
          .then(() => console.log('wait'))
          .delay(5000)
          .then(() => console.log('waited'))
      }
    }
  }
)
```