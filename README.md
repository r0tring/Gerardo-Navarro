# Nelg
Week 3 Peer Graded Assignement
makeCacheMatrix <- function(v = matrix(sample(1:200,30),15,15)) {
  Z <- NULL
  set <- function(y) {
    v <<- y
    Z <<- NULL
  }
  get <- function() v
  setsolve <- function(solve) Z <<- solve
  getsolve <- function() Z
  list(set = set, get = get,
       setsolve = setsolve,
       getsolve = getsolve)
}

cacheSolve <- function(v, ...) {
  Z <- x$getsolve()
  if(!is.null(s)) {
    message("getting inversed matrix")
    return(s)
  }
  data <- x$get()
  Z <- solve(data, ...)
  v$setsolve(s)
  Z
