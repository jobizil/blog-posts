# Deploying and Hosting a Custom Domain on Vercel

## Deploying and Hosting a Custom Domain on Vercel

>In this article, I will show you how to host a vanilla JavaScript application on [Vercel](https://vercel.com) and also how to use a custom domain from [Namecheap](https://namecheap.com).

## Getting Started
- To get started with this tutorial, we'll need a [Namecheap](https://www.namecheap.com/myaccount/signup/ "Namecheap's Signup Page") account, a [Github](https://github.com "Github's Homepage") account and a [Vercel](https://vercel.com "Visit Vercel's Homepage") account.
- You can get an HTML template for this tutorial [here](https://themes.3rdwavemedia.com/bootstrap-templates/free/  "Free Templates"). If you have your own HTML application you can use it too. _The goal is to successfully host our application on Vercel and set a custom domain from Namecheap._

> Note 🖊️: It is assumed that you have prior knowledge on how to use  [Git](https://git-scm.com/) and also understand how Github works. If not see this [article](https://product.hubspot.com/blog/git-and-github-tutorial-for-beginners) for a guide.

### Account Registration
- Navigate to Namecheap's [sign up](https://www.namecheap.com/myaccount/signup/ "Namecheap's Signup Page") and register a new account and confirm your account registration.
Once the account registration is completed, purchase your preferred [domain](https://www.namecheap.com/domains/) on Namecheap.

- Goto Github registration page and [register](https://github.com/signup "Github signup page") an account with them (if you don't already have one).
  - Create a new repository and call it any name you want. _I'll name mine `my-resume`._
  - Clone the repository into your machine where you have your code and then push it to your newly created repo.  
  
  ![Deployed code to repo](https://i.imgur.com/NXXwPv6.png "Deployed code to Github Repo" )
  _See this [article](https://guides.github.com/activities/hello-world/) on how to use Github._

On successfully pushing your code to Github, we'll have to create an account with [Vercel](https://vercel.com "Visit Vercel's Homepage") for our code deployment
- Navigate to the Vercel registration page and [register]() an account with them. You can register with their Github OAuth or another method pleasing to you.
  - On successful registration, click on the new Project option   
  
  ![Create Project](https://i.imgur.com/6AQqMm8.png "Create Project" )  
  On selecting the create Porject option, you can now import a project from your Github repository.  
  
  ![Import Repository](https://i.imgur.com/11x2blS.png?1 "Import Repository")
  
   - Select your vercel Scope (Account type ) usually it's single unless you are deploying for a team.
   
    ![Vercel Scope](https://i.imgur.com/r5VRaMR.png "Vercel Scope")
  - Select the project root folder
    
   ![Select Project root](https://i.imgur.com/keb5UL9.png "Select Project root") 
   
   - Name your project and deploy.
  ![Rename Project](https://i.imgur.com/4V1pTRy.png "Deploy Project" )

> Once your project has been deployed, you can visit it with the URL provided (so you see what you have deployed). Afterall, we'll use our custom domain from Namecheap.

- In your vercel app, click the `open dashboard` option to see an overview of your project.

- Select the `View Domains` option and inset the domain name you registered on namecheap

![View Domains](https://i.imgur.com/4L6qZOp.png "View Domains Option")
![Add Domain](https://i.imgur.com/9IWbx03.png "Add Domain")

- Select the `Edit` button on one of the domains inserted to view its configuration

![Edit Domain](https://i.imgur.com/NXFXZ1u.png "Edit Domain")

- Select `View DNS Records` and copy either the nameserver or the `A Records provided` 

![Imgur](https://i.imgur.com/Xl1pbne.png)

### Back to Namecheap

- Go to your dashboard and select `Domain List`  and click on `manage`

![Domain List](https://i.imgur.com/OBtXO5z.png "Select manage from domain")

- Select `Advanced DNS` and in the `Host Records` input the `A Record` and `CNAME Record` details from Vercel. 

![Advanced DNS](https://i.imgur.com/iKPQCF9.png "Advanced DNS")

- Wait for about 20 - 30 minutes for the record to provision.
- Finally, go back to your Vercel project and test out your new personalized domain.

It Works!!! ✅✅✅

> Now you no longer have to use subdomains whenever you deploy your application 

>In my next article, I'll talk about how to **Host a NodeJS API on [Heroku](https://heroku.com)**.


>If you like my content, kindly drop a ❤️ as this encourages me to do more and makes me feel I'm not alone in this space.  
 Let's connect on [Twitter](https://twitter.com/jobizil).


