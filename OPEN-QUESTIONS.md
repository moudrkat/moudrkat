# Open questions: what would you use this for?

I build these things because I want them myself. What I don't know is what *you* would do with them.
So this page is mostly questions, with my own guesses under each. Try one, and tell me where it broke or what you
wished it did. An issue is enough. A PR is better.

## Looking inside a model: [brainscope](https://github.com/moudrkat/brainscope)

```
pip install brainscope && brainscope --model tiny
```

Then point your app at it instead of your usual endpoint, and watch.

- **What does your model do that you can't explain?** That is the question I most want answered. Tell me what it was,
  and whether the lens showed you anything.
- **My guesses at what it is good for:** why an agent picked the wrong tool; whether your system prompt still counts
  after a long chat; whether a fine-tune changed what you think it changed. Try one of them on your own app.
- **Train something of your own:** a probe. `POST /probes/train` builds one from two contrasting personas ("Probes" in
  the README), and [hidden-intent](https://github.com/moudrkat/hidden-intent) is a worked example on a coding model.

## A decision model in a phone: [kneejerk](https://github.com/moudrkat/kneejerk), [probascope](https://github.com/moudrkat/probascope), [decide-me](https://github.com/moudrkat/decide-me)

A decision model doesn't write. It picks one of the options you give it, in one forward pass, and that fits in a phone.

- **What would you let a phone decide without asking a server?**
- **My guesses:** sorting what just arrived, offline; a yes or no before you bother a big model; anything where the
  data should not leave the device.
- **Start:** "Try it in five minutes" in kneejerk. probascope is the same thing as an Android app, with a look at
  where in the layers the answer formed.

## A model on a chip: [esp32-ai](https://github.com/moudrkat/esp32-ai)

A 3M-parameter model on an ESP32-S3 turns your sentence into a small program, and the same chip runs it. No network.

- **What should a chip that costs less than lunch understand without a network?**
- **My guesses:** a device you can tell what to do instead of learning its three buttons; a toy; a lab instrument that
  takes a sentence.
- **Talk to it your way:** write 20 requests the way *you* would say them and tell me which ones it got wrong. My own
  test sentences are too polite.
- **Train your own:** the model is trained from scratch on generated pairs of request and program. Add a family of
  your own in `research/oled/gen.py` and retrain ("Run it yourself" in the README).

## Steering in production: [hotwire-vllm](https://github.com/moudrkat/hotwire-vllm)

hotwire steers a model per request inside vLLM, with CUDA graphs on. **I want it running in somebody's production.**

- **You run vLLM?** `pip install hotwire-vllm`, run "Verify on your hardware" from the README, and send me the numbers.
- **Something stops you from shipping it?** That is the issue I want most.
- **Known gaps, if you'd rather build:** a strength relative to the token's own norm, and a read operation next to the
  write.

## Where did you use a local model?

Not a task. If you run a model locally in something real (a phone, a chip, a laptop that isn't allowed to phone home),
write me what it does and why it had to be local.

## If you get stuck

Open an issue and say where. I answer within a day. The first outside PR was merged and released the next morning.

The idea of keeping a list like this is Neel Nanda's
([200 Concrete Open Problems in Mechanistic Interpretability](https://www.alignmentforum.org/s/yivyHaCAmMJ3CqSyj)).
