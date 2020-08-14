# js-file-md5

Get a MD5 hash from a file with Javascript.

## Usage

#### `HTML`

```html
<input id="example-file" type="file" />
```

#### `Javascript`
```javascript
import md5 from 'js-file-md5';

const fileInput = document.querySelector('#example-file');

fileInput.addEventListener('change', function(e) {
  const file = e.target.files[0];

  md5(file).then(hash => {
    console.log(hash); // md5 hash
    console.log(btoa(hash)); // base64 encode
  }).catch(error => {
    throw error;
  });
});
```
