
Markov Decision Processes (MDPs) handle uncertainty in decision-making in several key ways, differentiating them from deterministic models: </br>
Handling Uncertainty in MDPs</br>
Stochastic transitions: MDPs model the uncertainty of action outcomes through probabilistic state transitions13. Unlike deterministic models where actions lead to fixed outcomes, MDPs allow for multiple possible next states, each with an associated probability.</br>
Reward uncertainty: While rewards are typically defined as deterministic functions in basic MDPs, extensions like uncertain MDPs can incorporate reward uncertainty4.</br>
Policy optimization: MDPs aim to find optimal policies that maximize expected cumulative rewards over time, accounting for the inherent uncertainty in state transitions3.</br>
Long-term planning: By considering future states and rewards through value functions, MDPs enable decision-making that accounts for long-term uncertainties3.</br>
Impact of Discount Factor γ</br>
The discount factor γ in MDPs significantly affects the agent's behavior:</br>
γ close to 0: The agent becomes myopic, focusing primarily on immediate rewards.</br>
γ close to 1: The agent values future rewards almost as much as immediate ones, leading to more far-sighted behavior.</br>
γ = 0: The agent only considers immediate rewards, ignoring future consequences.</br>
γ = 1: In infinite horizon problems, this can lead to infinite expected returns. In practice, it's often used for finite horizon or episodic tasks2</br></br>
Value Functions in MDPs</br>
Value functions are central to solving MDPs:</br>
State-value function V(s): Represents the expected cumulative discounted reward starting from state s and following the current policy.</br>
Action-value function Q(s,a): Represents the expected cumulative discounted reward starting from state s, taking action a, and then following the current policy.</br>
Optimal value functions: V* and Q* represent the maximum achievable values under any policy.</br>
Bellman equations: These recursive equations define the relationship between values of current and future states, forming the basis for many MDP solving algorithms3.</br>
Real-World MDP Scenario: Inventory Management</br>
Consider an inventory management system for a retail store:</br>
States (S): Inventory levels of a product (e.g., 0-100 units).</br>
Actions (A):</br>
Order more units (in various quantities)</br>
Don't order</br>
Rewards (R):</br>
Positive: Sales revenue</br>
Negative: Ordering costs, storage costs, stockout penalties</br>
Transition Probabilities (P):</br>
Probability of moving from one inventory level to another, based on:</br>
Uncertain demand (e.g., seasonal variations, market trends)</br>
Supply chain reliability (e.g., delivery delays)</br>
In this scenario, an MDP could optimize ordering decisions by balancing the trade-offs between maintaining sufficient stock, minimizing costs, and maximizing sales. The stochastic nature of customer demand and supply chain reliability is captured in the transition probabilities, making it a suitable problem for MDP modelin</br>
