import random
lst = ['robot'] * 10
lst += ['human'] * 10
random.shuffle(lst)
data = pd.DataFrame({'whoAmI':lst})
data.loc[data['whoAmI'] == 'robot', 'robots'] = 1
data.loc[data['whoAmI'] != 'robot', 'robots'] = 0
data.loc[data['whoAmI'] == 'human', 'humans'] = 1
data.loc[data['whoAmI'] != 'human', 'humans'] = 0
data.head()