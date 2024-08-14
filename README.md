# TartLabs Awesome React Calculator

TartLabs Awesome React Calculator is a React Component library. It gives you a simple calculator component to work in your project. It supports keyboard and you can paste your expression to get the result.


[![npm version](https://img.shields.io/badge/npm-2.0.0-blue.svg)](https://www.npmjs.com/package/tl-awesome-react-calculator)

## Installation

Use the npm or yarn to install

```bash
npm install -S tl-awesome-react-calculator
```
```bash
yarn add tl-awesome-react-calculator
```


## Usage

```javascript

import React, {Component} from 'react'
import {render} from 'react-dom'
import Calculator from "tl-awesome-react-calculator";

const style = {
  height: '24rem',
  width: '15rem'
}

class Demo extends Component {
  handleInput(input) {
    console.log(`${input.expression} is shown in the calculator, User clicked the ${input.key}`)
  }

  onResultChange(newResult) {
    console.log(newResult)
    console.log(`${newResult.expression} is validated as ${newResult.result} `)
  }
  render() {
    return <div className='calculator-demo' style={style}>
      <h1>Calculator</h1>
      <Calculator
        onNewInput={this.handleInput}
        onResultChange={this.onResultChange}/>
    </div>
  }
}

render(<Demo/>, document.querySelector('#demo'))
```
## Options

### Props
| Props  | Return Type   | Usage |
|---|---|--- |
| onNewInput  | object {expression: string, key: string} | Triggered when some input is entered|
| onResultChange  | object {expression: string, result: string}  | Returns the result shown in calculator and triggered whenever the result is changed|


### Note

Please set the **width and height** of the parent div of our the `<Calculator />` Component


## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)

## Node Version - 16