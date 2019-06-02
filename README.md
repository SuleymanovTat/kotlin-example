https://www.youtube.com/watch?v=6kBLGKS3dOY

import kotlinx.serialization.Serializable</b>
import kotlinx.serialization.json.Json</b>
import kotlinx.serialization.list</b>
import com.suleymanovtat.planapplication.Example as Example1</b>


fun calc() = 2</b>

fun main() {</b>
    //todo вызывать методы в whan</b>
    when (calc()) {</b>
        1 -> println("1")</b>
        2 -> println("2")</b>
        3 -> println("3")</b>
        else -> println("error")</b>
    }</b>
    println(Json.stringify(User.serializer(), user1))</b>
    val jsonList = Json.stringify(User.serializer().list, users)</b>
    println(jsonList)</b>

    val user = Json.parse(User.serializer(), userStr)</b>
    println(user)</b>

    val list: List<User> = Json.parse(User.serializer().list, usersStr)</b>
    println(list)</b>
}

//todo experimental</b>
@Experimental(level = Experimental.Level.WARNING)</b>
annotation class Example {</b>

}</b>


@Serializable</b>
data class User(val id: Int,
                val name: String,
                val lastName: String = "Suley",
                var work: String? = null

)</b>

val user1 = User(1, "ilmir1")</b>
val user2 = User(2, "ilmir2")</b>
val user3 = User(3, "ilmir3", "Nuri")</b>
val userStr = "{\"id\":1,\"name\":\"ilmir1\",\"lastName\":\"Suley\"}"</b>
val usersStr = "[{\"id\":1,\"name\":\"ilmir1\",\"lastName\":\"Suley\"},{\"id\":2,\"name\":\"ilmir2\",\"lastName\":\"Suley\"},{\"id\":3,\"name\":\"ilmir3\",\"lastName\":\"Nuri\"}]"</b>

var users = listOf<User>(user1, user2, user3)</b>
