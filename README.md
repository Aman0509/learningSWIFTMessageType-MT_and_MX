# SWIFT Message Types - MT and MX ISO 20022 - An Overview

## Basics of Swift

### SWIFT, SWIFTNet and SWIFT Code/BIC
SWIFT is the ‘Society for Worldwide Interbank Financial Telecommunication’, a member-owned cooperative through which the financial world conducts its business operations with speed, certainty and confidence. SWIFT enables customers to automate and standardize financial transactions, thereby lowering costs, reducing operational risk and eliminating inefficiencies from their operations.

SWIFT is solely a carrier of messages. It does not hold funds nor does it manage accounts on behalf of customers, nor does it store financial information on an on-going basis. As a data carrier, SWIFT transports messages between two financial institutions. This activity involves the secure exchange of proprietary data while ensuring its confidentiality and integrity.

Banks located in different locations in the world need to communicate with each other to perform their everyday operations. That communication forms the basis of numerous transactions taking place globally on a daily basis.\
Before the advent of SWIFT, banks used to communicate using telex, fax or phone, but it was very slow and not a secure way to communicate at all. So in 1973, around 239 banks from 15 countries created a cooperative headquartered in Belgium named Society for Worldwide
Interbank Financial Telecommunication, or SWIFT, to build a common messaging system.

![Alt SWIFT - SWIFT Message Types - MT and MX ISO 20022 - An Overview](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/swift.png)

Slowly, the number of member banks grew, and today more than 11000 banks are part of SWIFT communicating with each other using its network called SWIFTNet.

![Alt SWIFT - SWIFT Message Types - MT and MX ISO 20022 - An Overview](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/swiftnet.png)

***But how will one member identify another member of SWIFTNet?***

_Using an ID_.\
This ID is called the business identifier code or the SWIFT code. Here **'B'** stands for business and not bank. You may wonder why, because not only banks are financial institutions, but corporate can also become a member of SWIFT to communicate their instructions with financial institutions directly.

![Alt SWIFT - SWIFT Message Types - MT and MX ISO 20022 - An Overview](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/bic.png)

The swift code acts not only as an entity or member identifier, but it also contains important information about the location of the entity, which is used to redirect a SWIFT message to it.

**Let's understand how.**

SWIFT code are 8 to 11 correctors in length, for example, let's see how a branch of Deutsche Bank in Germany gets identified using BIC.

![Alt SWIFT - SWIFT Message Types - MT and MX ISO 20022 - An Overview](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/swift-example.png)

The first four alphabetical letters stand for that business entity. Here, DEUT stands for Deutsche Bank. So anywhere in the world, any SWIFT code for Deutsche Bank will start with
DEUT. Next two alphabetical letters from the specific country code where the branch is located,
DE stands for Deutschland or Germany. The next two letters can be alphabetical or numeric and they stand for the institution head office in the country, or the head office in a particular region in the country. Here, SS stands for Stuttgart, a city in Germany. So, *DEUT DE SS* is a valid eight characters SWIFT code. And if you don't add further characters to this code, it will indicate that it's the code of the Deutsche Bank main branch at Stuttgart city of Germany.
Now suppose you need to reach a particular branch.
Then a further three letter code is added to the code. Here, **648** denotes a particular branch in the Stuttgart region.

Another Example

|  |  |
| --- | ----------- |
| ![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/bic_eg_1.png) | ![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/bic_eg_2.png) |
| ![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/bic_eg_3.png) | ![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/bic_eg_4.png) |

**More Readings**
- [Prowide - About SWIFT](https://www.prowidesoftware.com/resources/SWIFT)

### SWIFT FIN and GPA Messages and MT Message Structure

Let's understand now how members communicate among each other in a SWIFT network.\
Communication between members happened using standardized message formats. You can imagine messaging standards as predefined format so that when such messages are exchanged between two parties following the same standard, they can decode and understand what the counterpart is trying to convey.

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/communication.png)

There are many kinds of messaging standards which are used globally to communicate among banks. The two standardized messages which are supported by SWIFT are ***MT and MX messages***.

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/types_of_msg_format.png)


> The MT messages are structured according to the specifications of the ISO 15022 standard and the newer MX messages according to the ISO 20022 standard.


**Side Note:**\
*ISO or International Organization for Standardization is an independent, non-governmental international organization which develops standards which provide the best way of doing something. They have joined hands with SWIFT to create these messaging standards.*

Let's know more about MT messages.\
These standardized MT messages are exchanged under SWIFTNet FIN service. FIN stands for financial messaging application.\
The FIN service comprises of the following two applications:
- Financial Messaging Application
- General Purpose Application (GPA)

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/types_of_SWIFTNet.png)

As pointed earlier that SWIFT MT messages follow ISO 15022 standard and here's how it looks like,

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/SWIFT_MT_sample_msg.png)

SWIFT messages consist of five blocks.

|  |  |
| --- | ----------- |
| ![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/block-1.png) | ![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/block-2.png) |
| ![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/block-3.png) | ![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/block-4.png) |
| ![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/block-5.png) |

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/MT_msg_IO_info.png)

