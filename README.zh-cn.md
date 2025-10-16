[![en-us](https://img.shields.io/badge/en-us-blue.svg)](https://github.com/MegumiKasuga/kasuga-maven/blob/master/README.md)
[![zh-cn](https://img.shields.io/badge/zh-cn-green.svg)](https://github.com/MegumiKasuga/kasuga-maven/blob/master/README.zh-cn.md)
# kasuga-maven
一个专用于maven依赖的仓库。

### 如何在自己的项目中使用这里列出的项目 ? 

Maven
``` xml
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
``` groovy
repositories {
    // 不是 'build-script' 闭包里的 'repositories' 闭包. 
    maven {
        url = "https://raw.github.com/MegumiKasuga/kasuga-maven/${artifact-2-use}/"
    }
}

dependencies {
  // 不是 'build-script' 闭包里的 'dependecies' 闭包. 
  implementation group: 'edu.carole', name: '${artifact-2-use}', version: '${artifact-version}'
}
```

ForgeGradle (For Minecraft ver 1.17.1+)
  - for more info : https://gist.github.com/SizableShrimp/66b22f1b24c255e1491c8d98d3f11f83
```

jarJar.enable()
minecraft {
  // 你在脚本中的 'Minecraft' 闭包
}

repositories {
    // 不是 'build-script' 闭包中的 'repositories' 闭包
    maven {
        url = "https://raw.github.com/MegumiKasuga/kasuga-maven/${artifact-2-use}/"
    }
}

dependencies {
  // 不是 'build-script' 闭包里的 'dependecies' 闭包. 
  minecraftLibrary group: 'edu.carole', name: '${artifact-2-use}', version: '${artifact-version}'
  jarJar(group: 'edu.carole', name: '${artifact-2-use}', version: ['${artifact-min-version}, ${artifact-max-version'))
}
```

### 目前列出的项目:
  - Mixed-Arithmetic-Logic-Interpreter (mali)
    
    仓库: https://github.com/MegumiKasuga/Mixed-Arithmetic-Logic-Interpreter
```
  ${artifact-2-use} = Mixed-Arithmetic-Logic-Interpreter  // 工件
  ${branch-2-use} = mali_${artifact_version}              // 分支
  ${artifact-version} = 1.1.0                             // 工件版本
  ${artifact-min-version} = 1.0.0                         // 工件最低版本
  ${artifact-max-version} = 2.0.0                         // 工件最高版本
```

  - BrainFuckJ (bfj)
    
    仓库: https://github.com/MegumiKasuga/BrainFuckJ
```
  ${artifact-2-use} = BrainFuckJ                          // 工件
  ${branch-2-use} = bfj_${artifact_version}               // 分支
  ${artifact-version} = 1.02                              // 工件版本
  ${artifact-min-version} = 1.02                          // 工件最低版本
  ${artifact-max-version} = 1.02                          // 工件最高版本
```
