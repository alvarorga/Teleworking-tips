# To launch remote jobs.
  
* Use tmux if it will take a long time. Open tmux, start the job and dettach the session with Ctrl+b d. You can always log latter into that session using `tmux attach`.

* Schedule jobs with the `at` command. Write: `at now + 2 minute`, then write all commands you want to execute, then press Ctrl+D. Other time options are: `at now + 3 hour`, `at 9:15 AM`, ...

* Schedule a lengthy job to be run in a tmux session: combine the previous two tricks. Use `at` and schedule it to open a tmux session that will automatically detach with your job inside. For example:
`tmux new-session -d -s my_session 'julia helloworld.jl'`

# To access journal articles through your academic institution with ssh

* `ssh institution_address 'wget -O- article_address' >> pdf_name`

## Different journal addresses:

* For APS (PRL, PRB, ...): susbsitute "abstract" by "pdf" in the article's webpage.

* For IOP: append "/pdf" at the end of the article's webpage.

* For Nature: append ".pdf" at the end of the article's webpage.
