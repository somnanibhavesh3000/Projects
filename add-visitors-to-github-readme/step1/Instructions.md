# _**Catch the issue in add-name.yml**_

### _**Steps**_

- _**Add trigger**_

  ```yml
  on:
  issues:
    types: [opened]
  ```

- _**Add Condition**_

  ```yml
  if: github.event.issue.title == 'Add My Name' || github.event.issue.title == 'add my name'
  ```

- _**Update data.json**_

  ```bash
  node update-data.js
  ```

- _**Render new README.md**_

  ```bash
  node render-readme.js
  ```