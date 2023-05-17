# 算法思想
利用已经匹配的结果加快模式串的滑动速度，设置next[j]数组
## 算法描述
    int Lndex_KMP(SStringS,SString T,int pos){
    i=pos,j=1;
    whlie(i<S.length &&j<T.length){
    if(j==0||S.ch[i]==T.ch[j]){i++;j++;}
    else 
    j=next[j];//不变，j后退
    }
    if(j>T.length) return i-T.length;//匹配成功
    else return 0;//*返回不匹配标志*
    }