For more info, refer [SWIFT MT Message Structure Blocks 1 to 5](https://www.paiementor.com/swift-mt-message-structure-blocks-1-to-5/)

**More Readings**
- [SWIFTNet for Corporate](https://www.nordea.com/en/doc/file-transfer-swiftnet-factsheet.pdf)
- [SWIFT Messaging Services](https://www.swift.com/node/13491)

### SWIFT Message Categories and Rules/ Guidelines of Messages

We've discussed about the basic structure of MT messages and it's five building blocks. Now let us know what are the different categories of MT messages available under the FIN service?\
There are total nine categories and a separate category for common messages which can be used under any category. Together, SWIFT covers messaging requirements for payment, securities, trade finance and foreign exchange and treasury.\
Interestingly, SWIFT does not provide services for card payments.

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/MT_msg_category.png)

Under each category, there are several messages. For example, under messages category 1 - customer payments and cheques, there is MT 101 - Request for transfer, MT 103 - Single customer credit transfer and so on.

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/category_example.png)

Each message is denoted using three digits.
- The first digit denotes the category it belongs to.
- The second digit denotes the group. For example, '0' denotes electronic, '1' denotes paper-based.
- The third digit provides the specific function.

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/MT_msg_decode.png)

Now, to use these different types of messages correctly, SWIFT also provides some rules and guidelines to structure the messages. There are four kinds of rules and guidelines for structuring SWIFT messages.

<u>**1. MT Network Validated Rules (NVR)**</u>

Network Validated Rules are rules for which an error code is defined in SWIFT. When the rules specified affect more than one field in the message, thus placing a condition on one of the field specified, they are called CN or conditional rules. Below is the example of a NVR for a MT 103 message which is the message format used for customer credit transfer between banks. You can see how presence and absence of fields are dependent on each other. And if the rule is not followed, an error will be thrown by the software and you can't proceed
without rectifying that error.

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/NVR.png)

<u>**2. MT Usage Rules**</u>

Usage rules are not validated on the network, meaning rules for which no area code is defined but are still mandatory for the correct usage of the message.

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/usage_rules.png)

For example, usage rule for MT 103 message says, when the current method is used for customer credit transfer, the originating bank must copy the content of field 20 of the MT 103 unchanged into field 21 of the related MT 202 COV (COV will be discussed later).\
What the rule is trying to say is in the current method of customer payment, two messages are used simultaneously a MT 103 message and a MT 202 COV message and the content of a particular field of the MT 103 should be copied as it is
in another field of the MT 202 COV. Now that this is actually done on not, SWIFT has no method to check for itself because SWIFT has no way to compare
two different messages automatically and generate any warning or error. ***That's why SWIFT has designed usage rules such as these to educate the user of the correct usage of each message.***

<u>**3. MT Guidelines**</u>

Guidelines are neither validated on the network nor are mandatory for the correct usage of the message. They basically concern group practices and can affect more than one field in a message or more than one SWIFT message.

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/MT_guidelines.png)

<u>**4. MT market practice rules**</u>

Market practice rules, as the name suggests, are a set of rules which are usually in practice or prevalent in the market. For example, the payments market practice group, or PMPG, is an independent body of payments subject matter experts from Asia Pacific, Europe and North America. It has published a set of market practice rules for category 2 messages proposing best practices and recommendations of structuring such messages.

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/MT_market_practices.png)

**More Readings**
- [Oracle ® FLEXCUBE Universal Banking Messaging System User Guide](https://docs.oracle.com/cd/E74659_01/html/MS/MS13_SWIFT_Messages.htm#Rar71230)

## Brief Overview of Payment System

### Brief Overview of Payment Systems

We have got an overall idea of the background of SWIFT and the messages but before we can start understanding the SWIFT payment messages, we need to have a brief idea about one more concept, which is, how payments work.

There are three main elements of a payment system or a clearing and settlement system.

>Messaging, Clearing and Settlement

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/payment_elements.png)

Let's understand what each means.

**1. Clearing**

First, what is meant by a clearing system. In simple words, it is reconciling and netting system before actual settlement of money can be done.

Let's take the simplest example of bilateral clearing. Two banks, A and B owe each other money. Bank A owes bank B five million dollars and bank B owes bank A seven million dollars. The two banks calculate between themselves and finally,bank B pays bank A two million dollars. This act is called netting or offsetting and this amount of two million is called the final position.

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/clearing_example_1.png)

Now, imagine the same thing with multiple banks, the more nodes you act in the system, the more complicated and cumbersome it becomes for the banks to do the calculations. This is multilateral clearing without a clearing house.

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/multilateral_clearing_without_clearing_house.png)

Here comes the role of a clearing house, instead of connecting with each other,
the banks instead connect with the clearing and settlement system. In short, the CSM, comprising the clearing house and the central bank settlement mechanism. The clearing system calculates the final position of the participating banks once or several times daily and finally, pushes the actual settlement transaction through the central bank settlement mechanism.

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/multilateral_clearing_with_clearing_house.png)

To summarize,

- ***Clearing is reconciliation and netting process.***
- ***Settlement is the actual mechanism of moving the funds from one account to another.***

