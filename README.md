# pychain_ledger
Python blockchain ledger system with streamlit web interface

## Technologies

Project uses:

[Pandas](https://pandas.pydata.org/)

[DataClasses](https://docs.python.org/3/library/dataclasses.html)

[Typing](https://docs.python.org/3/library/typing.html)

[Dotenv](https://pypi.org/project/python-dotenv/)

[Streamlit](https://docs.streamlit.io/)

[Web3](https://web3py.readthedocs.io/)

---

## Installation Guide

# Complete the following steps:

1 From your terminal, navigate to the project folder that contains your `.env` file and the `fintech_finder.py` and `crypto_wallet.py` files. Be sure to activate your Conda `dev` environment if it is not already active.

2 To launch the Streamlit application, type `streamlit run fintech_finder.py`.

3 On the resulting webpage, select a candidate that you would like to hire from the appropriate drop-down menu. Then, enter the number of hours that you would like to hire them for. (Remember, you do not have a lot of ether in your account, so you cannot hire them for long!)

4 Click the Send Transaction button to sign and send the transaction with your Ethereum account information. If the transaction is successfully communicated to Ganache, validated, and added to a block, a resulting transaction hash code will be written to the Streamlit application sidebar.



---

## Usage

Utilize terminal to interact with the program. Test the program by storing records when you run the PyChain ledger and user interface by running the Streamlit application and storing some mined blocks in the PyChain ledger. Then test the blockchain validation process by using your PyChain ledger.

!['Screen Shot of Streamlit'](https://github.com/hugokos/pychain_ledger/blob/master/Streamlit_Screenshot.JPG)



**Sample Code:**
```
# Create a select box to chose a FinTech Hire candidate
person = st.sidebar.selectbox('Select a Person', people)

# Create a input field to record the number of hours the candidate worked
hours = st.sidebar.number_input("Number of Hours")

st.sidebar.markdown("## Candidate Name, Hourly Rate, and Ethereum Address")

# Identify the FinTech Hire candidate
candidate = candidate_database[person][0]

# Write the Fintech Finder candidate's name to the sidebar
st.sidebar.write(candidate)

# Identify the FinTech Finder candidate's hourly rate
hourly_rate = candidate_database[person][3]

# Write the inTech Finder candidate's hourly rate to the sidebar
st.sidebar.write(hourly_rate)

# Identify the FinTech Finder candidate's Ethereum Address
candidate_address = candidate_database[person][1]

# Write the inTech Finder candidate's Ethereum Address to the sidebar
st.sidebar.write(candidate_address)

# Write the Fintech Finder candidate's name to the sidebar

st.sidebar.markdown("## Total Wage in Ether")
```

**Screen Shots from Ganache**


---

## Contributors

Hugo Kostelni

---

## License

Open Source
'