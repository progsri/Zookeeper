# Issues

## Does not compile
import org.apache.zookeeper.data.Stat in class OpResult.java is not found in the classpath.
Same is the case with import org.apache.zookeeper.proto.CheckVersionRequest ( not found )

These are in the zookeeper-jute sub module. run mvn install at parent that would generate the 
zookeeper-jute jar and then add it to the classpath
