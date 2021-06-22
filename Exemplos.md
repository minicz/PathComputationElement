# Exemplo 1
```
Qual topologia/demanda? 1
Topo:
{[r1,r2,100],[r1,r3,100],[r2,r3,100]}
Demandas:
[[r1_r2_1,r1,r2,10],[r1_r2_2,r1,r2,10],[r3_r2_1,r3,r2,10]]
Lista de Caminhos:
[[[r1,r2],[r1,r3,r2]],[[r1,r2],[r1,r3,r2]],[[r3,r2],[r3,r1,r2]]]
 
estado final:
{[r1,r2,80],[r1,r3,100],[r2,r3,90]}
[demanda([r1_r2_1,r1,r2,10],[r1,r2]),demanda([r1_r2_2,r1,r2,10],[r1,r2]),demanda([r3_r2_1,r3,r2,10],[r3,r2])]

real    0m19,255s
user    0m0,014s
sys     0m0,014s
```

# Exemplo 2
```
Qual topologia/demanda? 2
Topo:
{[r1,r2,100],[r1,r3,100],[r2,r3,100]}
Demandas:
[[r1_r2_1,r1,r2,90],[r1_r2_2,r1,r2,20],[r3_r2_1,r3,r2,80],[r3_r2_2,r3,r2,5]]
Lista de Caminhos:
[[[r1,r2],[r1,r3,r2]],[[r1,r2],[r1,r3,r2]],[[r3,r2],[r3,r1,r2]],[[r3,r2],[r3,r1,r2]]]
 
estado final:
{[r1,r2,5],[r1,r3,75],[r2,r3,0]}
[demanda([r1_r2_1,r1,r2,90],[r1,r2]),demanda([r1_r2_2,r1,r2,20],[r1,r3,r2]),demanda([r3_r2_1,r3,r2,80],[r3,r2]),demanda([r3_r2_2,r3,r2,5],[r3,r1,r2])]

real    0m0,499s
user    0m0,004s
sys     0m0,021s
```

# Exemplo 3
```
Qual topologia/demanda? 3
Topo:
{[r1,r2,100],[r1,r3,100],[r2,r3,100]}
Demandas:
[[r2_r3_1,r2,r3,70],[r1_r2_1,r1,r2,20],[r1_r2_2,r1,r2,45],[r1_r2_3,r1,r2,45]]
Lista de Caminhos:
[[[r2,r3],[r2,r1,r3]],[[r1,r2],[r1,r3,r2]],[[r1,r2],[r1,r3,r2]],[[r1,r2],[r1,r3,r2]]]
 
estado final:
{[r1,r2,10],[r1,r3,80],[r2,r3,10]}
[demanda([r2_r3_1,r2,r3,70],[r2,r3]),demanda([r1_r2_1,r1,r2,20],[r1,r3,r2]),demanda([r1_r2_2,r1,r2,45],[r1,r2]),demanda([r1_r2_3,r1,r2,45],[r1,r2])]

real    0m0,922s
user    0m0,009s
sys     0m0,014s
```

# Exemplo 4
```
Qual topologia/demanda? 4
Topo:
{[r1,r2,100],[r1,r3,100],[r2,r3,100]}
Demandas:
[[r2_r3_1,r2,r3,70],[r1_r2_1,r1,r2,40],[r1_r2_2,r1,r2,45],[r1_r2_3,r1,r2,45]]
Lista de Caminhos:
[[[r2,r3],[r2,r1,r3]],[[r1,r2],[r1,r3,r2]],[[r1,r2],[r1,r3,r2]],[[r1,r2],[r1,r3,r2]]]
 
*** error(failed,main/0)


real    0m1,496s
user    0m0,009s
sys     0m0,018s
```

