## async-await

````kotlin
GlobalScope.launch(Dispatchers.IO){
  val time = measureTimeMills{
    val response1 = async{ request1() }
    val response2 = async{ request2() }
    Log.d(TAG, "response1: ${response1.await()}")
    Log.d(TAG, "response2: ${response2.await()}")
  }
  Log.d(TAG, "requests took $time ms.")
}
````
