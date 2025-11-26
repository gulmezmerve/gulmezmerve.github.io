---
title: 
permalink: /gulmezphdinvitation/
author_profile: false
---



<div style="text-align:center; padding:20px; border-radius:10px;">
  <h1 style="color:#2c3e50; font-family:Arial, sans-serif;">
Welcome to my PhD defense
  </h1>
<h1 style="color:#2c3e50; font-family:Arial, sans-serif;">
Shining Light on Critical Gaps in Memory Safety:   <br>
From Programming Language to Hardware
</h1>


  <img
    src="/images/arenberg.jpg"
    alt="Arenberg castle"
    style="max-width:100%; border-radius:10px; margin-top:10px;"
  />
</div>



<div style="font-family: Arial, sans-serif;">
  📍 <strong>Place:</strong> 
  <a href="https://maps.app.goo.gl/hSKzHXiPrfyCQnv2A" target="_blank">
    Arenberg Castle, Leuven, Belgium
  </a> 

  <br>

  🕒 <strong>Time:</strong> 10:30-14.30 on December 10th, 2025. 

  <br>

  🎥 <a href="https://teams.microsoft.com/l/meetup-join/19:meeting_OThjN2NlMWUtNzBiMy00ZjMyLWI1NTItZDk1YzEwOTQwY2Mw@thread.v2/0?context=%7B%22Tid%22:%2292e84ceb-fbfd-47ab-be52-080c6b87953f%22,%22Oid%22:%223594cd17-5953-4511-8d53-8cfc799250e7%22,%22IsBroadcastMeeting%22:true,%22role%22:%22a%22%7D&btype=a&role=a" target="_blank">
      Live Stream
    </a>
  <br>

  🍽️ Reception 

  <p>
    Please confirm your attendance using this form if you plan to join in person  <br> 
    (if you have not yet received an online invitation and would like one)
    <a href="https://forms.gle/jJYGfXubDEvnzTeK7" target="_blank">
      https://forms.gle/jJYGfXubDEvnzTeK7
    </a>
  </p>
</div>

You can read my thesis [here](/files/author_version/gulmez_thesis_final.pdf)

<details>
  <summary style="cursor:pointer;">
    Popularized Abstract
  </summary>

  <p style="font-size: small;margin-top:10px;">
A significant challenge for the development of software that closely interacts with computer hardware is ensuring that every access to computer memory is valid, and
that all stored data in memory remains correct. Software that correctly operates on memory is called ``memory safe''. However, developers might make mistakes during programming that cause software to use memory incorrectly. For example, a program might read or write data outside the memory area that was reserved for it. Such mistakes, called ``memory-safety violations'', can cause the software application to crash or, in some cases, let hackers break into the computer system. This thesis addresses the gaps in existing state-of-the-art solutions for memory safety.

One common practice is to detect memory-safety violations after they occur, for example, with guard variables that check whether memory adjacent to the reserved area has been modified. However, detecting memory-safety violations just makes them less useful for hackers. Only detecting memory-safety violations does not
allow the application to continue its job since data might have been (accidentally or intentionally) overwritten and lost, or the wrong data
may have made its way throughout the application and corrupted its integrity. To overcome the challenge of detection-based approaches lacking resilience, this thesis proposes \textit{secure rewind and discard}, an approach that allows software to recover from memory-safety violations and continue its job without crashing. The rewind and discard approach requires
dividing the program into smaller parts, called \emph{domains}, which limit the effects of memory errors and can be discarded
without crashing the application if individual domains are corrupted.

Another approach for preventing memory safety errors is the use of memory-safe programming languages. These languages make programmers follow stricter rules
regarding how memory must be managed, manage memory on their behalf, and automatically add run-time checks to detect memory errors. This thesis examines Rust, a modern language with memory safety. However, Rust still permits developers to call into older, less safe code. We adapt secure rewind and discard to Rust, making it easier for developers to safeguard their Rust applications against errors in such older code.

Finally, memory safety can be enforced by computer hardware that validates
every memory reference against the memory area that is reserved for
that reference. This thesis extends such a hardware architecture, CHERI, which prevents many memory errors but cannot avoid \textit{uninitialized memory} issues, cases where memory content is undefined because the memory is read before being written. We extend CHERI to allow it to track which memory addresses have been written at a particular memory reference, before it allows memory to be read from there.

Through these contributions, this thesis furthers the pursuit of comprehensive memory safety solutions by shining light on previously under-represented challenges: \textit{improving software resilience and availability}, and \textit{preventing uninitialized memory access}.


  </p>
</details>



<details>
  <summary style="cursor:pointer;">
    Abstract
  </summary>

  <p style="font-size: small; margin-top:10px;">