# Exemplo 5
```
Qual topologia/demanda? 5
Topo:
{[sp,rj,10000],[sp,pr,5000],[pr,sc,5000],[sp,go,5000],[rj,sc,5000],[mg,go,5000],[rj,mg,5000]}
Demandas:
[[1,sp,rj,1000],[2,sp,rj,1000],[3,sp,pr,500],[4,sp,go,500],[5,mg,pr,250],[6,sc,go,250],[7,pr,rj,500],[8,pr,go,250],[9,rj,sc,500],[10,mg,go,250],[11,pr,sp,1000],[12,sc,rj,250],[13,rj,mg,1000],[14,sp,rj,500],[15,sp,go,250],[16,go,mg,500],[17,go,sc,500],[18,rj,sp,1000],[19,sp,rj,1000],[20,go,sc,250]]
Lista de Caminhos:
[[[sp,rj],[sp,pr,sc,rj],[sp,go,mg,rj]],[[sp,rj],[sp,pr,sc,rj],[sp,go,mg,rj]],[[sp,pr],[sp,rj,sc,pr],[sp,go,mg,rj,sc,pr]],[[sp,go],[sp,rj,mg,go],[sp,pr,sc,rj,mg,go]],[[mg,go,sp,pr],[mg,go,sp,rj,sc,pr],[mg,rj,sc,pr],[mg,rj,sp,pr]],[[sc,pr,sp,go],[sc,pr,sp,rj,mg,go],[sc,rj,mg,go],[sc,rj,sp,go]],[[pr,sc,rj],[pr,sp,rj],[pr,sp,go,mg,rj]],[[pr,sc,rj,mg,go],[pr,sc,rj,sp,go],[pr,sp,go],[pr,sp,rj,mg,go]],[[rj,sc],[rj,mg,go,sp,pr,sc],[rj,sp,pr,sc]],[[mg,go],[mg,rj,sc,pr,sp,go],[mg,rj,sp,go]],[[pr,sp],[pr,sc,rj,sp],[pr,sc,rj,mg,go,sp]],[[sc,rj],[sc,pr,sp,rj],[sc,pr,sp,go,mg,rj]],[[rj,mg],[rj,sc,pr,sp,go,mg],[rj,sp,go,mg]],[[sp,rj],[sp,pr,sc,rj],[sp,go,mg,rj]],[[sp,go],[sp,rj,mg,go],[sp,pr,sc,rj,mg,go]],[[go,mg],[go,sp,rj,mg],[go,sp,pr,sc,rj,mg]],[[go,sp,rj,sc],[go,sp,pr,sc],[go,mg,rj,sc],[go,mg,rj,sp,pr,sc]],[[rj,sp],[rj,sc,pr,sp],[rj,mg,go,sp]],[[sp,rj],[sp,pr,sc,rj],[sp,go,mg,rj]],[[go,sp,rj,sc],[go,sp,pr,sc],[go,mg,rj,sc],[go,mg,rj,sp,pr,sc]]]
 
estado final:
{[sp,rj,4750],[sp,pr,3000],[pr,sc,4000],[sp,go,3000],[rj,sc,2750],[mg,go,3750],[rj,mg,3750]}
[demanda([1,sp,rj,1000],[sp,rj]),demanda([2,sp,rj,1000],[sp,rj]),demanda([3,sp,pr,500],[sp,pr]),demanda([4,sp,go,500],[sp,go]),demanda([5,mg,pr,250],[mg,go,sp,pr]),demanda([6,sc,go,250],[sc,pr,sp,go]),demanda([7,pr,rj,500],[pr,sc,rj]),demanda([8,pr,go,250],[pr,sc,rj,mg,go]),demanda([9,rj,sc,500],[rj,sc]),demanda([10,mg,go,250],[mg,go]),demanda([11,pr,sp,1000],[pr,sp]),demanda([12,sc,rj,250],[sc,rj]),demanda([13,rj,mg,1000],[rj,mg]),demanda([14,sp,rj,500],[sp,rj]),demanda([15,sp,go,250],[sp,go]),demanda([16,go,mg,500],[go,mg]),demanda([17,go,sc,500],[go,sp,rj,sc]),demanda([18,rj,sp,1000],[rj,sp]),demanda([19,sp,rj,1000],[sp,rj]),demanda([20,go,sc,250],[go,sp,rj,sc])]

real    0m2,116s
user    0m0,013s
sys     0m0,012s
```

