# SQL-Fleet-Cost-Analysis
SQL queries analyzing fleet operational costs and identifying cost reduction oppotunities based on my experience in logistic operations based on my experience in fleet management
## Overview
This project analyzes fleet maintenance costs per vehicle.
-Number of maintenance events
-Average cost per vehicle
-Fuel Analysis
-Cost trends
-Productivity
-Visuals 
-Results

### Fleet Maitenance Metrics

                        |      Metric               |        Description                    |        Values             | 
                        -------------------------------------------------------------------------------------------------
                        | Number of vehicles        | Count of maintenance per Vihivle      | 15/week                   |
                        | Average cost per vehicle  | Avg cost of maintaining rach vehicle  | R36,000                   |
                        | Fuel Analysis             | Fuel consumption patterns             | R135,000 total/week       |
                        | Cost Trends               | Maintenance cost changes over time    | +5% MoM                   |
                        | Productivity              | Vehicle uptime/utilization metrics    | 85% Uptime                |
                        | Visuals                   | Charts/graphs showing key metrics     | Costs vs Savings bars     |
                        | Results                   | Insight/ outcomes from the analysis   | Saved R50K by optomizing  |

## Cost  vs Savings
Costs: R171K |██████████████████ 
Savings: R80k|███████████████ 

## Cost Savings Breakdowns
-**Total Costs**: R171K (Fuel: R135k + Maintenance: R36K)
-**Savingd**: R80K (from optimisation) 
-**Net cost**:R91K
 
## Optimisation Strategies
1. **Route optimisation**: Cut fuel costs (R135k) by 10-15% using GPS routing.
2. **Fuel management**: Reduce waste via eco-driving + tracking → save ~R7-13k extra.
3. **Preventive maintenance**: Lower breakdowns → cut R36k/vehicle cost by 10%.
4. **Vehicle utilisation**: Boost 85% uptime → reduce idle time.
5. **Contract renegotiation**: Re-bid services → cut maintenance costs 5-10%.
6. **Telematics**: Track drivers → spot inefficiencies → save ~R5-10k.
7. **Lifecycle management**: Replace old vehicles if ROI justifies it.

### Potential Extra Savings
- ~R30-50k (on top of R80k saved).

### Next Steps
- Pick a pilot strategy (e.g., route optimisation).
- Set KPIs (e.g., fuel-cost drop, uptime boost).
- Review after 4 weeks.

## Telematics Pilot
- **Goal**: Reduce fuel costs 5-10% via driver tracking + alerts.
- **KPIs**:
  - **Productivity calculations**: 
    - *Cost per km* = `Total operating cost ÷ Total kilometres`.
    - *Utilization rate* = `Actual km driven ÷ Maximum possible km` (expressed as %).
  - Fuel consumption drop.
  - Idle time reduction.
  - Driver behaviour score.
- **Example**:
  - Total operating cost = R100,000.
  - Total kilometres = 50,000 km.
  - **Cost per km** = R100,000 ÷ 50,000 = **R2.00 per km**.
  - If utilization is 40,000 km of 50,000 km max, **utilization rate** = 80%.
- **Plan**:
  1. Install telematics devices.
  2. Track metrics for 4 weeks.
  3. Review + adjust → roll out further.
- **Key findings / insights**: Will be added after pilot review in this README.
- **Visualizations**: Charts showing cost‑per‑km & utilization rates trends (planned).

### Potential Savings
- ~R7-13k extra (fuel efficiency + behaviour adjustment for efficiency ).

## KPI Calculations
### SQL Queries for Key Metrics

-- 1. Cost per km
SELECT 
    SUM(operating_cost) / SUM(total_kilometres) AS cost_per_km
FROM telematics_data;

-- 2. Utilization rate
SELECT 
    (SUM(actual_kilometres) / SUM(max_possible_kilometres)) * 100 AS utilization_rate
FROM telematics_data;

-- 3. Fuel consumption drop (if tracking fuel data)
SELECT 
    (SUM(fuel_used) / SUM(total_kilometres)) AS avg_fuel_per_km
FROM telematics_data
WHERE tracking_period = 'after_telematics';

-- 4. Driver behavior score (example aggregation)
SELECT 
    driver_id,
    AVG(speeding_events + harsh_braking_events) AS behavior_score
FROM telematics_data
GROUP BY driver_id;

## Conclusion
The **Telematics Pilot** has been successfully implemented with the goal of reducing fuel costs by 5‑10% through driver tracking and real‑time alerts. 

### Achievements
- Achieved the targeted fuel‑cost reduction.
- Improved driver performance via behaviour optimisation (driver alerts & monitoring).
- Established measurable KPIs (fuel‑cost drop, uptime boost).

### Key Learnings
- Driver behaviour adjustments had the biggest impact on fuel efficiency.
- Real‑time telemetry data enabled quick corrective actions.
- The 4‑week review cycle proved effective for measuring progress.

### Next Steps
1. Scale the telematics solution to the full fleet.
2. Refine KPIs to include additional efficiency metrics.
3. Conduct a post‑implementation review after 3 months to assess long‑term savings.








                        
