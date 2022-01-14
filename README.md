import re
string = input("Enter any string:->")
mylist=[]
vscore = 0
cscore = 0
vowels="aeiou|AEIOU"
for i in range(len(string)):
    for j in range(i,len(string)+1):
        if i==j:
            pass
        else:
          x=string[i:j]
          mylist.append(x)
print("Substrings:->")
print(mylist)
for i in mylist:
    if i[0] in vowels:
        vscore+=1
    else:
        cscore+=1
print("vowel finder's score:",vscore)
print("consonant finder's score:",cscore)
if vscore>cscore:
    print("vowel finder is winner")
if vscore<cscore:
    print("consnant finder is winner")
else:
    print("tied")
