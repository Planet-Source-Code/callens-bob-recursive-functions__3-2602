<div align="center">

## recursive functions


</div>

### Description

Some functions to show the use of recursion in programming. This contains Fibonacci,Towers of Hanoi,Ackermann function
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Callens Bob](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/callens-bob.md)
**Level**          |Beginner
**User Rating**    |4.0 (8 globes from 2 users)
**Compatibility**  |C, C\+\+ \(general\)
**Category**       |[Math](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/math__3-12.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/callens-bob-recursive-functions__3-2602/archive/master.zip)





### Source Code

//Towers of Hanoi
<br>//example: you have 4 disks and have to move all disks from 1 to 3. solve(4,1,3,2);
<br>void solve(int disks, int src,int dest, int stack)
<br>{
<br><dd>	if(disks==1)
<br><dd>	{
<br><dd> printf("Move from %d to %d\n",src,dest);
<br><dd>	}
<br> else {
<br>
<br><dd><dd>	solve(disks-1,src,stack,dest);
<br><dd><dd>	solve(1,src,dest,stack);
<br><dd><dd>	solve(disks-1,stack,dest,src);
<br><dd> }
<br>}
<br>//Fibonacci numbers
<br>int fab(int n)
<br>{
<br><dd> if(n==1 || n==2)
<br><dd>	 {
<br><dd><dd>	 return 1;
<br><dd>	 }
<br> <dd>else
<br><dd><dd>return (fab(n-1)+fab(n-2));
<br>
}
<br>//ackermann function
<br>int ack(int m,int n)
<br>{
<br><dd>if(m==0)
<br><dd>{
<br><dd><dd>return n+1;
<br><dd>}
<br>
<br><dd>if(n==0)
<br><dd>{
<br><dd><dd>return ack(m-1,1);
<br><dd>}
<br><dd>else
<br><dd><dd>	return ack(m-1,ack(m,n-1));
<br>}

