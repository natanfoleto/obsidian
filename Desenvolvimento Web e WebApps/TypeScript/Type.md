
Para não ficar sempre repetindo os tipos para todas as variáveis podemos criar Types para cada uma delas.

```ts
type IdType = string | number | undefined

let userId: IdType
let adminId: IdType

userId = 1
userId = "1"
userId = undefined

adminId = 1
adminId = "2"
adminId = undefined
```
