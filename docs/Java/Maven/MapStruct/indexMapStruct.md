# Introduction

MapStruct automates the process of creating a mapper to map data objects with model objects using annotations. It creates a mapper implementation at compile time which helps developer to figure out error during development and make is easy to understand.
At first, we need to create a mapper :

```
@Mapper
class StudentMapper {
   StudentMapper INSTANCE = Mappers.getMapper( StudentMapper.class );   
   StudentEntity modelToEntity(Student student);
}
```