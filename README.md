\documentclass[12pt,a4paper]{article}
\usepackage[utf8]{inputenc}
\usepackage{longtable}
\usepackage{hyperref}
\usepackage{blindtext}
\usepackage{mathptmx}
\usepackage[a4paper, 
    right=1in, 
    left=1.50in,   
    top=1in,      
    bottom=1in     
]{geometry}
\usepackage{setspace}
\usepackage{ragged2e}
\justifying
\onehalfspacing
\usepackage{graphicx}
\usepackage[utf8]{inputenc}
\usepackage{multicol}
\begin{document}
\begin{titlepage}
\newcommand{\HRule}{\rule{\linewidth}{0.5mm}}

\begin{center}
\includegraphics[width=.3\textwidth]{north-south-university-logo}\\[0.5cm]
  \textsc{\Large North South University}\\[0.5cm]
  
   
  
  
  
  \HRule\\[0.5cm]
  \textsc{\normalsize Junior Design}\\
  \textsc{\normalsize CSE299}\\
  \textsc{\normalsize Section 16}\\
  \textsc{\normalsize Rifat Ahmed Hassan (RIH)}\\
  
  \textsc{\normalsize Semester: Spring 2024}\\
  [0.5cm]
  
  \HRule\\[1cm]
 
  

  \textsc{\normalsize  \textbf{Submitted By-}}\\
  Group 5\\[0.3cm]
\begin{tabular}{|l|l|}
\hline
\textbf{Name} & \textbf{ID} \\ \hline
Abdullah Al Wasif & 2131465642 \\ \hline
Al-Fawsesh Habib & 2131230642 \\ \hline
Shadman Khan & 2122061642 \\ \hline
Naym Hasan Khan & 1621640042 \\ \hline
\end{tabular}\\[.3cm]



  

Submission Date: \ \ \     9 December   , 2024

\end{center}

\end{titlepage}
\newpage






\newpage
\pagenumbering{roman}
\section*{Declaration}
This is to certify that this Project is our original work. No part of this work has been submitted elsewhere partially or fully for the award of any other degree or diploma. Any material reproduced in this project has been properly acknowledged.\\[3cm]
Students’ names \& Signatures\\[.3cm]
\begin{enumerate}
    \item Abdullah Al Wasif\hspace{1cm}............................................\\[0.5cm]
    \item Al-Fawsesh Habib\hspace{1cm}............................................\\[0.5cm]
    \item Shadman Khan\hspace{1cm}............................................\\[0.5cm]
    \item Naym Hasan Khan\hspace{1cm}............................................\\[0.5cm]
\end{enumerate}
    




\newpage
\section*{APPROVAL}
We, Wasif, Habib, Shadman and Naym, members of CSE 299 (Junior Project Design) from the Electrical and Computer Engineering department of North South University; have worked on the project titled “Chitter Chatter” under the supervision of Mr. Rifat Ahmed Hassan (RIH) sir as a partial fulfillment of the requirement for the degree of Bachelors of Science in Engineering and has been accepted as satisfactory.\\[3cm]
Supervisor’s Signature\\[1cm]
............................................\\[0.5cm]
Lecturer\\
Department of Electrical Engineering \& Computer Science\\ North South University\\
Dhaka, Bangladesh.

\newpage
\section*{Acknowledgments}
By mercy of the Almighty, we have completed our junior design project entitled “Chitter Chatter”.
Foremost, we would like to express our sincere gratitude to our advisor Rifat Ahmed Hassan (RIH) for his continuous support in our project progress throughout the whole CSE 299 course, for his patience, motivation, enthusiasm, and immense knowledge. His guidance helped us in all the time of research, writing and completing of this project.
Our sincere thanks also go to North South University, Dhaka, Bangladesh for providing an opportunity in our curriculum which enabled us to have an industrial level experience as part of our academics.
Last but not the least, we would like to thank our family as their inspiration and guidance kept us focused and motivated.
 

\newpage


\begin{abstract}
    This paper describes the motivation, design and implementation details behind a real time messaging app we have built named Chitter Chatter. Chitter Chatter is a real time messaging app by which user can easily communicate with others. 

We always had a keen interest about how messaging applications like whatsapp, messenger work, how people can efficiently communicate with each others even from different parts of the world. Also, the existing messaging apps has a vast set of cutting edge features but how many of us even user all of them in our daily usage. These vast set of features made them cutting edge but at the same time made the apps laggy and heavy for older generations phone. So we thought of why not build an app that will not only offer the necessary features of a messaging app but also will be light. That’s how the idea of Chitter Chatter came along.

We have built an app that not only looks beautiful and easy to use but also is lightweight. We used Flutter to built the frontend of the app and also to give functionality and responsiveness to the app. We have used Firebase as our backend and it just made our app building process easy and efficient by it’s rich API options. By combining these two not only we have made our app visually pleasant to look at but also gave the necessary functionalities.

