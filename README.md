Script EKG is a fairly simple user component that contains several important pieces. An LFO oscillator in One-Shot mode, a Lua script that periodically resets the LFO timer so it never times out, and an Event Logger.
If the Lua Scripting Engine locks up on the core, the Lua script won't be able to reset the LFO timer and it will timeout, triggering a Fault output and creating an error log message in the Cores event log.
If for some reason the Lua scripting engine recovers, that status will be reflected and a warning message will be logged to the core.
There are signal flags in place that you can integrate into your design, or you can physically wire the output pins on the main component to whatever you would like.
On the main component, the first output pin is a Status output which can be wired to a Status Combiner, or a Monitoring Proxy. The second output pin is a Boolean output for the OK state. The third output is a Boolean output for the Fault state.


https://github.com/JesseBlanke/Q-SYS

MIT License

Copyright (c) 2025 JesseBlanke

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
