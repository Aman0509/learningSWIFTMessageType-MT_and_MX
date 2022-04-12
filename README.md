# SWIFT Message Types - MT and MX ISO 20022 - An Overview

## SWIFT, SWIFTNet and SWIFT Code/BIC
Banks located in different locations in the world need to communicate with each other to perform their everyday operations. That communication forms the basis of numerous transactions taking place globally on a daily basis.\
Before the advent of SWIFT, banks used to communicate using telex, fax or phone, but it was very slow and not a secure way to communicate at all. So in 1973, around 239 banks from 15 countries created a cooperative headquartered in Belgium named Society for Worldwide
Interbank Financial Telecommunication, or SWIFT, to build a common messaging system.

![Alt SWIFT - SWIFT Message Types - MT and MX ISO 20022 - An Overview](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/swift.png)

Slowly, the number of member banks grew, and today more than 11000 banks are part of SWIFT communicating with each other using its network called SWIFTNet.

![Alt SWIFT - SWIFT Message Types - MT and MX ISO 20022 - An Overview](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/swiftnet.png)

***But how will one member identify another member of SWIFTNet?***

_Using an ID_.\
This ID is called the business identifier code or the SWIFT code. Here B stands for business and not bank. You may wonder why, because not only banks are financial institutions, but corporate can also become a member of SWIFT to communicate their instructions with financial institutions directly.

![Alt SWIFT - SWIFT Message Types - MT and MX ISO 20022 - An Overview](https://github.com/Aman0509/learningSWIFTMessageType-MT_and_MX/blob/main/other/images/bic.png)

The swift code acts not only as an entity or member identifier, but it also contains important information about the location of the entity, which is used to redirect a SWIFT message to it.\

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

## References
- [SWIFT Message Types - MT and MX ISO 20022 - An Overview (Udemy Course)](https://www.udemy.com/course/swift-message-types-in-banking/)