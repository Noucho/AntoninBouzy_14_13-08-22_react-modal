# @noucho/react-modal

Responsive modal dialog component for React.

## Node version :
- Node v16.0.0
- npm v7.10.0

## Installation

To install, you can use [npm](https://npmjs.org/) or [yarn](https://yarnpkg.com):

    $ npm install @noucho/react-modal
    $ yarn add @noucho/react-modal

  - Use `<Modal>` tag inside your React app.

```jsx

import { Modal } from '@noucho/react-modal/dist'
import React from 'react'

export default function Form() {
  window.React = React

  const [isValid, setIsValid] = useState(false)
  
  const handleModalResponse = () => {
    setIsValid(false)
  }

  const handleAddFormSubmit = (e) => {
    e.preventDefault()
    setIsValid(true)
  }

  return (
    <section className="formContent">
      <h2 className="formTitle">Create Employee</h2>
      <form className="form" onSubmit={handleAddFormSubmit}>
        (...)
      </form>
      {isValid ? <Modal text="Employee Created !" handleResponse={handleModalResponse} /> : ''}
    </section>
  )
}

```