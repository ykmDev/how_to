# How To Solve "More Green Grass" Algorithm

## Description
They say that the grass is always greener on the other side. This means that other people always seem to be doing better than you.Since we are programmers, wg; can quantify the greenness of all the "other sides” by writing some code.

There are n gardens in a row. The gardens
are numbered 1 to n and the i-th garden
has a greenness of a[i], with higher numbers representing greener gardens. Let us define the “greenness on the other side” for the owner of the i-th garden as the greenest garden besides the i-th garden. Create a program to enumerate all of the "greenness on the other side" for every garden in a row.

Given the greenness of n gardens, please calculate the "greenness on the other side" for each garden.

## Ans
```
    function main($lines) {
    $input = array_map('intval', explode(" ", $lines[1]));
    sort($input);
    $mostMaxGrass = $input[count($input) - 1];
    $secondMaxGrass = $input[count($input) - 2];
    $result = [];
    $counter = 1;

    while ($counter <= count($input)) {
        array_push($result, $mostMaxGrass);
        $counter++;
    }
    if($secondMaxGrass != $mostMaxGrass) $result[count($result) - 1] = $secondMaxGrass;
    echo implode(PHP_EOL, $result);
    }
```