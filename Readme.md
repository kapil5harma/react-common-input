## React Common Input component

- A common react input component to be used as input, textarea, select depending on the configuration being provided.

- import Input from 'react-common-input'

- Your state would have a config object as follows:
  state = {
  title: {
  eleType: 'input',
  eleConfig: {
  label: 'Title',
  type: 'text',
  name: 'title',
  placeholder: 'Enter title'
  },
  value: '',
  validation: {
  required: true,
  minLength: 5,
  maxLength: 25
  },
  valid: false,
  touched: false
  },
  }

- Then you can use the input component as follows:
  <Input
  className='input'
  elementType={title.eleType}
  elementConfig={title.eleConfig}
  value={title.value}
  invalid={!title.valid}
  shouldValidate={title.validation}
  touched={title.touched}
  changed={event => this.inputChangeHandler(event, title)}
  />
