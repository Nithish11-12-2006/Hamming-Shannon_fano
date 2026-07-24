# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.4 , 0.19 , 0.16 , 0.15 , 0.15} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
google colab software

# Program:
```
import math

# Probabilities given
p = [0.4,0.19,0.16,0.15,0.15]
# Corresponding Huffman/Shannon-Fano code lengths
lk = [1,3,3,3,3]
n = len(p)

# Average Codeword Length
L = sum(p[k] * lk[k] for k in range(n))

# Entropy
hs = sum(p[k] * math.log(1 / p[k], 2) for k in range(n))
hs = round(hs, 3)

# Efficiency & Redundancy
eff = round(hs / L, 3)
red = round(1 - eff, 3)

# Variance of codeword length
var = sum(p[k] * (lk[k] - L) ** 2 for k in range(n))
var = round(var, 3)

print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff * 100}%")
print(f"Redundancy is : {red}")
print(f"Variance is : {var}")
```
# Calculation:
Compare the manually calculated value and the observed practical value.
<img width="916" height="1436" alt="image" src="https://github.com/user-attachments/assets/b983bc50-7761-4195-9623-128ce019c53c" />

<img width="916" height="1496" alt="image" src="https://github.com/user-attachments/assets/21be9826-ffb0-4d5a-a773-165ed84dda2d" />

<img width="1600" height="716" alt="image" src="https://github.com/user-attachments/assets/ae4a0223-b3f0-4d3c-8ad5-97096608526e" />


# Output

<img width="420" height="139" alt="image" src="https://github.com/user-attachments/assets/10dd9ad2-0b99-4cd7-b938-4af2b9ce3b5f" />


# Results:

For the given probabilities 0.4 , 0.19 , 0.16 , 0.15 , 0.15 Average Codeword Length is : 2.35 Entropy is : 2.228 Efficiency is : 94.8 % Redudancy is : 0.052 Variance is : 1.004

