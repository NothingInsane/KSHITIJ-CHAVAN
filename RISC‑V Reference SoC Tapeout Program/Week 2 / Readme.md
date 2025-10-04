<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>BabySoC - Part 1 README</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      line-height: 1.6;
      margin: 40px;
      background-color: #f9f9f9;
      color: #333;
    }
    h1, h2, h3 {
      color: #222;
    }
    code {
      background-color: #eee;
      padding: 2px 6px;
      border-radius: 4px;
      font-size: 0.95em;
    }
    ul {
      margin: 10px 0;
      padding-left: 20px;
    }
    section {
      margin-bottom: 30px;
    }
  </style>
</head>
<body>

  <h1>BabySoC - Part 1</h1>
  <p>
    This document describes the tasks implemented in <strong>Part 1 of BabySoC</strong>. 
    BabySoC is a simplified System-on-Chip (SoC) model created for learning fundamental SoC concepts. 
    It demonstrates integration of a simple CPU, memory, and peripheral interfaces.
  </p>

  <section>
    <h2>Overview</h2>
    <p>
      Part 1 of BabySoC introduces the following key components:
    </p>
    <ul>
      <li>A simple CPU core</li>
      <li>Memory subsystem</li>
      <li>Basic I/O interface</li>
    </ul>
  </section>

  <section>
    <h2>Tasks in Part 1</h2>
    <h3>1. Hello World Test</h3>
    <p>
      The first task involves running a basic <code>Hello World</code> program to verify toolchain setup, 
      CPU functionality, and basic I/O output.
    </p>

    <h3>2. Memory Read/Write Test</h3>
    <p>
      The second task checks memory operations. The CPU writes values to memory and reads them back 
      to ensure the memory interface is correctly integrated and functioning.
    </p>

    <h3>3. UART Communication Test</h3>
    <p>
      The third task validates communication between the CPU and the UART peripheral. 
      Data is transmitted via UART and observed to confirm correct integration of peripheral I/O.
    </p>
  </section>

  <section>
    <h2>Learning Objective</h2>
    <p>
      These tasks provide a practical introduction to SoC design. 
      They help learners understand the process of connecting a CPU to memory and peripherals, 
      testing system integration, and verifying correct functionality step by step.
    </p>
  </section>

</body>
</html>