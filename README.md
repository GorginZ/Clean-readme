

# **T3A3 Part A**



------



## Purpose

We were tasked with creating a website for a client who owns a home-cleaning business. The purpose of our app was to fulfill the clients criteria with respect to design and functionality.

The site was to be easily accessible by all users,  it was to have a clean design that communicated all information regarding srevices effectively. Acessability and easy straight-forward booking process are a core focus.

#### **Functionality / features**

Automatic quote generation.

This is the cornerstone of our app. This service will be displayed on the landing page. Users select how many bedrooms, bathrooms and wil see the price of the service instantly reflected in a quote. 

 

#### **Scheduling**

Users choose a time and date for their service and can set up recurring services. 



#### **Pre-paid with Stripe checkout**

Users pay the amount they were quoted. This feature encourages and gives ease of mind when signing up for a one off or recuring service and helps the business take on more regular customers. 

We have implemented stripe checkout for this feature of our app, which is a third party service that handles all the security, and other problems associated with using credit cards over the internet. Once the user has selected all their desired variables(Time/day, cleaning pack, etc) we will prompt them to checkout, which will take them to a separate page in which they can enter their card details and process the payment.

 

#### **Cleaner user profiles**

This is a place where the clients can get to meet the team that will be helping them out! We have a profile page for some of the employee's which will contain a small bio about the cleaner. This is to convey the reliability and familiarity of the service. 

 

#### **Authentication**

Customers do not need to log in to get a quote, customers will need to create an account if they are going to confirm a service and become a regular customer.  Signing in will allow them to access their current service plan, and change their plan or scheduled times.

 

#### **Images**

Profile pictures for the cleaners will be stored by using amazon's S3 cloud hosting service, *(we will also allow customers to upload photos with their comments.)

 

#### **Target audience**

The target audience for our clients app can be described as "Anybody that lives in a home" as anybody that lives in a house could be somebody that would use the service, however we have given special consideration to ensuring the app is accessible and inclusive with respect to acessability of the app itself and in our understanding of user-stories. Whether they're old and retired, young and busy, single mums, big family, injured and need help, air bnb needs a clean before next guest the app is targeting homes broadly. 

 

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
<img src="docs/Wireframes/Homepage-web.png">

**<u>Website</u>**

- The design contains white space on the left and right side throughout the website to allow for mobile design
- Each section of the website will either have an image or color blocked background to allow for contrast and maintain the color theme 
- Website is a single page scroll down site to ensure users can easily find out more before clicking on links 

**<u>Navbar</u>**

This website has a non-fixed navigation bar at the top of the page which allows easy access for the user. It is non-fixed to add to the asthetic of the website.

- The logo on the navber will allow users to access back to the homepage regardless of which page they are on
- The same Navbar is featured on most pages (except the form), allowing for persistant design 
- Highlights the most important links to the user - about me, services and login 
- Telephone number available just the situation customer wants to directly call the company to find out more information

**<u>Hero Image/Quotation</u>**

- A quick, simple quotation system allows users to find out how much it will cost to clean their house. 
- Quotation Function: To provide users with an immediate, approximate quotation dependent on their home. This is the most important aspect of the website hence displayed as the first item on the landing page. Price will be updated accordingly. 
- The first section of the website will include a background cover image which will take up approximately 85% of the front page, leaving room for the nav bar and a little bit of the section below. This was a concious decision as it will allow users to know that there is more information below the landing page image, prompting them to scroll down the website to find out more about the company. 

- Catch phrases that embody our company- peace of mind, cleaning checklist, eco-friendly products (which will be more clearly explained in the about me / services section)
  - Peace of mind - Housekeepers have had police checks done 
  - Cleaning checklist - thorough checklist to ensure all cleans are consistent
  - Eco-friendly products - safe for children, great for environment, may possibly reach a larger demographic of clients

**<u>About the Company</u>** 

- Second section of the website will provide a small insight for the user, emphasizing on family business. 
- Button allows clients to find out more on the company 

**<u>Services</u>** 

- The third section will provide quick snapshot of why users should invest their money into a cleaning company's service.
- Utilising cards and simple icons images to highlight and simplify the point

**<u>Reviews</u>**

- The fourth and last section of out website will contain client reviews. We have selected the arrows on the side to allow users to scroll through the different reviews and notify them there are more. 
- Reviews utilised to help gain customers trust and verify our excellent service from external sources of information 

**<u>Footer</u>**

- The foot bar contains the company details, social media icons and terms and conditions. 

- Social media icons for the user to find out more about us through the different mediums

- Online booking link functions as a link to the booking form, allowing user to access immediately rather than scrolling to the top of the page 

- Foot bar is present on most pages(except for the form), allowing for consistent design 

  

<img src="docs/Wireframes/Homepage-mobile.png">



**About Us page** 
<img src="docs/Wireframes/Aboutus-web.png">
<img src="docs/Wireframes/Aboutus-mobile.png">





**Services Page**

<img src="docs/Wireframes/Services-web.png">
<img src="docs/Wireframes/Services-mobile.png">

**Users are able to start the booking process then they press the booking from $XX button which will redirect to the below form:**
<img src="docs/Wireframes/Form1-web.png">
<img src="docs/Wireframes/Form1-mobile.png">
<img src="docs/Wireframes/Form2-web.png">
<img src="docs/Wireframes/Form2-mobile.png">
<img src="docs/Wireframes/Form3-web.png">
<img src="docs/Wireframes/Form3-mobile.png">

**After the stripe payment page, users are redirected to this page:**

<img src="docs/Wireframes/confirmation.png">

**Login Page**

Allows users to access their personal home page which contains details of their purchases and schedule of cleans
<img src="docs/Wireframes/login.png">

**Welcome Page**
<img src="docs/Wireframes/welcomepage.png">

**My Bookings (accessed from nav bar or welcome page)**
<img src="docs/Wireframes/allbookings.png">
<img src="docs/Wireframes/singleshowpagebooking.png">
<img src="docs/Wireframes/editbooking.png">
<img src="docs/Wireframes/userdetail.png">
<img src="docs/Wireframes/usereditpage.png">
<img src="docs/Wireframes/userpurchases.png">
<img src="docs/Wireframes/userpurchasessingle.png">
<img src="docs/Wireframes/TCpage.png">





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