**2. Settlement**

Let’s know a little more about **settlement systems**. The example mentioned previously, where first netting of the transaction is done and then the final position amount is settled is called the ***net settlement system***.

There is another method called the ***gross settlement system***. Here, no netting is done and each transaction is settled individually.
So, here, first bank A's customer will originate the payment of seven million dollars through bank A. Bank A pushes the transaction through the CSM where the settlement accounts of the two banks are debited and credited.\
Next, on receiving the credit on its settlement account, the receiving back finally credits the beneficiary seven million dollars.\
The same process will get repeated then bank B's customer wants to send bank A’s customer five million dollars. As no netting is involved in this process,
it happens real time. Hence the name, ***real time gross settlement***.\
This system is used then urgent transfers are to be made and also for high value transfers.

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/RTGS.png)

Another kind of settlement is a ***Real Time Final Settlement System*** or RTFS. Unlike RTGS, where the ultimate beneficiary gets paid only after the sending bank and receiving banks settlement accounts in the CSM get settled.
Here, first the ultimate beneficiaries account is credited after doing a transaction validation and the settlement account of the banks are settled later.\
Examples of such systems are IMPS in India or CHIPS in the USA.

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/RTFS.png)

**3. Messaging**

This entire communication between banks and CSM happens using messages. This is where SWIFT comes in. So, SWIFT is a messaging system. It is only a information carrier. It has no role in either clearing, nor settlement.\
As we know that SWIFT is a messaging system. It is only a information carrier.
It has no role in either clearing, nor settlement.

* Depending on purpose, the messages can be of two types, value messages which are used to move money from one account to another and non-value messages which don't move money but move information.

* Based on the form, messages can either be paper or in electronic form.

* The structure of messages follows standards. As we discussed earlier, standards are predefined formats which ensure that when such messages are exchanged between two parties following those standards, they can decode and understand what the counterpart is trying to convey.

    * Some standards are followed regionally. For example, in the USA, regional standards are Fedwire, CHIPS and NACHA format. In the UK, there is bankers automated clearing service or BACS standard 18 format.

    * When we talk about global standards, EDIFACT or Electronic Data Interchange for administration, commerce and transport is another messaging standard. ISO 8583 messaging standard is used for exchanging electronic transaction initiated by cardholders using payment cards.

    * **Next comes the global messaging standard that is our point of attention SWIFT with its two standard MT and MX.**

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/messaging_system.png)

So, we now get the bigger picture of the three elements of a payment system messaging, clearing and settlement. Some providers provide service for only one element, while some provide services from more than one. In reality, the payment system works as a combination of various providers.\
For example, SWIFT provide service for only the messaging part. CHIPS in the USA, STEP1, STEP2, EUR01 provide services for both messaging and clearing,
but are not involved in settlement. Whereas CHAPS in the UK or Fedwire in the USA provide all the three services.

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/combinations_of_C_M_S.png)

So, we understood that the payment systems operate within a single country.
They are denominated in the currency of that country. They are subject directly or indirectly to regulation by the government of that country. And of course, they enable multiple parties to transact with each other.

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/summary_module_3_1.png)

A cross-border payment must pass through two payment systems. Banks of one payment system needs to access banks in the other payment system. But how to do that?\
Here comes the role of **Correspondent Accounts**.

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/module_3_2.png)

### Correspondent Accounts and RMA

Let's take an example of two banks, Bank A in the euro payment zone and Bank B in the dollar payment zone. How can Bank A make payment in dollars and Bank B in the euro?

Simple. Bank A will become a customer of Bank B and Bank B can also become a customer of Bank A, though it's not mandatory to have a bilateral relationship.

How to become a customer?

Bank A will open its account in the books of Bank B in dollar currency. This account is called the Dollar Nostro account for Bank A and the same account is referred to as Bank A’s Vostro account by Bank B. So, Nostro and Vostro are
used to denote the same account depending on who is referring to the account.

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/module_3_3.png)

There is one more thing Bank A will do, it's an open a mirror account
of this nostro in its own books. This account does not contain any real money.
Just like a mirror reflects a real person, this account is used to reflect the actual transactions happening in the nostro account. The purpose of this is to keep track of the transactions and thus helping in reconciliation. The same process of account opening is repeated by bank B if there is a bilateral correspondent relationship.

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/module_3_4.png)

Now that the correspondent account relationships are set, the banks can communicate with each other securely using SWIFT. But there can be thousands of bank in the network. How will the banks control traffic?\
Here comes the relationship management application, or RMA of SWIFT.

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/module_3_5.png)

RMA+ service by SWIFT goes deeper and provides granular authorization to which
type of messages the correspondent can send. First, the two correspondence
exchange permission data between them. Based on that, the sender checks the message type against the permission data before sending a message to the receiver. This not only reduces the traffic volume, but is a form of risk management by acting as a first line of defense against fraud.

![Alt](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/module_3_6.png)

## References
- [SWIFT Message Types - MT and MX ISO 20022 - An Overview (Udemy Course)](https://www.udemy.com/course/swift-message-types-in-banking/)