# ece6913a-lab-3-cache-simulator-solved
**TO GET THIS SOLUTION VISIT:** [ECE6913A Lab 3-Cache Simulator Solved](https://www.ankitcodinghub.com/product/ece6913a-lab-3-cache-simulator-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;93694&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;ECE6913A Lab 3-Cache Simulator Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
&nbsp;

In this lab assignment you will implement a two-level (L1 and L2) cache simulator in C++. The cache simulator will take several parameters describing the cache (block size, associativity, etc.) along with a memory access trace file for an input program.

Cache Design

<ul>
<li>● &nbsp;Read Miss: on a read miss, the cache issues a read request for the data from the lower level of the cache. Once the data is returned, it is placed in an empty way, if one exists, or data in one of the ways is evicted to create room for the new data.○ The ways of the cache are numbered from {0,1, 2, …, W-1} for a W-way cache. If an empty way exists, data is placed in lowest numbered empty way.
○ Eviction is performed based on a round-robin policy. Each way has a counter that is initialized to 0, counts to W-1 and loops back to zero. The current value of the counter indicates the Way from which data is to be evicted. The counter is incremented by 1 after an eviction.
</li>
<li>● &nbsp;Write Hit: both the L1 and L2 caches are write-back caches.</li>
<li>● &nbsp;Write Miss: both the L1 and L2 caches are write no-allocate caches. On a write miss, thewrite request is forwarded to the lower level of the cache.</li>
<li>● &nbsp;Inclusive: the L1 and L2 caches are inclusive. This is the design we assumed in class, itmeans that all data in the L1 is also included in the L2, or that L1’s data is a subset of L2. If you’re interested, you can read about exclusive and non-inclusive caching design alternatives. They complicate the design but can offer higher performance (please don’t implement them in this lab, though!).</li>
</ul>
</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
Configuration File (config.txt):

The parameters of the L1 and L2 caches are specified in a configuration file. The format of the configuration file is as follows.

<ul>
<li>● &nbsp;Block size: Specifies the block size for the cache in bytes. This should always be a non- negative power of 2 (i.e., 1, 2, 4, 8, etc.).</li>
<li>● &nbsp;Associativity: Specifies the associativity of the cache. A value of “1” implies a direct-mapped cache, while a “0” value implies the cache is fully associative. Should always be a non- negative power of 2.</li>
<li>● &nbsp;Cache size: Specifies the total size of the cache data array in KiB.An example config file is provided below. It specifies a 16KiB direct-mapped L1 cache with 8-byte blocks, and a 32KiB 4-way set associative L2 cache with 16-byte blocks
Sample configuration file for L1 and L2 Cache: L1:

8

1

16 L2: 16 4 32

The skeleton code provided reads the config file and initializes variables for the L1 and L2 cache parameters.
</li>
</ul>
</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
Trace File (trace.txt):

Your simulator will need to take as input a trace file that will be used to compute the output statistics. The trace file will specify all the data memory accesses that occur in the sample program. Each line in the trace file will specify a new memory reference. Each line in the trace cache will therefore have the following two fields:

<ul>
<li>● &nbsp;Access Type: A single character indicating whether the access is a read (‘R’) or a write (‘W’).</li>
<li>● &nbsp;Address: A 32-bit integer (in unsigned hexidecimal format) specifying the memory addressthat is being accessed.

Fields on the same line are separated by a single space.

The skeleton code provided reads the trace file one line at a time in order. After each access, your code should emulate the impact of the access on the cache hierarchy.

Simulator Output:

For each cache access, your simulator must output whether the access caused a read or write hit or miss in the L1 and L2 caches, or, in the L2 cache, if it was not accessed. Each event is coded with a number, as shown below.

0: No Access 1: Read Hit 2: Read Miss 3: Write Hit 4: Write Miss

For example, if a read access Misses in the L1 cache but hits in the L2 cache, your simulator would output:

21

where the first number corresponds to the L1 cache event and the second to the L2 cache event.

(Note: when there is a read miss in L1 and read hit in L2, the L1 cache might have to evict some data to make room for the data returned by the L2 cache. If the evicted data is dirty, this will result in a write access to L2. If the write access to L2 results in a hit no data will be evicted/replaced. If it results in a miss, the data will be forwarded to main memory without changing the L2 cache state since the L2 cache is a write-no-allocate cache.)
</li>
</ul>
</div>
</div>
</div>
