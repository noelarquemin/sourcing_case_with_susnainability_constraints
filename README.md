# sourcing_case_with_susnainability_constraints
🏭 Strategic Sourcing Optimization: Cost vs. Resilience MILP ModelIntroductionThis repository presents a Mixed-Integer Linear Programming (MILP) model designed to solve a critical Strategic Sourcing challenge: finding the minimum total cost of procurement while adhering to strict sustainability (CO2) and risk management constraints.

This project demonstrates the application of Advanced Analytics (as discussed by IBM and industry leaders) to automate complex trade-off decisions, moving beyond tactical price negotiation to genuine supply chain strategy.

🎯 Strategic ObjectiveThe model's primary goal is to Minimize Total Sourcing Cost ($$\text{Cost}_{\text{Fixed}} + \text{Cost}_{\text{Variable}} + \text{Cost}_{\text{Shipping}}$$) subject to:Demand Fulfillment: All market demands must be met.Capacity Limits: Suppliers cannot exceed their production capacity.
Sustainability Constraint: Total CO2 emissions must remain below a pre-defined global limit.Binary Selection: Deciding which suppliers to onboard, thus incurring a large fixed cost (a core MILP component).

🚀 Key TechnologiesTechnologyRole in Strategic SourcingPythonCore implementation language.PuLPPowerful open-source library used to formulate and solve the MILP problem.Pandas/Matplotlib/SeabornData manipulation and professional visualization of the optimal sourcing strategy.

📁 Repository Structure.
├── src/
│   └── sourcing_optimizer.py  # The main MILP code and solver logic
├── README.md                  # Project overview
└── results/
    └── optimal_allocation.png # Output visualization (example)
    
📊 Case Study: Global T-Shirt ProcurementWe model a company sourcing 20,000 units for two markets (Europe and Asia) from three distinct suppliers, each with unique cost, capacity, and CO2 profiles.
Example Scenario Results (Optimal Solution)The model determines the flow that respects the Maximum CO2 Limit ($15,000$ kg), leading to the following strategic decisions:

MetricResultStrategic ImplicationOptimal Total Cost$286,000.00Minimum cost achieved under all constraints.Actual CO2 Emission$13,600.00$ kgThe model successfully enforced the sustainability target.Supplier India (High CO2)NOT SELECTEDThe fixed cost of $50,000 was avoided, and the high $\text{CO}_2$ unit cost was prohibitive under the constraint.

Sourcing AllocationGermany to Asia ($8,000$ units), USA to Europe ($12,000$ units).Diversified sourcing network built for resilience and optimal cost.💻 How to Run the 
Install Dependencies:Bashpip install pulp pandas matplotlib seaborn

Execute the script:Bashpython src/sourcing_optimizer.py

The script will print the numerical output to the console and generate the professional visual allocation chart.💡 Strategic TakeawayThis project confirms that pure Cost 

Minimization (tactical sourcing) often fails to meet corporate goals for sustainability and risk. The MILP model provides the quantitative backing needed by a Strategic Buyer to justify spending more ($ \text{vs. the lowest theoretical cost}$) to achieve a robust and ethically compliant supply chain.
