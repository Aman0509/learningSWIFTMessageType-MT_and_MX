# SWIFT Message Types - MT and MX ISO 20022 - An Overview

## SWIFT, SWIFTNet and SWIFT Code/BIC
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

## SWIFT FIN and GPA Messages and MT Message Structure

Let's understand now how members communicate among each other in a SWIFT network.\
Communication between members happened using standardized message formats. You can imagine messaging standards as predefined format so that when such messages are exchanged between two parties following the same standard, they can decode and understand what the counter party is trying to convey.

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

## SWIFT Message Categories and Rules/ Guidelines of Messages

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

## References
- [SWIFT Message Types - MT and MX ISO 20022 - An Overview (Udemy Course)](https://www.udemy.com/course/swift-message-types-in-banking/)