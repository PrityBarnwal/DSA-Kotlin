# Filter Movies
## OverView

```ruby
fun filterLogs(): String {
    
      val logDump = "name=John Trust, username=john3, email=john3@gmail.com, id = 434453;name=Hannah Smith, username=hsmith, email=hsm@test.com, 1d = 23312;name=Hannah Smith, username=hsmith, 1d = 3223423, email=hsm@test.com;name=Robert M, username=rm44, id = 222342, email=rm@me.com;name Robert M, username=rm4411, id = 5535, email=rm@me.com;name=Susan Vee, username=sv55, id = 443432 , email=susanv123@me.com;name=Robert Nick, username=rnick33, 1d = 23432, email=rnick@gmail.com;name=Robert Nick II, username=rnickTemp34, 1d = 23432, email=rnick@gmail.com;name=Susan Vee, username=sv55, id = 443432, email=susanv123@me.com;"
    
    val seenUsernames = mutableSetOf<String>()
    val filteredLogs = mutableListOf<String>()

    // Split by semicolon and iterate over each log item
    logDump.split(";").forEach { logItem ->
        val trimmedLog = logItem.trim()

        // Extract username using regex
        val usernameRegex = "username\\s*=\\s*([a-zA-Z0-9]+)".toRegex()
        val matchResult = usernameRegex.find(trimmedLog)

        if (matchResult != null) {
            val username = matchResult.groupValues[1]
            if (!seenUsernames.contains(username)) {
                // Remove `id` or malformed `1d` properties and trailing commas
                var logWithoutId = trimmedLog.replace("\\b[1iI]?d\\s*=\\s*[^,;]+,?\\s*".toRegex(), "")
                logWithoutId = logWithoutId.replace(",\\s*$".toRegex(), "").trim() // Remove trailing comma
                filteredLogs.add(logWithoutId)
                seenUsernames.add(username)
            }
        }
    }

    // Join filtered logs into a single string with semicolon delimiters
    return filteredLogs.joinToString("; ")
}
```
```ruby
fun main(){
    val result = filterLogs()
    println(result)
}
```

## Output

```ruby
name=John Trust, username=john3, email=john3@gmail.com; name=Hannah Smith, username=hsmith, email=hsm@test.com; name=Robert M, username=rm44, email=rm@me.com; name Robert M, username=rm4411, email=rm@me.com; name=Susan Vee, username=sv55, email=susanv123@me.com; name=Robert Nick, username=rnick33, email=rnick@gmail.com; name=Robert Nick II, username=rnickTemp34, email=rnick@gmail.com
```
