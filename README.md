## Generate a random secret key for HS256

```
    public static void main(String[] args) {
        SecureRandom secureRandom = new SecureRandom();
        byte[] key = new byte[32]; // 32 bytes = 256 bits for HS256
        secureRandom.nextBytes(key);
        String encodedKey = Base64.getEncoder().encodeToString(key);
        System.out.println(encodedKey);
    }
```