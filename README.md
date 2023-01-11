# React Simple Select

A React component who provides a select input handling the state value.

## Installation

Install tz-react-simple-select with npm

```bash
  npm install tz-react-simple-select
```

or with Yarn

```bash
yarn add tz-react-simple-select
```

## Usage/Examples

```typescript
import { FC, useState } from 'react'
import { Select } from 'tz-react-simple-select'

const App: FC<{}> = () => {
  const [favoriteIceCreamFlavour, setFavoriteIceCreamFlavour] = useState<string>('')

  const favoriteIceCreamFlavourOpts = [
    {
      label: 'Chocolate',
      value: 'chocolate',
    },
    {
      label: 'Vanilla',
      value: 'vanilla',
    },
    {
      label: 'Cookie',
      value: 'cookie',
    },
    {
      label: 'Mint',
      value: 'Mint',
    },
  ]

  const onChange = (e: ChangeEvent<HTMLInputElement>) => {
    setFavoriteIceCreamFlavour(e.target.value)
  }

  return (
    <div>
      <Select
        label="What's your favorite ice cream flavour ?"
        options={favoriteIceCreamFlavourOpts}
        value={favoriteIceCreamFlavour}
        onChange={setFavoriteIceCreamFlavour}
        id='favoriteFlavour'
      />
    </div>
  )
}

export default App
```

## Feedback

If you have any feedback, please reach out to us at tom.zidani@gmail.com

## License

[MIT](https://choosealicense.com/licenses/mit/)
