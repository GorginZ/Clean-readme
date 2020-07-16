

# **T3A3 Part A**



------



## Purpose

We were tasked with creating a website for a client who owns a home-cleaning business. The purpose of our app was to fulfill the clients criteria with respect to design and functionality.

The site was to be easily accessible by all users,  it was to have a clean design that communicated all information regarding services effectively. Acessability and easy straight-forward booking process are a core focus.

#### **Functionality / features**

Automatic quote generation.

This is the cornerstone of our app. This service will be displayed on the landing page. Users select how many bedrooms, bathrooms and wil see the price of the service instantly reflected in a quote. 

 

#### **Scheduling**

Users choose a time and date for their service and can set up recurring services. 



#### **Pre-paid with Stripe checkout**

Users pay the amount they were quoted. This feature encourages and gives ease of mind when signing up for a one off or recurring service and helps the business take on more regular customers. 

We have implemented stripe checkout for this feature of our app, which is a third party service that handles all the security, and other problems associated with using credit cards over the internet. Once the user has selected all their desired variables(Time/day, cleaning pack, etc) we will prompt them to checkout, which will take them to a separate page in which they can enter their card details and process the payment.

 

#### **Cleaner user profiles**

This is a place where the clients can get to meet the team that will be helping them out! We have a profile page for some of the employee's which will contain a small bio about the cleaner. This is to convey the reliability and familiarity of the service. 

 

#### **Authentication**

Customers do not need to log in to get a quote, customers will need to create an account if they are going to confirm a service and become a regular customer.  Signing in will allow them to access their current service plan, and change their plan or scheduled times.

 

#### **Images**

Profile pictures for the cleaners will be stored by using amazon's S3 cloud hosting service, *(we will also allow customers to upload photos with their comments.)

 

#### **Target audience**

The target audience for our clients app can be described as "Anybody that lives in a home" as anybody that lives in a house could be somebody that would use the service, however we have given special consideration to ensuring the app is accessible and inclusive with respect to accessability of the app itself and in our understanding of user-stories. Whether they're old and retired, young and busy, single mums, big family, injured and need help, air bnb needs a clean before next guest the app is targeting homes broadly. 

 

## **Tech stack**

 

#### **Deployment**



\- Heroku(API)

\- Netlify(Client)

\- Puma(Local)

\- Github(Linked to netlify/heroku)

 

**Source control**

 

\- Git

\- Github

 

**Gems / Libraries**

 

****

**Other**

 

\- Ruby (Code-Base)

\- Javascript (Code-Base)

\- HTML (Code-Base)

\- CSS (Styling)

\- VScode (Writing code)

\- Rails(Ruby framework)

\- React(Javascript library)

 





<img src="docs/r1.png" width="800">



<img src="docs/data-flow-diagram.png" width="800">







------

1. User enters webpage.

2. User uses the tools on the front page to generate a quote.

3. User follows the prompts to create the appointment.

4. Before finalising the payment the system will check if the user is logged in.

5. If not logged in, the user will be prompted to log in, or create an account.

6. The user data is then stored in our database

7. Once logged in, the user will be redirected to the finalise payment page.

8. The user finalises their payment and the data is then stored in our database.

9. The user can then access all past, current or future appointments(events).




**R2**




<img src="docs/r2.png" width="800">





<img src="docs/Untitled Diagram-3.png" width="800">






**R3**



<img src="docs/r3.png" width="800">



 

\## R4 User stories

 

\1. Julie is a single, working mum with 2 kids and doesn't have time for cleaning with her busy lifestyle, she needs the option to have consistent affordable cleaning performed in her house!

 

\2. Amanda and Simon are partners living together and both working full time with no kids, we clean up after ourselves but don't have the time to do deep cleaning, we want to have the choice to just get the deep cleaning done!

 

\3. Keith and Sue are elderly and retired, they don't have the energy to clean their house anymore, they also don't make much mess. They would like to have the physically taxing cleaning done in their house(vacuuming, mopping, etc)!

 

\4. John has allergies and would like the option for the cleaners to use eco-friendly and hypo-allergenic cleaning materials.

 

\5. Sally has a visual impairment, it is important that the website is accessible to her even if she can’t see the screen.

 

\6. Kate runs a successful AirBNB business and doesn't have the time to clean the houses anymore, she would like to be able to book multiple houses for regular cleaning.

 

\7. Mike is a single adult working full time and studying, he doesn't have time to clean and wants to be able to quickly and easily choose the right cleaning service.

 

\8. Peter is an elderly man living alone, he is not very tech savvy and needs a website that is easy to navigate and would like to be able to request help if he has a problem.

 

\9. Keith has a physical impairment, it is important that he is able to use the website to its fullest functionality.

 

\10. Zoe has several houses, she would like the flexibility to have multiple services ongoing for the different houses(all under 1 account).

 

\11. Jacob is moving houses and doesn’t need a regular cleaning service, he is excited that he can book a 1 time clean without making an account.

 

\12. Micah is an admin at "Man with a Broom" it is important to him to be able to edit/remove any reviews that are misleading or inappropriate.

 

-Revision and Refinement

 

In revising our user stories we found that we needed to change our stories to better align with our values and MVP. In particular we wanted our user stories to be inclusive and representative of all people who would seek these services. It was important for us that these reflect the needs and expectations of all different parts of the community. Accessibility is likely a key pillar for a house-cleaning business concept and it is important for us that this also informs our discussions and decisions regarding site navigation.

 

In terms of refinement, we started with broader features, as well as less emphasis on accessibility, we wanted to focus more on the MVP features of our product, as well as putting a strong emphasis on accessibility. We changed our user stories to better reflect these ideals.

 





**R4**



<img src="docs/r4.png" width="800">







**R5**



<img src="docs/r5.png" width="800">



<img src="docs/erd.png" width="800">


```
Project Man_with_a_Broom {
  database_type: "PostgreSQL"
}

Table user {
  id bigint pk
  username text
  email text
  password encrypted_password

}

Table user_address {
  id bigint pk
  street_address text
  state text
  post_code encrypted_password
  event fk
  
}

Table booking_service {
id bigint pk
  service_id fk
  booking_id fk
  time interger
  quantity integer
}
Table service {
id bigint pk
 title string
 price integer
}
Table booking {

id bigint pk
user_id integer
user_address_id bigint pk
date_of date
price integer
}

Table event_meta {
  id bigint pk
  event_id fk
  meta_key bigint
  meta_value bigint
}
Table event {
  id bigint pk
  address fk
  time datetime

}




Ref: "user"."id" < "user_address"."id"

Ref: "user_address"."id" < "booking"."user_address_id"

Ref: "user"."id" < "booking"."user_id"

Ref: "booking_service"."service_id" > "service"."id"

Ref: "booking"."id" < "booking_service"."booking_id"

Ref: "user_address"."event" < "event"."id"
```