Some of the key features are easy email verification, password reset, sending message, photos and emojis, sharing status, adding new users, robust searching and many more.

The goal of this app is to provide us with the knowledge of learning how real time messaging systems work and to offer a lightweight and user-friendly version of some of the existing messaging apps.

\end{abstract}
\newpage
\section*{List of Figures \& Tables}
\begin{center}
 \begin{tabular}{|l|l|l|}
\hline
\textbf{Fig. No.} & \textbf{Figure caption} & \textbf{Page No.} \\ \hline
3.2.1 & Client-Server Architecture & 5 \\ \hline
3.4.1 & Database Schema & 6 \\ \hline
Table 4.1 & Weekly Progress & 20 \\ \hline
5.1.1 & Create Account Screen & 20 \\ \hline
5.1.2 & Profile picture And Name Selection Screen & 20 \\ \hline
5.1.3 & Email Verification Screen & 20 \\ \hline
5.1.4 & Login Screen & 21 \\ \hline
5.1.5 & Password Reset Screen & 21 \\ \hline
5.1.6 & Home Page & 21 \\ \hline
5.1.7 & Profile Screen & 21 \\ \hline
5.1.8 & Help Screen & 21 \\ \hline
5.1.9 & Contact Screen & 21 \\ \hline
5.1.10 & Messaging Screen & 21 \\ \hline
5.1.11 & Status Screen & 21 \\ \hline
5.2.1 & Web Login Screen & 22 \\ \hline
5.2.2 & Web Profile picture And Name Selection Screen & 22  \\ \hline
5.2.3 & Web Password Reset Screen & 22 \\ \hline
5.2.4 & Web Email Verification Screen & 22 \\ \hline
5.2.5 & Web HomePage & 22 \\ \hline
5.2.6 & Chat Screen & 22 \\ \hline
\end{tabular}\\[.3cm]   
\end{center}

\newpage
\tableofcontents
\newpage

\section{Overview}
\pagenumbering{arabic}
\subsection{Introduction}
Real-time messaging apps revolutionized digital communication by enabling instant message transmission across devices and networks. These applications use sophisticated  technologies to deliver messages in milliseconds after they are sent, creating near-instantaneous communication experiences. Users can exchange text, multimedia, and engage in group conversations with immediate delivery and read receipts. Unlike traditional messaging methods, real-time messaging apps provide live, synchronized communication that bridges geographical distances, allowing people to connect and interact as if they were in the same physical space.


\subsection{Project Defination}
Chitter-Chatter is a real-time messaging program that allows users to communicate instantly via text, photo and emoji. The platform, which is available across both web and mobile platforms, allows for seamless chatting and includes features such as sending message, photos, sharing status. Users can easily engage with friends, family, and colleagues using a simple, intuitive interface built for quick and easy digital interaction.

\subsection{Purpose of our project/ motivation}
The motivation of this app is to provide users with a simple, user-friendly and lightweight app that allows users to seamlessly communicate with others. Although the majority of other messaging apps have a large feature set, some users who are new to messaging apps and lack technological expertise may find these programs to be bulky and even overwhelming. Our app provides a pleasing experience yet is lightweight for the little bit older generations of phones.

\subsection{Project Goal}
The goal of Chitter Chatter is to create a lightweight, user-friendly real-time messaging app that simplifies communication for users of all technical levels. Designed to be visually appealing and responsive, the app offers essential features like efficient login and registration, text, photo, and emoji messaging, status sharing, and robust search capabilities. By focusing on simplicity and efficiency, Chitter Chatter aims to deliver a seamless messaging experience while remaining accessible to users with older devices, bridging the gap between necessary functionality and everyday usability.

\subsection{Summary}
Chitter Chatter is a real-time messaging app designed to simplify communication with essential features like text, photo, and emoji messaging, status sharing, and user-friendly search. Inspired by the complexities of existing messaging apps, it addresses the need for a lightweight alternative that performs well on older devices without overwhelming users. It ensures efficiency, responsiveness, and visual appeal. The app’s goal is to provide a seamless, accessible messaging experience for users of all technical levels, bridging the gap between simplicity and functionality.



\section{Existing Systems and solution adopted}

\subsection{Introduction}
Some of the popular real-time messaging applications like WhatsApp, Facebook Messenger, and Telegram, really are on of their kind. While these platforms are feature-rich and offer cutting-edge technologies, they often face challenges such as excessive resource consumption, complexity, and lack of optimization for older devices. This section analyzes the impact of these issues on user experience and explains the solutions implemented in Chitter Chatter to address these shortcomings. 

