---
title: mr::synchronized_pool_resource
parent: Memory Resources
grand_parent: Memory Management
nav_exclude: true
has_children: true
has_toc: false
---

# Struct `mr::synchronized_pool_resource`

A mutex-synchronized version of <code><a href="/thrust/api/classes/classmr_1_1unsynchronized__pool__resource.html">unsynchronized&#95;pool&#95;resource</a></code>. Uses <code>std::mutex</code>, and therefore requires C++11.

**Template Parameters**:
**`Upstream`**: the type of memory resources that will be used for allocating memory 

**Inherits From**:
[`mr::memory_resource< Upstream::pointer >`](/thrust/api/classes/classmr_1_1memory__resource.html)

<code class="doxybook">
<span>#include <thrust/mr/sync_pool.h></span><br>
<span>template &lt;typename Upstream&gt;</span>
<span>struct mr::synchronized&#95;pool&#95;resource {</span>
<span>public:</span><span>&nbsp;&nbsp;typedef <i>see below</i> <b><a href="/thrust/api/classes/structmr_1_1synchronized__pool__resource.html#typedef-unsync_pool">unsync&#95;pool</a></b>;</span>
<br>
<span>&nbsp;&nbsp;typedef <i>see below</i> <b><a href="/thrust/api/classes/structmr_1_1synchronized__pool__resource.html#typedef-lock_t">lock&#95;t</a></b>;</span>
<br>
<span>&nbsp;&nbsp;typedef <i>see below</i> <b><a href="/thrust/api/classes/structmr_1_1synchronized__pool__resource.html#typedef-void_ptr">void&#95;ptr</a></b>;</span>
<span class="doxybook-comment">/* Inherited from <code><b><a href="/thrust/api/classes/classmr_1_1memory__resource.html">mr::memory&#95;resource&lt; Upstream::pointer &gt;</a></b></code> */</span><br>
<span>&nbsp;&nbsp;typedef <i>see below</i> <b><a href="/thrust/api/classes/classmr_1_1memory__resource.html#typedef-pointer">pointer</a></b>;</span>
<br>
<span>&nbsp;&nbsp;static <a href="/thrust/api/classes/structmr_1_1pool__options.html">pool_options</a> </span><span>&nbsp;&nbsp;<b><a href="/thrust/api/classes/structmr_1_1synchronized__pool__resource.html#function-get_default_options">get&#95;default&#95;options</a></b>();</span>
<br>
<span>&nbsp;&nbsp;<b><a href="/thrust/api/classes/structmr_1_1synchronized__pool__resource.html#function-synchronized_pool_resource">synchronized&#95;pool&#95;resource</a></b>(Upstream * upstream,</span>
<span>&nbsp;&nbsp;&nbsp;&nbsp;<a href="/thrust/api/classes/structmr_1_1pool__options.html">pool_options</a> options = get&#95;default&#95;options());</span>
<br>
<span>&nbsp;&nbsp;<b><a href="/thrust/api/classes/structmr_1_1synchronized__pool__resource.html#function-synchronized_pool_resource">synchronized&#95;pool&#95;resource</a></b>(<a href="/thrust/api/classes/structmr_1_1pool__options.html">pool_options</a> options = get&#95;default&#95;options());</span>
<br>
<span>&nbsp;&nbsp;void </span><span>&nbsp;&nbsp;<b><a href="/thrust/api/classes/structmr_1_1synchronized__pool__resource.html#function-release">release</a></b>();</span>
<br>
<span>&nbsp;&nbsp;virtual void_ptr </span><span>&nbsp;&nbsp;<b><a href="/thrust/api/classes/structmr_1_1synchronized__pool__resource.html#function-do_allocate">do&#95;allocate</a></b>(std::size_t bytes,</span>
<span>&nbsp;&nbsp;&nbsp;&nbsp;std::size_t alignment = alignof(std::max&#95;align&#95;t)) override;</span>
<br>
<span>&nbsp;&nbsp;virtual void </span><span>&nbsp;&nbsp;<b><a href="/thrust/api/classes/structmr_1_1synchronized__pool__resource.html#function-do_deallocate">do&#95;deallocate</a></b>(void_ptr p,</span>
<span>&nbsp;&nbsp;&nbsp;&nbsp;std::size_t bytes,</span>
<span>&nbsp;&nbsp;&nbsp;&nbsp;std::size_t alignment = alignof(std::max&#95;align&#95;t)) override;</span>
<span class="doxybook-comment">/* Inherited from <code><b><a href="/thrust/api/classes/classmr_1_1memory__resource.html">mr::memory&#95;resource&lt; Upstream::pointer &gt;</a></b></code> */</span><br>
<span>&nbsp;&nbsp;virtual </span><span>&nbsp;&nbsp;<b><a href="/thrust/api/classes/classmr_1_1memory__resource.html#function-~memory_resource">~memory&#95;resource</a></b>() = default;</span>
<span class="doxybook-comment">/* Inherited from <code><b><a href="/thrust/api/classes/classmr_1_1memory__resource.html">mr::memory&#95;resource&lt; Upstream::pointer &gt;</a></b></code> */</span><br>
<span>&nbsp;&nbsp;<a href="/thrust/api/classes/classmr_1_1memory__resource.html#typedef-pointer">pointer</a> </span><span>&nbsp;&nbsp;<b><a href="/thrust/api/classes/classmr_1_1memory__resource.html#function-allocate">allocate</a></b>(std::size_t bytes,</span>
<span>&nbsp;&nbsp;&nbsp;&nbsp;std::size_t alignment = alignof(std::max&#95;align&#95;t));</span>
<span class="doxybook-comment">/* Inherited from <code><b><a href="/thrust/api/classes/classmr_1_1memory__resource.html">mr::memory&#95;resource&lt; Upstream::pointer &gt;</a></b></code> */</span><br>
<span>&nbsp;&nbsp;void </span><span>&nbsp;&nbsp;<b><a href="/thrust/api/classes/classmr_1_1memory__resource.html#function-deallocate">deallocate</a></b>(<a href="/thrust/api/classes/classmr_1_1memory__resource.html#typedef-pointer">pointer</a> p,</span>
<span>&nbsp;&nbsp;&nbsp;&nbsp;std::size_t bytes,</span>
<span>&nbsp;&nbsp;&nbsp;&nbsp;std::size_t alignment = alignof(std::max&#95;align&#95;t));</span>
<span class="doxybook-comment">/* Inherited from <code><b><a href="/thrust/api/classes/classmr_1_1memory__resource.html">mr::memory&#95;resource&lt; Upstream::pointer &gt;</a></b></code> */</span><br>
<span>&nbsp;&nbsp;__host__ __device__ bool </span><span>&nbsp;&nbsp;<b><a href="/thrust/api/classes/classmr_1_1memory__resource.html#function-is_equal">is&#95;equal</a></b>(const <a href="/thrust/api/classes/classmr_1_1memory__resource.html">memory_resource</a> & other) const;</span>
<span class="doxybook-comment">/* Inherited from <code><b><a href="/thrust/api/classes/classmr_1_1memory__resource.html">mr::memory&#95;resource&lt; Upstream::pointer &gt;</a></b></code> */</span><br>
<span>&nbsp;&nbsp;virtual __host__ virtual __device__ bool </span><span>&nbsp;&nbsp;<b><a href="/thrust/api/classes/classmr_1_1memory__resource.html#function-do_is_equal">do&#95;is&#95;equal</a></b>(const <a href="/thrust/api/classes/classmr_1_1memory__resource.html">memory_resource</a> & other) const;</span>
<span>};</span>
</code>

## Member Types

<h3 id="typedef-unsync_pool">
Typedef <code>mr::synchronized&#95;pool&#95;resource::unsync&#95;pool</code>
</h3>

<code class="doxybook">
<span>typedef <a href="/thrust/api/classes/classmr_1_1unsynchronized__pool__resource.html">unsynchronized_pool_resource</a>< Upstream ><b>unsync_pool</b>;</span></code>
<h3 id="typedef-lock_t">
Typedef <code>mr::synchronized&#95;pool&#95;resource::lock&#95;t</code>
</h3>

<code class="doxybook">
<span>typedef std::lock_guard< std::mutex ><b>lock_t</b>;</span></code>
<h3 id="typedef-void_ptr">
Typedef <code>mr::synchronized&#95;pool&#95;resource::void&#95;ptr</code>
</h3>

<code class="doxybook">
<span>typedef Upstream::pointer<b>void_ptr</b>;</span></code>

## Member Functions

<h3 id="function-get_default_options">
Function <code>mr::synchronized&#95;pool&#95;resource::&gt;::get&#95;default&#95;options</code>
</h3>

<code class="doxybook">
<span>static <a href="/thrust/api/classes/structmr_1_1pool__options.html">pool_options</a> </span><span><b>get_default_options</b>();</span></code>
Get the default options for a pool. These are meant to be a sensible set of values for many use cases, and as such, may be tuned in the future. This function is exposed so that creating a set of options that are just a slight departure from the defaults is easy. 

<h3 id="function-synchronized_pool_resource">
Function <code>mr::synchronized&#95;pool&#95;resource::&gt;::synchronized&#95;pool&#95;resource</code>
</h3>

<code class="doxybook">
<span><b>synchronized_pool_resource</b>(Upstream * upstream,</span>
<span>&nbsp;&nbsp;<a href="/thrust/api/classes/structmr_1_1pool__options.html">pool_options</a> options = get&#95;default&#95;options());</span></code>
Constructor.

**Function Parameters**:
* **`upstream`** the upstream memory resource for allocations 
* **`options`** pool options to use 

<h3 id="function-synchronized_pool_resource">
Function <code>mr::synchronized&#95;pool&#95;resource::&gt;::synchronized&#95;pool&#95;resource</code>
</h3>

<code class="doxybook">
<span><b>synchronized_pool_resource</b>(<a href="/thrust/api/classes/structmr_1_1pool__options.html">pool_options</a> options = get&#95;default&#95;options());</span></code>
Constructor. The upstream resource is obtained by calling <code>get&#95;global&#95;resource&lt;Upstream&gt;</code>.

**Function Parameters**:
**`options`**: pool options to use 

<h3 id="function-release">
Function <code>mr::synchronized&#95;pool&#95;resource::&gt;::release</code>
</h3>

<code class="doxybook">
<span>void </span><span><b>release</b>();</span></code>
Releases all held memory to upstream. 

<h3 id="function-do_allocate">
Function <code>mr::synchronized&#95;pool&#95;resource::&gt;::do&#95;allocate</code>
</h3>

<code class="doxybook">
<span>virtual void_ptr </span><span><b>do_allocate</b>(std::size_t bytes,</span>
<span>&nbsp;&nbsp;std::size_t alignment = alignof(std::max&#95;align&#95;t)) override;</span></code>
Allocates memory of size at least <code>bytes</code> and alignment at least <code>alignment</code>.

**Function Parameters**:
* **`bytes`** size, in bytes, that is requested from this allocation 
* **`alignment`** alignment that is requested from this allocation 

**Returns**:
A pointer to void to the newly allocated memory. 

**Exceptions**:
**`thrust::bad_alloc`**: when no memory with requested size and alignment can be allocated. 

**Implements**: [`do_allocate`](/thrust/api/classes/classmr_1_1memory__resource.html#function-do_allocate)

<h3 id="function-do_deallocate">
Function <code>mr::synchronized&#95;pool&#95;resource::&gt;::do&#95;deallocate</code>
</h3>

<code class="doxybook">
<span>virtual void </span><span><b>do_deallocate</b>(void_ptr p,</span>
<span>&nbsp;&nbsp;std::size_t bytes,</span>
<span>&nbsp;&nbsp;std::size_t alignment = alignof(std::max&#95;align&#95;t)) override;</span></code>
Deallocates memory pointed to by <code>p</code>.

**Function Parameters**:
* **`p`** pointer to be deallocated 
* **`bytes`** the size of the allocation. This must be equivalent to the value of <code>bytes</code> that was passed to the allocation function that returned <code>p</code>. 
* **`alignment`** the size of the allocation. This must be equivalent to the value of <code>alignment</code> that was passed to the allocation function that returned <code>p</code>. 

**Implements**: [`do_deallocate`](/thrust/api/classes/classmr_1_1memory__resource.html#function-do_deallocate)

