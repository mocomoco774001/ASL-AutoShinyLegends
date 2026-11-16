# Japanese Crystal VC branch

This branch adapts the Gen II Celebi encounter detector and guest-code patch for the Japanese Crystal Virtual Console memory layout.

The address changes are based on the Japanese VC layout. A successful CI build verifies compilation only; real hardware validation on a Japanese New 3DS VC installation is still required before relying on the plugin.


## Performance tuning

The per-frame Crystal ROM probe now has a bounded memory-query budget, and the Celebi context scan is reduced to 32 KiB per frame with a bounded query count. This is a performance experiment only; timing and encounter correctness still require real-hardware validation.