\subsection{Existing Solutions}
Apps like WhatsApp, Facebook Messenger, and Telegram may be the best but they come with some issues:
\begin{itemize}
    \item \textbf{High Resource Usage:} Many apps are resource-intensive, leading to slower performance, especially on older devices.
    \item \textbf{Complex Features:} Overloaded with advanced features, they can overwhelm users who prefer simplicity.
    \item \textbf{Large App Size:} Excessive storage requirements make these apps less accessible for devices with limited space.
    \item \textbf{Limited Accessibility:} Heavy reliance on modern hardware excludes users with older or low-spec devices.
\end{itemize}

\subsection{Proposed Solutions}
To overcome the limitations of existing messaging apps, a set of targeted solutions is proposed:
\begin{itemize}
    \item \textbf{Lightweight Design:} Optimize the app to ensure smooth performance even on older devices by reducing resource consumption.
    \item \textbf{Essential Features Only:} Focus on core functionalities like messaging, photo sharing, and status updates, avoiding unnecessary complexities.
    \item \textbf{RResponsive UI:} Focus on creating a user-friendly, visually appealing, and responsive interface.
    \item \textbf{Compact App Size:} Optimize assets and code to ensure the app requires minimal storage space without sacrificing functionality.
\end{itemize}

\subsection{Adopted Solutions and reasons}
To address the challenges identified in existing messaging apps, Chitter Chatter adopts the following solutions, ensuring improved performance, simplicity, and user experience.
\begin{itemize}
    \item \textbf{Optimized Design:} The app is efficient for older devices, ensuring smooth performance and reduced resource usage.
    \item \textbf{Core Features Focus:} Chitter Chatter offers only essential features like messaging, photo sharing, and status updates, keeping the app simple and lightweight.
    \item \textbf{Firebase Backend:} Leveraging Firebase’s rich APIs, Chitter Chatter ensures real-time synchronization and efficient data management. This not only enhances speed and reliability but also minimizes data usage, making it a cost-effective solution.
    \item \textbf{Flutter UI:} Built using Flutter, the app delivers a visually appealing and responsive interface. The cross-platform nature of Flutter ensures consistent performance across mobile and web platforms, while its flexibility allows for a clean and intuitive user experience.
\end{itemize}

\subsection{Summary}
The section highlighted limitations of popular messaging apps, such as high resource usage, complex features, and large app size. To address these challenges, Chitter Chatter adopts targeted solutions, including compatibility for older devices, a focus on essential features, efficient real-time communication powered by Firebase, and a responsive interface built with Flutter. These measures ensure a lightweight, user-friendly app that offers seamless performance, and accessibility across diverse devices.



\section{Technical Description}

\subsection{Design Overview}
Chitter-Chatter integrates a robust UI framework with reliable backend services and secure data management. Below is an overview of its design components:
\begin{itemize}
    \item \textbf{User Interface (UI):} Built using Flutter, the app provides a cross-platform, responsive interface for both mobile and web users. The UI emphasizes simplicity, with intuitive navigation and visually appealing layouts.
    \item \textbf{Backend:} Powered by Firebase, the backend ensures real-time data synchronization and efficient handling of requests. Firebase Cloud Functions are used to manage server-side logic, enabling automation and dynamic functionality.
    \item \textbf{Database:} Firebase's Cloud Firestore, a NoSQL database, is used for real-time data storage and retrieval. The database stores user profiles, chat messages, pictures, and statuses.
    \item \textbf{Authentication:} Firebase Authentication handles all user authentication tasks, including sign-in, and registration. Email verification, password reset, and secure storage of credentials are implemented using Firebase APIs.
    \item \textbf{APIs:} Firebase APIs are used extensively for operations like authentication and data synchronization. Additional APIs are integrated for functionalities such as sending email verifications and handling forgotten passwords.
\end{itemize}
\subsection{Client-Server Architecture}
Chitter Chatter employs a robust client-server architecture to enable real-time communication and efficient data management. The client-side, developed using Flutter, provides a responsive and user-friendly interface that seamlessly interacts with the server. The server-side functionality is powered by Firebase, which handles backend operations and ensures reliable performance.
Firebase serves as the central hub for managing the app’s database, authentication, and real-time messaging. It stores user information, messages, and other data in a cloud-hosted NoSQL database, ensuring quick and scalable access. The authentication system, including sign-in, registration, email verification, and password reset, is implemented using Firebase Authentication APIs. This architecture allows the client-side application to send requests to Firebase’s backend services, which process and return data in real-time.\\
\begin{center}
  \includegraphics[width=.6\textwidth]{client.png}  \\
    Fig 3.2.1: Client-Server Architecture
\end{center}