Memory safety refers to a program’s property of ensuring that memory is accessed only
in valid and intended ways. Memory-safety guarantees can be reinforced through
programming languages with built-in safety features, such as garbage collection,
compile- and run-time checks, or through hardware-based solutions like capability
architectures. This thesis focuses on the gaps in the current state of the art: the
lack of fault tolerance of software-based mitigations for C and C++, limits of the
memory-safety properties in Rust, and initialization-time safety in hardware capability
architectures, such as CHERI.
C and C++ are still the preferred languages for system programming, embedded
systems, and various critical applications due to their performance. However, these
languages lack built-in memory-safety properties. While several well-known defense
techniques can mitigate common faults and memory safety vulnerabilities in software,
many do not address the challenge of software resilience and availability—specifically,
whether a system can continue to function and remain responsive under attack or when
subjected to malicious inputs. As a solution, we propose secure rewind and discard
of isolated domains as an efficient and secure method of improving the resilience
of software that is targeted by run-time attacks. We show the practicability of our
methodology by realizing a software library for Secure Domain Rewind and Discard
(SDRaD) and demonstrate how SDRaD can be applied to real-world software.
Rust has performance characteristics close to traditional system programming
languages such as C and C++ but, unlike these languages, Rust has memory safety
guarantees enforced by compile-time analysis. However, in order to interact with
hardware or call into non-Rust libraries, Rust provides unsafe language features that
shift responsibility for ensuring memory safety to the developer. Failing to do so
may lead to memory-safety violations in Rust code, which can violate the safety of
the entire application. To shield safe program sections from safety violations that
may happen through unsafe language features, we adapt SDRaD to protect Rust code.
To be practical, security features such as SDRaD must be easy for developers to
adopt. We design a Rust-native application programming interface for SDRaD that
leverages Rust’s powerful metaprogramming features to enable easy sandboxing of
unsafe interfaces.
Up to 10% of memory-safety vulnerabilities in languages like C and C++ stem from
uninitialized variables. Capability-based addressing, such as CHERI, mitigates many
memory defects, including spatial and temporal safety violations at an architectural
level. CHERI, however, does not handle undefined behavior from uninitialized
variables. We extend the CHERI capability model to include “conditional capabilities”,
enabling memory-access policies based on prior operations. This allows enforcement
of policies that satisfy memory-safety objectives such as “no reads to memory without
at least one prior write”.
Through these contributions, this thesis furthers the pursuit of comprehensive memory
safety solutions by shining light on previously under-represented challenges: improving
software resilience and availability and preventing uninitialized memory access.
As complementary contributions, this thesis presents an efficient and comprehensive
system call interposition mechanism, and provides compiler-assisted automated
compartmentalization for Rust. In addition, it evaluates different memory-safety-
defense techniques, such as stack canaries and shadow stacks, in terms of their
effectiveness and performance. Orthogonally to these works, it proposes an extension
to CHERI for enforcing data oblivious computation to harden software against timing
side channels. Finally, it discusses environmental sustainability considerations related
to SDRaD.

  </p>
</details>

<h3>Contributions</h3>
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
        <strong>Mon CHÉRI: Mitigating Uninitialized Memory Access with Conditional Capabilities</strong><br>
        M. Gülmez, H. Englund, J. T. Mühlberg, T. Nyman<br>In Proceedings of the 46th IEEE Symposium on Security and Privacy (S&P 2025)<br>
        DOI: <a href="https://doi.org/10.1109/SP61157.2025.00133
" target="_blank">https://doi.org/10.1109/SP61157.2025.00133</a> <br>
        Pre-print: <a href="https://arxiv.org/abs/2407.08663" target="_blank">https://arxiv.org/abs/2407.08663</a>
    </p>
</div>

<h3>Complementary Contributions</h3>
<div style="font-size: small; line-height: 1.5;">
    <p>
        <strong>System Call Interposition Without Compromise</strong><br>
        A. Jacobs, M. Gülmez, A. Andries, S. Volckaert, A. Voulimeneas<br>
        2024 54th Annual IEEE/IFIP International Conference on Dependable Systems and Networks (DSN), Brisbane, Australia, 2024, pp. 183-194.<br>
        DOI: <a href="https://doi.org/10.1109/DSN58291.2024.00030" target="_blank">https://doi.org/10.1109/DSN58291.2024.00030</a>
    </p>
<p>
    <strong>
        <span style="
            color: transparent;
            background-color: black;
            border-radius: 3px;
            padding: 0 0.3em;
        ">
            thanks! adriaan for your support!
        </span>
    </strong><br>
        J. Zhang, M. Gülmez, T. Nyman, G. Tan
        <br> (under submission)
    <br>
</p>
    <p>
        <strong>Do we still need canaries in the coal mine? Measuring shadow stack effectiveness in countering stack smashing</strong><br>
        H. Depyudt, M. Gülmez, T. Nyman, J. T. Mühlberg
        <br>
        Availability, Reliability and Security (ARES 2025). Lecture Notes in Computer Science, vol 15993. Springer, Cham.<br>
        DOI: <a href="https://doi.org/10.1007/978-3-032-00627-1_10
" target="_blank">https://doi.org/10.1007/978-3-032-00627-1_10</a><br>
        Pre-print: <a href="https://www.arxiv.org/abs/2412.16343" target="_blank">https://www.arxiv.org/abs/2412.16343</a>
    </p>
    <p>
        <strong>BLACKOUT: Data-Oblivious Computation with Blinded Capabilities</strong><br>
        H. ElAtali, M. Gülmez, T. Nyman, N. Asokan <br>
        32nd ACM Conference on Computer and Communications Security (CCS ’25)<br>
        Pre-print: <a href="https://arxiv.org/pdf/2504.14654" target="_blank">https://arxiv.org/pdf/2504.14654</a>
    </p>
    <p>
        <strong>Exploring the Environmental Benefits of In-Process Isolation for Software Resilience</strong><br>
        M. Gülmez, T. Nyman, C. Baumann, J. T. Mühlberg<br>
        In Proceedings of 53rd Annual IEEE/IFIP International Conference on Dependable Systems and Networks – Supplemental Volume (DSN-S 2023).<br>
        DOI: <a href="http://doi.org/10.1109/DSN-S58398.2023.00056" target="_blank">http://doi.org/10.1109/DSN-S58398.2023.00056</a><br>
        Pre-print: <a href="https://arxiv.org/abs/2306.02131" target="_blank">https://arxiv.org/abs/2306.02131</a>
    </p>
</div>