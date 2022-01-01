##############################################################################################################

# ░██████╗██████╗░  ███████╗░█████╗░░█████╗░
# ██╔════╝██╔══██╗  ██╔════╝██╔══██╗██╔══██╗
# ╚█████╗░██████╔╝  ██████╗░██║░░██║██║░░██║
# ░╚═══██╗██╔═══╝░  ╚════██╗██║░░██║██║░░██║
# ██████╔╝██║░░░░░  ██████╔╝╚█████╔╝╚█████╔╝
# ╚═════╝░╚═╝░░░░░  ╚═════╝░░╚════╝░░╚════╝░

##############################################################################################################

import pandas as pd

# There are 2 tables on the Wikipedia page
# we want the first table

payload=pd.read_html('https://en.wikipedia.org/wiki/List_of_S%26P_500_companies')
first_table = payload[0]
second_table = payload[1]

df = first_table

# # print(df.head())


# Print only symbols
# print(df['Symbol'])

##############################################################################################################
# S&P 500 tickers in a list
##############################################################################################################
symbols = df['Symbol'].values.tolist()
print(symbols[:15]) # Print only the first 15 elements. Example x[:,1] this is 2d slicing, here x[row_index, column_index]


# # Check the size of a matrix in numpy
# import numpy as np
# print(np.shape(symbols))


names = df['Security'].values.tolist()
print(names[:15])


#show unique economy sectors
sectors = df['GICS Sector'].values.tolist()
sectors = set(sectors)
print(sectors)


##############################################################################################################
# Advanced screening of S&P 500 stocks
##############################################################################################################
# real_estate_df = df[df['GICS Sector'] == 'Real Estate']
# real_estate_symbols = real_estate_df['Symbol'].values.tolist()

# print(real_estate_symbols)



##############################################################################################################
# All sectors dataframe
##############################################################################################################
# # pretty printing of pandas dataframe
# pd.set_option('expand_frame_repr', False) 

# for sector in sectors:
#     sector_df = df[df['GICS Sector'] == sector]
    
#     # delete unnecessary columns
#     del sector_df['SEC filings']
#     del sector_df['Headquarters Location']
#     del sector_df['Date first added']
#     del sector_df['CIK']
#     del sector_df['Founded']
    
    
#     #print(sector_df.head())
#     print(sector_df)
    
#     print('--------------------------------------')


##############################################################################################################
# Export to csv file
##############################################################################################################
df.to_csv('S&P500 list.csv', index=False)

# Save to a specific path as follows
# df.to_csv(r'C:\Users\george\VisualStudio Projects\export_dataframe.csv', index = False)


##############################################################################################################
# Access to a specific row and column of the Pandas dataframe
##############################################################################################################
# print(df['Security'][5])
# print(df['GICS Sector'][5])

# print(df[:]['Security'])

# df.loc[5,["Security", 'Symbol']]

# print(df.iloc[1,1])

# print(df.loc[:,["Security", 'Symbol']])
# print(df.iloc[:,[1,0]])