\subsection{Database Design}
Chitter Chatter uses Firebase Cloud Firestore as its database, providing a scalable, cloud-hosted NoSQL solution for storing and managing app data.
\begin{itemize}
    \item {Users Collection:}
    \begin{itemize}
        \item Each document is identified by a unique UserId.
        \item Contains user profile information.
        \item Has two sub-collections: chatList and Stories.
    \end{itemize}
    \item {Chats Collection:} 
    \begin{itemize}
        \item Each document is identified by a unique ChatId.
        \item Contains message-related information including participants, sender, receiver, and timestamp.
    \end{itemize}
    \item {Sub-Collections of Users:} 
    \begin{itemize}
        \item ChatList: Contains chat-related metadata for each user.
        \item Stories: Stores individual story documents with date and status.
    \end{itemize}
    \item {The schema uses standard data types:} 
    \begin{itemize}
        \item string for text-based fields and also profile photo field as it is Base64 encoded.
        \item boolean for true/false states.
        \item timestamp for date and time information.
        \item array<string> for lists of items (like participants).
    \end{itemize}
\end{itemize}


\subsection{Database Schema}
\begin{center}
  \includegraphics[width=.6\textwidth]{db.png}  \\
    Fig 3.4.1: Database Schema
\end{center}

\subsection{Technology Stack}

 \subsubsection{UI Framework:}
\begin{multicols}{2}
Flutter is a cross-platform UI framework used to build Chitter Chatter’s responsive and visually appealing interface. It enables seamless development for both mobile and web platforms with a single code-base. Known for its fast rendering and customizable widgets, Flutter ensures a consistent and intuitive user experience across all devices.   

\begin{center}
  \includegraphics[width=.7\textwidth]{flutter.png} 
\end{center}
    \columnbreak
\end{multicols}
  


\subsubsection{Programming Language:}
\begin{multicols}{2}
Dart is the programming language used to develop Chitter Chatter's frontend with Flutter. Designed for client-side development, Dart offers features like a rich standard library, strong typing, and asynchronous programming, enabling smooth and efficient application performance.   

\begin{center}
  \includegraphics[width=.3\textwidth]{dart.png} 
\end{center}
    \columnbreak
\end{multicols}

\newpage
\subsubsection{Backend:}
\begin{multicols}{2}
Firebase is the backend platform for Chitter Chatter, enabling real-time communication, secure authentication, and seamless app functionality. Its APIs handle critical processes like user sign-in, registration, email verification, and password recovery. Firebase ensures efficient backend operations and enhances app performance through its powerful tools and integrations.  
\columnbreak
\begin{center}
  \includegraphics[width=.5\textwidth]{firebase.png} 
\end{center}
    
\end{multicols}
\subsubsection{Database:}
\begin{multicols}{2}
Firestore, a NoSQL database by Firebase, is used in Chitter Chatter to manage and store app data efficiently. It supports real-time data synchronization, ensuring instant updates for messages, user profiles, and statuses across devices. Firestore’s flexible structure enables dynamic data handling, while robust indexing ensures quick and efficient queries. Its security rules safeguard data access and maintain user privacy, making it ideal for scalable applications like Chitter Chatter. 

\begin{center}
  \includegraphics[width=.4\textwidth]{firestore.png} 
\end{center}
    \columnbreak
\end{multicols}

\subsection{User Interface (UI) Design}
\subsubsection{Design Principles:}
Chitter Chatter’s UI design is rooted in simplicity, accessibility, and aesthetic appeal. By adhering to minimalist design principles, the app avoids overwhelming users with unnecessary elements, creating an interface that is both functional and visually clean. Consistent use of colors, typography, and spacing establishes a cohesive visual identity. Throughout the project we tried different styles and emphasized on clarity and intuitive navigation, ensuring that users can access features easily, regardless of their familiarity with messaging apps.
\subsubsection{Responsive Layout:}
Built with Flutter, Chitter Chatter’s layout is fully responsive, adapting seamlessly to various devices, including smartphones, tablets, and web browsers. This ensures that users experience a consistent look and feel, regardless of screen size or orientation. Feature like platform-specific optimizations ensure that the app is consistent on responsiveness and aesthetics across devices, delivering a smooth experience for both mobile and web users.

\subsubsection{User Experience (UX) Considerations:}
The app prioritizes user comfort and engagement by focusing on intuitive interactions and thoughtful design elements. Icons and buttons are clearly labeled and logically placed, making navigation straightforward. Features like real-time feedback for actions, smooth transitions between screens enhance usability. Additionally, the design takes into account accessibility, ensuring the app is user-friendly for individuals with varying levels of technological expertise. This focus on UX creates a satisfying and efficient experience for all users.

\subsection{Description of the system}
\subsubsection{Registering to the app}
User will be able to register to the app with essential information like email, phone number and password. So that, user can register to the app as a user and use all the features of the app.
    \subsection*{Confirmation}
    \textbf{Success:}
    \begin{itemize}
        \item User inputs the email address. 
        \item User inputs the phone number with appropriate country code.
        \item User enters a strong password that must contain capital letters, small letters, numbers, special characters and a minimum length of 6.
        \item User re-enters the same password.
        \item User clicks on the register button to move forward in the next screen.
    \end{itemize}
    
    \textbf{Failure:}
    \begin{itemize}
        \item If user enters an email that was already registered to the app, user can not use the same email and will get an error message.
        \item If user enters a phone number that was already registered to the app, user can not use the same phone number and will get an error message.
        \item If user enters a password that does not follow the convention, user will get error message.
        \item If user re-enters a password that does not match with the previous password that was entered user will get error message.
    \end{itemize}

