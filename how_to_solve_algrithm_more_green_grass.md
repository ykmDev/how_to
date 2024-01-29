# How To Solve "More Green Grass" Algorithm

## Description
They say that the grass is always greener on the other side. This means that other people always seem to be doing better than you.Since we are programmers, wg; can quantify the greenness of all the "other sides” by writing some code.

There are n gardens in a row. The gardens
are numbered 1 to n and the i-th garden
has a greenness of a[i], with higher numbers representing greener gardens. Let us define the “greenness on the other side” for the owner of the i-th garden as the greenest garden besides the i-th garden. Create a program to enumerate all of the "greenness on the other side" for every garden in a row.

Given the greenness of n gardens, please calculate the "greenness on the other side" for each garden.

## Ans
```
function main($grass) {
  $input = $gardenlist = array_map('intval', explode(" ", $grass[1]));
  rsort($input);
  $result = array_fill(0, (count($input)), $input[0]);
  $result[array_search($input[0], $gardenlist)] = $input[1];
  echo implode(PHP_EOL, $result);
}

$array = array();
while (true) {
  $stdin = fgets(STDIN);
  if ($stdin == "") {
    break;
  }
  $array[] = rtrim($stdin);
}
main($array);
```