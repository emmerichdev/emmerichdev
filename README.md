# Hi there 👋 I'm Emmerich

```kotlin
object Profile {
    val name = "Emmerich"
    val role = "Software Developer"
    
    object AboutMe {
        val education = "Pursuing a Bachelor's degree in Computer Science"
        val interests = listOf(
            "Political Enthusiast",
            "Competitive Swimming"
        )
        
        fun introduction() = """
            I'm passionate about software development and I am constantly learning more and expanding my knowledge.
            When I'm not coding, you can find me absorbed in politics, swimming laps in the pool, or gaming!
        """.trimIndent()
    }
    
    object CurrentlyLearning {
        val technologies = setOf(
            Technology("Rust", "Systems Programming"),
            Technology("OpenCV", "Computer Vision"),
            Technology("Machine Learning", "AI")
        )
        
        fun display() = technologies.joinToString("\n") { "- ${it.name}: ${it.category}" }
    }
    
    object Skills {
        val languages = listOf("Java", "Kotlin", "Python", "JS", "TS")
        val frontend = listOf("React", "Tailwind", "Flutter", "Android")
        val backend = listOf("Node", "Kafka", "Spring Boot")
        val databases = listOf("PostgreSQL", "MongoDB", "Redis")
        val devOps = listOf("Grafana", "Docker", "Kubernetes")
        
        fun formatSkillSection(title: String, skills: List<String>) = 
            "$title: ${skills.joinToString(", ")}"
            
        fun getAllSkills() = """
            ${formatSkillSection("Languages", languages)}
            ${formatSkillSection("Frontend", frontend)}
            ${formatSkillSection("Backend", backend)}
            ${formatSkillSection("Databases", databases)}
            ${formatSkillSection("DevOps", devOps)}
        """.trimIndent()
    }
    
    fun printResume() {
        println("# $name - $role")
        println("\n## About Me")
        println(AboutMe.introduction())
        println("\n## Currently Learning")
        println(CurrentlyLearning.display())
        println("\n## Skills")
        println(Skills.getAllSkills())
    }
}

data class Technology(val name: String, val category: String)

fun main() {
    Profile.printResume()
}
```

## 📫 Connect With Me
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](www.linkedin.com/in/emmerichb)
