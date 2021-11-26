%meteuler.m
fprintf('Método de Euler para resolver ecuaciones diferenciales\n')
f=input('Ingrese la ecuación diferencial de la forma: dy/dx=f(x,y): ','s');
x0=input('Ingrese el primer punto x0:');
x1=input('Ingrese el segundo punto x1:');
y0=input('Ingrese la condición inicial y(x0):');
n=input('Ingrese el número de pasos n:');
h=(x1-x0)/n;
xs=x0:h:x1;
y1=y0;
fprintf('\n''it x0 x1 y1');
for i=1:n
   it=i-1;
   x0=xs(i);
   x=x0;
   x1=xs(i+1);
   y=y0;
   y1=y0+h*eval(f);
  
   fprintf('\n%2.0f%10.6f%10.6f%10.6f\n',it,x0,x1,y1);
   y0=y1;
end
fprintf('\n El punto aproximado y(x1) es = %10.6f\n',y1);
