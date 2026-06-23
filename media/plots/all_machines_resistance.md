fig_all <- plot_ly(all_data, x = ~Machine, y = ~PartResistance, color = ~interaction(Pressure, Temperature), type = 'box')
