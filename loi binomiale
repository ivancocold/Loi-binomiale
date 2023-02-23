#Nombre d'essais. Cette variable doit être un entier supérieur ou égal à 1
n=10


#Probabilité de succès. Cette variable doit être comprise entre 0 et 1.
p=1/4


#Fonction de combinaisons de k dans n
def comb(n, k):
    if k > n//2:
        k = n-k
    x = 1
    y = 1
    i = n-k+1
    while i <= n:
        x = (x*i)//y
        y += 1
        i += 1
    return x


#Fonction de calcul d'avoir exactement a succès
def exact(a):
  r=(comb(n,a)*(p**a)*((1-p)**(n-a)))
  return r


#Fonction de calcul de la probabilité d'avoir au moins a succès
def aumoins(a):
  r=0
  i=a
  while i<=n:
    r=r+exact(i)
    i=i+1
  return r


#Fonction de calcul de la probabilité d'avoir plus de a succès
def plus(a):
  r=0
  i=a+1
  while i<=n:
    r=r+exact(i)
    i=i+1
  return r


#Fonction de calcul de la probabilité d'avoir au plus a succès
def auplus(a):
  r=0
  i=0
  while i<=a:
    r=r+exact(i)
    i=i+1
  return r


#Fonction de calcul de la probabilité d'avoir moins de a succès
def moins(a):
  r=0
  i=0
  while i<a:
    r=r+exact(i)
    i=i+1
  return r


#Fonction de calcul de l'espérence
def esp():
  return n*p


#Fonction de calcul de la variance
def var():
  return n*p*(1-p)

