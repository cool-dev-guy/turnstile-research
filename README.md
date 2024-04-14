# turnstile-research
A study on cloudflare turnstile.Proof of concept.

# reversing.

- On starting from the root,The cloudflare's final useful function is the `rr()` function.because it assigns the `l.response`(what we need) to the `cl-cloudflare` widget.
- Reversing it,we can find a function `i(a,b,c)` with parameters `(l,widget_name,boolean)` the boolean is flase for `succuess` of the challenge.
  * what is `l` ,its one of the most important variable,which almost have every data about the key and its logging and benchmarks.
- On further investigation we can find a sitch case 
  where we can see `a.response = n.token;`,so now we understood that `n.token` has the `token`
