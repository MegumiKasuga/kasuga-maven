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
    // Not the 'repositories' closure in the 'build-script' closure.
    maven {
        url = "https://raw.github.com/MegumiKasuga/kasuga-maven/${artifact-2-use}/"
    }
}

dependencies {
  // Not the 'dependencies' closure in the 'build-script' closure.
  implementation group: 'edu.carole', name: '${artifact-2-use}', version: '${artifact-version}'
}
```

ForgeGradle (For Minecraft ver 1.17.1+)
  - for more info : https://gist.github.com/SizableShrimp/66b22f1b24c255e1491c8d98d3f11f83
```

jarJar.enable()
minecraft {
  // Your minecraft closure in script
}

repositories {
    // Not the 'repositories' closure in the 'build-script' closure.
    maven {
        url = "https://raw.github.com/MegumiKasuga/kasuga-maven/${artifact-2-use}/"
    }
}

dependencies {
  // Not the 'dependencies' closure in the 'build-script' closure.
  minecraftLibrary group: 'edu.carole', name: '${artifact-2-use}', version: '${artifact-version}'
  jarJar(group: 'edu.carole', name: '${artifact-2-use}', version: ['${artifact-min-version}, ${artifact-max-version'))
}
```

### Listed Proj:
  - Mixed-Arithmetic-Logic-Interpreter (mali)
    
    Repo: https://github.com/MegumiKasuga/Mixed-Arithmetic-Logic-Interpreter
```
  ${artifact-2-use} = Mixed-Arithmetic-Logic-Interpreter
  ${branch-2-use} = mali
  ${artifact-version} = 1.0.0
  ${artifact-min-version} = 1.0.0
  ${artifact-max-version} = 2.0.0
```
