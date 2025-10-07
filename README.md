# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
data=pd.read_csv("titanic_dataset.csv")
df=pd.DataFrame(data)
print(df)

<img width="1219" height="686" alt="Screenshot (21)" src="https://github.com/user-attachments/assets/48f54f7d-fd2f-426e-bc2f-fd91ba67a41a" />


import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
data=pd.read_csv("titanic_dataset.csv")
df=pd.DataFrame(data)
print(df)
df.shape
(891,12)
df.set_index("PassengerId",inplace=True)
df
<img width="670" height="707" alt="Screenshot (22)" src="https://github.com/user-attachments/assets/49487217-1fc1-47e8-ae5d-b53f1c1a8192" />

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
data=pd.read_csv("titanic_dataset.csv")
df=pd.DataFrame(data)
print(df)
df.nunique()


<img width="592" height="576" alt="Screenshot (23)" src="https://github.com/user-attachments/assets/121efe8b-c9bb-4112-88db-2e1a02a359e4" />

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
data=pd.read_csv("titanic_dataset.csv")
df=pd.DataFrame(data)
print(df)
df['Sex'].value_counts()


<img width="775" height="697" alt="Screenshot (24)" src="https://github.com/user-attachments/assets/8c6a0d42-6293-452b-b5f9-a166c9c05afd" />


import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
data=pd.read_csv("titanic_dataset.csv")
df=pd.DataFrame(data)
print(df)
df.Survived.unique()

df.rename(columns={"Sex":"Gender"},inplace=True)
df

<img width="669" height="659" alt="Screenshot (25)" src="https://github.com/user-attachments/assets/5b0fe4f1-fdb2-4259-85d2-d9b9431f3ebb" />

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
data=pd.read_csv("titanic_dataset.csv")
df=pd.DataFrame(data)
print(df)
sns.countplot(data=df)

<img width="597" height="708" alt="Screenshot (26)" src="https://github.com/user-attachments/assets/8d7adaf9-0f30-4d75-81d9-f34820538a6e" />
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
data=pd.read_csv("titanic_dataset.csv")
df=pd.DataFrame(data)
print(df)
sns.countplot(x='Survived',hue="Sex",data=df)

<img width="698" height="753" alt="Screenshot (29)" src="https://github.com/user-attachments/assets/4696c0d1-0c1b-4e26-97a4-99dea3c14a87" />

mport pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
data=pd.read_csv("titanic_dataset.csv")
df=pd.DataFrame(data)
print(df)
sns.catplot(x="Survived",hue="Sex",data=df,kind='count')

<img width="428" height="554" alt="Screenshot (31)" src="https://github.com/user-attachments/assets/d8b28f48-e38d-4a0a-abea-d2d0c1a6aac8" />



import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
data=pd.read_csv("titanic_dataset.csv")
df=pd.DataFrame(data)
print(df)
sns.catplot(x='Survived',hue="Sex",data=df,kind='violin')



<img width="900" height="645" alt="Screenshot (32)" src="https://github.com/user-attachments/assets/676a834b-b4ae-42be-84a1-8c06580f61d2" />
<img width="639" height="467" alt="Screenshot (33)" src="https://github.com/user-attachments/assets/cdaf394a-641b-4c49-9a15-9395f77fdff1" />



import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
data=pd.read_csv("titanic_dataset.csv")
df=pd.DataFrame(data)
print(df)
sns.boxplot(data=df)



<img width="630" height="698" alt="Screenshot (34)" src="https://github.com/user-attachments/assets/be30ea08-ad7a-4a1a-8309-03d348e42155" />



import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
data=pd.read_csv("titanic_dataset.csv")
df=pd.DataFrame(data)
print(df)
df.boxplot(column='Survived',by='Sex')


<img width="654" height="706" alt="Screenshot (35)" src="https://github.com/user-attachments/assets/843aee8f-5688-49ed-a64e-071f3c2e4749" />


import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
data=pd.read_csv("titanic_dataset.csv")
df=pd.DataFrame(data)
print(df)
sns.scatterplot(data=df)


<img width="667" height="705" alt="Screenshot (36)" src="https://github.com/user-attachments/assets/596b43ab-a676-477d-b66a-d72d6f4f532b" />


