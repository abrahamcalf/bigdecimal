<p align="center">
        ✖︎ Arithmetic operation in BigDecimal made easier
</p>

<p align="center">
  <a href="https://github.com/abranhe"><img src="https://abranhe.com/badge.svg"></a>
  <!-- <a href="https://maven-badges.herokuapp.com/maven-central/com.abranhe.easymath/EasyMathBigDecimal/badge.svg"><img src="#"></a> -->
	<a href="https://cash.me/$abranhe"><img src="https://cdn.abraham.gq/badges/cash-me.svg"></a>
	<a href="https://www.patreon.com/abranhe"><img src="https://cdn.abraham.gq/badges/patreon.svg" /></a>
	<a href="https://github.com/abranhe/bigdecimal/blob/master/LICENSE"><img src="https://img.shields.io/github/license/abranhe/bigdecimal.svg" /></a>
  <a href="https://travis-ci.org/abranhe/bigdecimal"><img src="https://img.shields.io/travis/abranhe/bigdecimal.svg?logo=travis" /></a>
</p>

# Why?

- No big deal working with **BigDecimal** operations
- Clean and focused
- Actively maintained

# Adding Dependency

```xml
<dependency>
        <groupId>com.abranhe.bigdecimal</groupId>
        <artifactId>bigdecimal</artifactId>
        <version>1.0.0</version>
</dependency>
```

# Adding Library

```java
import com.abranhe.bigdecimal.Operations;
```


## Usage

> Example 1

```java
import com.abranhe.bigdecimal.Operations;
import java.math.BigDecimal;

public static void main(String[] args){

        BigDecimal x = new BigDecimal("124567890.0987654321");
        BigDecimal y = new BigDecimal("987654321.123456789");

        System.out.println(Operations.add(x, y));
        //=> 1112222211.2222222211
}
```

> Example 2

```java
import java.math.BigDecimal;

public static void main(String[] args){

        BigDecimal x = new BigDecimal("124567890.0987654321");
        BigDecimal y = new BigDecimal("987654321.123456789");

        Operations o = new Operations();
        System.out.println(com.abranhe.bigdecimal.Operations.divide(x, y));
        //=> 0.12613
}
```
> Example 3

```java
import com.abranhe.bigdecimal.Operations.divide;
import java.math.RoundingMode;
import java.math.BigDecimal;

public static void main(String[] args){

        BigDecimal x = new BigDecimal("124567890.0987654321");
        BigDecimal y = new BigDecimal("987654321.123456789");

        System.out.println(divide(x, y, 9, RoundingMode.FLOOR));
        //=> 0.126124988
}
```

# API

### Addition

> Add two BigDecimal numbers

```java
public static BigDecimal add(BigDecimal x, BigDecimal y);
```

**Parameters:**
  - **x** - Big decimal number
  - **y** - Big decimal number

**Returns:**

Addition of `x` plus `y`

### Subtraction

> Add two BigDecimal numbers

```java
public static BigDecimal subtract(BigDecimal x, BigDecimal y);
```

**Parameters:**
  - **x** - Big decimal number
  - **y** - Big decimal number

**Returns:**

Subtraction of `x` minus `y`

### Multiplication

> Multiplication between two BigDecimal numbers

```java
public static BigDecimal multiply(BigDecimal x, BigDecimal y);
```

**Parameters:**
  - **x** - Big decimal number
  - **y** - Big decimal number

**Returns:**

Multiplication of `x` times `y`

### Division

> Division between two BigDecimal numbers

```java
public static BigDecimal divide(BigDecimal x, BigDecimal y, int scale, RoundingMode roundingMode);
```

**Parameters:**
  - **x** - Big decimal number
  - **y** - Big decimal number
  - **scale** - Scale of the BigDecimal quotient to be returned
  - **roundingMode** - Rounding mode to apply

**Returns:**

Division of `x` by `y`

### Default Division

> Division between two BigDecimal numbers

```java
public static BigDecimal divide(BigDecimal x, BigDecimal y);
```

**Parameters:**

  - **x** - Big decimal number
  - **y** - Big decimal number

**Default**

  - ~~**scale**~~ - `5`
  - ~~**roundingMode**~~ - `CEILING`

**Returns:**

Division of `x` by `y`


# Team

|[![Carlos Abraham Logo](https://avatars3.githubusercontent.com/u/21347264?s=50&v=4)](https://abranhe.com)|
| :-: |
| [Carlos Abraham](https://github.com/abranhe) |


# License

[MIT](https://github.com/abranhe/bigdecimal/blob/master/LICENSE) License © [Carlos Abraham](https://github.com/abranhe/)
