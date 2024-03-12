# kasuga-maven
A maven Repo that provides survices for dependencies.

### How to use projects listed in this mvn repo ? 

Maven
```
<dependency>
  <groupId>edu.carole</groupId>
  <artifactId>${artifact-2-use}</artifactId>
  <version>${artifact-version}</version>
</dependency>

<repository>
    <id>${artifact-2-use}</id>
    <url>https://raw.github.com/MegumiKasuga/kasuga-maven/${branch-2-use}/</url>
</repository>
```

Gradle
```
repositories {
    // Not the 'repositories' tag in the 'build-script' tag.
    maven {
        url = "https://raw.github.com/MegumiKasuga/kasuga-maven/${artifact-2-use}/"
    }
}

dependencies {
  // Not the 'dependencies' tag in the 'build-script' tag.
  implementation group: 'edu.carole', name: '${artifact-2-use}', version: '${artifact-version}'
}
```

### Listed Proj:
  - Mixed-Arithmetic-Logic-Interpreter (mali)
    
    Repo: https://github.com/MegumiKasuga/Mixed-Arithmetic-Logic-Interpreter
```
${artifact-2-use} = Mixed-Arithmetic-Logic-Interpreter
${branch-2-use} = mali
${artifact-version} = 1.0.0
```
