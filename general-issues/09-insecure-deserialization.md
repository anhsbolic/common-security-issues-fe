# 09 Insecure Deserialization di Frontend (JSON.parse & Co.)

## Problem
Parsing input JSON tanpa validasi dapat menyebabkan prototype pollution atau crash.

## Risk
- Manipulasi object bawaan
- Potensi eksekusi kode tidak terduga

## Example (Before)
```javascript
const data = JSON.parse(userInput); // tanpa validasi
```

## Solution (After)
```javascript
const data = JSON.parse(userInput);
if (!validateSchema(data)) throw new Error('Invalid data');
```

## How to Avoid
1. Validasi hasil parse dengan schema (Ajv/Joi).
2. Tangani error parsing dengan try/catch.
3. Jangan izinkan field dinamis tanpa whitelist.
