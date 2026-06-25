# Houdini_Fast_Tools
Space with day to day houdini tools 

### this space is for the Super_Split tool
https://github.com/AdriDevVfx/Houdini_Fast_Tools/tree/main/Super_Split

add a new tool to your shelf 
![image](https://github.com/user-attachments/assets/9282fa06-5811-4870-b595-ecb99863e5f6)

![image](https://github.com/user-attachments/assets/5775742e-9045-4647-8c0e-3370e4163e74)

enjoy it =)
float seed = vertexColor.r;

float speedX = lerp(0.8, 2.3, frac(seed * 13.7));
float speedZ = lerp(0.5, 1.9, frac(seed * 27.3));

float ampX = lerp(0.01, 0.04, frac(seed * 51.2));
float ampZ = lerp(0.01, 0.05, frac(seed * 89.1));

float phaseX = seed * 17.123;
float phaseZ = seed * 43.891;

float x =
    sin(Time * speedX + phaseX) +
    0.5 * sin(Time * speedX * 2.7 + phaseX * 1.8);

float z =
    cos(Time * speedZ + phaseZ) +
    0.5 * cos(Time * speedZ * 3.1 + phaseZ * 2.3);

pos.x += x * ampX;
pos.z += z * ampZ;
