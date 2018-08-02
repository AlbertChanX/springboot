

## Repository

> Repository蕴含着真正的`OO`概念，即一个数据仓库角色，负责所有对象的持久化管理。
Repository是相对对象而言，DAO则是相对数据库而言，虽然可能是同一个东西 ，但侧重点完全不同。


### CrudRepository

> CrudRepository类如其名，可以胜任最基本的CRUD操作。
其中save方法在可两用，参数中不存在主键时执行insert操作，存在主键则执行update操作，相当于是一个upsert操作。

### PagingAndSortingRepository

```
Iterable<T> findAll(Sort sort);
Page<T> findAll(Pageable pageable);
```

> PagingAndSortingRepository继承了`CrudRepository`接口，
增加了分页和排序的方法。

### JpaRepository

> JpaRepository则进一步在PagingAndSorting的基础上，扩展了部分功能：
  
* 查询列表（返回值为List）
* 批量删除
* 强制同步
* Example查询


## Refer

* [Spring Boot Repository - SegmentFault](https://segmentfault.com/a/1190000012346333)
