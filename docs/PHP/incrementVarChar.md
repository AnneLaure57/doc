https://stackoverflow.com/questions/46343127/auto-increment-the-varchar-value-obtained-from-database

$num = 'MOB' . str_pad($su + substr($ids, 3), 6, '0', STR_PAD_LEFT);

https://stackoverflow.com/questions/52218027/generate-a-random-number-between-1-and-999/52218095

echo(mt_rand(1,999));

https://maymay.net/blog/2004/12/19/generating-random-letters-in-php/
 $int = rand(0,51);
    $a_z = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ";
    $rand_letter = $a_z[$int];
    return $rand_letter;

https://stackoverflow.com/questions/4851298/regular-expression-to-find-the-number-0-or-decimal

A simple regex to validate a number:

^\d+(\.\d+)?$
This should work for a number with optional leading zeros, with an optional single dot and more digits.

^...$ - match from start to end of the string (will not validate ab12.4c)
\d+ - At least one digit.
(...)? - optional group of...
\.\d+ - literal dot and one or more digits.

https://levelup.gitconnected.com/writing-a-regex-to-detect-a-range-of-numbers-why-not-just-parse-the-string-to-integers-instead-8a24089eab0b


/^([0-9]+)\.([0-9]{2})$/

https://stackoverflow.com/questions/32008429/regex-fails-with-decimal-digits-00-causes-preg-match-to-return-false