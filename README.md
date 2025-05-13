# comp307-lab-1-understanding-process-concepts-solved
**TO GET THIS SOLUTION VISIT:** [Comp307 LAB 1-Understanding Process Concepts Solved](https://www.ankitcodinghub.com/product/comp307-lab-1-understanding-process-concepts-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;92128&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;Comp307 LAB 1-Understanding Process Concepts Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

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

<div class="kksr-stars-active" style="width: 0px;">
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
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="section">
<div class="layoutArea">
<div class="column">
LAB-1 (Understanding Process Concepts)

<ol>
<li>Write a C program to implement process System calls ? [Hint use fork())]</li>
<li>How many processes are created in a given program? #include &lt;stdio.h&gt;
#include &lt;unistd.h&gt; int main()

{

int i;

for (i = 0; i &lt; 4; i++) fork();

return 0;

}
</li>
<li>When will line J be reached? #include &lt;sys/types.h&gt;
#include &lt;stdio.h&gt; #include &lt;unistd.h&gt; int main()

{

pid_t pid;

/* fork a child process */

pid = fork();

if (pid &lt; 0) { /* error occurred */ fprintf(stderr, “Fork Failed”);

return 1;

}

else if (pid == 0) { /* child process */ execlp(“/bin/ls”,”ls”,NULL);

printf(“LINE J”);

}

else { /* parent process */

/* parent will wait for the child to complete */ wait(NULL);

printf(“Child Complete”);

}

return 0;

}
</li>
</ol>
</div>
</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="section">
<div class="layoutArea">
<div class="column">
<ol start="4">
<li>What are the pid values?

#include &lt;sys/types.h&gt;

#include &lt;stdio.h&gt; #include &lt;unistd.h&gt; int main()

{

pid_t pid, pid1;

/* fork a child process */

pid = fork();

if (pid &lt; 0) { /* error occurred */ fprintf(stderr, “Fork Failed”);

return 1;

}

else if (pid == 0) { /* child process */ pid1 = getpid();

printf(“child: pid = %d”,pid); /* A */ printf(“child: pid1 = %d”,pid1); /* B */

}

else { /* parent process */

pid1 = getpid();

printf(“parent: pid = %d”,pid); /* C */ printf(“parent: pid1 = %d”,pid1); /* D */ wait(NULL);

}

return 0;

}
</li>
<li>What will be at Line X and Line Y?
#include &lt;sys/types.h&gt; #include &lt;stdio.h&gt; #include &lt;unistd.h&gt; #define SIZE 5

int nums[SIZE] = {0,1,2,3,4}; int main()

{

int i;

pid t pid;

pid = fork();

if (pid == 0) {

for (i = 0; i &lt; SIZE; i++) {

nums[i] *= -i;

printf(“CHILD: %d “,nums[i]); /* LINE X */
</li>
</ol>
</div>
</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="section">
<div class="layoutArea">
<div class="column">
}

}

else if (pid &gt; 0) {

wait(NULL);

for (i = 0; i &lt; SIZE; i++)

printf(“PARENT: %d “,nums[i]); /* LINE Y */ }

return 0;

}

</div>
</div>
</div>
</div>
