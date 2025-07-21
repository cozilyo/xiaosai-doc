# 小噻文档

> 文档说明，即将补充......

```java
List<ProductTypeEntity> productTypeEntities = productTypeService.list(Wrappers.lambdaQuery(ProductTypeEntity.class)
                .select(ProductTypeEntity::getId, ProductTypeEntity::getName)
                .like(StringUtils.isNotEmpty(req.getName()), ProductTypeEntity::getName, req.getName())
                .eq(ProductTypeEntity::getIsShow, IsHandleEnum.YES.getCode()));
```
