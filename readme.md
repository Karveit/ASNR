# Auto StrongName Remover/Resigner
>*这个StrongName Removing呢，我们就有几年用StrongNameRemove，旁边一个StrongName Killer。最痛苦的，就是相关程序集甚至是BAML把这个强签名的引用到里面，去签名的时候一下子就……然后就是用刀片刮也不行了，这个就是签名是最痛苦的，而且这个效率efficiency……*

A simple tool to remove/resign assemblies' strong name (public key & public key token) automatically. 

It not only removes the strong name information in the target assembly (`AssemblyDef`), but also tracks and removes tokens for all relevant assemblies (`AssemblyRef`), BAMLs (`AssemblyInfo`), and CustomAttributes (Currently support `InternalsVisibleToAttribute`). By this way, the target StrongName is completely  removed from all assemblies (maybe). Mixed assemblies are supported (thanks to dnlib).

Usage:

	asnr.exe <filename(main assembly)> [/r <.snk file path>]

ASNR uses [**dnlib**](https://github.com/0xd4d/dnlib) (by 0xd4d , LICENSE: MIT) and [**ConfuserEx**](https://github.com/yck1509/ConfuserEx) (by yck1509 , LICENSE: MIT)


---

by Ulysses , wdwxy12345@gmail.com


