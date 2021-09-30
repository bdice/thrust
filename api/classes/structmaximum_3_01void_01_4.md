---
title: maximum< void >
parent: Generalized Identity Operations
grand_parent: Predefined Function Objects
nav_exclude: true
has_children: true
has_toc: false
---

# Struct `maximum< void >`

<code class="doxybook">
<span>struct maximum&lt; void &gt; {</span>
<span>public:</span><span>&nbsp;&nbsp;using <b><a href="/thrust/api/classes/structmaximum_3_01void_01_4.html#using-is_transparent">is&#95;transparent</a></b> = <i>see below</i>;</span>
<br>
<span>&nbsp;&nbsp;template &lt;typename T1,</span>
<span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;typename T2&gt;</span>
<span>&nbsp;&nbsp;__thrust_exec_check_disable__ __host__ constexpr __device__ auto </span><span>&nbsp;&nbsp;<b><a href="/thrust/api/classes/structmaximum_3_01void_01_4.html#function-operator()">operator()</a></b>(T1 && t1,</span>
<span>&nbsp;&nbsp;&nbsp;&nbsp;T2 && t2) const;</span>
<span>};</span>
</code>

## Member Types

<h3 id="using-is_transparent">
Type Alias <code>maximum&lt; void &gt;::is&#95;transparent</code>
</h3>

<code class="doxybook">
<span>using <b>is_transparent</b> = void;</span></code>

## Member Functions

<h3 id="function-operator()">
Function <code>maximum&lt; void &gt;::&gt;::operator()</code>
</h3>

<code class="doxybook">
<span>template &lt;typename T1,</span>
<span>&nbsp;&nbsp;typename T2&gt;</span>
<span>__thrust_exec_check_disable__ __host__ constexpr __device__ auto </span><span><b>operator()</b>(T1 && t1,</span>
<span>&nbsp;&nbsp;T2 && t2) const;</span></code>
