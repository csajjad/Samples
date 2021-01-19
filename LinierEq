import pandas as pd
import numpy as np

vector_a=pd.read_excel("linear.xlsx",sheet_name="vector_a")

vector_b=pd.read_excel("linear.xlsx",sheet_name="vector_b")
vector_a_inv = pd.DataFrame(np.linalg.pinv(vector_a.values), vector_a.columns,vector_a.index)

vector_c=vector_a_inv.dot(vector_b)
with pd.ExcelWriter('linear.xlsx', engine='openpyxl', mode='a') as writer:  
     vector_c.to_excel(writer,sheet_name="Result")
