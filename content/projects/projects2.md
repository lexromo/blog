---
title: "Phishing Attack (Cybersecurity class final project)"
date: 2023-12-05T23:15:00+07:00
slug: 
category: 
summary:
description: 
cover:
  image: "zphisher.png"
  alt:
  caption: 
  relative: true
showtoc: true
draft: false
---

# DO NOT USE THIS TOOL FOR MALICIOUS PURPOSES!

Phishing is a form of cybercrime that involves attempting to acquire sensitive information, such as usernames, passwords, and credit card details, by posing as a trustworthy entity in electronic communication.

Engaging in such activities is against the law and violates ethical standards. It's important to use your cybersecurity knowledge and skills to protect and secure systems, data, and individuals from cyber threats, rather than using them for malicious purposes.

This was a final project from my Operating Systems Cybersecurity class.

## Small summary
Phishing attacks are illegal when conducted without explicit permission from the target (in my case I had the permission because it was a final project from my cybersecurity course), and unethical hacking practices are strictly discouraged. However, if you're conducting a phishing simulation or attack as part of an authorized cybersecurity project or penetration testing be shure you have written permission from the target or organization. here's a general approach I followed using an Open Source Zphisher (a popular open-source phishing tool). 

## Steps I followed to Perform a Phishing Simulation Using Zphisher

### Obtain Authorization:

Before beginning the phishing simulation, I made sure to get explicit permission from my professor to target my classmates. This was part of a cybersecurity project for my postgraduate studies. The professor outlined the scope, and I had clear authorization to simulate a phishing attack on my classmates within the academic context.

I strongly recommend always obtaining written authorization that clearly outlines the scope of your activities before conducting any cybersecurity testing. This should include all the boundaries and limitations of the engagement. As a cybersecurity professional, it's essential to make this a habit to ensure that your work remains ethical, legal, and transparent at all times.
### Install Zphisher:

To start, I installed Zphisher on my Kali Linux system. This is an open-source tool for phishing simulations, and I used it to replicate a phishing attack. I cloned the repository from GitHub using the following commands:

        git clone https://github.com/htr-tech/zphisher.git
        cd zphisher
        chmod +x zphisher.sh
        ./zphisher.sh

I ensured that both Git and PHP were installed, as they were necessary for the tool to work properly.

### Select Phishing Templates:

Once Zphisher was running, I had the option to choose from different phishing page templates like Facebook, Instagram, or Gmail. For this simulation, I selected the Facebook template, which generated a login page that closely resembled the real Facebook login screen. This was the platform I used to simulate a social engineering attack.

### Setting Up the Phishing Link:

Zphisher provided different options for hosting the phishing page. I chose Ngrok because it allowed me to create a public URL, which made it easy to share with my classmates. After selecting Ngrok, Zphisher generated a link that I used to send out the phishing attempt.
Although I could have used other methods like Serveo or localhost, Ngrok was the simplest way to ensure that the phishing link was accessible outside my local network.

### Strategy used:

As part of my phishing simulation project, I employed different strategies to target my classmates by leveraging a range of social media platforms, including Facebook, Instagram, Gmail, and Outlook. This approach allowed me to replicate real-world phishing scenarios, where attackers often tailor their tactics to the specific platform a user frequents.

Facebook:
  For classmates who were active on Facebook, I used a phishing template that mimicked the Facebook login page. I sent personalized messages via email that appeared to come from a trusted Facebook-related source, prompting them to "log in" to resolve a security issue. The goal was to see how effectively I could entice them to click the link and enter their credentials.

Instagram:
  For those more engaged on Instagram, I crafted messages that looked like typical Instagram notifications. These messages indicated suspicious activity on their accounts, urging them to verify their details by logging in. The Instagram phishing page resembled the actual Instagram login screen, aiming to capture their credentials in the same way.

Gmail:
  I used a Gmail-themed phishing template for classmates who primarily used Google services. The phishing email I crafted warned of unusual login attempts on their Google account and included a link to "secure" their account. The fake login page was designed to replicate the Gmail login process, tricking users into revealing their credentials.

Outlook:
  For classmates who relied on Outlook for their emails, I created a similar phishing email, pretending to be a security alert from Microsoft. The link redirected them to a fake Outlook login page, which was carefully designed to mimic the real thing. This helped simulate how phishing attacks can target users of professional email platforms like Outlook.

By using multiple social media platforms and tailoring the phishing messages to suit the habits of my classmates, I demonstrated how attackers customize their phishing tactics based on the victim's digital behavior. This not only made the simulation more realistic but also showcased the importance of being vigilant across all platforms, not just one.

### Sending the Link to My Classmates:

With the phishing link ready, I crafted an email that mimicked a legitimate message, similar to how real phishing attacks appear. I sent the link to my classmates as part of the experiment. My goal was to simulate a real-world phishing scenario, but since this was a controlled test, only my classmates—within the scope of the project—received the link.
### Monitoring the Results:

As my classmates clicked the link and entered their credentials, Zphisher captured the data and displayed it in my terminal. I was able to see the login details entered, but this information was only used for the purposes of the project.

I reviewed how my classmates responded—whether they clicked the link and entered their credentials. This allowed me to observe how effective the phishing attempt was and how my peers reacted to the simulation.
### Simulating an Incident Response:

After completing the phishing simulation, I demonstrated how the organization (in this case, our class) could respond to such an attack. I discussed potential responses like notifying the IT security team and mitigating the damage. This was important for showing how quickly an organization can detect and respond to a phishing attempt.

### Documenting the Simulation:

After the simulation was completed, I documented everything. I created a detailed report that outlined:

How the phishing simulation was set up and carried out.

The tools I used, such as Zphisher and Ngrok.

The response of my classmates (how many clicked the link, how many submitted credentials).

Recommendations for improving cybersecurity awareness and defenses against phishing attacks.

### Cleanup:

Once the test was over, I made sure to clean everything up. I closed the Zphisher session, stopped the Ngrok tunnel, and deleted the Zphisher files from my machine:
        rm -rf zphisher

This ensured that no vulnerabilities or open connections remained after the simulation.
### Provide Recommendations:

After this phishing simulation, I presented recommendations to all my classmates for preventing similar real-world phishing attacks. This included:

User training: Conduct regular cybersecurity awareness sessions.

Email filtering: Implement strong spam filtering solutions.

Multi-factor authentication (MFA): Recommend the use of MFA to protect against stolen credentials.

### Final Thoughts on the Phishing Simulation Project:

Through this phishing simulation, I gained valuable insights into both the effectiveness of phishing attacks and the awareness levels among my classmates. Despite many of them being cybersecurity students, some still fell victim to the simulation by clicking the phishing links. In many cases, this was because they were not fully aware of the subtle social engineering tactics I employed.

One key factor that contributed to the success of the attack on certain classmates was the research I conducted beforehand. By gathering information about their social media habits, interests, and platforms they frequently used, I was able to craft highly convincing phishing messages tailored to each individual. This personalization made it easier for them to trust the phishing link, despite their cybersecurity background.

On the other hand, there were classmates who did not fall for the attack. Their higher levels of cybersecurity awareness and cautious approach to clicking links, especially those related to sensitive accounts, played a critical role in their defense. This highlights the importance of proper training and constant vigilance, even for those who are well-versed in cybersecurity.

This project reinforced the reality that phishing remains one of the most effective attack vectors, and that even professionals in the field can be caught off guard if they are not paying close attention. It also emphasized the need for continuous awareness training and better user education, as the human element remains the weakest link in cybersecurity.


