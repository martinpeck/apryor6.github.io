
# Bokeh Square Cross Glyph


```python
from bokeh.plotting import figure, output_file, show
from bokeh.models import Range1d
from bokeh.io import export_png

fill_color = '#BBBBBB'
line_color = 'black'
output_file("../../figures/square_cross.html")

p = figure(plot_width=400, plot_height=400)
p.square_cross(x=0,y=0,size=100, fill_alpha=1,fill_color=fill_color,
         line_alpha=1, line_color=line_color, line_dash='dashed', line_width=5)
p.square_cross(x=0,y=1,size=100, fill_alpha=0.8, fill_color=fill_color,
         line_alpha=1, line_color=line_color, line_dash='dotdash', line_width=8)
p.square_cross(x=1,y=0,size=100, fill_alpha=0.6, fill_color = fill_color,
         line_alpha=1, line_color=line_color, line_dash='dotted', line_width=13)
p.square_cross(x=1,y=1,size=100, fill_alpha=0.4, fill_color = fill_color,
         line_alpha=1, line_color=line_color, line_dash='solid', line_width=17)
p.x_range = Range1d(-0.5,1.5, bounds=(-1,2))
p.y_range = Range1d(-0.5,1.5, bounds=(-1,2))
show(p)
export_png(p, filename="../../figures/square_cross.png");
```
