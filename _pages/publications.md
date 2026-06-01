---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
You can also find my articles on <u><a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

---

## Security & Systems

### 2025

**[Shining Light on Critical Gaps in Memory-Safety: From Programming Language to Hardware](/files/author_version/gulmez_thesis_final.pdf)**  
**Merve Gülmez**  
*PhD Thesis, KU Leuven, Belgium, 2025*  
[[PDF]](/files/author_version/gulmez_thesis_final.pdf)

<details>
<summary>BibTeX</summary>
<pre>
@phdthesis{gulmez2025phd,
  title = {Shining Light on Critical Gaps in Memory-Safety: From Programming Language to Hardware},
  author = {G{\"u}lmez, Merve and Joosen, Wouter and M{\"u}hlberg, Jan Tobias and Baumann, Christoph},
  school = {KU Leuven},
  address = {Leuven, Belgium},
  year = {2025},
  url = {https://lirias.kuleuven.be/4274569&lang=en}
}
</pre>
</details>

---

**[BLACKOUT: Data-Oblivious Computation with Blinded Capabilities](https://arxiv.org/abs/2504.14654)**  
Hossam ElAtali, **Merve Gülmez**, Thomas Nyman, N. Asokan  
*ACM SIGSAC Conference on Computer and Communications Security (CCS '25), Taipei, Taiwan, 2025*  
[[PDF]](/files/author_version/2025_blackout.pdf) &nbsp; [[arXiv]](https://arxiv.org/abs/2504.14654) &nbsp; [[Talk]](https://www.youtube.com/watch?v=YcWzuwbvdic) &nbsp; [[Artifact]](https://github.com/blindedcapabilities)

<details>
<summary>BibTeX</summary>
<pre>
@inproceedings{ElAtali25a,
  author    = {ElAtali, Hossam and Gülmez, Merve and Nyman, Thomas and Asokan, N.},
  title     = {BLACKOUT: Data-Oblivious Computation with Blinded Capabilities},
  booktitle = {Proceedings of the 2025 ACM SIGSAC Conference on Computer and
               Communications Security},
  series    = {CCS '25},
  year      = {2025},
  pages     = {2039--2053},
  location  = {Taipei, Taiwan},
  isbn      = {9798400715259},
  doi       = {10.1145/3719027.3765169},
  url       = {https://doi.org/10.1145/3719027.3765169},
  publisher = {Association for Computing Machinery},
  address   = {New York, NY, USA}
}
</pre>
</details>

---

**[Mon CHÉRI: Mitigating Uninitialized Memory Access with Conditional Capabilities](https://arxiv.org/abs/2407.08663)**  
**Merve Gülmez**, Håkan Englund, Jan Tobias Mühlberg, Thomas Nyman  
*46th IEEE Symposium on Security and Privacy (S&P '25), San Francisco, CA, 2025*  
[[PDF]](/files/author_version/2025_mon_cheri_author_version.pdf) &nbsp; [[arXiv]](https://arxiv.org/abs/2407.08663) &nbsp; [[GitHub]](https://github.com/ConditionalCapabilities) &nbsp; [[Poster]](/files/poster/mon_cheri_poster_SP2025.pdf) &nbsp; [[Slides]](/files/presentation/Gulmez_moncheri_SP.pptx)

<details>
<summary>BibTeX</summary>
<pre>
@inproceedings{Gulmez25a,
  author    = {Gülmez, Merve and Englund, Håkan and Mühlberg, Jan Tobias and Nyman, Thomas},
  title     = {Mon CHÉRI: Mitigating Uninitialized Memory Access with Conditional Capabilities},
  booktitle = {46th IEEE Symposium on Security and Privacy (S\&P 2025)},
  year      = {2025},
  pages     = {829--847},
  month     = may,
  issn      = {2375-1207},
  doi       = {10.1109/SP61157.2025.00133},
  url       = {https://doi.ieeecomputersociety.org/10.1109/SP61157.2025.00133},
  publisher = {IEEE Computer Society},
  address   = {Los Alamitos, CA, USA}
}
</pre>
</details>

---

**[Do We Still Need Canaries in the Coal Mine? Measuring Shadow Stack Effectiveness in Countering Stack Smashing](https://arxiv.org/pdf/2412.16343)**  
Hugo Depuydt, **Merve Gülmez**, Thomas Nyman, Jan Tobias Mühlberg  
*International Conference on Availability, Reliability and Security (ARES '25), 2025*  
[[PDF]](/files/author_version/2025_ares-coalmine.pdf) &nbsp; [[arXiv]](https://arxiv.org/pdf/2412.16343)

<details>
<summary>BibTeX</summary>
<pre>
@inproceedings{Depyudt25,
  author    = {Depuydt, Hugo and Gülmez, Merve and Nyman, Thomas and Mühlberg, Jan Tobias},
  title     = {Do We Still Need Canaries in the Coal Mine?
               Measuring Shadow Stack Effectiveness in Countering Stack Smashing},
  booktitle = {Availability, Reliability and Security},
  year      = {2025},
  pages     = {193--205},
  isbn      = {978-3-032-00627-1},
  doi       = {10.1007/978-3-032-00627-1_10},
  url       = {https://doi.org/10.1007/978-3-032-00627-1_10},
  publisher = {Springer Nature Switzerland},
  address   = {Cham}
}
</pre>
</details>

---

### 2024

**[System Call Interposition Without Compromise](https://gulmezmerve.github.io/files/2024-lazypoline.pdf)**  
Adriaan Jacobs, **Merve Gülmez**, Alicia Andries, Stijn Volckaert, Alexios Voulimeneas  
*54th Annual IEEE/IFIP International Conference on Dependable Systems and Networks (DSN '24), 2024*  
[[PDF]](/files/2024-lazypoline.pdf) &nbsp; [[GitHub]](https://github.com/lazypoline)

<details>
<summary>BibTeX</summary>
<pre>
@inproceedings{Jacobs2024a,
  title={System Call Interposition Without Compromise},
  author={Jacobs, Adriaan and G{\"u}lmez, Merve and Andries, Alicia and Volckaert, Stijn and Voulimeneas, Alexios},
  booktitle={54th Annual IEEE/IFIP International Conference on Dependable Systems and Networks (DSN)}, 
  year={2024},
  pages={183-194},
  doi={10.1109/DSN58291.2024.00030}
}
</pre>
</details>

---

### 2023

**[Friend or Foe Inside? Exploring In-Process Isolation to Maintain Memory Safety for Unsafe Rust](https://arxiv.org/pdf/2306.08127.pdf)**  
**Merve Gülmez**, Thomas Nyman, Christoph Baumann, Jan Tobias Mühlberg  
*IEEE Secure Development Conference (SecDev '23), Atlanta, GA, 2023*  
[[PDF]](https://arxiv.org/pdf/2306.08127.pdf) &nbsp; [[GitHub]](https://github.com/secure-rewind-and-discard/secure-rewind-and-discard-rust-ffi)

<details>
<summary>BibTeX</summary>
<pre>
@inproceedings{Gulmez23d,
  author    = {Gülmez, Merve and Nyman, Thomas and Baumann, Christoph and Mühlberg, Jan Tobias},
  title     = {Friend or Foe Inside? Exploring In-Process Isolation to
               Maintain Memory Safety for Unsafe Rust},
  booktitle = {2023 IEEE Secure Development Conference (SecDev)},
  year      = {2023},
  month     = oct,
  pages     = {54--66},
  location  = {Atlanta, GA, USA},
  doi       = {10.1109/SecDev56634.2023.00020},
  url       = {https://doi.ieeecomputersociety.org/10.1109/SecDev56634.2023.00020},
  publisher = {IEEE Computer Society},
  address   = {Los Alamitos, CA, USA}
}
</pre>
</details>

---

**[Rewind & Discard: Improving Software Resilience using Isolated Domains](../files/2023-dsn-sdrad.pdf)**  
**Merve Gülmez**, Thomas Nyman, Christoph Baumann, Jan Tobias Mühlberg  
*53rd Annual IEEE/IFIP International Conference on Dependable Systems and Networks (DSN '23), Porto, Portugal, 2023*  
[[PDF]](/files/2023-dsn-sdrad.pdf) &nbsp; [[arXiv]](https://arxiv.org/pdf/2205.03205.pdf) &nbsp; [[GitHub]](https://secure-rewind-and-discard.github.io/)

<details>
<summary>BibTeX</summary>
<pre>
@inproceedings{Gulmez23a,
  author    = {Gülmez, Merve and Nyman, Thomas and Baumann, Christoph and Mühlberg, Jan Tobias},
  title     = {Rewind \& Discard: Improving Software Resilience Using Isolated Domains},
  booktitle = {Proceedings of 53rd Annual IEEE/IFIP International Conference on
               Dependable Systems and Networks},
  series    = {DSN '23},
  year      = {2023},
  month     = jun,
  pages     = {402--416},
  location  = {Porto, Portugal},
  issn      = {2158-3927},
  doi       = {10.1109/DSN58367.2023.00046},
  url       = {http://doi.org/10.1109/DSN58367.2023.00046},
  publisher = {IEEE Computer Society},
  address   = {Washington, DC, USA}
}
</pre>
</details>

---

**[Exploring the Environmental Benefits of In-Process Isolation for Software Resilience](https://arxiv.org/pdf/2306.02131.pdf)**  
**Merve Gülmez**, Thomas Nyman, Christoph Baumann, Jan Tobias Mühlberg  
*53rd Annual IEEE/IFIP International Conference on Dependable Systems and Networks — Supplemental Volume (DSN-S '23), Porto, Portugal, 2023*  
[[arXiv]](https://arxiv.org/pdf/2306.02131.pdf)

<details>
<summary>BibTeX</summary>
<pre>
@inproceedings{Gulmez23b,
  author    = {Gülmez, Merve and Nyman, Thomas and Baumann, Christoph and Mühlberg, Jan Tobias},
  title     = {Exploring the Environmental Benefits of In-Process Isolation for
               Software Resilience},
  booktitle = {Proceedings of 53rd Annual IEEE/IFIP International Conference on
               Dependable Systems and Networks - Supplemental Volume (DSN-S)},
  series    = {DSN '23},
  year      = {2023},
  month     = jun,
  pages     = {203--205},
  location  = {Porto, Portugal},
  issn      = {2833-292X/23},
  doi       = {10.1109/DSN-S58398.2023.00056},
  url       = {http://doi.org/10.1109/DSN-S58398.2023.00056},
  publisher = {IEEE Computer Society},
  address   = {Washington, DC, USA}
}
</pre>
</details>

---

**[The Climate Crisis is a Digital Rights Crisis: Exploring the Civil-Society Framing of Two Intersecting Disasters](https://limits.pubpub.org/pub/8544yai8/release/1)**  
Fieke Jansen, **Merve Gülmez**, Becky Kazansky, Narmine Abou Bakari, Claire Fernandez, Harriet Kingaby, Jan Tobias Mühlberg  
*9th Workshop on Computing within Limits (LIMITS '23), 2023*  
[[PDF]](https://www.beetzsee.de/posts/papers/2023-limits-digital-rights.pdf)

<details>
<summary>BibTeX</summary>
<pre>
@inproceedings{jansen_2023_climate_digital_justice,
  title = {The {Climate} {Crisis} is a {Digital} {Rights} {Crisis}: {Exploring} the {Civil}-{Society} {Framing} of {Two} {Intersecting} {Disasters}},
  doi = {10.21428/bf6fb269.b4704652},
  booktitle = {Proceedings of the 9th Workshop on {Computing} within {Limits} (LIMITS 2023)},
  publisher = {PubPub},
  author = {Jansen, Fieke and G{\"u}lmez, Merve and Kazansky, Becky and Bakari, Narmine Abou and Fernandez, Claire and Kingaby, Harriet and M{\"u}hlberg, Jan Tobias},
  year = {2023},
  url = {https://www.beetzsee.de/posts/papers/2023-limits-digital-rights.pdf}
}
</pre>
</details>

---

**[The Trust Model for Multi-Tenant 5G Telecom Systems Running Virtualized Multi-Component Services](https://5ghosts.eu/publications/deliverables/D1_3.pdf)**  
*5GHOSTS Project Deliverable, 2022*  
[[PDF]](https://5ghosts.eu/publications/deliverables/D1_3.pdf)

---

## Wireless Communications

### 2021

**[Deep Learning-Aided Spatial Multiplexing with Index Modulation](https://arxiv.org/pdf/2202.02856.pdf)**   
[[arXiv]](https://arxiv.org/pdf/2202.02856.pdf)

<details>
<summary>BibTeX</summary>
<pre>
@inproceedings{10.1007/978-3-030-70866-5_14,
  author = {Turhan, Merve and {\"O}zt{\"u}rk, Ersin and {\c{C}}{\i}rpan, Hakan Ali},
  booktitle = {Machine Learning for Networking},
  editor = {Renault, {\'E}ric and Boumerdassi, Selma and M{\"u}hlethaler, Paul},
  isbn = {978-3-030-70866-5},
  pages = {226--236},
  publisher = {Springer International Publishing},
  title = {Deep Learning-Aided Spatial Multiplexing with Index Modulation},
  year = {2021}
}
</pre>
</details>

---

### 2019

**[Deep Convolutional Learning-Aided Detector for Generalized Frequency Division Multiplexing with Index Modulation](https://arxiv.org/pdf/2202.02876.pdf)**   
*30th Annual IEEE International Symposium on Personal, Indoor and Mobile Radio Communications (PIMRC '19), 2019*  
[[arXiv]](https://arxiv.org/pdf/2202.02876.pdf)

<details>
<summary>BibTeX</summary>
<pre>
@INPROCEEDINGS{8904193,
  author={Turhan, Merve and Öztürk, Ersin and Çırpan, Hakan Ali},
  booktitle={2019 IEEE 30th Annual International Symposium on Personal, Indoor and Mobile Radio Communications (PIMRC)}, 
  title={Deep Convolutional Learning-Aided Detector for Generalized Frequency Division Multiplexing with Index Modulation}, 
  year={2019},
  pages={1-6},
  doi={10.1109/PIMRC.2019.8904193}
}
</pre>
</details>

---

**[Deep Learning-Aided Generalized Frequency Division Multiplexing](https://www.researchgate.net/publication/333783086_Deep_Learning-Aided_Generalized_Frequency_Division_Multiplexing)**  
[[ResearchGate]](https://www.researchgate.net/publication/333783086_Deep_Learning-Aided_Generalized_Frequency_Division_Multiplexing)

---

## Theses

**[Deep Learning-Aided Data Detection for Future Wireless Communication Systems](/files/master_thesis.pdf)**  
*Master's Thesis, Istanbul Technical University, 2021*  
[[PDF]](/files/master_thesis.pdf)

---

## Posters

* [Unlimited Lives: Secure In-Process Rollback with Isolated Domains](/files/SDROB_Poster-E-5CG2171BCR.pdf)
* [Mon CHÉRI — IEEE S&P 2025](/files/poster/mon_cheri_poster_SP2025.pdf)
* [DSbD Memory Safety for Telecommunications](/files/poster/dsbd.pdf)

---

## Open Source

* [secure-rewind-and-discard](https://secure-rewind-and-discard.github.io/) — SDRaD: Secure Rewind and Discard of Isolated Domains
* [lazypoline](https://github.com/lazypoline) — System call interposition without compromise
* [blindedcapabilities](https://github.com/blindedcapabilities) — BLACKOUT artifact
