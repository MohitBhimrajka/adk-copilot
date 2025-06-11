# Configurating Bidi-streaming behaviour - Agent Development Kit

**Source URL:** https://google.github.io/adk-docs/streaming/configuration/

---

# Configurating streaming behaviour[¶](#configurating-streaming-behaviour "Permanent link")

There are some configurations you can set for live(streaming) agents.

It's set by [RunConfig](https://github.com/google/adk-python/blob/main/src/google/adk/agents/run_config.py). You should use RunConfig with your [Runner.run\_live(...)](https://github.com/google/adk-python/blob/main/src/google/adk/runners.py).

For example, if you want to set voice config, you can leverage speech\_config.

```
voice_config = genai_types.VoiceConfig(
    prebuilt_voice_config=genai_types.PrebuiltVoiceConfigDict(
        voice_name='Aoede'
    )
)
speech_config = genai_types.SpeechConfig(voice_config=voice_config)
run_config = RunConfig(speech_config=speech_config)

runner.run_live(
    ...,
    run_config=run_config,
)

```