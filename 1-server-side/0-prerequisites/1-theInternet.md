# 

[Original post](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/How_does_the_Internet_work)



```java
public class CaesarCipher {
  public String encrypt(String input, int key) {
    String alphabet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
    String shiftedAlphabet = alphabet.substring(key) +
                             alphabet.substring(0,key);
    StringBuilder sb = newStringBuilder(input);
    for (int i = 0; i <sb.length(); i++) {
      char c = sb.charAt(i);
      int idx = alphabet.indexOf(c);
    }
  }
}
```

```java
public class CaesarCipher{
    private String alphabet;
    private String shiftedAlphabet;

    // Create a constructor to initialize an CaesarCipher object when it's created using `new`
    public CaesarCipher(int key){
        alphabet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
        shiftedAlphabet = alphabet.substring(key) +
                             alphabet.substring(0,key);
    }

    public String encrypt(String input){
        StringBuilder sb = new StringBuilder(input);
        for (int i = 0; i < sb.length(); i++) {
            char c = sb.charAt(i);
            int idx = alphabet.indexOf(c);
            if (idx != -1)
            {
                c = shiftedAlphabet.charAt(idx);
                sb.setCharAt(i, c);
            }
        }

        return sb.toString();
    }
}
```
