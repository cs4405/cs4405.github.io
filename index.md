---
layout: minimal
title: CS4405 Analysis of Concurrent and Distributed Programs
nav_exclude: true
seo:
  type: Course
  name: CS4405 Analysis of Concurrent and Distributed Programs\
---

# {{ site.tagline }}
{: .mb-2 }
{{ site.description }}
{: .fs-6 .fw-300 }

{% assign instructors = site.staffers | where: 'role', 'Instructor' %}
{% for staffer in instructors %}
{{ staffer}}
{% endfor %}


## Course description:

Software systems are becoming highly concurrent and distributed to utilize modern multicore architectures and increasing speed and bandwidth in networks. Shared-memory concurrency in multicore programs and message-passing concurrency in distributed programs share many common abstractions and problems.

In the multicore era, all performance-critical software employs some form of concurrent programming; typically shared memory concurrency. In this setting,
programmers use a number of primitives to develop efficient and correct concurrent programs. To do so the programmers have to understand the behaviors of the primitives and reason about them. It is also important to match the programming paradigms and underlying architectures. For instance, traditionally programmers have assumed that a multithreaded program executed simply by interleaving the executions of its threads—a model known as sequential consistency (SC). This assumption is, however, invalidated both by mainstream multicore architectures, which often execute instructions out of order, and by compilers, whose optimizations affect the outcomes of concurrent programs. As a result, concurrent programs have more outcomes than SC allows.

In the distributed setting, the units of concurrency are independent processes that do not share memory but communicate by exchanging asynchronous messages. The execution of such a system involves two main sources of nondeterminism: concurrency and partial failures. As the processes run concurrently, the exchanged messages can be delivered and processed in many different orderings. The distributed set of processes is also prone to network of process failures. The trade-off between the system’s availability in the existence of failures and the consistency between the processes gives rise to a spectrum of weak consistency notions. It is important to reason about concurrency, possible failures, and consistency guarantees to implement distributed programs correctly and understand their behavior.

This course aims to explore analysis techniques for concurrent and distributed programs.

## Course organization

* **5 ECTS:** You need to devote at least 140 hours of study for this course.  
* **Online meetings:** The course consists of 14 2-hour meetings. You are not required, but you are strongly encouraged, to attend.
* **Assignments:** Two homework assignments ((2 x 10%) of the course grade)
* **Project:** Project implementation, report, and a presentation (80% of the course grade)
* **Teams:** The students are responsible to form teams and communicate them to the course TAs.
<!-- * **Teaching Assistants:** Teaching assistants will provide you with feedback on your assignments and projects. Do be active in asking questions, but don’t expect them to provide you with solutions. (TODO: Office hours?) -->

## Teaching assistants

{% assign tas = site.staffers | where: 'role', 'TA' %}
{% for staffer in tas %}
{{ staffer }}
{% endfor %}

## Course schedule:

{% for module in site.modules %}
{{ module }}
{% endfor %}

The schedule is subject to small changes during the term.
 
## Course projects:
 
- **Data Race Detection in C/C++ Concurrent Programs:** In this project, you will detect data races in the executions of C11 concurrent programs. [More information](files/2022-shared-memory-project.pdf)

- **Checking linearizability or sequential consistency of a distributed database system:** In this project, you will test a distributed database of your choice and check whether its executions satisfy linearizability or sequential consistency properties. [More information](files/2022-distributed-systems-project.pdf)

Alternatively, you can suggest your own project that involves **replicating an existing work** or **proposing a new approach to an existing problem**. If you have exciting ideas for the course project, contact the TA's and the teachers to determine the context of your project. 