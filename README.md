# wills_control_flow
control_flow_for_shipping 
#cost for ground shipping 
weight = 1.5
drone_weight = 1.5
cost = 0 
d_cost = 0
"""control flow to calculate shipping cost 
which is calculated by weight * price per pound + flat charge"""
if weight <= 2:
  cost = 1.50 * weight + 20 
elif (weight > 2) and (weight <= 6):
  cost = 3.0 * weight + 20
elif (weight > 6) and (weight <= 10):
  cost = 4.0 * weight + 20
elif (weight > 10):
  cost = 4.75 * weight + 20
else:
  cost = 125 
#cost for drone shipping 
if drone_weight <= 2:
  d_cost = 4.50 * weight
elif (drone_weight > 2) and (drone_weight <= 6):
  d_cost = 9.0 * weight 
elif (drone_weight > 10):
  d_cost = 14.25 * weight 
  

# the price comparison 
print("for a drone delivery you are looking at " + "$ " + str(d_cost) + " for " + str(drone_weight) + " pounds." )
print('for ground shipping you are looking at' + "$" + str(cost) + " for " + str(weight) + "pounds.")
if cost > d_cost:
  print("ground shipping is therfor cheaper")
elif cost == d_cost:
  print("The costs are the same")
elif cost < d_cost:
  print("The drone is cheaper")
