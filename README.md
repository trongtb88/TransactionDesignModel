# TransactionDesignModel


Tables

Account(account_id, owner_user_id)
Transaction(transaction_id, transaction_detail_type, transaction_detail_id)
TransactionLeg(account_id, transaction_id, amount, type(debig/credit))

PreCondition

- Account(account_id: user1, owner_user_id: 1)
- Account(account_id: systemdeposit1, owner_user_id: system1)

When user deposit

CreateTransaction() transactinn_id
CreateTransactionLeg(transaction_id, amount, type: debit, account_id: user1account)
CreateTransactionLeg(transaction_id, amount, type: credit, account_id: systemdeposit1)

Create user balance
Sum(account credit amounts) - Sum (account debit amounts)



