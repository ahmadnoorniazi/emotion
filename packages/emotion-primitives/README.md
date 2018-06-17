# Emotion primitives

> Style and render primitives interfaces across multiple targets with emotion

## Introduction

Emotion primitives makes it easy to style and render primitives across multiple platforms like `Web`, `React Native` and `Sketch` using the similar `emotion` API.

## Install

```
npm install emotion-primitives
```

or if you use yarn

```
yarn add emotion-primitives
```

This package also depends on `react` and `react-primitives` so make sure you've them installed.

## Example

```js
import React from 'react'
import { ThemeProvider } from 'emotion-theming'

const emotion = require('emotion-primitives')

const theme = {
  color: 'hotpink',
  backgroundColor: 'purple'
}

const Container = emotion.View`
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 50px;
  border: 5px solid red;
  background-color: ${props => props.theme.backgroundColor}
`

const Description = emotion.Text({
  color: 'hotpink'
})

const Image = emotion.Image`
  padding: 40px;
`

const emotionLogo =
  'https://emotion.sh/static/emotion-a76dfa0d18a0536af9e917cdb8f873b9-a69fb.png'

class App extends React.Component {
  render() {
    return (
      <ThemeProvider theme={theme}>
        <Container borderRadius="10px">
          <Description fontSize={45} fontWeight="bold">
            Emotion Primitives
          </Description>
          <Image
            source={{
              uri: emotionLogo,
              height: 150,
              width: 150
            }}
          />
        </Container>
      </ThemeProvider>
    )
  }
}
```

[![Edit 03r1rxv7jl](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/s/03r1rxv7jl)

## Supported primitives

* **Text**

* **View**

* **Image**