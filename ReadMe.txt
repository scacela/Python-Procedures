ReadMe
------------------------------------------------------------------------
Sam Cacela
Villanova University
------------------------------------------------------------------------

These two projects required the construction of various functions written
in Python. Each function performs its own operation on the argument(s) it
passes. Arguments are either lists (vectors), or matrices (vectors of vectors).

------------------------------------------------------------------------


Python Procedures I.



vadd(v, w)		returns the sum of vectors v and w.

cmult(c, v)		returns the scalar multiple of vector v by scalar
			(field element) c.

vzero(n)		returns the zero vector of n elements.

vneg(v)			returns the additive inverse of vector v.

dot(v, w)		returns the dot product of vectors v and w.

sbasis(j, n)		returns the n-vector with a 1 in the nth position
			and 0 elsewhere.

vsum(vlist)		returns the sum of a list of vectors.

lincomb(clist, vlist)	returns the linear combination of vectors in vlist
			using the coefficients in clist.

madd(A, B)		returns the sum of matrices A and B.

cmmult(c, A)		returns the scalar multiple of matrix A by scalar
			(field element) c.

mzero(m, n)		returns the zero m * n matrix

mneg(A)			returns the additive inverse of matrix A.

ID(n)			returns the n * n identity matrix.

shape(A)		returns the 2-list giving the number of rows and
			columns of A in that order.

transpose(A)		returns the reflection of matrix A, where the rows
			become columns and the columns become rows.

mvmult(A, v)		returns the vector obtained by multiplying v by
			matrix A.

mmult(A, B)		returns the product of compatible matrices A and B.

acompatible(A, B)	returns true if matrices A and B have the same
			shape (so that they can be added), returns false
			otherwise.

mcompatible(A, B)	returns true if matrices A and B have compatible
			shapes (so that they can be multiplied as AB),
			returns false otherwise.

mtov(A)			returns the vector representation of matrix A
			(returns a list of numbers).

swap(j, k, A)		returns a new matrix after exchanging the jth 
			and kth rows of matrix A.

addrow(c, j, k, A)	returns a new matrix after adding c times the jth
			row of matrix A to the kth row of A and writing
			the result in the kth row of A

augment(A, B)		returns a new matrix after concatenating each row
			of matrix B to the corresponding row of matrix A.
			A and B must have the same number of rows, but may
			have a different number of columns.

------------------------------------------------------------------------


Python Procedures II.



isvectorset(x)		returns true if x is a list of vectors of the same
			length, so that represents a set of vectors in Rn
			for some value n, returns false otherwise.

ismatrix(x)		is a renaming of isvectorset(x) so that the procedure
			can be used in the context of matrices rather than
			that of sets of vectors.

determinant(A)		returns the determinant of matrix A (returns a single
			number).

issquare(A)		returns true if matrix A is square, returns false
			otherwise.

islinind(x)		returns true if x is a list of linearly independent
			vectors, and returns false if the vectors are linearly
			dependent. Produces an error message if the argument
			is not of the proper format.

isextra(i, x)		returns true if the ith vector in the list of vectors
			x is extra in the sense that:
	
			Span(x) = Span(x-{xi})

			returns false if the spans are different. Produces a
			descriptive error message if the argument is not of
			the proper format.

coordinates(x, B)	returns the coordinates of the vector x with respect
			to the basis B.

isUT(M)			returns true if M is a square matrix that is upper
			triangular, and returns false if M is not upper
			triangular. Produces a descriptive error message if
			the argument is not of the proper format.

check_for_zeros(M,i,j)	checks matrix M to see if only zeros exist at or below
			row i in column j, returns a list giving the count of
			nonzero entries and the index of the first nonzero
			value, in that order.

swap(j, k, A)		(see Python Procedures I)

make_ident(rows, cols)	returns the identity matrix with dimensions rows * cols.

invertUT(M)		returns the inverse of the upper triangular matrix M,
			assuming M is invertible.

null(A)			returns a basis for the null space of matrix A.

span(S)			returns a basis for the span of the set of vectors S.
			Produces a descriptive error message if the argument
			is not of the proper format.

backsub(A, b)		returns the solution to the equation Ax = b, assuming
			A is in upper triangular form, is square, and is
			non-singular (has a nonzero determinant).
