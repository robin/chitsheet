--- 
as3_formulas: |-
  CONVERT RADIANS TO DEGREES AND DEGREES TO RADIANS
  radians = degrees * Math.PI / 180
  degrees = radians * 180 / Math.PI
  
  ROTATE TO THE MOUSE (OR ANY POINT)
  dx = mouseX - sprite.x;
  dy = mouseY - sprite.y;
  sprite.rotation = Math.atan2(dy, dx);
  
  GET THE DISTANCE BETWEEN TWO POINTS
  dx = x2 - x1;
  dy = y2 - y1;
  dist = Math.sqrt(dx*dx + dy*dy);
  
  CONVERT ANGULAR VELOCITY TO X, Y VELOCITY
  vx = speed * Math.cos(angle);
  vy = speed * Math.sin(angle);
  
  CONVERT ANGULAR ACCELERATION (ANY FORCE ACTING ON AN OBJECT) TO X, Y ACCELERATION
  ax = force * Math.cos(angle);
  ay = force * Math.sin(angle);
  
  ADD ACCELERATION TO VELOCITY
  vx += ax;
  vy += ay;
  
  ADD VELOCITY TO POSITION
  sprite.x += vx;
  sprite.y += vy;
