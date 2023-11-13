
===


```
class Solution:
    def longestCommonPrefix(self, strs: List[str]) -> str:
        a = ''
        if len(strs) == 1:
            return strs[0]
        s = sorted(strs)
        first = s[0]
        last = s[-1]
        for i in range( min(len(first),len(last)) ):
            if first[i] != last[i]:
                return a
            else:
                a += first[i]
        return a
```
