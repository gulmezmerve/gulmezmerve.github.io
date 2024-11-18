---
title: "Shining Light on Gaps in Run-time Defenses: 
From Programming Language to Hardware Design"
permalink: /dissertation/
author_profile: false
---
This page contains the upcoming doctoral thesis and the related publications. 
### Abstract 

Modern computers are rooted in the Von Neumann architecture, which introduced a design for stored-program computers where programmable memory holds *both program code*---instructions the computer executes---*and data*---the information the program processes. While this design revolutionized computing, it also created the need to separate code from various types of data to prevent unauthorized memory access.
Historically, the risks of improper memory access were first formally acknowledged in 1972 through studies commissioned by the US military.
The destructive potential of memory-related bugs for networked computers became clear after the 1988 Morris Worm incident, which exploited a buffer overflow to spread from one computer to another via the early Internet, ultimately causing widespread denial-of-service attacks affecting roughly 10% of all connected computers.

These risks remain as critical today as memory-related vulnerabilities continue to be exploited in cyberattacks. Google Project Zero's "0day In the Wild" dataset reveals that over 70% of zero-day vulnerabilities discovered between July 2014 and June 2022 were attributed to memory-safety issues. At the same time, the potential consequences of a Morris Worm-scale incident are much higher. The 2024 Crowdstrike incident disabled roughly 1% of Windows computers caused billions of US dollars worth of damages in disruptions in various sectors critical for society. The incident was caused by an accidentally introduced memory error in a Windows operating system driver while leading international cybersecurity organizations are advocating for the need to adopt memory-safety principles across the software industry. 

Memory-safety guarantees can be reinforced through programming languages with built-in safety features, such as garbage collection or compile-time and run-time checks, or through hardware-based solutions like fine-grained capability architectures.
This thesis focuses on the gaps in the current state of the art: the lack of fault tolerance of software-based mitigations for C and C++,
limits of the memory-safety properties in Rust, and initialization-time safety in hardware capability architectures, such as CHERI.

C and C++ are still the preferred languages for system programming, embedded systems, and various critical applications due to their performance. However, these languages lack built-in memory-safety properties.
While several well-known defense techniques can mitigate common faults and memory safety vulnerabilities in software, many do not address the challenge of software resilience and availability—specifically, whether a system can continue to function and remain responsive under attack or when subjected to malicious inputs. As a solution, we propose *secure rewind and discard of isolated domains* as an efficient and secure method of improving the resilience of software that is targeted by run-time attacks. 
We show the practicability of our methodology by realizing a software library for Secure Domain Rewind and Discard (SDRaD) and demonstrate how SDRaD can be applied to real-world software. 

Rust has performance characteristics close to traditional system programming languages such as C and C++ but, unlike these languages, Rust has memory safety guarantees enforced by compile-time analysis. However, in order to interact with hardware or call into non-Rust libraries, Rust provides *unsafe* language features that shift responsibility for ensuring memory safety to the
developer. Failing to do so may lead to memory-safety violations in Rust code, which can violate the safety of the entire application. To shield safe program sections from safety violations that may happen in through unsafe language features, we adapt SDRaD to protect Rust code. To be practical, security features such as SDRaD must be easy for developers to adopt. We design a Rust-native application programming interface for SDRaD that leverages Rust's powerful metaprogramming features to enable easy sandboxing of unsafe interfaces.

Up to 10% of memory-safety vulnerabilities in languages like C and C++ stem from uninitialized variables. Capability-based addressing, such as the University of Cambridge's CHERI, mitigates many memory defects, including spatial and temporal safety violations at an architectural level. CHERI, however, does not handle undefined behavior from uninitialized variables. We extend the CHERI capability model to include "*conditional capabilities*", enabling memory-access policies based on prior operations. This allows enforcement of policies that satisfy memory-safety objectives such as "*no reads to memory without at least one prior write*".

Through these contributions, this thesis furthers the pursuit of comprehensive memory safety solutions by shining light on previously under-represented challenges: improving software resilience and availability and preventing uninitialized memory access.

<h3>Publications</h3>
<div style="font-size: small; line-height: 1.5;">
    <p>
        <strong>Rewind & Discard: Improving Software Resilience Using Isolated Domains</strong><br>
        M. Gülmez, T. Nyman, C. Baumann, J. T. Mühlberg<br>
        In Proceedings of 53rd Annual IEEE/IFIP International Conference on Dependable Systems and Networks (DSN 2023).<br>
        DOI: <a href="http://doi.org/10.1109/DSN58367.2023.00046" target="_blank">http://doi.org/10.1109/DSN58367.2023.00046</a>
    </p>
    <p>
        <strong>Friend or Foe Inside? Exploring In-Process Isolation to Maintain Memory Safety for Unsafe Rust</strong><br>
        M. Gülmez, T. Nyman, C. Baumann, J. T. Mühlberg<br>
        In Proceedings of IEEE Secure Development Conference 2023 (SecDev 2023).<br>
        DOI: <a href="https://doi.org/10.1109/SecDev56634.2023.00020" target="_blank">https://doi.org/10.1109/SecDev56634.2023.00020</a><br>
        Pre-print: <a href="https://arxiv.org/abs/2306.08127" target="_blank">https://arxiv.org/abs/2306.08127</a>
    </p>
    <p>
        <strong>Mon CHÈRI ♡ Adapting Capability Hardware Enhanced RISC with Conditional Capabilities</strong><br>
        M. Gülmez, H. Englund, J. T. Mühlberg, T. Nyman<br>
        (under submission).<br>
        Pre-print: <a href="https://arxiv.org/abs/2407.08663" target="_blank">https://arxiv.org/abs/2407.08663</a>
    </p>
</div>

<h3>Other Publications</h3>
<div style="font-size: small; line-height: 1.5;">
    <p>
        <strong>SandCell: Lightweight and Flexible Sandboxing in Rust</strong><br>
        J. Zhang, M. Gülmez, T. Nyman, G. Tan <br>
        (under submission)<br>
    </p>
    <p>
        <strong>System Call Interposition Without Compromise</strong><br>
        A. Jacobs, M. Gülmez, A. Andries, S. Volckaert, A. Voulimeneas<br>
        2024 54th Annual IEEE/IFIP International Conference on Dependable Systems and Networks (DSN), Brisbane, Australia, 2024, pp. 183-194.<br>
        DOI: <a href="https://doi.org/10.1109/DSN58291.2024.00030" target="_blank">https://doi.org/10.1109/DSN58291.2024.00030</a>
    </p>
    <p>
        <strong>Exploring the Environmental Benefits of In-Process Isolation for Software Resilience</strong><br>
        M. Gülmez, T. Nyman, C. Baumann, J. T. Mühlberg<br>
        In Proceedings of 53rd Annual IEEE/IFIP International Conference on Dependable Systems and Networks – Supplemental Volume (DSN-S 2023).<br>
        DOI: <a href="http://doi.org/10.1109/DSN-S58398.2023.00056" target="_blank">http://doi.org/10.1109/DSN-S58398.2023.00056</a><br>
        Pre-print: <a href="https://arxiv.org/abs/2306.02131" target="_blank">https://arxiv.org/abs/2306.02131</a>
    </p>
</div>