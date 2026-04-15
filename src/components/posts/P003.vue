<script setup>
</script>

<template>
  <div class="box">
    <h2>Prompt Injection Attacks in Large Language Models</h2>
    <div class="twoRow">
      <h3>#003</h3>
      <h3 style="text-align: right;">/ 15 APR 2026</h3>
    </div>
    <hr>
    <p>Closing out my senior year of college in summer of 2025, I was required to write a research paper for my computer science pathway. It took me a while to think of a topic I really wanted to focus on; computer science was such a broad field with a vast umbrella of topics falling under it's name. But of course as the AI bubble grew larger and larger, with more investment into the technology than ever, how could I not choose a topic revolving around AI? And as a cybersecurity double major, it seemed appropriate to discuss the security of AI.</p>
    <br>
    <p>After lots of delibration, I decided to research prompt injection on various AI models.</p>
    <br>
    <p>Below is a write-up giving the gist of my paper, organized by section. Since this post will just give a general rundown of what my research was about, I'd encourage you to go read the full paper located <a href="https://cisse.info/journal/index.php/cisse/issue/view/18" class="textLink">HERE</a> on the CISSE.info website. </p>
    <br>
    <h3>INTRO</h3>
    <br>
    <p class="margin-4top">With AI becoming more prevalent today, it's intergration is expanding. AI is now handling senstive information such as emails and databases, and further, more important intergrations are to come. Can artificial intellegence really be trusted to handle important data while vulnerable to attacks themselves? One of the biggest threats to modern AI chatbots is prompt injection, which involves sending a malicious payload in the form of a request to trick the AI into giving an answer that exposes critical data.</p>
    <br>
    <h3>METHODOLOGY</h3>
    <br>
    <p class="margin-4top">To test vulnerabilites to prompt injection, the experiment uses five different local AI models being attacked by with the same prompt injection payloads. To test these payloads, I used Ollama due to it's version control. If I used an online chatbot, it's versioning could change during this experiment, resulting in different answers. I can also use AI that are trained varying amounts of data, to see whether AI trained on more data are more secure.</p>
    <br>
    <p>The models used in the experiment consisted of deepseek r1, llama3.2, tinyllama, gemma3, and qwen3. I first used 16 different prompt injection payloads on the base models, without any modifications to how they receive the prompts. After they returned an answer, I would score the response on whether it was tricked by the payload or gave a blanket response that did not answer the prompt injection payload. After gathering that data, I used various methods to santize the input, such as string replacement, and collected that data as well. </p>
    <br>
    <h3>RESULTS</h3>
    <br>    
    <p class="margin-4top">Before the introduction of prompt injection mitigation, the AI models only ignored the prompt injection about half of the time. A marginal increase in protection against prompt injection was observed after introducing simple methods such as string replacement. However, while these methods did work, it's important to acknowledge that methods such as string replacement could result in a less reliable output, as the user's input is modified. </p>
    <br>
  </div>
</template>