\subsubsection{Picking profile photo and name}
User will be able to select profile picture and name. So that, user can make their profile intuitive and distinguishable.
    \subsection*{Confirmation}
    \textbf{Success:}
    \begin{itemize}
        \item After user have provided valid information in the registration screen, user is redirected to this screen. 
        \item User clicks on the little plus icon on the profile photo selecting area.
        \item User selects a photo from the gallery.
        \item User types in the name of his choice.
        \item User clicks on the tick icon to move forward in the next screen.
    \end{itemize}
    
    \textbf{Failure:}
    \begin{itemize}
        \item If user do not pick any image and try to move on to the next screen, user will get proper error message.
        \item If user do not type in any name and try to move on to the next screen, user will get proper error message.
    \end{itemize}

    
\subsubsection{Verifying email}
Users will be able to verify their email address. So that, no one else can arbitrarily use their email address to create any account.
    \subsection*{Confirmation}
    \textbf{Success:}
    \begin{itemize}
        \item After user is done selecting their profile picture and name user can come to this screen. 
        \item User clicks on the verify button on the screen.
        \item A verification email will be sent to the provided email address.
        \item That email will contain a link and when user clicks on the link the user becomes verified.
        \item As soon as the user is verified the verify button will turn to continue button.
        \item User can click on the resend email button to get the verification email again.
    \end{itemize}
    
    \textbf{Failure:}
    \begin{itemize}
        \item If for some reason the user do not get verified even after clicking on the link the verify button will not turn into continue button and user can not move to the next screen.
        \item Then user have to click on resend email button to get the email again.
    \end{itemize}

\subsubsection{Logging into the app}
User will be able to log into their account. So that, user can use the app's features.
    \subsection*{Confirmation}
    \textbf{Success:}
    \begin{itemize}
        \item User provides his email and password. 
        \item User clicks on the login button.
        \item User logs into his account and moves to the homepage.
    \end{itemize}
    
    \textbf{Failure:}
    \begin{itemize}
        \item If user provides wrong email or password user will get appropriate error message.
    \end{itemize}

\subsubsection{Resetting password}
Users will be able to reset their password. So that, they do not have to worry about forgetting their password.
    \subsection*{Confirmation}
    \textbf{Success:}
    \begin{itemize}
        \item User clicks on the forgot password button. 
        \item User is then redirected to the forgot password screen.
        \item User provides an email address and clicks on the send email button.
        \item A password reset email is sent to the provided email address.
        \item The email will contain a link and user clicks on the link.
        \item User then redirected to another screen where he will have to type in his new password and click on save button to reset his password.
        \end{itemize}
    
    \textbf{Failure:}
    \begin{itemize}
        \item If user do not get any reset email user have to reload the screen and click on the send email button again.
    \end{itemize}

\subsubsection{Getting help for different features}
User will be able to get some walk-through for some core features of the app. So that, user can always look at the guidelines for using a features.
    \subsection*{Confirmation}
    \textbf{Success:}
    \begin{itemize}
        \item User clicks on the help icon. 
        \item User User then redirected to the help and support page where users get various guides for features.
        \item User clicks in any of them.
        \item User can see step by step guideline to use that features.
    \end{itemize}
    
    \textbf{Failure:}
    \begin{itemize}
        \item If due to connectivity issue the icon is not visible user can reload the app.
    \end{itemize}


\subsubsection{Searching through the recent chat list}
Users can search through the recent chat list to find any desired contact. So that, they do not have to scroll through the list.
    \subsection*{Confirmation}
    \textbf{Success:}
    \begin{itemize}
        \item User clicks on the search icon. 
        \item User then moved to the search page.
        \item User search users by name.
        \item User finds the desired contact or person.
        \item User clicks on that person to move into the chat screen.
    \end{itemize}
    
    \textbf{Failure:}
    \begin{itemize}
        \item If the person is not found the app will give the user proper feedback.
    \end{itemize}

\subsubsection{Logging out form the account}
Users will be able to log out from their account. So that, they can keep their account safe while login elsewhere and join from another account.
    \subsection*{Confirmation}
    \textbf{Success:}
    \begin{itemize}
        \item User clicks on the logout icon. 
        \item User then logged out from his account and moves to the login screen.
    \end{itemize}
    
    \textbf{Failure:}
    \begin{itemize}
        \item If due to connectivity issue the icon is not visible user can reload the app.
    \end{itemize}

