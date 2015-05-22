Acoustic Communication
========
<p>This is the demo for Acoustic communication (as a potential alternative of NFC)</p>

<h2>Basic princinple</h2>
<p>
The current implementation is based on Frequency Shift Keying, every 2-bit is mapped to one frequency 
among 4 freq total and the corresponding waveform of 441 bits long. A marker byte 10 is used for indicating
the start of the UID. CRC bytes are attached at the end of the byte sequence for error correction. 
Sampling frequency is 44KHz. The decoder used FFT.
</p>
<p>As an example, 7-byte UID takes roughly (7+2)*8/2*441/44Khz = 360ms to transmit. </p>

</p>
Encode： Generator.java
<br/>
Decode: Receiver.java
</p>
<br/>
By xuq
<br/>
Email: xuq22@mcmaster.ca
<br>

<h2>Already implemented</h2>
<ul>
<li> Can identify 7-byte UID with latency < 5 sec </li>
<li> Detection range < 10cm (even longer also works, can be controlled by speaker volume bar)</li>
<li> a degree of tolerance to background noise (human conversation, music, …)</li>
<li> robustness to phone orientation</li>
<li> A listening background task</li>
<li> CRC32 is included.</li>
</ul>

<h2>TODO</h2>
<ul>
<li>Improve efficiency</li>
<li>Synchronization</li>
</ul>
