# 随机薛定谔方程 
## subsection约化密度矩阵的重构
对环境部分，采用相干态表象，满足完备性关系
$$
\begin{equation}
    \int d^2\alpha e^{-|\alpha|^2}\ket{\alpha}\bra{\alpha}=I
\end{equation}
$$

对于系统与环境的初态，满足
$$
\begin{equation}
    \begin{aligned}
        \ket{\Phi_{tot}(t)}&\\
        &=\int d^2\alpha\ket{\alpha}\bra{\alpha}\ket{\phi_{tot}(t)}
        \\
        &=\int d^2\alpha e^{-|\alpha|^2}\ket{\varphi_{a^*}(t)}\otimes\ket{\alpha}
    \end{aligned}
\end{equation}
$$

构造约化密度矩阵
$$
\begin{equation}\begin{aligned}
    \hat{\rho}_{sys}(t)&=\int d^2\alpha e^{-|\alpha|^2}\ket{\varphi_{a^*}(t)}\otimes\ket{\alpha}\int d^2\alpha e^{-|\alpha|^2}\bra{\alpha}\otimes\bra{\varphi_{a^*}}
    \\&=\int d^2\alpha e^{-|\alpha|^2}\ket{\varphi_{a^*}(t)}\bra{\varphi_{a^*}(t)}\otimes\int d^2 \alpha\ket{\alpha}\bra{\alpha}
    \\&=\int d^2\alpha e^{-|\alpha|^2}\ket{\varphi_{a^*}(t)}\bra{\varphi_{a^*}(t)}
    \\&=M_z[\ket{\varphi_{a^*}(t)}\bra{\varphi_{a^*}(t)}]\end{aligned}
\end{equation}
$$

对于$\int d^2\alpha e^{-|\alpha|^2}$的计算，可假设$\alpha$满足高斯分布，由积分运算换为求和运算。
## 系统波函数的演化方程
对波函数进行表象变换$\ket{\phi}=e^{i\omega a^{\dagger}at}\ket{\Phi_{tot}(t)}$
$$
\begin{equation}
\begin{aligned}
    \frac{d\ket{\phi}}{dt}&=\frac{de^{i\omega a^{\dagger}at}}{dt}\ket{\Phi_{tot}(t)}+e^{i\omega a^{\dagger}at}\frac{d\ket{\Phi_{tot}(t)}}{dt}
    \\&=\omega a^{\dagger}a\ket{\Phi_{tot}(t)}+e^{i\omega a^{\dagger}at}\frac{H_{sys}+V+H_{env}}{i\hbar}\ket{\Phi_{tot}(t)}
    \\&=[\omega a^{\dagger}a-\omega a^{\dagger}a+-\frac{i}{\hbar}e^{i\omega a^{\dagger}at}(H_{sys}+V)]\ket{\Phi_{tot}(t)}
    \\&=[-\frac{i}{\hbar}e^{i\omega a^{\dagger}at}(H_{sys}+V)]e^{-i\omega a^{\dagger}at}e^{i\omega a^{\dagger}at}\ket{\Phi_{tot}(t)}
    \\&=-\frac{i}{\hbar}(H_{sys}-e^{i\omega a^{\dagger}at}Ve^{-i\omega a^{\dagger}at})\ket{\phi}
\end{aligned}
\end{equation}
$$

对于相干态 $\ket{\alpha(t)}=e^{-i\omega_ia^{\dagger}_ia_it}\ket{\alpha_0}$，满足如下方程
$$
\begin{equation}
\begin{aligned}
    \frac{d}{dt}e^{i\omega a^{\dagger}at}&\int d^2\alpha\ket{\varphi_{a^*}(t)}\otimes\ket{\alpha(t)}
    \\
    &=\frac{d}{dt}de^{i\omega a^{\dagger}at}\int d^2\alpha\ket{\varphi_{a^*}(t)}\otimes e^{-i\omega_ia^{\dagger}_ia_it}\ket{\alpha_0}
    \\
    &=\frac{d\int d^2\alpha\ket{\varphi_{a^*}(t)}\otimes \ket{\alpha_0}}{dt}