\subsubsection{Changing profile information}
Users will be able to edit their profile information. So that, they can make necessary changes whenever they find it necessary.
    \subsection*{Confirmation}
    \textbf{Success:}
    \begin{itemize}
        \item User clicks on the user's profile picture or name on the homepage. 
        \item User then redirected to the profile screen.
        \item User can edit their name, phone number or profile photo.
        \item User clicks on the save changes button.
        \item User's profile info changed.
    \end{itemize}
    
    \textbf{Failure:}
    \begin{itemize}
        \item If user keep any of the field blank user will get appropriate error message and can not change the profile information.
    \end{itemize}

\subsubsection{Displaying recent chat list}
Users will be able to see the recent contacts who they are connected with. So that, they can quickly find users who they have made a conversation with.
    \subsection*{Confirmation}
    \textbf{Success:}
    \begin{itemize}
        \item In the home page under the chats tab user finds the recent chat list. 
        \item This are the users who are connected to the current user.
        \item User clicks on any of the users.
        \item User redirected to the chat screen of that contact.
    \end{itemize}
    
    \textbf{Failure:}
    \begin{itemize}
        \item If due to connectivity issue the list is not shown, user will see loading indicator or proper feedback.
    \end{itemize}
    
\subsubsection{Deleting user from the chat list}
Users will be able to delete any of the contact in the chat list. So that, they can remove unwanted contacts.
    \subsection*{Confirmation}
    \textbf{Success:}
    \begin{itemize}
        \item User clicks on the bin icon on the right side of each contacts. 
        \item User gets a pop-up confirmation screen.
        \item User clicks on delete and that contact is deleted from the chat list.
        \item User clicks on cancel, the app will do nothing.
    \end{itemize}
    
    \textbf{Failure:}
    \begin{itemize}
        \item If the contact is not deleted on first try user can reload the app to check if the contact is deleted or not.
        \item If the contact is not deleted then user have to repeat the same process again.
    \end{itemize}

\subsubsection{Finding saved contacts}
Users will be able to see contacts which are saved on their mobile phones. So that, they can add a new user by saving his contact number on their mobile.
    \subsection*{Confirmation}
    \textbf{Success:}
    \begin{itemize}
        \item User clicks on the green button on the bottom right corner of the screen. 
        \item User then redirected to the contacts page where all the contacts which are saved in the users mobile phone will be shown.
        \item User clicks on any of the contact.
        \item User goes to that contact's chat screen.
        \item If that contact was not already present in the recent chat list, the user will be added to the recent chat list.
    \end{itemize}
    
    \textbf{Failure:}
    \begin{itemize}
        \item If user clicks on a contact that is not registered in the app the user will see appropriate error message like "The contact is not registered in the app".
    \end{itemize}

\subsubsection{Searching saved contacts}
Users will be able to search contacts which are saved on their mobile phone. So that, they can find a specific contact quickly by just writing the name of the user.
    \subsection*{Confirmation}
    \textbf{Success:}
    \begin{itemize}
        \item User clicks on the search icon in the top right corner in the contacts page. 
        \item User then redirected to the search page.
        \item User types in the name of the user.
        \item User finds the user.
        \item User can click on that user to move to that chat screen if that user is registered in that app.
    \end{itemize}
    
    \textbf{Failure:}
    \begin{itemize}
        \item If no user found of that name user will get feedback like "No user found."
        \item After finding the contact when user clicks on the contact and if that is not registered in the app the user will see appropriate error message like "The contact is not registered in the app".
    \end{itemize}

\subsubsection{Viewing active status}
Users will be able to see if the other user is online or offline also when the user was last seen. So that, they can know when to actively participate in a conversation or leave a message for future reference.
    \subsection*{Confirmation}
    \textbf{Success:}
    \begin{itemize}
        \item User can see other user's active status just below the user's name. 
        \item When user is in the chat screen the status indicator will turn green meaning the user is online.
        \item If any user leaves the chat screen the indicator will turn Grey meaning offline.
        \item User can also see when the user was last active.
    \end{itemize}
    
    \textbf{Failure:}
    \begin{itemize}
        \item If the indicators are not updated due to connectivity issue user have to restart the app.
    \end{itemize}

\subsubsection{Sending message}
Users will be able to send message to other users. So that, they can actively communicate with others.
    \subsection*{Confirmation}
    \textbf{Success:}
    \begin{itemize}
        \item User types in message in the input text field in the chat screen. 
        \item User clicks on the send button on the right side of the text input field.
        \item The message is sent.
    \end{itemize}
    
    \textbf{Failure:}
    \begin{itemize}
        \item If due to connectivity issue the message is not send user can check his connection or restart the app, as message will not be sent.
    \end{itemize}

\subsubsection{Sending emoji}
Users will be able to send emojis to other users. So that, they can make their chatting experience fun.
    \subsection*{Confirmation}
    \textbf{Success:}
    \begin{itemize}
        \item User clicks on the emoji icon in the left most side in the input text field. 
        \item User gets various kinds of emojis.
        \item User clicks on the emojis and then click on the send button to send the emojis.
    \end{itemize}
    
    \textbf{Failure:}
    \begin{itemize}
        \item If there is connectivity issue the emojis will not load. User have to fix the connectivity issue first.
    \end{itemize}

