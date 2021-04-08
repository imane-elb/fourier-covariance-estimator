# Financial Data Analysis via Non Uniform Fourier Transform
## Authors 
* Imane El Bouzid : imane.elbouzid@student-cs.fr
* Richard John Lin : richardjohn.lin@student-cs.fr
## Malliavin Mancino Covariance Estimator
The Malliavin Mancino estimator is a non parametric covariance and volatility estimator that does not rely on the assumption of asset data synchronacy. The main idea behind it is to estimate the covariance matrix's Fourier coefficients by using the asset log-prices' Fourier coefficients thanks to the Bohr convolution formula. Indeed, if we denote by $dp_{i}$ the asset $S_{i}$'s log-price and $\mathscr{F}(f)(k)$ the Fourier coeffecient of order $k$ of the function $f$ :
\begin{equation*}
    \frac{1}{2 \pi} \mathscr{F}\left(\Sigma^{i, j}\right)=\mathscr{F}\left(d p^{i}\right) * \mathscr{F}\left(d p^{j}\right),
\end{equation*}
where : 
\begin{equation*}
    \left(\mathscr{F}\left(d p^{i}\right) * \mathscr{F}\left(d p^{j}\right)\right)(k):=\lim _{N \rightarrow \infty} \frac{1}{2 N+1} \sum_{|s| \leq N} \mathscr{F}\left(d p_{i}\right)(s) \mathscr{F}\left(d p_{j}\right)(k-s)
\end{equation*}
The initial complexity of the Malliavin Mancino estimator as provided in [A Fourier transform for Non Parametric Estimation of Multivariate Volatility](https://projecteuclid.org/journals/annals-of-statistics/volume-37/issue-4/A-Fourier-transform-method-for-nonparametric-estimation-of-multivariate-volatility/10.1214/08-AOS633.f) is $O(N^{2})$. This project's aim is to implement more efficient computation algorithms using the Non Uniform Fourier Transform and to benchmark the coded algorithms regarding their speed and accuracy.
