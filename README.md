Submission to : Governance

Topics related : Web2 to Web3, Technical content, Future of work

## Inspiration
Problematic of Social Media management.

**Solve problem for a community to organise their social network accounts by themselves.**

Many associations and human organisations have to own a social network page. For necessities, for facilities or for many other reasons, an association can need to have a social network page. 
And in some cases, the association can want to use an horizontal way to manage theses accounts. 

So from this problem we can about three solutions. 

Level 1 : To use actual tools offer by a DAO (proposal, bounty and rights permissions) to make it. The DAO by its rules decide an action to make on social network account through vote kind proposal. After, the community always through the DAO decides an IP address will made the action. If he doesn't made it, he isn't rewarded and apply some restrictions in accordance to the rules of the community. 

Level 2 :  To link DAO with an API social account (like twitter or reddit) and automate publication through Function Call option in the DAO. 
Each member can vote depends on his rights in the DAO, determined by the association. 


Level 3 : To link a DAO with a Web3 social account as myriad on octopus network.
This can be easier because apparently everything are on-chain

## What it does

Level 1 : We are providing a documentation for association wants to onboard with DAOs. It is doing on AstroDAO. The goal is really accessibility for not crypto users. 
We want that people don't think about Blockchain. Don't think about 'what is it ?', 'what is mean blockchain?'. 
Just use IF IT'S USEFUL FOR YOU. 
For example in a little association, it can be hard to control who did something with the social accounts that are often shared to allow more reactivity.


Level 2 (Detailing our Proof of Concept) :  An association could put a proposal with type `post` and `content` of its, as : 
```bash
near call $MY_DAO add_proposal '{
  "proposal" : {
             "kind" : {
                      "post" : {
                                       "content" : "I want to make this, post on twitter account of the association. I WILL SUCCESSSSS !!!"
                                      }
                             }
                         }
}' --accountId my-account.near 
```
We have the idea to use a python code to check if a certain transaction happen on the contract and so act on the web by the way of the contract tell. 
We need to do something like that : 
```python
if proposal_approved == true : 
      text_posted = proposal_description
      make : post_with_api(text_posted)
else
     do_nothing
```
With a such code we can link the dao wallet and API social account in the python code, make run the python code by a crontab job and proposals on dao should act as wanted. 

Level 3 : If there exists a contract of a social web3 app (compatible with near) we can just make a call from FunctionCall proposal kind. When proposal is approved, DAO will make the request automatically (for example make a post on this app).  


## How we built it

Level 1 : A doc as easy as possible, with most informations on 'how to onboard' possible.

Level 2 : We made a schema for the Proof of Concept with core idea of the API use. 

Level 3 : We made abstract contract to show attempted interactions. 
 
## Challenges we ran into

Level 1 : Difficulty to be exhaustive in this time range. 

Level 2 : Impossibility to find a contract to make an API call for us. We didn't success to develop one by themselves.

Level 3 : Difficulties with near integrations on some appchains (use myriad contract from a _near call_). It's an ecosystem which exponentially growth and as Illia told in his Keynote : "We still need to find combinations with Web3 primitives". 


## Accomplishments that we're proud of

Level 1 : As the doc is not complete. It's really one of our main goal to onboard new people who has truly need of the blockchain without know it before. Maybe we can find totally new use never mind before (as in Open Forest Protocol, we can see people who use it to prove the ownership of a Forest (in Brazil). This is a not thinking use case before but it's a useful way to prove ownership and existants of the Forest in an open-source and verifiable 



Level 3 : This integration can allow a true network effect across communities. It can onboard near-user in new Social Web3 App in providing DAO content related. 

## What we learned

We learned a lot through the different challenges we ran into, especially on how to interact with the different dapps in the near ecosystem.
We also learned how to create a bridge between the web2 world and the near ecosystem.

## What's next for DAO4SocialAccount

Level 3 : This can enhance the content available in web3 Social media like Myriad or Social08. If the submission of posts aren’t made by an individual, it’s easy to publish them on a lot of platforms at the same time (for instance on twitter and myriad). This would bring a lot of contents to those emerging platforms, and help users transition into them without losing the content they are used to see.

Another step is to find organisations willing to try our solution and give us feedbacks. We know some little associations, such as local food banks, that would be interested.

If we can even give them some near for their DAO creation, that would be huge. Once they're onboarded onto our decentralized social media product, they would be just one small step to fully transfert into a DAO format for all their other needs.

## LINKS
**Youtube** : https://www.youtube.com/watch?v=bjp4fmTr-k8
**Slides** : https://docs.google.com/presentation/d/1W53uEVnVQTWjG7pexAofirLmDdcpLB_d4pzt98f_3NU/edit?usp=sharing