# Exemplo 6
```
Qual topologia/demanda? 6
Topo:
{[sp,rj,10000],[sp,pr,5000],[pr,sc,5000],[sp,go,5000],[rj,sc,5000],[mg,go,5000],[rj,mg,5000]}
Demandas:
[[1,sp,rj,1000],[2,sp,rj,1000],[3,sp,pr,500],[4,sp,go,500],[5,mg,pr,250],[6,sc,go,250],[7,pr,rj,500],[8,pr,go,250],[9,rj,sc,500],[10,mg,go,250],[11,pr,sp,1000],[12,sc,rj,250],[13,rj,mg,1000],[14,sp,rj,500],[15,sp,go,250],[16,go,mg,500],[17,go,sc,500],[18,rj,sp,1000],[19,sp,rj,1000],[20,go,sc,250],[21,go,mg,500],[22,mg,sc,500],[23,sp,mg,1000],[24,pr,mg,500],[25,pr,rj,500],[26,go,rj,500],[27,pr,sp,1000],[28,sp,rj,1000],[29,pr,sp,500],[30,pr,mg,500]]
Lista de Caminhos:
[[[sp,rj],[sp,pr,sc,rj],[sp,go,mg,rj]],[[sp,rj],[sp,pr,sc,rj],[sp,go,mg,rj]],[[sp,pr],[sp,rj,sc,pr],[sp,go,mg,rj,sc,pr]],[[sp,go],[sp,rj,mg,go],[sp,pr,sc,rj,mg,go]],[[mg,go,sp,pr],[mg,go,sp,rj,sc,pr],[mg,rj,sc,pr],[mg,rj,sp,pr]],[[sc,pr,sp,go],[sc,pr,sp,rj,mg,go],[sc,rj,mg,go],[sc,rj,sp,go]],[[pr,sc,rj],[pr,sp,rj],[pr,sp,go,mg,rj]],[[pr,sc,rj,mg,go],[pr,sc,rj,sp,go],[pr,sp,go],[pr,sp,rj,mg,go]],[[rj,sc],[rj,mg,go,sp,pr,sc],[rj,sp,pr,sc]],[[mg,go],[mg,rj,sc,pr,sp,go],[mg,rj,sp,go]],[[pr,sp],[pr,sc,rj,sp],[pr,sc,rj,mg,go,sp]],[[sc,rj],[sc,pr,sp,rj],[sc,pr,sp,go,mg,rj]],[[rj,mg],[rj,sc,pr,sp,go,mg],[rj,sp,go,mg]],[[sp,rj],[sp,pr,sc,rj],[sp,go,mg,rj]],[[sp,go],[sp,rj,mg,go],[sp,pr,sc,rj,mg,go]],[[go,mg],[go,sp,rj,mg],[go,sp,pr,sc,rj,mg]],[[go,sp,rj,sc],[go,sp,pr,sc],[go,mg,rj,sc],[go,mg,rj,sp,pr,sc]],[[rj,sp],[rj,sc,pr,sp],[rj,mg,go,sp]],[[sp,rj],[sp,pr,sc,rj],[sp,go,mg,rj]],[[go,sp,rj,sc],[go,sp,pr,sc],[go,mg,rj,sc],[go,mg,rj,sp,pr,sc]],[[go,mg],[go,sp,rj,mg],[go,sp,pr,sc,rj,mg]],[[mg,go,sp,rj,sc],[mg,go,sp,pr,sc],[mg,rj,sc],[mg,rj,sp,pr,sc]],[[sp,rj,mg],[sp,pr,sc,rj,mg],[sp,go,mg]],[[pr,sc,rj,mg],[pr,sc,rj,sp,go,mg],[pr,sp,rj,mg],[pr,sp,go,mg]],[[pr,sc,rj],[pr,sp,rj],[pr,sp,go,mg,rj]],[[go,sp,rj],[go,sp,pr,sc,rj],[go,mg,rj]],[[pr,sp],[pr,sc,rj,sp],[pr,sc,rj,mg,go,sp]],[[sp,rj],[sp,pr,sc,rj],[sp,go,mg,rj]],[[pr,sp],[pr,sc,rj,sp],[pr,sc,rj,mg,go,sp]],[[pr,sc,rj,mg],[pr,sc,rj,sp,go,mg],[pr,sp,rj,mg],[pr,sp,go,mg]]]
 
estado final:
{[sp,rj,1750],[sp,pr,1500],[pr,sc,2500],[sp,go,2000],[rj,sc,750],[mg,go,2750],[rj,mg,1750]}
[demanda([1,sp,rj,1000],[sp,rj]),demanda([2,sp,rj,1000],[sp,rj]),demanda([3,sp,pr,500],[sp,pr]),demanda([4,sp,go,500],[sp,go]),demanda([5,mg,pr,250],[mg,go,sp,pr]),demanda([6,sc,go,250],[sc,pr,sp,go]),demanda([7,pr,rj,500],[pr,sc,rj]),demanda([8,pr,go,250],[pr,sc,rj,mg,go]),demanda([9,rj,sc,500],[rj,sc]),demanda([10,mg,go,250],[mg,go]),demanda([11,pr,sp,1000],[pr,sp]),demanda([12,sc,rj,250],[sc,rj]),demanda([13,rj,mg,1000],[rj,mg]),demanda([14,sp,rj,500],[sp,rj]),demanda([15,sp,go,250],[sp,go]),demanda([16,go,mg,500],[go,mg]),demanda([17,go,sc,500],[go,sp,rj,sc]),demanda([18,rj,sp,1000],[rj,sp]),demanda([19,sp,rj,1000],[sp,rj]),demanda([20,go,sc,250],[go,sp,rj,sc]),demanda([21,go,mg,500],[go,mg]),demanda([22,mg,sc,500],[mg,go,sp,rj,sc]),demanda([23,sp,mg,1000],[sp,rj,mg]),demanda([24,pr,mg,500],[pr,sc,rj,mg]),demanda([25,pr,rj,500],[pr,sc,rj]),demanda([26,go,rj,500],[go,sp,rj]),demanda([27,pr,sp,1000],[pr,sp]),demanda([28,sp,rj,1000],[sp,rj]),demanda([29,pr,sp,500],[pr,sp]),demanda([30,pr,mg,500],[pr,sc,rj,mg])]

real    0m1,017s
user    0m0,010s
sys     0m0,017s
```

