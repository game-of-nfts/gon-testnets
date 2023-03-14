# Table of Task Flows

## Explanation

**Flow**

i --(1)--> s means that you transfer an NFT from IRISnet(i) to Stargaze(s) through channel is-1(si-1). Check the channel table to find what is-1 represents.

**Id**

Each different flow has a unique id. In task we use flow-id to refer to a flow we want participants to follow and transfer NFT.

**Style**

Never-go-back: No class-id prefix removal during the transfer flow (i.e. i --(1)--> s --(2)--> i ). This means when transferring the NFT back to iris from stargaze through is-2, it will result in a new Collection created on iris, even though the NFT is back on iris.

Revisit:  At least one class-id prefix removal during the transfer flow (i.e. i --(1)--> s --(1)--> j --(1)--> s --(2)--> i ). For example, when transferring the NFT back to stargaze from juno through js-1, there’s no new Collection created on stargaze. Hence a removal happened.

Backtrack:  All class-id prefixes are finally removed in the transfer flow (i.e. i --(1)--> s --(1)--> i ). The original NFT on iris is back and unlocked.
		

## Flow Table for Stage 2

| Flow Id | Style         | Flow                                                                |
|---------|---------------|---------------------------------------------------------------------|
| a1      | never-go-back | i --(1)--> s --(1)--> j --(1)--> i                                  |
| a2      | never-go-back | i --(1)--> u --(1)--> o --(1)--> i                                  |
| a3      | never-go-back | i --(1)--> s --(1)--> j --(1)--> u --(1)--> i                       |
| a4      | never-go-back | i --(1)--> s --(1)--> o --(1)--> j --(1)--> i                       |
| a5      | never-go-back | i --(1)--> s --(1)--> j --(1)--> u --(1)--> o --(1)--> s --(1)--> i |
| a6      | never-go-back | i --(1)--> o --(1)--> s --(1)--> u --(1)--> o --(1)--> j --(1)--> i |
| b1      | revisit       | i --(1)--> s --(1)--> u --(1)--> s --(2)--> i                       |
| b2      | revisit       | i --(1)--> u --(1)--> o --(1)--> u --(2)--> i                       |
| b3      | revisit       | i --(1)--> j --(1)--> u --(1)--> j --(2)--> i                       |
| b4      | revisit       | i --(1)--> j --(1)--> s --(1)--> j --(2)--> i                       |
| c1      | backtrack     | i --(1)--> s --(1)--> j --(1)--> s --(1)--> i                       |
| c2      | backtrack     | i --(1)--> o --(1)--> u --(1)--> o --(1)--> i                       |
| c3      | backtrack     | i --(1)--> s --(1)--> j --(1)--> u --(1)--> j --(1)--> s --(1)--> i |
| c4      | backtrack     | i --(1)--> u --(1)--> s --(1)--> o --(1)--> s --(1)--> u --(1)--> i |


## Flow Table for Stage 3

| Flow Id | Style         | Flow                                                     |
|---------|---------------|----------------------------------------------------------|
| f1      | never-go-back | i --(1)--> s --(1)--> j --(1)--> u --(1)--> o --(1)--> i |
| f2      | never-go-back | i --(1)--> s --(1)--> j --(1)--> u --(1)--> o --(2)--> i |
| f3      | never-go-back | i --(1)--> s --(1)--> j --(1)--> u --(2)--> o --(1)--> i |
| f4      | never-go-back | i --(1)--> s --(1)--> j --(1)--> u --(2)--> o --(2)--> i |
| f5      | never-go-back | i --(1)--> s --(1)--> j --(2)--> u --(1)--> o --(1)--> i |
| f6      | never-go-back | i --(1)--> s --(1)--> j --(2)--> u --(1)--> o --(2)--> i |
| f7      | never-go-back | i --(1)--> s --(1)--> j --(2)--> u --(2)--> o --(1)--> i |
| f8      | never-go-back | i --(1)--> s --(1)--> j --(2)--> u --(2)--> o --(2)--> i |
| f9      | never-go-back | i --(1)--> s --(2)--> j --(1)--> u --(1)--> o --(1)--> i |
| f10     | never-go-back | i --(1)--> s --(2)--> j --(1)--> u --(1)--> o --(2)--> i |
| f11     | never-go-back | i --(1)--> s --(2)--> j --(1)--> u --(2)--> o --(1)--> i |
| f12     | never-go-back | i --(1)--> s --(2)--> j --(1)--> u --(2)--> o --(2)--> i |
| f13     | never-go-back | i --(1)--> s --(2)--> j --(2)--> u --(1)--> o --(1)--> i |
| f14     | never-go-back | i --(1)--> s --(2)--> j --(2)--> u --(1)--> o --(2)--> i |
| f15     | never-go-back | i --(1)--> s --(2)--> j --(2)--> u --(2)--> o --(1)--> i |
| f16     | never-go-back | i --(1)--> s --(2)--> j --(2)--> u --(2)--> o --(2)--> i |
| f17     | never-go-back | i --(2)--> s --(1)--> j --(1)--> u --(1)--> o --(1)--> i |
| f18     | never-go-back | i --(2)--> s --(1)--> j --(1)--> u --(1)--> o --(2)--> i |
| f19     | never-go-back | i --(2)--> s --(1)--> j --(1)--> u --(2)--> o --(1)--> i |
| f20     | never-go-back | i --(2)--> s --(1)--> j --(1)--> u --(2)--> o --(2)--> i |
| f21     | never-go-back | i --(2)--> s --(1)--> j --(2)--> u --(1)--> o --(1)--> i |
| f22     | never-go-back | i --(2)--> s --(1)--> j --(2)--> u --(1)--> o --(2)--> i |
| f23     | never-go-back | i --(2)--> s --(1)--> j --(2)--> u --(2)--> o --(1)--> i |
| f24     | never-go-back | i --(2)--> s --(1)--> j --(2)--> u --(2)--> o --(2)--> i |
| f25     | never-go-back | i --(2)--> s --(2)--> j --(1)--> u --(1)--> o --(1)--> i |
| f26     | never-go-back | i --(2)--> s --(2)--> j --(1)--> u --(1)--> o --(2)--> i |
| f27     | never-go-back | i --(2)--> s --(2)--> j --(1)--> u --(2)--> o --(1)--> i |
| f28     | never-go-back | i --(2)--> s --(2)--> j --(1)--> u --(2)--> o --(2)--> i |
| f29     | never-go-back | i --(2)--> s --(2)--> j --(2)--> u --(1)--> o --(1)--> i |
| f30     | never-go-back | i --(2)--> s --(2)--> j --(2)--> u --(1)--> o --(2)--> i |
| f31     | never-go-back | i --(2)--> s --(2)--> j --(2)--> u --(2)--> o --(1)--> i |
| f32     | never-go-back | i --(2)--> s --(2)--> j --(2)--> u --(2)--> o --(2)--> i |