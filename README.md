## Lexical-Scoping
makeCacheMatrix<-function(x=matrix()){
j<-NULL
set<-function(y)
x<<-y
j<<-NULL
}
get<-function()x
setInverse<-function(inverse)j<<-inverse
getInverse<-function()j
list(set=set,get=get,
setInverse=setInverse,
getInverse=getInverse)
}

cacheSolve<-functions(x,...)
##Return a matrix that is the inverse of 'x'
j<-x$getInverse()
if(!is.null(j)){
message("getting cached data")
return(j)
