# ***CSE 15L lab Report 3***   
Name: William Share


## Part 1


**A Failure Inducing Input:**

```
@Test
  public void testAverageWithoutLowest(){
    double[] arr = {1.0, 1.0, 3.0, 2.0, 6.0};
    assertEquals(3.0 ,ArrayExamples.averageWithoutLowest(arr), 0.1);
  }
```
This test case would fail because the method unintentionally adds up all of the doubles within the array except for the lowest double, in this case 1.0. However. this only works if the lowest double is a unique double. If there are multiple instances of the lowest double in the array then the sum won't be added properly, thus failing the test case. 

**A Non-Failure Inducing Input:** 

```
@Test
  public void testAverageWithoutLowest1(){
    double[] arr = {1.0, 2.0, 3.0, 2.0, 5.0};
    assertEquals(3.0 ,ArrayExamples.averageWithoutLowest(arr), 0.1);
  }
```

This test case passes because there is a unique lowest double within the array, that being 1.0, so the method works because it is excluding the lowest double.

**The symptom:**

![image](https://github.com/wshare26/cse15l-lab-reports/assets/156359336/874818a9-6424-4122-a2d8-43ca295c6282)

As you can see the first test case expects 3.0 but the actual is 2.75 which is not intended. The second test case expects 3.0 and the actual is 3.0 due to there being a unique lowest double.




**The bug:**
```
  static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    for(double num: arr) {
      if(num < lowest) { lowest = num; }
    }
    double sum = 0;
    for(double num: arr) {
      if(num != lowest) { sum += num; }
    }
    return sum / (arr.length - 1);
  }
```

The test case is failing due to not adding the lowest double to the sum. This works only when there is a unique lowest double, but when there are multiple lowest doubles present in the array, it does not work.


**Method Fixed:**
```
  static double averageWithoutLowest(double[] arr) {
    if(arr == null){
      throw new NullPointerException("invalid input");
    }

    if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    for(double num: arr) {
      if(num < lowest) { lowest = num; }
    }
    double sum = 0;
    for(double num: arr) {
      sum += num;
    }
    sum = sum - lowest;
    return sum / (arr.length - 1);
  }
```
This fix addresses the issue by adding all of the doubles up and subtracting only one instance of the lowest double.

## Part 2

*Command Chosen: find*

**First interesting command-line option: Finding files that end in .txt**

Example 1:
Finding files that end in "21.txt"

```
[user@sahara ~/docsearch/technical]$ find . -type f -name "*21.txt"
./biomed/ar321.txt
./biomed/1471-2164-4-21.txt
./biomed/1477-7827-1-21.txt
./biomed/1471-2121-2-21.txt
./biomed/1471-2334-1-21.txt
./biomed/1471-2458-2-21.txt
./biomed/1471-2121-3-21.txt
./biomed/1472-6750-2-21.txt
./biomed/1471-230X-2-21.txt
```
Example 2:
Finding files that end in "33.txt"

```
[user@sahara ~/docsearch/technical]$ find . -type f -name "*33.txt"
./biomed/1471-2180-1-33.txt
./biomed/1471-2407-2-33.txt
./biomed/1471-2164-3-33.txt
```

**Second interesting command-line option: Finding a single file by name:**

Example 3:
Finding file "1471-2105-3-38.txt"

```
[user@sahara ~/docsearch/technical]$ find / -name "1471-2105-3-38.txt" 2>/dev/null
/home/docsearch/technical/biomed/1471-2105-3-38.txt
```
Example 4:
Finding file "chapter-1.txt"

```
[user@sahara ~/docsearch/technical]$ find / -name "chapter-1.txt" 2>/dev/null
/home/docsearch/technical/911report/chapter-1.txt
```

**Third interesting command-line option: Finding file that contains various texts:**

Example 5:
Finding text "WE HAVE SOME PLANES"
```
[user@sahara ~]$ find ~/docsearch/technical/911report/ -name "*txt" -exec grep -H "WE HAVE SOME PLANES" {} \;
/home/docsearch/technical/911report/chapter-1.txt:"WE HAVE SOME PLANES"
```

Example 6:
Finding text "A DECLARTION OF WAR"

```
[user@sahara ~]$ find ~/docsearch/technical/911report/ -name "*txt" -exec grep -H "A DECLARATION OF WAR" {} \;
/home/docsearch/technical/911report/chapter-2.txt:            A DECLARATION OF WAR
```

**Fourth interesting command-line option: Listing directories**

Example 7:
Listing directories in "docsearch/"

```
[user@sahara ~]$ find ~/docsearch/ -type d
/home/docsearch/
/home/docsearch/lib
/home/docsearch/technical
/home/docsearch/technical/911report
/home/docsearch/technical/biomed
/home/docsearch/.git
/home/docsearch/.git/branches
/home/docsearch/.git/refs
/home/docsearch/.git/refs/tags
/home/docsearch/.git/refs/remotes
/home/docsearch/.git/refs/remotes/origin
/home/docsearch/.git/refs/heads
/home/docsearch/.git/info
/home/docsearch/.git/objects
/home/docsearch/.git/objects/pack
/home/docsearch/.git/objects/info
/home/docsearch/.git/logs
/home/docsearch/.git/logs/refs
/home/docsearch/.git/logs/refs/remotes
/home/docsearch/.git/logs/refs/remotes/origin
/home/docsearch/.git/logs/refs/heads
/home/docsearch/.git/hooks
```

Example 8:
Listing directories in "docsearch/technical/"

```
[user@sahara ~]$ find ~/docsearch/technical/ -type d
/home/docsearch/technical/
/home/docsearch/technical/911report
/home/docsearch/technical/biomed
```