\subsubsection{Sending pictures}
User will be able to send pictures to other users. So that, they can express themselves better and send pictures to others.
    \subsection*{Confirmation}
    \textbf{Success:}
    \begin{itemize}
        \item User clicks on the attachment icon just to the right of the emoji icon in the input text field. 
        \item User can select pictures from the gallery.
        \item User clicks on the picture and the picture is sent.
    \end{itemize}
    
    \textbf{Failure:}
    \begin{itemize}
        \item If there is connectivity issue the pictures in gallery will not load. User have to fix the connectivity issue first.
    \end{itemize}

\subsubsection{Indication of unread message}
Users will be able to know if they have unread messages. So that, they can respond to messages that they have not read yet.
    \subsection*{Confirmation}
    \textbf{Success:}
    \begin{itemize}
        \item User gets a new message. 
        \item The chat gets a blue indicator on the profile picture and the chat is highlighted.
        \item User clicks on the chat.
        \item User reads the message.
        \item The indicator disappears.
    \end{itemize}
    
    \textbf{Failure:}
    \begin{itemize}
        \item If the user can not see the indicator instantly user may have connectivity issue. User can reload the app.
    \end{itemize}
    
\subsubsection{Searching messages}
Users will be able to search old messages. So that, they can quickly locate specific details shared in past conversations.
    \subsection*{Confirmation}
    \textbf{Success:}
    \begin{itemize}
        \item User clicks on the search icon on the rightmost corner of the chat screen 
        \item User then redirected to the search screen.
        \item User types in the message.
        \item User finds the searched message.
    \end{itemize}
    
    \textbf{Failure:}
    \begin{itemize}
        \item If the searched message does not exists, user will see appropriate messages like "No messages found".
    \end{itemize}

\subsubsection{Sharing notes}
Users will be able to share short texts on the app. So that, they can share thoughts, announcements, or simple messages without starting a full conversation.
    \subsection*{Confirmation}
    \textbf{Success:}
    \begin{itemize}
        \item User clicks on the status tab in the homepage. 
        \item User redirected to the status screen where user can see short notes shared by other users as well as by him.
        \item User clicks on the plus(+) button on the left most corner of the status screen.
        \item User clicks on the plus icon.
        \item A text field will appear and user can type in a short note, maximum length of 250 characters.
        \item User clicks on the share button to share the note among all other users.
    \end{itemize}
    
    \textbf{Failure:}
    \begin{itemize}
        \item If the user can see the uploaded note instantly user might have some connectivity issue and have to send the status again.
    \end{itemize}

\subsection{Authentication And Security}
\subsubsection{User Registration:}
    \begin{itemize}
        \item Users provide a unique email, phone number, and password during registration.
        \item The app checks the uniqueness of the email through firebase authentication and phone number through firestore query, triggering an error if duplicates are found.
        \item Passwords must meet specific criteria: uppercase, lowercase, numbers, special characters, and a minimum length of 6 characters.
        \item After registration, an email verification process is triggered, requiring users to verify their email before logging in.
    \end{itemize}

\subsubsection{Email Verification:}
    \begin{itemize}
        \item After registration, Firebase sends a verification email with a confirmation link.
        \item The user must click the link to verify their email, ensuring account validity.
        \item Users cannot go to login screen until the email is verified, adding an extra layer of security.
    \end{itemize}
\subsubsection{ Login Process:}
    \begin{itemize}
        \item Users must log in with their email and password.
        \item Firebase Authentication checks the credentials and allows access if they match.
        \item If the user provides incorrect credentials, an error message is displayed, notifying them of the invalid email or password.
    \end{itemize}
\subsubsection{ Password Storage and Security:}
    \begin{itemize}
        \item Passwords are stored securely in Firebase Authentication using hashed encryption, ensuring that they are never stored in plain text.
        \item Firebase uses advanced encryption algorithms like SCRYPT to hash passwords, making it computationally infeasible to retrieve the original password.
    \end{itemize}

\subsubsection{User Data Storage:}
    \begin{itemize}
        \item Firebase Authentication handles storing email, and password.
        \item Sensitive data is stored securely, and only hashed passwords are kept in Firebase's database.
        \item Additional user information, such as phone number, profile details and preferences, are stored in Firebase Firestore, with strict security rules to control access.
    \end{itemize}
\subsubsection{Security Measures:}
    \begin{itemize}
        \item SSL/TLS encryption ensures secure data transmission during authentication processes.
        \item Firebase Security Rules protect user data in Firestore, limiting access based on authentication status and user permissions.
    \end{itemize}



\section{Project Progress}
\begin{center}
 \includegraphics[width=.7\textwidth]{week.png}\\[0.5cm]
  \textsc{ Table 4.1: Weekly Progress}\\[0.5cm]   
