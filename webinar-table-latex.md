---
layout: none
comment: this is pretty close to raw latex
---
<pre>
\begin{tabular{lp{4in}}
  \hline
  \textbf{Date} & \textbf{\emph{Title}, Presenter(s)} \\
  \hline
{% for webinar in site.posts %}
  {{ webinar.date | date: "%F" }} & 
    {% raw %}\emph{{% endraw %}{{ webinar.title}},{% raw %}}{% endraw %} {{ webinar.author }} \\
  {% endfor %}
  \hline
\end{tabular}
</pre>