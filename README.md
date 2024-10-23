---
title: Benchlm
emoji: 👀
colorFrom: gray
colorTo: indigo
sdk: static
pinned: false
license: apache-2.0
short_description: llm benchmarks
---
TESTS:
   KNOWLEDGE:
      TQA - Truthful QA
      JEOPARDY - 100 Question JEOPARDY quiz
   LANGUAGE:
      LAMBADA - Language Modeling Broadened to Account for Discourse Aspects
   UNDERSTANDING:
      WG - Winogrande
      BOOLQ - Boolean questions
      STORYCLOZE - Story questions
      OBQA - Open Book Question / Answer
      SIQA - Social IQ
      RACE - Reading comprehension dataset from examinations
      MMLU - massive multitask language understanding
      MEDQA - medical QA
   REASONING
      CSQA - Common Sense Question Answer
      COPA - Choice of Plausible Alternatives
      HELLASWAG - Hella Situations with Adversarial Generations
      PIQA - Physical Interaction: Question Answering
      ARC - A12 Reasoning Challenge
      AGIEVAL - AGIEval logiqa, lsat, sat
      AGIEVALC  - Gaokao SAT, logiqa, jec (Chinese)
      MUSR - Multimodal Semantic Reasoning
   COT:
      GSM8K - Grade School Math CoT
      BBH  - Beyond the Imitation Game Bench Hard CoT
      MMLUPRO - massive multitask language understanding pro CoT
      AGIEVAL - satmath, aquarat
      AGIEVALC  - mathcloze, mathqa (Chinese)
      MUSR - Multimodal Semantic Reasoning
      APPLE - 100 custom Apple Questions
   CODE:
      HUMANEVAL - Python
      HUMANEVALP - Python, extended test
      HUMANEVALX - Python, Java, Javascript, C++
      MBPP - Python
      MBPPP - Python, extendend test
      CRUXEVAL - Python
      USE {TEST}FIM FOR FIM TEST, i.e. HUMANEVAL->HUMANEVALFIM

    METHODOLOGY: All CoT tests are zero shot.
                 All MC tests do two queries, 1 with answers in test order and 2nd with answers circularly shifted 1.
                 To score a correct answer in MC both queries must answer correctly.
                 Winogrande using logprob completion (evaluates the probability of a common completion for the two possible cases).
                 Tests are run using a modified llama.cpp server (supporting logprob completion mode) and/or textsynth server where noted.

TEST       |  MODELA   |  MODELB 
-----------|-----------|--------
WINOGRANDE |   1.0     |   0.5