\end{center}




\section{Result and Discussions}

\subsection{App}
\begin{multicols}{3}

\begin{center}
  \includegraphics[width=.2\textwidth]{reg.jpg} \\
  Fig 5.1.1: Create Account Screen\\
  \includegraphics[width=.2\textwidth]{user info.jpg}\\
  Fig 5.1.2: Name Selection Screen\\
  \includegraphics[width=.2\textwidth]{email.jpg}\\
  Fig 5.1.3: E.V. Screen\\
  \includegraphics[width=.2\textwidth]{login.jpg}\\
  Fig 5.1.4: Login Screen\\
  \includegraphics[width=.2\textwidth]{forgot pass.jpg}\\
  Fig 5.1.5: Password Reset Screen\\
  \includegraphics[width=.2\textwidth]{homepage.jpg}\\
  Fig 5.1.6: HomePage\\
  \columnbreak
  \includegraphics[width=.2\textwidth]{profile.jpg}\\
  Fig 5.1.7: Profile Screen\\
  \includegraphics[width=.2\textwidth]{help.jpg}\\
  Fig 5.1.8: Help Screen\\
  \includegraphics[width=.2\textwidth]{contact.jpg}\\
  Fig 5.1.9: Contact Screen\\
  \includegraphics[width=.2\textwidth]{message.jpg}\\
  Fig 5.1.10: Messaging Screen\\
  \includegraphics[width=.2\textwidth]{status.jpg}\\
  Fig 5.1.11: Status Screen\\
\end{center}
    
\end{multicols}
\newpage
\subsection{Web}
\begin{multicols}{2}

\begin{center}
  \includegraphics[width=.4\textwidth]{weblogin.png} \\
  Fig 5.2.1: Login Screen\\
  \includegraphics[width=.4\textwidth]{web user info.png}\\
  Fig 5.2.2: Info set screen\\
  \includegraphics[width=.4\textwidth]{web forgot password.png}\\
  Fig 5.2.3: Password Reset Screen\\
  \columnbreak
  \includegraphics[width=.4\textwidth]{web email ver.png}\\
  Fig 5.2.4: E.V Screen\\
  \includegraphics[width=.4\textwidth]{web home.png}\\
  Fig 5.2.5: HomePage\\
  \includegraphics[width=.4\textwidth]{web chat.png}\\
  Fig 5.2.6: Chat Screen\\
 
\end{center}
    
\end{multicols}
\newpage
\subsection{Future Consideration}
Chitter Chatter aims to evolve into a comprehensive real-time communication platform with several advanced features planned for future updates. Group messaging will enable users to interact and collaborate in dedicated chat rooms, fostering a sense of community. End-to-end encryption will be implemented to ensure that all conversations remain private and secure, protecting user data from unauthorized access. File sharing functionality will allow users to exchange documents, videos, and other media seamlessly. Additionally, audio and video calling features will provide a more interactive and engaging communication experience, making Chitter Chatter a versatile and all-in-one messaging solution.

\section{Conclusion}
Chitter Chatter represents a streamlined and efficient approach to real-time messaging, combining essential features with a lightweight design. By leveraging Flutter for a responsive UI and Firebase for backend functionality, the app delivers a user-friendly experience that is accessible across devices. Core features such as email verification, password security, and intuitive navigation ensure reliability and ease of use, while robust authentication and data security measures prioritize user privacy. The app addresses common issues in existing platforms, offering a fast and seamless alternative suited to diverse user needs. With plans to introduce advanced features like group messaging, end-to-end encryption, file sharing, and audio/video calling, Chitter Chatter is positioned to grow into a versatile communication tool. This project underscores the integration of cutting-edge technologies to create a scalable, secure, and user-focused messaging app, meeting both current demands and future expectations.

\newpage
\section{GitHub Link}
Here is the link of our GitHub project repository.\\
\url{https://github.com/whowasif/ChitterChatter-299-project.git}

\fontsize{10}{15}\selectfont
\section{References}

[1] Flutter and dart Tutorial, "Flutter \& Dart Tutorial for Beginners," YouTube, Apr. 15, 2020. Available: \url{https://www.youtube.com/watch?v=VPvVD8t02U8}.\\

[2] Flutter Documentation, "Learn Flutter: Get Started with Fundamentals," Flutter Official Documentation. Available: \url{https://docs.flutter.dev/get-started/fundamentals}. \\

[3] Firebase Fundamentals, "Firebase Full Course – Learn Firebase for Web, iOS, Android," YouTube, Aug. 10, 2021. Available:\url{https://www.youtube.com/watch?v=fgdpvwEWJ9M&t=4s}.\\

[4] Dart Basics, "Dart Cheat Sheet," Dart Official Documentation. Available: \url{https://dart.dev/resources/dart-cheatsheet}.  



\end{document}
