# Searching Algorithms

|  | Only on sorted array? | Time Complexity | Note |
|----------------------|-----------------------|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Linear Search | no | $ O(n) $ |  |
| Binary Search  | yes | $ O(log(n)) $ | Time complexity can be written as T(n) = T(n/2) + c, then use master theorem to derive it. |
| Jump Search | yes | $ O(\sqrt{n}) $ | The most optimal jump step $m$ is $m=\sqrt(n)$. Jump search is often used is system where traverse backward is costly (only has to traverse back once). |
| Interpolation Search | yes | Average $ O(log(log(n)))  $ Worst $ O(n) $ | An improvement of binary search on uniformly distributed array. Instead of checking the middle like binary search, interpolation search checks according to the value of the key being searched. |

