# 13.-Roman-to-Integer
class Solution {
    public int romanToInt(String s){
        char a[]=s.toCharArray();
        int c=0;
        for(int i=0;i<s.length();i++)
        {
            if(a[i]=='I')
            {
                if(i+1!=s.length())
                {
                    if(a[i+1]=='V')
                    {
                        c+=4;
                         i++;
                    }
                    else if(a[i+1]=='X')
                    {
                        c+=9;
                         i++;
                    }
                    else
                        c+=1;
                }
                else
                    c+=1;
            }
            else  if(a[i]=='V')
                    c+=5;
            else if(a[i]=='X')
            {
                if(i+1!=s.length())
                {
                    if(a[i+1]=='L')
                    {
                        c+=40;
                         i++;
                    }
                    else if(a[i+1]=='C')
                    {
                        c+=90;
                         i++;
                    }
                    else
                        c+=10;
                }
                else
                    c+=10;
            }
            else if(a[i]=='L')
                    c+=50;
            else if(a[i]=='C')
            {
                if(i+1!=s.length())
                {
                    if(a[i+1]=='D')
                    {
                        c+=400;
                         i++;;
                    }
                    else if(a[i+1]=='M')
                    {
                        c+=900;
                         i++;
                    }
                    else
                        c+=100;
                }
                else
                    c+=100;
            }
            else if(a[i]=='D')
                    c+=500;
            else if(a[i]=='M')
                    c+=1000;
        }
        return c;
    }
}
