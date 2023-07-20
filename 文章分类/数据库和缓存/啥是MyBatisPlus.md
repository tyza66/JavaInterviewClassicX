# 啥是MyBatisPlus
- MyBatisPlus是MyBatis的增强工具，在MyBatis的基础上只做增强不做改变
- 它为简化开发、提高效率而设计
- MyBatisPlus支持所有MyBatis原生的特性
- 所以引入MyBatis-Plus不会对现有的MyBatis构架产生任何影响
- 在实现Mapper的时候可以继承BaseMapper<T>，就可以直接使用里面的方法（只有基本简单的，太复杂的要自己处理）
- 在Service层的实现类中可以直接继承ServiceImpl<M, T>，就可以直接使用里面的方法