# Exemplo 7
```
Qual topologia/demanda? 7
Topo:
{[sp,rj,10000],[sp,pr,5000],[pr,sc,5000],[sp,go,5000],[rj,sc,5000],[mg,go,5000],[rj,mg,5000]}
Demandas:
[[1,sp,rj,1000],[2,sp,rj,1000],[3,sp,pr,500],[4,sp,go,500],[5,mg,pr,250],[6,sc,go,250],[7,pr,rj,500],[8,pr,go,250],[9,rj,sc,500],[10,mg,go,250],[11,pr,sp,1000],[12,sc,rj,250],[13,rj,mg,1000],[14,sp,rj,500],[15,sp,go,250],[16,go,mg,500],[17,go,sc,500],[18,rj,sp,1000],[19,sp,rj,1000],[20,go,sc,250],[21,go,mg,500],[22,mg,sc,500],[23,sp,mg,1000],[24,pr,mg,500],[25,pr,rj,500],[26,go,rj,500],[27,pr,sp,1000],[28,sp,rj,1000],[29,pr,sp,500],[30,pr,mg,500],[31,sc,go,500],[32,sc,pr,250],[33,pr,go,250],[34,rj,sc,500],[35,sp,rj,1000]]
Lista de Caminhos:
[[[sp,rj],[sp,pr,sc,rj],[sp,go,mg,rj]],[[sp,rj],[sp,pr,sc,rj],[sp,go,mg,rj]],[[sp,pr],[sp,rj,sc,pr],[sp,go,mg,rj,sc,pr]],[[sp,go],[sp,rj,mg,go],[sp,pr,sc,rj,mg,go]],[[mg,go,sp,pr],[mg,go,sp,rj,sc,pr],[mg,rj,sc,pr],[mg,rj,sp,pr]],[[sc,pr,sp,go],[sc,pr,sp,rj,mg,go],[sc,rj,mg,go],[sc,rj,sp,go]],[[pr,sc,rj],[pr,sp,rj],[pr,sp,go,mg,rj]],[[pr,sc,rj,mg,go],[pr,sc,rj,sp,go],[pr,sp,go],[pr,sp,rj,mg,go]],[[rj,sc],[rj,mg,go,sp,pr,sc],[rj,sp,pr,sc]],[[mg,go],[mg,rj,sc,pr,sp,go],[mg,rj,sp,go]],[[pr,sp],[pr,sc,rj,sp],[pr,sc,rj,mg,go,sp]],[[sc,rj],[sc,pr,sp,rj],[sc,pr,sp,go,mg,rj]],[[rj,mg],[rj,sc,pr,sp,go,mg],[rj,sp,go,mg]],[[sp,rj],[sp,pr,sc,rj],[sp,go,mg,rj]],[[sp,go],[sp,rj,mg,go],[sp,pr,sc,rj,mg,go]],[[go,mg],[go,sp,rj,mg],[go,sp,pr,sc,rj,mg]],[[go,sp,rj,sc],[go,sp,pr,sc],[go,mg,rj,sc],[go,mg,rj,sp,pr,sc]],[[rj,sp],[rj,sc,pr,sp],[rj,mg,go,sp]],[[sp,rj],[sp,pr,sc,rj],[sp,go,mg,rj]],[[go,sp,rj,sc],[go,sp,pr,sc],[go,mg,rj,sc],[go,mg,rj,sp,pr,sc]],[[go,mg],[go,sp,rj,mg],[go,sp,pr,sc,rj,mg]],[[mg,go,sp,rj,sc],[mg,go,sp,pr,sc],[mg,rj,sc],[mg,rj,sp,pr,sc]],[[sp,rj,mg],[sp,pr,sc,rj,mg],[sp,go,mg]],[[pr,sc,rj,mg],[pr,sc,rj,sp,go,mg],[pr,sp,rj,mg],[pr,sp,go,mg]],[[pr,sc,rj],[pr,sp,rj],[pr,sp,go,mg,rj]],[[go,sp,rj],[go,sp,pr,sc,rj],[go,mg,rj]],[[pr,sp],[pr,sc,rj,sp],[pr,sc,rj,mg,go,sp]],[[sp,rj],[sp,pr,sc,rj],[sp,go,mg,rj]],[[pr,sp],[pr,sc,rj,sp],[pr,sc,rj,mg,go,sp]],[[pr,sc,rj,mg],[pr,sc,rj,sp,go,mg],[pr,sp,rj,mg],[pr,sp,go,mg]],[[sc,pr,sp,go],[sc,pr,sp,rj,mg,go],[sc,rj,mg,go],[sc,rj,sp,go]],[[sc,pr],[sc,rj,mg,go,sp,pr],[sc,rj,sp,pr]],[[pr,sc,rj,mg,go],[pr,sc,rj,sp,go],[pr,sp,go],[pr,sp,rj,mg,go]],[[rj,sc],[rj,mg,go,sp,pr,sc],[rj,sp,pr,sc]],[[sp,rj],[sp,pr,sc,rj],[sp,go,mg,rj]]]
 
estado final:
{[sp,rj,750],[sp,pr,1000],[pr,sc,1500],[sp,go,1500],[rj,sc,0],[mg,go,2500],[rj,mg,1500]}
[demanda([1,sp,rj,1000],[sp,rj]),demanda([2,sp,rj,1000],[sp,rj]),demanda([3,sp,pr,500],[sp,pr]),demanda([4,sp,go,500],[sp,go]),demanda([5,mg,pr,250],[mg,go,sp,pr]),demanda([6,sc,go,250],[sc,pr,sp,go]),demanda([7,pr,rj,500],[pr,sc,rj]),demanda([8,pr,go,250],[pr,sc,rj,mg,go]),demanda([9,rj,sc,500],[rj,sc]),demanda([10,mg,go,250],[mg,go]),demanda([11,pr,sp,1000],[pr,sp]),demanda([12,sc,rj,250],[sc,rj]),demanda([13,rj,mg,1000],[rj,mg]),demanda([14,sp,rj,500],[sp,rj]),demanda([15,sp,go,250],[sp,go]),demanda([16,go,mg,500],[go,mg]),demanda([17,go,sc,500],[go,sp,rj,sc]),demanda([18,rj,sp,1000],[rj,sp]),demanda([19,sp,rj,1000],[sp,rj]),demanda([20,go,sc,250],[go,sp,rj,sc]),demanda([21,go,mg,500],[go,mg]),demanda([22,mg,sc,500],[mg,go,sp,rj,sc]),demanda([23,sp,mg,1000],[sp,rj,mg]),demanda([24,pr,mg,500],[pr,sc,rj,mg]),demanda([25,pr,rj,500],[pr,sc,rj]),demanda([26,go,rj,500],[go,sp,rj]),demanda([27,pr,sp,1000],[pr,sp]),demanda([28,sp,rj,1000],[sp,rj]),demanda([29,pr,sp,500],[pr,sp]),demanda([30,pr,mg,500],[pr,sc,rj,mg]),demanda([31,sc,go,500],[sc,pr,sp,go]),demanda([32,sc,pr,250],[sc,pr]),demanda([33,pr,go,250],[pr,sc,rj,mg,go]),demanda([34,rj,sc,500],[rj,sc]),demanda([35,sp,rj,1000],[sp,rj])]

real    0m1,249s
user    0m0,009s
sys     0m0,022s
```

