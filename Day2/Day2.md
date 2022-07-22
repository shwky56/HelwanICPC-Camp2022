# **HelwanICPC Camp2022 Day 2**

</br>

## **Lecture Toic**

- [**HelwanICPC Camp2022 Day 2**](#helwanicpc-camp2022-day-2)
  - [**Lecture Toic**](#lecture-toic)
  - [Mod Operation](#mod-operation)
  - [**Bit Operators**](#bit-operators)
  - [**Maximum Subbarray**](#maximum-subbarray)
    - [**Code:**](#code)
  - [**Compare Function**](#compare-function)
<!--* [*Pair*](#pair)
* [*Struct*](#struct)-->
* [*Compare Function*](#compare-function)
<!--* [*Struct Operators*](#struct-operators)
* [*CSES sorting problems*](#CSES-sorting-problems)
-->
</br>

---

</br>

## Mod Operation

</br>

* ### **Resources:**
  
  * [*https://www.mathsisfun.com/numbers/modulo.html*](https://www.mathsisfun.com/numbers/modulo.html)
  
</br>

* ### **Problem:**

  1. <https://vjudge.net/contest/505473#problem/F>

</br>

---

</br>

## **Bit Operators**

</br>

* ### **Resources:**
  
  * <https://www.programiz.com/cpp-programming/bitwise-operators>

</br>

* ### **Problem:**

  1. <https://vjudge.net/contest/505473#problem/F>

</br>

---

</br>

## **Maximum Subbarray**

</br>

### **Code:**

```cpp
 int n;
    cin>>n;ll cnt=0, mx=LONG_LONG_MIN;
    ll arr[n];
    for(int i=0;i<n;i++){
        cin>>arr[i];
    }
   

    ll cur = 0 , opt = LONG_LONG_MIN;
    for(int i = 0; i < n; i++){
        if(ar[i] > cur+ar[i]){
            cur = ar[i];
            l = i;
        } else {
            cur = cur + ar[i];
        }
        if(cur > opt){
            opt = cur;
            OptL = l;
            r = i;
        }
    }
    cout << opt << endl;
```

</br>

* ### **Resources:**
  
  * <https://www.geeksforgeeks.org/sort-c-stl/>

</br>

* ### **Problems:**

  1. <https://vjudge.net/contest/505473#problem/G>

</br>

---

</br>

## **Compare Function**

</br>

* ### **Resources:**
  
  * <https://www.geeksforgeeks.org/largest-sum-contiguous-subarray/>

</br>

* ### **Problems:**
    [*Problems 1 The Z sequence*](https://vjudge.net/contest/506001#problem/N)

</br>

* ### **Solution**
  
</br>

  * ```cpp
    #include<bits/stdc++.h>
    using namespace std;
    #define fast_cin() ios_base::sync_with_stdio(false); cin.tie(NULL); cout.tie(NULL)

    int cmp(int a,int b){
        if(a%2==0 && b%2==0){
            return a<b;
        }
        else if(a&1 && b&1){
            return b<a;
        }
        
        else
        return (b%2==0 && a&1);
    }

    int main(){
        fast_cin()
        int n ;
        cin >> n ;
        int arr[n];
        for(int i=0;i<n;i++)
        cin >> arr[i];
        sort(arr, arr+n,cmp);
        for(int i=0;i<n;i++)
        cout << arr[i]<< " ";

    }
    ```

</br>

* ### **Code:**
  
</br>

  * ```cpp
    #include <bits/stdc++.h>
    #define fast_cin()              ios_base::sync_with_stdio(false); cin.tie(NULL); cout.tie(NULL)
    using namespace std;
    void solve(){

    }

    bool cmp(string a , string b){
        if(a.size() < b.size())
            return true;
        else if(a.size() == b.size()){
            return a < b;
        }
        return false;
    }

    int main()
    {
        fast_cin();
        int n;
        cin >> n;
        string str[n];
        for(int i = 0; i < n; i++){
            cin >> str[i];
        }
        sort(str,str+n);
        for(int i=0;i<n;i++)
            cout<<str[i]<<" ";
        cout<<endl;

        sort(str , str + n , cmp);
        for(int i=0;i<n;i++)
            cout<<str[i]<<" ";
        cout<<endl;
        return 0;
    }
    ```

---

</br>
