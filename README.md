<p><strong><font size="5">Information</font></strong></p>
GPT4-X-Alpaca 30B 4-bit working with GPTQ versions used in Oobabooga's Text Generation Webui and KoboldAI.
<p>Quantized using <i>--true-sequential</i> and <i>--act-order</i> optimizations.</p>
This was made using Chansung's GPT4-Alpaca Lora: https://huggingface.co/chansung/gpt4-alpaca-lora-30b

<p><strong>Training Parameters</strong></p>
<ul><li>num_epochs=10</li><li>cutoff_len=512</li><li>group_by_length</li><li>lora_target_modules='[q_proj,k_proj,v_proj,o_proj]'</li><li>lora_r=16</li><li>micro_batch_size=8</li></ul>

<p><strong><font size="5">Benchmarks</font></strong></p>

<strong>Wikitext2</strong>: 4.481280326843262

<strong>Ptb-New</strong>: 8.539161682128906

<strong>C4-New</strong>: 6.451964855194092

<strong>Note</strong>: This version does not use <i>--groupsize 128</i>, therefore evaluations are minimally higher. However, this version allows fitting the whole model at full context using only 24GB VRAM.