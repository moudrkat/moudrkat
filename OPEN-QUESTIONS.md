# Open questions I'd love help with

Things I can't get to, or can't do alone. Each one says where to start and how you'd know you're done.
Small is fine. A result that says "no, it doesn't" is a result. Open an issue in the repo, or just send the PR.

The idea of keeping such a list is Neel Nanda's ([200 Concrete Open Problems in Mechanistic Interpretability](https://www.alignmentforum.org/s/yivyHaCAmMJ3CqSyj)); the one-command starts and "swap one thing and it's yours" are how Andrej Karpathy and Georgi Gerganov build their repos. I'm copying people who do this well.

## Five minutes

| | start | done when |
|---|---|---|
| **Talk to the chip model your way** | [esp32-ai](https://github.com/moudrkat/esp32-ai): write 20 requests the way *you* would say them | you've told me which ones it got wrong. My own test sentences are too polite |
| **Run Maxwell on your computer** | [maxwell-on-a-chip](https://github.com/moudrkat/maxwell-on-a-chip): `host/maxwell 28 demon` | you've found a paragraph funnier than mine. It goes in the README, with your name |

## An evening

| | start | done when |
|---|---|---|
| **Put your own dead physicist on a chip** | maxwell-on-a-chip: edit `books.txt`, run `./train.sh` | Darwin, Newton or Lovelace loops when cold and rambles when warm |
| **The first real thermometer** | maxwell-on-a-chip: an ESP32-S3, an OLED, an SHT40, `./flash.sh` | a photo or a video of the screen. Nobody has run it on hardware yet, me included |
| **Another display** | maxwell-on-a-chip: the SH1106 path in `firmware/maxwell/display.h` is untested | it works on a 1.3" panel |
| **A new thing to draw** | esp32-ai: one family in `research/oled/gen.py` (a shape, an animation) | the retrained model draws it and the interpreter check still passes |
| **Your steering method on SteerBench** | [steering-mechanics/steerbench](https://github.com/moudrkat/steering-mechanics/tree/main/steerbench) | a row in the table, with your method's name on it |

## A real project

| | start | done when |
|---|---|---|
| **Is post-training a refrigerator?** | maxwell-on-a-chip: fine-tune the model toward coherent sentences, then repeat `measure.py` | the entropy-against-temperature curve of the tuned model, next to the original. My guess: it shifts right. I have not measured it |
| **Strength relative to the activation** | [hotwire-vllm](https://github.com/moudrkat/hotwire-vllm): today the vector has a fixed scale; some benchmarks need `alpha × the token's own norm` | it passes `hotwire.verify` and doesn't slow the unsteered path |
| **A read operation in hotwire** | hotwire-vllm: it writes into the residual stream but cannot read from it | activations of chosen layers come back with the response, CUDA graphs still on |
| **A probe of your own, live** | [brainscope](https://github.com/moudrkat/brainscope): the "Bring your own" section of its README | your probe shows up in the lens on your app's real traffic |
| **Does a direction act as a switch on small models?** | on a 4M model that writes programs, adding a direction to the finished model didn't move behaviour gradually: nothing, nothing, then a different program. Is that the model's size, or the task? | the same measurement on one other small model. The code comes with the robot repo, soon |

## If you get stuck

Open an issue and say where. I answer within a day. The first outside PR was merged and released the next morning.
