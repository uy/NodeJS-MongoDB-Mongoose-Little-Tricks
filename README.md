Creating Compound index from code
======

```javascript
const mongoose = require('mongoose')

const Wholala = new mongoose.Schema({
  field1: { type: String, required: [true, 'required.'] },
  field2: { type: String, required: [true, 'required.'] },
  field3: { type: String, required: [true, 'required.'] }
})

Wholala.index({ field1: 1, field2: 1, field3: 1 }, { unique: true })

module.exports = mongoose.model('Wholala', Wholala, 'Wholala')
```
