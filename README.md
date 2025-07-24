# Hi there 👋 I'm Emmerich

```kotlin
object Profile {
    val name = "Emmerich"
    val role = "Software Developer"
    
    object AboutMe {
        val education = "B.S. Computer Science (in progress)"
        val interests = listOf("Politics", "Swimming", "Gaming")
        val bio = "Passionate dev always learning. I code, swim, and follow politics!"
    }
    
    val learning = listOf("ML/AI", "Python")
    val skills = mapOf(
        "Languages" to listOf("Java", "Kotlin", "C#","Rust"),
        "Frontend" to listOf("React", "Tailwind", "Android", "IOS"),
        "Backend" to listOf("Node", "Kafka", "Spring"),
        "DBs" to listOf("Most SQL databases", "MongoDB", "Redis"),
        "DevOps" to listOf("Grafana", "Docker", "K8s", "Git", "Actions", "CI/CD")
    )
    
    fun printResume() {
        println("# $name - $role")
        println("\n${AboutMe.bio}\n${AboutMe.education}")
        println("\nLearning: ${learning.joinToString()}")
        println("\nSkills:\n${skills.map { "- ${it.key}: ${it.value.joinToString()}"}.joinToString("\n")}")
    }
}

fun main() { Profile.printResume() }
```