# Exemplo 8
```
Qual topologia/demanda? 8
Topo:
{[sp,rj,10000],[sp,pr,5000],[pr,sc,5000],[sp,go,5000],[rj,sc,5000],[mg,go,5000],[rj,mg,5000]}
Demandas:
[[1,sp,rj,1000],[2,sp,rj,1000],[3,sp,pr,500],[4,sp,go,500],[5,mg,pr,250],[6,sc,go,250],[7,pr,rj,500],[8,pr,go,250],[9,rj,sc,500],[10,mg,go,250],[11,pr,sp,1000],[12,sc,rj,250],[13,rj,mg,1000],[14,sp,rj,500],[15,sp,go,250],[16,go,mg,500],[17,go,sc,500],[18,rj,sp,1000],[19,sp,rj,1000],[20,go,sc,250],[21,go,mg,500],[22,mg,sc,500],[23,sp,mg,1000],[24,pr,mg,500],[25,pr,rj,500],[26,go,rj,500],[27,pr,sp,1000],[28,sp,rj,1000],[29,pr,sp,500],[30,pr,mg,500],[31,sc,go,500],[32,sc,pr,250],[33,pr,go,250],[34,rj,sc,500],[35,sp,rj,1000],[36,rj,sc,250],[37,sp,mg,250],[38,sc,mg,250],[39,pr,rj,250],[40,pr,go,250]]
Lista de Caminhos:
[[[sp,rj],[sp,pr,sc,rj],[sp,go,mg,rj]],[[sp,rj],[sp,pr,sc,rj],[sp,go,mg,rj]],[[sp,pr],[sp,rj,sc,pr],[sp,go,mg,rj,sc,pr]],[[sp,go],[sp,rj,mg,go],[sp,pr,sc,rj,mg,go]],[[mg,go,sp,pr],[mg,go,sp,rj,sc,pr],[mg,rj,sc,pr],[mg,rj,sp,pr]],[[sc,pr,sp,go],[sc,pr,sp,rj,mg,go],[sc,rj,mg,go],[sc,rj,sp,go]],[[pr,sc,rj],[pr,sp,rj],[pr,sp,go,mg,rj]],[[pr,sc,rj,mg,go],[pr,sc,rj,sp,go],[pr,sp,go],[pr,sp,rj,mg,go]],[[rj,sc],[rj,mg,go,sp,pr,sc],[rj,sp,pr,sc]],[[mg,go],[mg,rj,sc,pr,sp,go],[mg,rj,sp,go]],[[pr,sp],[pr,sc,rj,sp],[pr,sc,rj,mg,go,sp]],[[sc,rj],[sc,pr,sp,rj],[sc,pr,sp,go,mg,rj]],[[rj,mg],[rj,sc,pr,sp,go,mg],[rj,sp,go,mg]],[[sp,rj],[sp,pr,sc,rj],[sp,go,mg,rj]],[[sp,go],[sp,rj,mg,go],[sp,pr,sc,rj,mg,go]],[[go,mg],[go,sp,rj,mg],[go,sp,pr,sc,rj,mg]],[[go,sp,rj,sc],[go,sp,pr,sc],[go,mg,rj,sc],[go,mg,rj,sp,pr,sc]],[[rj,sp],[rj,sc,pr,sp],[rj,mg,go,sp]],[[sp,rj],[sp,pr,sc,rj],[sp,go,mg,rj]],[[go,sp,rj,sc],[go,sp,pr,sc],[go,mg,rj,sc],[go,mg,rj,sp,pr,sc]],[[go,mg],[go,sp,rj,mg],[go,sp,pr,sc,rj,mg]],[[mg,go,sp,rj,sc],[mg,go,sp,pr,sc],[mg,rj,sc],[mg,rj,sp,pr,sc]],[[sp,rj,mg],[sp,pr,sc,rj,mg],[sp,go,mg]],[[pr,sc,rj,mg],[pr,sc,rj,sp,go,mg],[pr,sp,rj,mg],[pr,sp,go,mg]],[[pr,sc,rj],[pr,sp,rj],[pr,sp,go,mg,rj]],[[go,sp,rj],[go,sp,pr,sc,rj],[go,mg,rj]],[[pr,sp],[pr,sc,rj,sp],[pr,sc,rj,mg,go,sp]],[[sp,rj],[sp,pr,sc,rj],[sp,go,mg,rj]],[[pr,sp],[pr,sc,rj,sp],[pr,sc,rj,mg,go,sp]],[[pr,sc,rj,mg],[pr,sc,rj,sp,go,mg],[pr,sp,rj,mg],[pr,sp,go,mg]],[[sc,pr,sp,go],[sc,pr,sp,rj,mg,go],[sc,rj,mg,go],[sc,rj,sp,go]],[[sc,pr],[sc,rj,mg,go,sp,pr],[sc,rj,sp,pr]],[[pr,sc,rj,mg,go],[pr,sc,rj,sp,go],[pr,sp,go],[pr,sp,rj,mg,go]],[[rj,sc],[rj,mg,go,sp,pr,sc],[rj,sp,pr,sc]],[[sp,rj],[sp,pr,sc,rj],[sp,go,mg,rj]],[[rj,sc],[rj,mg,go,sp,pr,sc],[rj,sp,pr,sc]],[[sp,rj,mg],[sp,pr,sc,rj,mg],[sp,go,mg]],[[sc,pr,sp,rj,mg],[sc,pr,sp,go,mg],[sc,rj,mg],[sc,rj,sp,go,mg]],[[pr,sc,rj],[pr,sp,rj],[pr,sp,go,mg,rj]],[[pr,sc,rj,mg,go],[pr,sc,rj,sp,go],[pr,sp,go],[pr,sp,rj,mg,go]]]
 
estado final:
{[sp,rj,0],[sp,pr,0],[pr,sc,1000],[sp,go,1000],[rj,sc,0],[mg,go,2250],[rj,mg,750]}
[demanda([1,sp,rj,1000],[sp,rj]),demanda([2,sp,rj,1000],[sp,rj]),demanda([3,sp,pr,500],[sp,pr]),demanda([4,sp,go,500],[sp,go]),demanda([5,mg,pr,250],[mg,go,sp,pr]),demanda([6,sc,go,250],[sc,pr,sp,go]),demanda([7,pr,rj,500],[pr,sc,rj]),demanda([8,pr,go,250],[pr,sc,rj,mg,go]),demanda([9,rj,sc,500],[rj,sc]),demanda([10,mg,go,250],[mg,go]),demanda([11,pr,sp,1000],[pr,sp]),demanda([12,sc,rj,250],[sc,rj]),demanda([13,rj,mg,1000],[rj,mg]),demanda([14,sp,rj,500],[sp,rj]),demanda([15,sp,go,250],[sp,go]),demanda([16,go,mg,500],[go,mg]),demanda([17,go,sc,500],[go,sp,rj,sc]),demanda([18,rj,sp,1000],[rj,sp]),demanda([19,sp,rj,1000],[sp,rj]),demanda([20,go,sc,250],[go,sp,rj,sc]),demanda([21,go,mg,500],[go,mg]),demanda([22,mg,sc,500],[mg,go,sp,rj,sc]),demanda([23,sp,mg,1000],[sp,rj,mg]),demanda([24,pr,mg,500],[pr,sc,rj,mg]),demanda([25,pr,rj,500],[pr,sc,rj]),demanda([26,go,rj,500],[go,sp,rj]),demanda([27,pr,sp,1000],[pr,sp]),demanda([28,sp,rj,1000],[sp,rj]),demanda([29,pr,sp,500],[pr,sp]),demanda([30,pr,mg,500],[pr,sc,rj,mg]),demanda([31,sc,go,500],[sc,pr,sp,go]),demanda([32,sc,pr,250],[sc,pr]),demanda([33,pr,go,250],[pr,sc,rj,mg,go]),demanda([34,rj,sc,500],[rj,sc]),demanda([35,sp,rj,1000],[sp,rj]),demanda([36,rj,sc,250],[rj,mg,go,sp,pr,sc]),demanda([37,sp,mg,250],[sp,rj,mg]),demanda([38,sc,mg,250],[sc,pr,sp,rj,mg]),demanda([39,pr,rj,250],[pr,sp,rj]),demanda([40,pr,go,250],[pr,sp,go])]

real    0m1,610s
user    0m0,019s
sys     0m0,011s
```