---
layout: none
comment: this is pretty close to raw latex
---
{% assign archive_base = "https://ideas-productivity.org/events/hpc-best-practices-webinars/\#webinar" %}
<pre>
\begin{table}
\begin{tabular}{lp{0.85\textwidth}}
  \hline
  \textbf{Date} & \textbf{\emph{Title}, Presenter(s)} \\
  \hline
{% for webinar in site.webinars %}
  {% capture seqnum %}{{ webinar.webinar-id | prepend: "00" | slice: -3, 3 }}{% endcapture %}
  {{ webinar.date | date: "%F" }} & 
    {% raw %}\emph{\href{{% endraw %}{{ archive_base }}{{ seqnum }}{% raw %}}{{% endraw %}{{ webinar.title}}{% raw %}}}{% endraw %}, {{ webinar.author }} \\
  {% endfor %}
  \hline
\end{tabular}
\end{table}
</pre>
