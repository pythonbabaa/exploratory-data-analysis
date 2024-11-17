git clone https://github.com/yourusername/repository-name.git
cd repository-name
pip install -r requirements.txt
/home/a/Desktop/user_data.csv
import numpy as np
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
user_data = pd.read_csv('/home/a/Desktop/user_data.csv')
user_data.describe()
user_data = user_data.drop(['user_ID', 'user_level'], axis=1)
user_data = user_data.rename(columns={'first_order_month': 'first_month_order'})
sns.boxplot(x=user_data['purchase_power'])
plt.figure(figsize=(20,10))
c= user_data.corr()
sns.heatmap(c, cmap='BrBG', annot=True)
