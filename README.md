## Exploiting Uses of Uninitialized Stack Variables in Linux Kernels to Leak Kernel Pointers

Information leaks are the most prevalent type of vulnerabilities among all known vulnerabilities in Linux kernel.
Many of them are caused by the use of uninitialized variables or data structures.
It is generally believed that the majority of information leaks in Linux kernel are low-risk and do not have severe impact due to the difficulty (or even the impossibility) of exploitation.
As a result, developers and security analysts do not pay enough attention to mitigating these vulnerabilities.
Because of this, these vulnerabilities are usually assigned low CVSS scores or without any CVEs assigned.
Moreover, many patches that address uninitialized data use bugs in Linux kernel are not accepted, leaving billions of Linux systems vulnerable.

Nonetheless, information leak vulnerabilities in Linux kernel are not as low-risk as people believe.
In this paper, we present a generic approach that converts stack-based information leaks in Linux kernel into kernel pointer leak vulnerabilities, which can be used to defeat modern security defenses such as KASLR.
Taking an exploit that triggers an information leak in Linux kernel, our approach automatically converts it into a highly impactful exploit that leaks pointers to either kernel functions or the kernel stack.
We evaluate our approach on four known CVEs and one security patch in Linux kernel and demonstrate its effectiveness.
Our findings provide solid evidence for Linux kernel developers and security analysts to treat information leaks in Linux kernel more seriously.

Paper: [[PDF]](https://haehyun.github.io/papers/leak-kptr-woot20.pdf)

``` tex
@inproceedings{cho2020exploiting,
	title        = {{Exploiting Uses of Uninitialized Stack Variables in Linux Kernels to Leak Kernel Pointers}},
	author       = {Cho, Haehyun and Park, Jinbum and Kang, Joonwon and Bao, Tiffany and Wang, Ruoyu and Shoshitaishvili, Yan and Doup{\'e}, Adam and Ahn, Gail-Joon},
	booktitle    = {In Proceedings of the 14th USENIX Workshop on Offensive Technologies (WOOT)},
	month        = Aug,
	year         = 2020,
	address      = {Online},
}
```

For detail information on our tool, please refer the [[README]](https://github.com/sefcom/leak-kptr/blob/master/tool/README.md) file in the tool directory.