\end{aligned}
\end{equation}
$$

整理得到
$$
\begin{equation}
    \begin{aligned}
        \frac{d}{dt}&\int d^2\alpha\ket{\varphi_{a^*}}\otimes \ket{\alpha_0}
        \\
        &=-\frac{i}{\hbar}(H_{sys}-e^{i\omega a^{\dagger}at}Ve^{-i\omega a^{\dagger}at})\int d^2\alpha\ket{\varphi_{a^*}}\otimes \ket{\alpha_0}
    \end{aligned}
\end{equation}
$$

对系统波函数部分
$$
\begin{equation}
    \frac{d}{dt}\ket{\varphi_{a^*}(t)}=-\frac{i}{\hbar}(H_{sys}-e^{i\omega a^{\dagger}at}Ve^{-i\omega a^{\dagger}at})\ket{\varphi_{a^*}(t)}
\end{equation}
$$

假设相互作用具有$V=(a^\dagger+a)$，则
$$
\begin{equation}
    \begin{aligned}
        \frac{d}{dt}\ket{\varphi_{a^*}(t)}&=-\frac{i}{\hbar}(H_{sys}+e^{i\omega a^{\dagger}at}Ve^{-i\omega a^{\dagger}at})\ket{\varphi_{a^*}(t)}\\&=-\frac{i}{\hbar}H_{sys}+\frac{iq}{\hbar}\sum\limits_i\chi_i(e^{i\omega t}a^{\dagger}+e^{-i\omega t}a)\ket{\varphi_{a^*}(t)}
\label{NMSDM0}
    \end{aligned}
\end{equation}
$$

在相干态表象下运用下列关系
$$
\begin{equation}
    a^{\dagger}\rightarrow a^{*},a\rightarrow \frac{\partial}{\partial \alpha^*}
\end{equation}
$$

式$\ref{NMSDM0}$进一步化简为
$$
\begin{equation}
    \begin{aligned}
        \frac{d}{dt}\ket{\varphi_{a^*}(t)}=-\frac{i}{\hbar}H_{sys}+\frac{iq}{\hbar}\sum\limits_i\chi_i(e^{i\omega_i t}a^{*}+e^{-i\omega_i t}\frac{\partial}{\partial a^*})\ket{\varphi_{a^*}(t)}
    \end{aligned}
\end{equation}
$$

定义随机过程
$$
\begin{equation}
    \begin{aligned}
        Z_a(t)=\sum\limits_i\chi_ia^*e^{i\omega t}
    \end{aligned}
\end{equation}
$$

通过链式规则
$$
\begin{equation}
    \begin{aligned}
        \sum\limits_{i}\chi _ie^{-i\omega_it}\frac{\partial}{\partial a_{i}^*} &=\int ds\sum\limits_{i}\chi _ie^{-i\omega_it}\frac{\delta}{\delta Z_a(s)}\frac{\delta Z_a(s)}{\delta a_i^*}
        \\&=\int ds\sum\limits_{i}\chi _ie^{-i\omega_it}\chi_ie^{-i\omega_is}\frac{\delta}{\delta Z_a(s)}
        \\&=\int ds\sum\limits_{i}\chi_i^2e^{-i\omega_i(t-s)}\frac{\delta}{\delta Z_a(s)}
    \end{aligned}
\end{equation}
$$

方程进一步化简为
$$
\begin{equation}
    \begin{aligned}
        \frac{d}{dt}&\ket{\varphi_{a^*}(t)}=\\
        &[-\frac{i}{\hbar}H_{sys}+\frac{iq}{\hbar}Z_a(t)+\frac{i}{\hbar}q^{\dagger}\int ds\sum\limits_{i}\chi_i^2e^{-i\omega_i(t-s)}\frac{\delta}{\delta Z_a(s)}]\ket{\varphi_{a^*}(t)}
    \end{aligned}
\end{equation}
$$
