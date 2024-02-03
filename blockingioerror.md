```
2022-01-28 14:22:29,196 ERROR app uWSGIWorker40Core0 : Exception on /index [GET]                       
Traceback (most recent call last):                                                                     
  File "/home/agora/agora-server/venv/lib/python3.7/site-packages/flask/app.py", line 2447, in wsgi_app
    response = self.full_dispatch_request()                                                            
  File "/home/agora/agora-server/venv/lib/python3.7/site-packages/flask/app.py", line 1952, in full_disp
atch_request                                                                                           
    rv = self.handle_user_exception(e)                                                                 
  File "/home/agora/agora-server/venv/lib/python3.7/site-packages/flask_cors/extension.py", line 165, in
 wrapped_function                                                                                      
    return cors_after_request(app.make_response(f(*args, **kwargs)))                                   
  File "/home/agora/agora-server/venv/lib/python3.7/site-packages/flask/app.py", line 1821, in handle_us
er_exception                                                                                           
    reraise(exc_type, exc_value, tb)                                                                   
  File "/home/agora/agora-server/venv/lib/python3.7/site-packages/flask/_compat.py", line 39, in reraise
    raise value                                                                                        
  File "/home/agora/agora-server/venv/lib/python3.7/site-packages/flask/app.py", line 1950, in full_disp
atch_request                                                                                           
    rv = self.dispatch_request()                                                                       
  File "/home/agora/agora-server/venv/lib/python3.7/site-packages/flask/app.py", line 1936, in dispatch_
request                                                                                                
    return self.view_functions[rule.endpoint](**req.view_args)                                         
  File "./app/agora.py", line 100, in node                                                             
    auto_pull_nodes=n.auto_pull_nodes() if current_app.config['ENABLE_AUTO_PULL'] else [],             
  File "./app/db.py", line 269, in auto_pull_nodes                                                     
    nodes = [node for node in nodes if node not in self.pull_nodes() and node.uri not in banned_nodes] 
  File "./app/db.py", line 269, in <listcomp>                                                          
    nodes = [node for node in nodes if node not in self.pull_nodes() and node.uri not in banned_nodes] 
  File "./app/db.py", line 254, in pull_nodes                                                          
    nodes.extend(subnode.pull_nodes())                                                                 
  File "./app/db.py", line 558, in pull_nodes                                                          
    print(f'in pull_nodes for {self.uri}')                                                             
BlockingIOError: [Errno 11] write could not complete without blocking  

```