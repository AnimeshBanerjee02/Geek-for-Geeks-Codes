import math
class Solution:
    def closestPalindrome(self, n):
        n = int(n)
        if n<10:
            return n
        elif math.log(n,10)-int(math.log(n,10))==0:
            return n-1
        else:
            out=str(n)
            ll=int((len(out)+1)/2)
            first_Half=out[:ll]
            if len(out)%2==0:
                n1=int(first_Half+first_Half[::-1])
                n2=int(str(int(first_Half)+1)+str(int(first_Half)+1)[::-1])
                n3=int(str(int(first_Half)-1)+str(int(first_Half)-1)[::-1])
            else:
                n1=int(first_Half[:-1]+first_Half[::-1])
                n2=int(str(int(first_Half)+1)[:-1]+str(int(first_Half)+1)[::-1])
                n3=int(str(int(first_Half)-1)[:-1]+str(int(first_Half)-1)[::-1])
            if abs(n-n3)<=abs(n-n1) and abs(n-n3)<=abs(n-n2):
                out=n3
            elif abs(n-n1)<=abs(n-n2):
                out=n1
            else:
                out=n2
            return out
