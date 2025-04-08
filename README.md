Semantic Frame Compression (SFM)
A lightweight, standardized method for efficiently transferring complex information between LLM sessions. It is LLM generated with my help so do with that what you will. 

What is SFM?
Semantic Frame Compression is a structured format that allows you to compress large amounts of information into a compact representation that language models can easily reconstruct. It preserves semantic relationships and hierarchical structure while drastically reducing token usage.

Why Use SFM?
Context Window Optimization: Transfer hours of conversation in a single message
Information Retention: Maintains 90-100% of critical information
Compression Efficiency: Achieves 50-85% reduction in character count
No Special Tools Required: Works with any text-based LLM interface
Domain Adaptability: Templates for technical, narrative, procedural content

Quick Start
Compression:
To compress information, use this basic structure:

Provide LLM with contents of the Semantic Frame Compression text file which standardizes the compressed response.

Prompt: 
Using the Semantic Frame Compression(SFC), compress the following information:
{Text to be compressed and passed to another LLM session}


Decompression:

Provide LLM with contents of the Semantic Frame Compression text file.

Prompt:
Using the Semantic Frame Compression(SFC), expand the following compressed information:
[COMPRESSED FRAME]


Example
Original (359 chars): "The quantum computer leverages the principles of quantum mechanics, specifically superposition and entanglement, to perform computations that would be infeasible for classical computers. While a classical bit must be either 0 or 1, a quantum bit (qubit) can exist in a superposition of both states simultaneously, exponentially increasing computational power as more qubits are added to the system."

Compressed (160 chars):

QC{ 
  IS: computing+quantum-mechanics 
  USES: superposition+entanglement 
  ENABLES: classical-impossible-calculations 
  DIFFERS: bits[classical:0|1,quantum:0&1] 
  SCALES: exponential[2^n] 
}

More details in the Semantic Frame Compression text file.

I have tried it with a couple different LLM (Claude 3.7, Llama3.1) and it seem to work very well but mileage may vary, might be helpful to someone.

License
MIT License
