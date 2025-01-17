# PseudoRandom

## Introduction

The PseudoRandom component is a component that generates pseudo-random numbers.

?> The PseudoRandom component is meant as a direct replacement for PHP [`mt_rand()`](https://www.php.net/manual/en/function.mt-rand.php), [`rand()`](https://www.php.net/manual/en/function.rand.php) functions.

## Usage

```php
use Psl\PseudoRandom;

$random_number = PseudoRandom\int();
$random_float = PseudoRandom\float();
```

## API

### Functions

* `PseudoRandom\int(int $min = Math\INT64_MIN, int $max = Math\INT64_MAX): int`

  Returns a pseudo-random integer in the given range.

  * `$min`: The minimum value.
  * `$max`: The maximum value.

  If `$min` is greater than `$max`, `Psl\Exception\InvarViolationException` is thrown.

  > This function does not cause any external mutations.

  ```php
  use Psl\PseudoRandom;

  $random_number = PseudoRandom\int(0, 10);

  // 0 <= $random_number <= 10
  ```

* `PseudoRandom\float(): float`

  Returns a pseudo-random float in the range of [0.0, 1.0].

  ```php
  use Psl\PseudoRandom;

  $random_float = PseudoRandom\float();

  // 0.0 <= $random_float <= 1.0
  ```

  > This function does not cause any external mutations.
