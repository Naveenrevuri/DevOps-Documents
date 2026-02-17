#1️⃣ Jacoco PlugIn Add In POM.XML
```bash
<build>
    <plugins>
        <!-- Other plugins -->

        <!-- JaCoCo plugin -->
        <plugin>
            <groupId>org.jacoco</groupId>
            <artifactId>jacoco-maven-plugin</artifactId>
            <version>0.8.11</version> <!-- latest stable -->
            <executions>
                <execution>
                    <goals>
                        <goal>prepare-agent</goal> <!-- instrument code before tests -->
                    </goals>
                </execution>
                <execution>
                    <id>report</id>
                    <phase>test</phase>
                    <goals>
                        <goal>report</goal> <!-- generate report after tests -->
                    </goals>
                      <configuration>
                        <!-- Exclude DTO, Entity, Config, Demo packages -->
                        <excludes>
                            <exclude>com/example/demo/dto/*</exclude>
                            <exclude>com/example/demo/entity/*</exclude>
                            <exclude>com/example/demo/config/*</exclude>
                            <exclude>com/example/demo/exceptions/*</exclude>
                            <exclude>com/example/demo/*</exclude>
                            
                        </excludes>
                </execution>
            </executions>
        </plugin>
    </plugins>
</build>
```
#2️⃣ Run Unit Test
```bash
clean verify
```
#3️⃣  Analyze Coverage Report 
     1) IN Side project: target/site/jacoco/index.html
     2)Controller + Service layer unit tests + exceptions cover cheste coverage 80-90%
