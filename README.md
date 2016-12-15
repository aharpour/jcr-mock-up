JcrMockup
============

Mock your hippo cms console exports in memory. In memory jcr mock, backed by mockito.

##Examples
```
Session session = JcrMockUp.mockJcrSession("/content.xml");
Node node = session.getRootNode();

node.addNode("foobar", "jcrmockup:foobar");
Node newNode = node.getNode("foobar");
```

##Limitations
 * No support of patterns for getProperty and getNode
 * No support of type constraints according to cnd (e. g. the property defintions is multiple when there are multiple values present)
 * javax.jcr.Node#isType() doesn't support sub types
 * javax.jcr.Value#setValue is not supported
 * workspaces are not supported
 * session.copy is not supported