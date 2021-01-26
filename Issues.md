# Issues

##  org.apache.zookeeper.data & org.apache.zookeeper.proto
import org.apache.zookeeper.data.Stat in class OpResult.java is not found in the classpath.
Same is the case with import org.apache.zookeeper.proto.CheckVersionRequest ( not found )

These are in the zookeeper-jute sub module. run mvn install at parent that would generate the 
zookeeper-jute jar and then add it to the classpath

## ParseException
Exception in thread "main" java.lang.NoClassDefFoundError: org/apache/commons/cli/ParseException
at org.apache.zookeeper.ZooKeeperMain.<clinit>(ZooKeeperMain.java:105)

- Looks like commons-cli is not in the classpath. To fix add
commons-cli in the project structure -> Libraries. Make sure it
  add to the zookeeper project as the ZooKeeperMain is in the zookeeper project.
  
## JLine support is disabled
add Jline library to the zookeeper project classpath