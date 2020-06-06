A boutique brewery has two warehouses from which it distributes beer to five carefully chosen bars.
At the start of every week, each bar sends an order to the brewery’s head office for so many crates
of beer, which is then dispatched from the appropriate warehouse to the bar.

The brewery would like to have an interactive computer program which they can run week by week to
tell them which warehouse should supply which bar so as to minimize the costs of the whole operation. 
For example, suppose that at the start of a given week the brewery has 1000 cases at warehouse A, 
and 4000 cases at warehouse B, and that the bars require 500, 900, 1800, 200, and 700 cases respectively.
Which warehouse should supply which bar?

The model is formulated as an integer program using PulP

data_file.txt - use this file to change input parameters to the model

The data is structured in the following format - 
row1 - number_of_warehouses = n
row2 - number_of_custormes = m
row3 - supply_at_w_1	supply_at_w_2   ... supply_at_w_n
row4 - demand_cust_1	demand_cust_2	... demand_cust_m
row5 - cost of transport from warehouse 1 to all customers
row6 - cost of transport from warehouse 2 to all customers
.
.
(add rows for all warehouses till n warehouses) 
row7 - upper limit on transport arcs from warehouse1 to all customers
row8 - upper limit on transport arcs from warehouse2 to all customers
.
.
(add rows for all warehouses till n warehouses) 
row9 - lower limit on transport arcs from warehouse1 to all customers
row10 - lower limit on transport arcs from warehouse2 to all customers
.
.
(add rows for all warehouses till n warehouses) 

To add more warehouses, just keep adding approprite parameters

Just run all the cells from optimization_model.ipynb once you once you have
updated your parameters.