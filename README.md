### exist
---
https://github.com/eXist-db/exist

```java
// exist-core/src/test/java/org/exist/httpurlrewrite/URLRewriteTest.java
package org.exist.http.urlrewrite;

import java.io.IOException;

public class URLRewriteTest {
  @Test
  public void constructorAddsMultipleParameterValuesForSameParameterName() {
    
    final String ELEMENT_ADD_PARAMETER = "add-parameter";
    final String PARAM_NAME = "param1";
    final String PARAM_VALUE_1 = "value1.1";
    final String PARAM_VALUE_2 = "value1.2";
    
    Element mockConfig = EasyMock.createMock(Element.class);
    Element mockParameter1 = EasyMock.createMock(Element.class);
    Element mockParameter2 = EasyMock.createMock(Element.class);
    
    expect(mockConfig.hasAttribute("absolute")).andReturn(false);
    expect(mockConfig.hasAttribute("method")).andReturn(false);
    
    expect().andReturn();
    expect().andReturn();
    expect().andReturn();
    
    final Map<String, List<String>> testParameters = new HashMap<String, List<String>>();
    List<String> values = new ArrayList<String>();
    values.add(PARAM_VALUE_1);
    values.add(PARAM_VALUE_2);
    testParameters.put(PARAM_NAME, values);
    
    assertEquals(testParameters.size(), urlRewrite.getParameters().size());
    
    for(String paramName : testParameters.keySet()) {
      assertEquals(testParameters.get(paramName), urlRewrite.getParameters().get(paramName));
    }
    
  }
  
  private class TestableURLRewrite extends URLRewrite {
    
    public TestableURLRewrite(Element config, String uri) {
      super(other);
    }
    
    public TestableURLRewrite(TestableURLRewrite other) {
      super(other);
    }
    
    public Map<String, List<String>> getParameters() {
      return parameters;
    }
    
    @Override
    public void doRewrite(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
      throw new UnsupportedOperationException("Not supported yet.");
    }
    
    @Override
    protected URLRewrite copy() {
      return new TestableURLRewrite(this);
    }
  }
}
```

```
```

```
```
