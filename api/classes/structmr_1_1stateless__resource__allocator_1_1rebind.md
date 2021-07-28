---
title: mr::stateless_resource_allocator::rebind
nav_exclude: true
has_children: true
has_toc: false
---

# Struct `mr::stateless_resource_allocator::rebind`

The <code>rebind</code> metafunction provides the type of an <code><a href="/api/classes/classmr_1_1stateless__resource__allocator.html">stateless&#95;resource&#95;allocator</a></code> instantiated with another type.

**Template Parameters**:
**`U`**: the other type to use for instantiation. 

<code class="doxybook">
<span>#include <thrust/mr/allocator.h></span><br>
<span>template &lt;typename U&gt;</span>
<span>struct mr::stateless&#95;resource&#95;allocator::rebind {</span>
<span>public:</span><span>&nbsp;&nbsp;typedef <i>see below</i> <b><a href="/api/classes/structmr_1_1stateless__resource__allocator_1_1rebind.html#typedef-other">other</a></b>;</span>
<span>};</span>
</code>

## Member Types

<h3 id="typedef-other">
Typedef <code>mr::stateless&#95;resource&#95;allocator::rebind::other</code>
</h3>

<code class="doxybook">
<span>typedef <a href="/api/classes/classmr_1_1stateless__resource__allocator.html">stateless_resource_allocator</a>< U, Upstream ><b>other</b>;</span></code>
The typedef <code>other</code> gives the type of the rebound <code><a href="/api/classes/classmr_1_1stateless__resource__allocator.html">stateless&#95;resource&#95;allocator</a></code>. 

