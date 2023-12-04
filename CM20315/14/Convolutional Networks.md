We use the operation of [convolution](https://en.wikipedia.org/wiki/Convolution), usually represented by the $\ast$ symbol.

This is essentially the sum of element-wise multiplication of some parameters known as a *kernel* which has a few properties:
* *Kernel size* $(n\times m)$ - how many parameters this kernel has - this is not necessarily the size of the matrix. This is usually, but not mandatory, square or 'even' on all axes.
	Example: $[\omega_1, \omega_2, \omega_3]$ 
* *Dilation* - this intersperses your kernel with zeroes. Dilation $1$ adds $1$ zero between each weight, and so on.
	Example: $[\omega_1, 0, \omega_2, 0, \omega_3]$ 

More things:
- *Stride* - shift the kernel by $n$ positions each input:
	Example stride=$1$:
	$$\begin{array}{cccc}
		&\omega_1 &\omega_2 &\omega_3\\
		&\downarrow &{\color{red} \downarrow} &\downarrow\\
		[&h_1 &h_2 &h_3 &h_4 &h_5]
	\end{array}$$
$$\begin{array}{cccc}
		&&\omega_1 &\omega_2 &\omega_3\\
		&&\downarrow &{\color{red} \downarrow} &\downarrow\\
		[&h_1 &h_2 &h_3 &h_4 &h_5]
	\end{array}$$
$$\begin{array}{cccc}
		&&&\omega_1 &\omega_2 &\omega_3\\
		&&&\downarrow &{\color{red} \downarrow} &\downarrow\\
		[&h_1 &h_2 &h_3 &h_4 &h_5]
	\end{array}$$
	Example stride=$2$:
	$$\begin{array}{cccc}
		&\omega_1 &\omega_2 &\omega_3\\
		&\downarrow &{\color{red} \downarrow} &\downarrow\\
		[&h_1 &h_2 &h_3 &h_4 &h_5]
	\end{array}$$
	$$\begin{array}{cccc}
		&&&\omega_1 &\omega_2 &\omega_3\\
		&&&\downarrow &{\color{red}\downarrow} &\downarrow\\
		[&h_1 &h_2 &h_3 &h_4 &h_5]
	\end{array}$$
- *Zero padding*:
	This is a policy on edge values: it allows us to keep the same input-output size by padding the outer edges with zeroes.
- *Valid convolutions*
	 This is the opposite to zero padding: it makes the output smaller such that we only use values from our input. 
	