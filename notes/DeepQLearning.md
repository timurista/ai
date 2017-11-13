## Experience Replay
car has same wall, etc.

but sensor input
similar vectors, car will learn very well for this model of the world.

You need a neural network to readjust to the world.

In environemnt, we don't want patterns in natur to bias our understanding.
COrrelated or interdependent

We use states
    Experience REplay
    Memory of Agent once reaches a certain threshold
    randomly selects uniformly distrubted sample from batch of experiences then goes through and learns from them

## Exeprience Replay
    1. state
    2. actions
    3. rewards
    4. 
Sometimes rare experiences can be helpful
    but you need LONG TERM memory
    you can organize batch as rolling window

### advantage
    1) save rare expereinces
    2) stops sequentail 
    3) More experiences you can learn from... possibly faster.

## Selecting Q Values
    How do you know which one?
    why not take BEST qvalue

We can use softmax function, or e-greedy, e-soft and Softmax.

Why do we have differnt type?
    exploration vs exploitation?
    q2 is best --> agent must go and explore

Agent get's stuck
    agent might in up in localied max, because it hasn't kept walking to find a better result
        it is just going to keep taking the same action even though there might be somehting better out there

    Never want to start exploring,
        you want to keep learning
        so does agent

## episolon-greedy
selects one with best qvalue, highest qvalue expect for epsioln percent of time. so 90% you select best of the time, but 10% you will take another action, Greedily selecting best action, but not that episolon part of the time

## More advanced version
    Softmax in our examples

tutorial on annex #2 where we talk about the concept
    convultion nueral networks
        -- in next section we are going to use them in the next part


How softmax works
`f_j(z) = (e ^z_j) / SUM k (e^z_k)`
it will squash them and values will add to 1
what happens is you select best q values, but they are actual values
    we get 0.05, 0.90
    ... we get everything form 0 -> 1.0
    so we get probabilities
    most natural way to apply softmax is to use this probabilities for how often we will take those actions

softmax best action will have highest probability, but 5% of time we take q2, q3.
    so it gets better and better and probabilities will change higher and higher

Not just randomly selecting action
    we are doing it based on q-values explored
    we are not using epsilon
        vbde, epsilon greedy algorithm
        adjust value based on state it is in


