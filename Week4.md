
def MonteCarl(TRIES): <br/>
    num_in_area = 0<br/>
   
    for _ in range(TRIES):<br/>
        x = random.uniform(0, 1)<br/>
        y = random.uniform(0, 1)<br/>
       
        if y <= -x**2 + 1:<br/>
            num_in_area += 1<br/>
   
    shadow_area = num_in_area / TRIES<br/>
    return shadow_area<br/>
