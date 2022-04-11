s=[input() for _ in range(int(input()))]
r=[]
for i in range(len(s)):
    a1=False
    n1=0
    t1=False
    o1=False
    d=' '.join(s[i]).split(' ')
    for c in d:
        if c in ["a"]:
            a1=True
        if c in ['t']:
            t1=True
        if c in ['o']:
            o1=True
        if c in ['n']:
            n1+=1
    if n1>1:
        if int(a1)+int(t1)+int(o1)+2==5:
            r.append(str(i+1))
f=[s[int(i)-1] for i in r]
for i in range(len(f)):
    d=' '.join(s[i]).split(' ')
        for j in range(len(d)):
            if d[j] not in ['a','n','t','o','n']:
                del d[j]
            
print(f)
