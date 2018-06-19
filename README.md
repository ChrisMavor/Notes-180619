# Notes-180619
Notes for vector and matrix cheinging for size and type
def MatrixSizeCheck(a,b):
  if type(a)==type(b):
    if type(a[0])==type(b[0]):
      if len(a[0]) == len(b):
        return True
      else:
        return False
    else:
      return "Incorrect sizing. Make use both are lists not integers."
  else:
    return "Incorrect sizing. Make use both are lists not integers."


testa = [[1],[2]]
testb=[[2]]
print(MatrixSizeCheck(testa,testb))

def VectorCheckMult(v,w):
  if type(v)==list and type(w)==list:
    if len(v)!=len(w):
      return "Incorrect sizing. Make sure both inputs are a single list of the same length. Make sure inputs are not integers, matrices(list of lists), or strings."
    elif type(v[0])==int and type(v[0])==int:
      row=0
      for i in range(len(v)):
        row+=v[i]*w[i]
      return row  
    else:
      return  "Incorrect sizing. Make sure both inputs are a single list of the same length. Make sure inputs are not integers, matrices(list of lists), or strings."
  else:
    return  "Incorrect sizing. Make sure both inputs are a single list of the same length. Make sure inputs are not integers, matrices(list of lists), or strings."

testv = [1,2]
testw = 'a'
print(VectorCheckMult(testv,testw))
