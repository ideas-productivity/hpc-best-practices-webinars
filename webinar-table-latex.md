---
layout: default
---
<pre>
\begin{tabular{lp{4in}}
  \hline
  \textbf{Date} & \textbf{\emph{Title}, Presenter(s)} \\
  \hline
{% for webinar in site.posts %}
  {{ webinar.date | date: "%F %I:%M %P %Z" }} & 
    {% raw %}\emph{{% endraw %}{{ webinar.title}},{% raw %}}{% endraw %} {{ webinar.author }} \\
  {% endfor %}
  \hline
\end{tabular}
