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
    
    val learning = listOf("Rust", "OpenCV", "ML/AI")
    val skills = mapOf(
        "Languages" to listOf("Java", "Kotlin", "Python", "JS", "TS", "C#", "Rust"),
        "Frontend" to listOf("React", "Tailwind", "Flutter", "Android"),
        "Backend" to listOf("Node", "Kafka", "Spring Boot"),
        "DBs" to listOf("PostgreSQL", "MongoDB", "Redis"),
        "DevOps" to listOf("Grafana", "Docker", "K8s")
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
