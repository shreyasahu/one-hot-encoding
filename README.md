# one-hot-encoding
contains funtion for doing onehot encoding and also contains code to see full dataframe without dots.

    def onehot(df,column):
      df[column]=pd.Categorical(df[column])
      dfc=pd.get_dummies(df[column],prefix='category')
      df=pd.concat([df,dfc],axis=1)
      return df
      
      df=onehot(df,'Neighborhood')
