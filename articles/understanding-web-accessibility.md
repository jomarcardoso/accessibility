# Understanding Web accessibility

With the evolution of the web, many features have been added, and the way to develop a website today is not the same as it was 10 years ago, much less when the web started. These many years of enhancement have made the web great but also hard to learn everything that has been present since its beginning in 1991. It is understandable that courses skip over all this knowledge and go directly to a framework, allowing students to quickly start working. This approach is fair, but at some point, developers must cover this content to become complete professionals. I hope that this article serves as a step back to understand web accessibility before following any rules to build your accessible websites.

## 1. Introduction

At school, at least here in Brazil, the most common way to learn something is by rote memorization, and it makes sense since you don't have to use that learning for anything else but the test. I was always a kid who questioned a lot because I had a personal difficulty learning without understanding the subject 100%. It was common for me to interrupt the class when I was trying to understand something that my colleagues didn't realize they didn't know either, simply because they didn't need to deeply understand something to use it, especially in a test that would happen a few weeks later.

I used to always try to understand the concept behind the rule or the trick when I found out that it was a rule. A trick that took me years to realize was in mathematics: in an equation, you can invert the operation and move a number to the other side of the equality. I was in college when a good teacher explained that it was only a trick, but under the hood, the operation is to perform the same operation on both sides of the equality, and the result of this is like sending a value to the other side with the reverse operation. I understood that the rule was a trick, and since then, I have been able to solve equations without risking misunderstanding the trick.

Web accessibility nowadays is often seen as merely following the WCAG recommendations, instead of understanding the real problem we are solving by following those rules. This lack of knowledge may lead us to create a feature that meets the guidelines but without any idea if it actually serves the users of the website. Therefore, if the objective is to provide the best experience for everyone, we must first understand the users and their disabilities and the tools we have to serve them well.

## 2. Development

As mentioned in the introduction of this article, we need to understand web users and their potential disabilities to provide the best experience that helps overcome their difficulties, which often extend beyond the internet. I am not going to delve deeply into the topic of disabilities in this article, as I have already written about it in ["Understanding Functional Differences in Web Accessibility".](./the-users-pt.md) The text ahead is sectioned by disability, with each section providing a summary of what these users need and how to give them an ideal experience.

### 2.1 Physical disability

These users may have limitations that decrease the precision of their arm and finger movements, and can include people with amputated limbs, partial or full paralysis. For desktop devices, some of them might use only the keyboard to navigate, or another restrictive assistive technology depending on the disability. Smartphone users, in most cases, need elements on the screen to be large enough to touch without making mistakes.

To cater to this audience, on desktop pages, we need to avoid the necessity of using a cursor and allow navigation through buttons using either the keyboard or any other assistive technology. Users should be able to scroll through all content and access controllers such as links, buttons, and inputs using the keyboard. Elements in focus must be highlighted properly so that users know what they will activate
