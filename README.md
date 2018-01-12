# awesome-embedded-c-testing [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

> A curated list of delightful Embedded Systems Testing  [libraries, techniques](#techs) and [references](#resources)!

*Please read the [contribution guidelines](contributing.md) before contributing.*

# Table of Contents

<!-- TOC depthFrom:2 depthTo:6 orderedList:false updateOnSave:false withLinks:true -->

- [Testing Techniques](#techs)
    - [RTOS](#rtos)
    - [main](#main)
    - [Infinite Loops](#Infinite Loops)
    - [Private data](#Private data)
    - [Registers](#Registers)
    - [CANOpen](#canopen)
        - [Open Source](#open-source)
        - [Proprietary](#proprietary)
    - [Serialization](#serialization)
    - [RTOSs](#rtoss)
        - [Free or Open Source](#free-or-open-source)
        - [Commercial](#commercial)
    - [Testing](#testing)
    - [Frameworks](#frameworks)
    - [STL](#stl)
- [Resources](#resources)
    - [Other Lists](#other-lists)
    - [Podcasts](#podcasts)
    - [Videos](#videos)
    - [Books](#books)
    - [Standards](#standards)
    - [Tools](#tools)
    - [Embedded Linux](#embedded-linux)
    - [Courses](#courses)
- [License](#license)

<!-- /TOC -->

## Testing Techniques 

### RTOS

To test software that uses multithreading and tasks, follow this posts:

http://blog.wingman-sw.com/archives/282 
http://blog.wingman-sw.com/archives/288 
http://blog.wingman-sw.com/archives/303 

### main

http://vandervoord.net/blog/2015/5/19/unit-test-how-main-

### Infinite Loops

http://vandervoord.net/blog/2015/5/19/unit-test-how-infinite-loops

### Private data

http://vandervoord.net/blog/2015/5/24/unit-test-how-private-data

### Registers

http://vandervoord.net/blog/2015/5/24/unit-test-how-registers
http://vandervoord.net/blog/2015/5/24/unit-test-how-faking-changing-registers
http://vandervoord.net/blog/2015/5/24/unit-test-how-verifying-multiple-register-writes

## Tools for Integration

### CANOpen

#### Open Source

- [CanFestival](http://www.canfestival.org/) - CanFestival focuses on providing an ANSI-C platform independent CANOpen® stack that can be built as master or slave nodes on PCs, Real-time IPCs, and Microcontrollers.
- [CANopenNode](https://github.com/CANopenNode/CANopenNode) - CANopenNode is written in ANSI C in object-oriented way. It runs on different microcontrollers, as standalone application or with RTOS

#### Proprietary

- [Ixxat](https://www.ixxat.com/products/products-industrial/protocol-software-and-apis/protocol-software/canopen-protocol-software)
- [port](http://www.port.de/en/products/canopen.html)
- [ESA's microCANOpen Plus](http://www.canopenstore.com/pip/microcanopen-plus.html)
- [emtas](https://www.emtas.de/en/produkte/canopen-master-stack)

### Serialization

- [nanopb](https://koti.kapsi.fi/jpa/nanopb/) - Nanopb is a plain-C implementation of Google's Protocol Buffers data format. It is targeted at 32 bit microcontrollers, but is also fit for other embedded systems with tight (2-10 kB ROM, <1 kB RAM) memory constraints.
- [mpack](https://github.com/ludocode/mpack) - A C encoder/decoder for [MessagePack](http://msgpack.com) messages suitable for resource constriants embedded systems. Supports disabling dynamic memory allocation and overriding malloc, free, and realloc.
- [tinycbor](https://github.com/01org/tinycbor) - Intel's implementation of [CBOR](http://cbor.io/) designed for their IOT-based applications and processors

### RTOS
#### Free or Open Source

- [TinyOS](https://github.com/tinyos/tinyos-main) - A operating system designed for low-power wireless devices, such as those used in sensor networks, ubiquitous computing, personal area networks, smart buildings, and smart meters.
- [ContikiOS](https://github.com/contiki-os/contiki) - A free Operating System with focus to provide standardized low-power wireless communication for a wide range of hardware platforms.
- [FreeRTOS](http://www.freertos.org/) - A free use Real Time Operating system which is widely used and supports a large number of platforms.
- [RIOT](https://github.com/RIOT-OS/)  - A free OS for IoT devices providing foundational trust services. The trust services include device identity, sealing, attestation, and data integrity. The term “Robust” is used because the minimal trusted computing base is tiny, and because RIoT capabilities can remotely re-establish trust in devices that have been compromised by malware.
- [RTEMS](https://www.rtems.org/) - Real-Time Executive for Multiprocessor Systems or RTEMS is an open source Real Time Operating System (RTOS) that supports open standard application programming interfaces (API) such as POSIX. It is used in space flight, medical, networking and many more embedded devices using processor architectures including ARM, PowerPC, Intel, Blackfin, MIPS, Microblaze and more.
 [Fuschia](https://github.com/fuchsia-mirror/magenta) - Magenta is the core platform that powers the Fuchsia OS. Magenta is composed of a microkernel (source in kernel/...) as well as a small set of userspace services, drivers, and libraries (source in system/...) necessary for the system to boot, talk to hardware, load userspace processes and run them, etc. Fuchsia builds a much larger OS on top of this foundation.
 
#### Commercial

- [SafeRTOS](https://www.highintegritysystems.com/safertos/) - Certified version of FreeRTOS by TUEV SUED against IEC 61508 (basic functional safety standard) up to SIL3 (the highest safety integrity level for a single software component), ISO 26262 ASIL D (automotive standard) and EN62304 (medical device standard).
- [INTEGRITY/INTEGRITY-178](http://www.ghs.com/products/rtos/integrity.html#performance) - Two commercial RTOS variants targeting to power embedded systems with total reliability, absolute security, and maximum real-time performance. The variant INTEGRYTY-178 has a lot of safety and security certifications.
- [PikeOS](https://www.sysgo.com/products/pikeos-hypervisor/) - A commercial micro-kernel based operating system with a small footprint and certified for DO-178 (avionics), IEC-61508 (industrial), ISO-26262 (automotive).
- [Rocket](http://www.windriver.com/products/operating-systems/rocket/) - A free embedded operating system specifically designed to quickly and easily build small, intelligent devices in Wind Rivers cloud-based development environment, Wind River Helix™ App Cloud.
- [Nucleus RTOS](https://www.mentor.com/embedded-software/nucleus/) - Commercial, highly scalable micro-kernel based real-time operating system designed for scalability and reliability.
- [uC/os](https://www.micrium.com/rtos/kernels/) - µC/OS-II and µC/OS-III are preemptive, highly portable, and scalable real-time kernels. You can test them out for free, but you must pay to put them into a product.
- [TI-RTOS](www.ti.com/tool/ti-rtos) - A real-time operating system for TI microcontrollers, It Includes TCP/IP and USB stacks, a FAT file system, and device drivers, Most of the TI-RTOS components are released under the BSD License.

### Testing

- [CppUTest](https://cpputest.github.io/) - unit testing and mocking framework for C/C++ with a focus on working for embedded systems!
- [ceedling, unity and cmock](http://www.throwtheswitch.org/) - Unit testing, mocking and build framework written in C with ruby for generating and building.
- [doctest](https://github.com/onqtam/doctest) - A lightweight and feature-rich C++98/C++11 single-header testing framework for unit tests and TDD.
- [Mockitopp](https://github.com/tpounds/mockitopp) - A C++ mocking framework inspired by the ideas developed for Mockito written by Szczepan Faber, et al. The purpose is to provide similar construction semantics for creating mock objects leading to smaller, more readable test cases. It is designed to be a lightweight framework allowing you to mock dependencies for a system under test using a simple descriptive domain specific language. The goal is to help create simpler, less brittle test cases; ultimately, leading to less maintenance overhead in the future.
- [Trompeloeil](https://github.com/rollbear/trompeloeil) - A thread safe header only mocking framework for C++14 using the Boost Software License 1.0
- [Catch](https://github.com/catchorg/Catch2) - A modern, C++-native, header-only, test framework for unit-tests, TDD and BDD - using C++11, C++14, C++17 and later (or C++03 on the Catch1.x branch)

### Frameworks

- [Arduino](https://www.arduino.cc/)
- [ARM mbed](https://www.mbed.com/en/) - The ARM mbed IoT Device Platform provides the operating system, cloud services, tools and developer ecosystem to make the creation and deployment of commercial, standards-based IoT solutions possible at scale.


## Resources

### Other Lists

- [Single File Libs](https://github.com/nothings/single_file_libs) - Single File libraries for C++ and C. Some might be useful for embedded systems use.

### Podcasts

- [Embedded](http://embedded.fm/) - Elicia White and Christopher White interview makes, hackers and engineers who work on embedded systems
- [The Amp Hour](http://www.theamphour.com/)
- [Sparkgap](http://thesparkgap.net/)

### Videos

- [wingman-sw](http://blog.wingman-sw.com) - More on the embedded software

### Books

- Domeika, Max: [Software Development for Embedded Multi-core Systems: A Practical Guide Using Embedded Intel Architecture](https://www.elsevier.com/books/software-development-for-embedded-multi-core-systems/domeika/978-0-7506-8539-9), Newnes, 1st, 2008 (ISBN-10: 0750685395, ISBN-13: 978-0750685399)
- González, Alex: [Embedded Linux Projects Using Yocto Project Cookbook](https://www.packtpub.com/virtualization-and-cloud/embedded-linux-projects-using-yocto-project-cookbook), Packt Publishing Limited, 1st edition, 2015 (ISBN-10: 1784395188, ISBN-13: 9781784395186)
- Hagar, Jon Duncan: [Software Test Attacks to Break Mobile and Embedded Devices](https://www.crcpress.com/Software-Test-Attacks-to-Break-Mobile-and-Embedded-Devices/Hagar/p/book/9781466575301), Chapman & Hall/Crc, 1st, 2013 (ISBN-10: 1466575301, ISBN-13: 978-1466575301)
- Simmonds, Chris: [Mastering Embedded Linux Programming](https://www.packtpub.com/networking-and-servers/mastering-embedded-linux-programming), Packt Publishing Limited, 1st edition, 2015 (ISBN-10: 1784392537, ISBN-13: 9781784392536)
- [Making Embedded Systems by Elicia White](https://www.amazon.com/Making-Embedded-Systems-Patterns-Software/dp/1449302149) - Covers the basics of embedded systems architecture, design and patterns.
- [Test Driven Developmet for Embedded C by James Grenning](https://www.amazon.com/Driven-Development-Embedded-Pragmatic-Programmers/dp/193435662X/ref=asap_bc?ie=UTF8) - How to approach test driven development for embedded devices written in C.

### Standards

- [Embedded C Coding Standards](http://www.barrgroup.com/Embedded-Systems/Books/Embedded-C-Coding-Standard) - Coding standards for embedded C from the Barr Group.

### Tools

- [PlatformIO](http://platformio.org/) - PlatformIO is an open source ecosystem for IoT development
Cross-platform build system. Continuous and IDE integration. Arduino and ARM mbed compatible

### Embedded Linux

- [yocto](https://www.yoctoproject.org/) - Yocto is a tool for creating custom embedded linux systems

### Courses

- [C++ programming in Qt FrameWork Part I (udemy)](https://www.udemy.com/c-programming-creating-applications-with-qt-framework/) - not free

## License

[![CC0](http://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, [Riccardo Ancona](http://raa.altervista.org) has waived all copyright and related or neighboring rights to this work.
