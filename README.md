# swagger-ref-error-demo

A sample application to show swagger codegen error when a primitive json schema is referenced from another json schema.

[title.json](https://github.com/abhijith-prabhakar/swagger-ref-error-demo/blob/master/src/main/resources/v1/schema/title/title.json) is referring to common [currency_code.json](https://github.com/abhijith-prabhakar/swagger-ref-error-demo/blob/master/src/main/resources/v1/schema/common/currency_code.json) which breaks swagger codegen.  If you remove below entry from title.json codegen works fine.

```javascript
 "currency" : {
    "$ref": "./common/currency_code.json"
 }
```

The same was tried on v2.2.1 and v2.2.2-SNAPSHOT of Swagger Codegen.

Interesting below entry works fine.

```javascript
 "copies": {
      "type": "array",
      "description": "List of copies for this title",
      "items": {
        "$ref": "./title/copy.json"
      }
    }
```