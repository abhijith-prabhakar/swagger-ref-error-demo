# swagger-ref-error-demo

A sample application to show swagger codegen error when two different versions of same file is referenced


Below are two versions of currency code placed in different folders.

[V1](https://github.com/abhijith-prabhakar/swagger-ref-error-demo/tree/diff_versions_issue4218/src/main/resources/v1/schema/common/v1) of [currency_code.json](https://github.com/abhijith-prabhakar/swagger-ref-error-demo/blob/diff_versions_issue4218/src/main/resources/v1/schema/common/v1/currency_code.json)
[V2](https://github.com/abhijith-prabhakar/swagger-ref-error-demo/tree/diff_versions_issue4218/src/main/resources/v1/schema/common/v2) of [currency_code.json](https://github.com/abhijith-prabhakar/swagger-ref-error-demo/blob/diff_versions_issue4218/src/main/resources/v1/schema/common/v2/currency_code.json)

Swagger codegen generates only one CurrencyCode.java.  It picks which version depends on where is it defined in the API.
  
[ISSUE-4218](https://github.com/swagger-api/swagger-codegen/issues/4218) has been opened for this.  

The same was tried on v2.2.1 and v2.2.2-SNAPSHOT of Swagger Codegen.