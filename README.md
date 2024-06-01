<p align="left">
<img src="https://i.imgur.com/t23TXuR.png" height="20%" width="20%" alt="daubert standard"/>
</p>

Introduction

Memory forensics is the analysis of data within a computer’s volatile memory. Volatile memory refers to forms of temporary memory on a computer that are power-dependent – meaning that when the computer is turned off, the contents of the volatile memory are lost. While there are forms of non-volatile memory, such as Read Only Memory (ROM), they have typically been limited to storing firmware.

 

For forensic investigators, volatile memory can provide valuable and unique insights into a system’s activity. This can include data such as open network connections, recently executed commands, encryption keys, account credentials, and running processes. Often, critical data relating to an attack or threat will only exist in the system’s memory. In fact, many network-based security solutions, such as firewalls and antivirus tools, are unable to detect forms of malware that are written directly into a computer’s volatile memory. As attack methods become increasingly sophisticated, memory forensics tools and skills are in high demand for today’s forensic investigators.

 

Forensic investigators capture volatile memory in a memory dump, which you may also see referred to as a core dump or system dump. A memory dump is a snapshot of the computer’s memory at a specific moment. Because all programs, whether legitimate or malicious, must be loaded into memory to execute, memory dumps can contain valuable forensic data about the state of the system before, during, or after an incident.

 

In this lab, you will learn how to use different tools for creating a memory dump. You will also learn how to analyze memory dumps and identify evidence of malware.



Lab Overview

SECTION 1 of this lab has two parts, which should be completed in the order specified.

 

    In the first part of the lab, you will capture a system memory dump using DumpIt.

    In the second part of the lab, you will analyze a memory dump using Paraben’s E3.

SECTION 2 of this lab allows you to apply what you learned in SECTION 1 with less guidance and different deliverables, as well as some expanded tasks and alternative methods. You will use two alternative tools to capture and analyze system memory: FTK Imager and Volatility. You will also use the Density Scout utility to assess suspicious files and determine whether they contain viruses.

 

Finally, you will explore the virtual environment on your own in SECTION 3 of this lab to answer a set of questions and challenges that allow you to use the skills you learned in the lab to conduct independent, unguided work - similar to what you will encounter in a real-world situation.



Learning Objectives

Upon completing this lab, you will be able to:

 

    Create a memory dump using DumpIt.

    Create a memory dump using FTK Imager.

    Analyze a memory dump using E3.

    Analyze a memory dump using Volatility.

    Identify signs of malware in memory dumps using Density Scout.



Topology

This lab contains the following virtual machines. Please refer to the network topology diagram below.

 

    vWorkstation (Windows: Server 2019)

 

<img src="https://i.imgur.com/OS9S5HV.png" height="20%" width="20%" alt="daubert standard"/>



Tools and Software

The following software and/or utilities are required to complete this lab. Students are encouraged to explore the Internet to learn more about the products and tools used in this lab.

 

    DumpIt
    Paraben's E3
    FTK Imager
    Volatility
    DensityScout



Deliverables

Upon completion of this lab, you are required to provide the following deliverables to your instructor:

 

SECTION 1

 

    Lab Report file, including screen captures of the following:

 

    DumpIt success notification
    List of processes in the memory dump
    Registry keys opened by the Hooker.exe process
    Files opened by the hooker.exe process

 

    Any additional information as directed by the lab:

 

    Record the start times for the oldest process and the newest process.
    Document your findings for the conhost.exe process. What is it and what is it used for?
    Document your findings for the hooker.exe process. What is it and what is it used for?

 

SECTION 2

 

    Lab Report file, including screen captures of the following:

 

    Memory capture finished successfully confirmation
    DensityScout results.

 

    Any additional information as directed by the lab:

 

    Document your findings for the rvlkl.exe process. What is it and what is it used for?
    Document whether any processes are flagged as hidden.
    Document whether the netscan module displays network usage associated with the Hooker.exe or rvlkl.exe processes.
    Document any information you were able to gather about port 56610.

 

SECTION 3

 

    Lab Report file, including screen captures of the following:

 

    FixtureComputer.exe process, and all those below it, in the pslist output
    Output of the yarascan
    Output of your privilege comparison

 

    Any additional information as directed by the lab:

 

    Document the three processes that connected to 205.134.253.10:4444.
    Document the name and purpose of the software you discovered.
