# soapui-spring-boot-starter

### Requirements
------------
**[SoapUI](https://github.com/SmartBear/soapui) must be installed on your Maven Repository.**

### Maven Dependency

``` xml
<dependency>
	<groupId>com.github.hiwepy</groupId>
	<artifactId>soapui-spring-boot-starter</artifactId>
	<version>${project.version}</version>
</dependency>
```

### Usage

#### Step 1 ：Copy SoapUI Jar Files

> Copy soapui-5.4.0.jar、soapui-5.4.0-sources.jar、analytics-core-5.4.0.jar、out-app-analytics-provider-5.4.0.jar to D:\

#### Step 2 ：Deploy soapui-5.4.0.jar、soapui-5.4.0-sources.jar、analytics-core-5.4.0.jar、out-app-analytics-provider-5.4.0.jar to Maven Repository

```bash
mvn deploy:deploy-file -DgroupId=com.eviware -DartifactId=soapui -Dversion=5.4.0 -Dpackaging=jar -Dfile=D:\soapui-5.4.0.jar -Durl=${repositoryUrl} -DrepositoryId=${repositoryId}
mvn deploy:deploy-file -DgroupId=com.eviware -DartifactId=soapui -Dversion=5.4.0 -Dpackaging=jar -Dfile=D:\soapui-5.4.0-sources.jar -Dclassifier=sources -Durl=${repositoryUrl} -DrepositoryId=${repositoryId}
mvn deploy:deploy-file -DgroupId=com.smartbear.utils.analytics -DartifactId=smartbear-analytics -Dversion=5.4.0 -Dpackaging=pom -Dfile=D:\smartbear-analytics-5.4.0.pom -Durl=${repositoryUrl} -DrepositoryId=${repositoryId}
mvn deploy:deploy-file -DgroupId=com.smartbear.utils.analytics -DartifactId=analytics-core -Dversion=5.4.0 -Dpackaging=jar -Dfile=D:\analytics-core-5.4.0.jar -Durl=${repositoryUrl} -DrepositoryId=${repositoryId}
mvn deploy:deploy-file -DgroupId=com.smartbear.utils.analytics -DartifactId=out-app-analytics-provider -Dversion=5.4.0 -Dpackaging=jar -Dfile=D:\out-app-analytics-provider-5.4.0.jar -Durl=${repositoryUrl} -DrepositoryId=${repositoryId}
```

### Some Useful Classes

```java
com.eviware.soapui.impl.WsdlInterfaceFactory
com.eviware.soapui.impl.wsdl.support.wsdl.CachedWsdlLoader
com.eviware.soapui.impl.wsdl.support.wsdl.UrlWsdlLoader
com.eviware.soapui.impl.wsdl.support.wsdl.WsdlImporter
com.eviware.soapui.impl.wsdl.support.wsdl.WsdlUtils
com.eviware.soapui.impl.wsdl.support.soap.SoapUtils

com.eviware.soapui.support.xml.XmlUtils
com.eviware.soapui.support.JsonUtil
com.eviware.soapui.support.SecurityScanUtil

com.eviware.soapui.support.scripting.SoapUIScriptEngineRegistry
```
