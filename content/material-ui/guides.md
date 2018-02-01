
## 如何使用material-ui

### 安装

 - npm i material-ui@next -s
 - npm install --save material-ui-icons(图标)

### 实例

~~~js
import React from 'react';

import { withStyles } from 'material-ui/styles'
import Button from 'material-ui/Button'
const styles = theme => ({
  button: {
    margin: theme.spacing.unit,
  },
  input: {
    display: 'none'
  }
})
function RaisedButtons(props) {
  const { classes } = props
  return (
    <div>
      <Button raised className={classes.button}>
        Default
      </Button>
      <Button raised color="primary" className={classes.button}>
        Primary
      </Button>
      <Button raised color="secondary" className={classes.button}>
        Secondary
      </Button>
      <Button raised color="secondary" disabled className={classes.button}>
        Disabled
      </Button>
      <input
        accept="image/*"
        className={classes.input}
        id="raised-button-file"
        multiple
        type="file"
      />
      <label htmlFor="raised-button-file">
        <Button raised component="span" className={classes.button}>
          Upload
        </Button>
      </label>
    </div>
  )
}

export default withStyles(styles)(RaisedButtons)
~~~