import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
data=pd.read_csv("titanic_dataset.csv")
df=pd.DataFrame(data)
print(df)
sns.scatterplot(x=df['Age'],y=df['Fare'])


<img width="546" height="718" alt="Screenshot (37)" src="https://github.com/user-attachments/assets/d78a1a79-3345-4859-af10-84db9f1ea5ec" />



import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
data=pd.read_csv("titanic_dataset.csv")
df=pd.DataFrame(data)
print(df)
sns.jointplot(x='Age',y='Fare',data=df)


<img width="335" height="611" alt="Screenshot (38)" src="https://github.com/user-attachments/assets/e1bf2a34-5843-441a-a7be-3329b062747e" />



import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
data=pd.read_csv("titanic_dataset.csv")
df=pd.DataFrame(data)
print(df)
sns.jointplot(x='Age',y='Fare',data=df,kind='kde')


<img width="462" height="601" alt="Screenshot (39)" src="https://github.com/user-attachments/assets/303811be-67e0-4abd-a23d-57488c6f0498" />



import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
data=pd.read_csv("titanic_dataset.csv")
df=pd.DataFrame(data)
print(df)
sns.jointplot(x='Age',y='Fare',data=df,kind='hist')

<img width="445" height="610" alt="Screenshot (40)" src="https://github.com/user-attachments/assets/da8be247-8ad7-49c5-9880-1a7db242cbb8" />



import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
data=pd.read_csv("titanic_dataset.csv")
df=pd.DataFrame(data)
print(df)
sns.pairplot(data=df)


<img width="800" height="652" alt="Screenshot (41)" src="https://github.com/user-attachments/assets/fe44ea84-4042-437b-b095-c71b8e2bfc9c" />
<img width="705" height="627" alt="Screenshot (42)" src="https://github.com/user-attachments/assets/40933665-d795-4415-8bb4-dc91e204bf46" />

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
data=pd.read_csv("titanic_dataset.csv")
df=pd.DataFrame(data)
print(df)
corr1=df.select_dtypes(include=['number']).corr()
sns.heatmap(corr1,annot=True)




<img width="646" height="716" alt="Screenshot (43)" src="https://github.com/user-attachments/assets/6c3ef952-06db-4e54-bf80-229db512c9de" />



import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
data=pd.read_csv("titanic_dataset.csv")
df=pd.DataFrame(data)
print(df)
sns.catplot(x='Sex',col='Survived',data=df,kind='count',color='green')



<img width="843" height="676" alt="Screenshot (44)" src="https://github.com/user-attachments/assets/da59e65d-5e79-466d-aeb6-82efc5ec593d" />

<img width="993" height="649" alt="Screenshot (45)" src="https://github.com/user-attachments/assets/77c7021e-0438-4f4e-8abc-37a263b181cc" />

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
data=pd.read_csv("titanic_dataset.csv")
df=pd.DataFrame(data)
print(df)
fig,ax1=plt.subplots(figsize=(8,5))
pd=sns.boxplot(ax=ax1,x='Pclass',y='Age',hue='Sex',data=df)



<img width="619" height="697" alt="Screenshot (46)" src="https://github.com/user-attachments/assets/8bf81924-c418-4727-bb62-6ab43db4be77" />


import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
data=pd.read_csv("titanic_dataset.csv")
df=pd.DataFrame(data)
print(df)
sns.catplot(data=df,col='Survived',x='Sex',hue="Pclass",kind='count')





<img width="653" height="716" alt="Screenshot (47)" src="https://github.com/user-attachments/assets/3c16c728-22f3-403a-bac0-6281f8ff38f1" />



import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
data=pd.read_csv("titanic_dataset.csv")
df=pd.DataFrame(data)
print(df)
sns.pairplot(df)



<img width="890" height="787" alt="Screenshot (48)" src="https://github.com/user-attachments/assets/272933c8-e166-44b3-b3d8-d985ebef1bf5" />
<img width="753" height="724" alt="Screenshot (49)" src="https://github.com/user-attachments/assets/eaf51f8b-bd89-4857-9d13-8a113f1335be" />




# RESULT
        <<INCLUDE YOUR RESULT HERE>>
