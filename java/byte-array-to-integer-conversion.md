# Byte array to integer conversion

The easiest way of converting an array of bytes representing a number into an integer is using `ByteBuffer.wrap()`:

```java
int value = ByteBuffer.wrap(array, startIndex, length)
  .order(ByteOrder.LITTLE_ENDIAN)
  .getInt();
```

By default, it uses `ByteOrder.BIG_ENDIAN`.