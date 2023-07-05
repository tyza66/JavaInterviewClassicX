# String链接数据库用什么连接池
- Apache Commons DBCP：这是基于Apache Commons的连接池实现，可以方便第与Hibernate、Mybatis等ORM框架集成
- c3p0：是由Charles A. Leiserson教授主推的连接池实现，它提供了丰富的配置选项，可以更好地满足不同场景下的需求
- HikariCP：这是一个由Hikari Japan公司开发的连接池实现，被广泛应用于生产环境中。它具有出色的性能和稳定性，并支持多种数据库
- Druid：这是一个较为新兴的连接池实现，具有强大的*监控和诊断功能*，可以帮助开发者*快速定位和解决问题*。此外，Druid还提供了*可插拔*的数据源实现，可以方便地支持*不同类型的数据库*