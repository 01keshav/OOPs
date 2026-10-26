# OOPs, DSA and OS Course

A free study site for GEC students: **OOP in Java** **Data Structure and Algorithms** (Java, C++ and C) and **Operating Systems** (C, dark red theme), with simple explanations, animated diagrams, verified code with real output and practice questions.

**Live site:** https://01keshav.github.io/OOPs/
**DSA:** https://01keshav.github.io/OOPs/dsa.html
**OS:** https://01keshav.github.io/OOPs/os.html

---

## Subjects

| Subject | Course code | Topics | Status |
|---------|-------------|--------|--------|
| **OOPs in Java** | 105303 | 48 topics, 6 units | Live |
| **Data Structure and Algorithms** | 105302 | 39 topics, 6 units | Live (Java, C++, C) |
| **Operating Systems** | 105305 | 37 topics, 6 units | Live (C code, animated diagrams) |
| Digital Electronics | - | - | Coming soon |
| Discrete Mathematics | - | - | Coming soon |

A subject bar at the top of every page lets you switch between subjects. Subjects that are not ready yet show a "coming soon" message.

---

## What is inside every topic

**Learn**
- Clear definition first
- One numbered section per sub-concept
- Animated diagrams (stack, queue, tree, graph, linked list)
- Uses, advantages, limitations and common mistakes
- Quick revision list at the end
- ELI5 dropdown in simple Hinglish with real-life examples

**Practice**
- Code with real, verified output
- DSA code in **Java, C++ and C** with one-click language switch
- Practice questions from easy to hard
- Copy question button to paste into your favourite AI
- Copy notes, Print or Save as PDF, and My notes box


### Site features

- Neumorphic design with a dark and light mode toggle (DSA uses a pure black dark theme)
- Mark as complete button with progress bar, saved on your device
- Search, table of contents, previous and next buttons
- Topics outside the syllabus are marked in red with a skip popup
- Works on phones: scrollable menu and no sideways scroll
- Share button for WhatsApp, Telegram, X, LinkedIn, mail and copy link

---

## Syllabus coverage

<details>
<summary><b>OOPs in Java (course 105303)</b></summary>

| Unit | Topics |
|------|--------|
| 1. OOP Concepts and Java Basics | History, procedural vs OOP, JDK/JRE/JVM, data types, operators, control structures, first program |
| 2. Objects, Classes and Constructors | Class, object, methods, array of objects, constructors, method binding, static, access modifiers, `this`, garbage collection, inner classes, String |
| 3. Inheritance, Interfaces and Packages | Inheritance types, `super`, Object class, `final`, overloading, overriding, abstraction, interfaces, encapsulation, packages |
| 4. Exception Handling | Error vs exception, try/catch/finally, throw vs throws, custom exceptions |
| 5. Multithreading | Process vs thread, creating threads, lifecycle, priority, synchronization, inter-thread communication |
| 6. Files, Collections and JDBC | File streams, Collections framework, List/Set/Queue/Map, JDBC |

</details>

<details>
<summary><b>Data Structure and Algorithms (course 105302)</b></summary>

| Unit | Topics |
|------|--------|
| 1. Introduction | Terminologies, operations, algorithm analysis, asymptotic notations, time-space trade-off, arrays, recursion, worked complexity examples |
| 2. Stacks and Queues | Stack ADT, expression conversion and evaluation, queue, circular queue, priority queue, deque, queue using stacks |
| 3. Linked Lists | Singly, insertion and deletion, linked stack and queue, header nodes, doubly, circular, reverse and cycle detection, polynomial addition |
| 4. Searching, Sorting and Hashing | Linear and binary search, selection, bubble, insertion, quick, merge, heap sort, comparison, hashing |
| 5. Trees | Terminologies, binary, threaded, BST, AVL, applications, B tree and B+ tree |
| 6. Graph | Terminologies, representations, BFS, DFS and their complexity |

</details>

---

## Run it locally

No build step and no dependencies.

```bash
git clone https://github.com/01keshav/OOPs.git
cd OOPs
# open index.html (OOPs), dsa.html (DSA) or os.html (OS) in any browser
```

## Project structure

```text
OOPs/
  index.html     OOPs in Java course
  dsa.html       Data Structure and Algorithms course
  os.html        Operating Systems course
  README.md
  LICENSE
```

## Tech

Plain HTML, CSS and JavaScript, one self-contained file per subject. Progress, notes and theme are stored in your browser's `localStorage`. Nothing is sent to any server.

## Contributing

Found a bug, a wrong output or a missing topic? Pull requests are welcome.

1. Fork the repo
2. Create a branch: `git checkout -b fix/topic-name`
3. Make your change and test it in a browser
4. Open a pull request with a short description

Please keep code examples short, make sure they compile, and paste the real output.

## License

Released under the [MIT License](LICENSE).

Made by [Keshav](https://github.com/k4hav) | [Portfolio](https://k4hav.vercel.app)
