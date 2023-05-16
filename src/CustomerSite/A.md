A. Startup 

1. JWT not present, OpenId is implemented
2. services
            .AddTransient<IClaimsTransformation, CustomClaimsTransformation>()
            .AddScoped<ExceptionHandlerAttribute>()
            .AddScoped<RequestLoggerActionFilter>()
3. InitializeRepositoryServices


B. Views, 
    I.      Home
            1. Index.html => _LandingPage => Partial RazorPage
            2. @page not used? how's this razor page working then ?
            3. SubscriptionParameters => Is this to add more fields to the Landing page ? 
            4. To send or call the Mulesoft API, we need to implement something in the SubscriptionOperation method
            5. method has 4 params, but we are sending 3 i/o params, how is it working ?
            6.  a. Index.cshtml => used _Landingpage
                b. Privacy => for privacy
                c. ProcessMessage => In b/w landing page kinda page, c => g can load all subscriptions
                d. SubscriptionDetail => Change plan
                e. SubscriptionLogDetail => Reads from Sub Logs, SubscriptionAuditLogs
                f. SubscriptionQuantityDetail => Change quantity
                g. Subscriptions => All Subscriptions
    II.     Shared
    III.    _ViewImports
    IV.     _ViewStart    

C. Controllers,
    I.      Webhook
            1. AzureWebhookController => This is like entry point for the webhook calls. must be a html page calling these. 
    II.     AccountController => SignIn => redirects thru AuthenticationProperties, SignOut, SignedOut
    III.    BaseController => this is used in HomeController, 
    IV.     HomeController => everything related to the landing page, always authenticated

D. WebhookHandler,

E. CustomerSite.csproj

F. 


QUESTIONS: 
1. Do we need to send emails from the Landing Page / Azure ? need SMTP details
2. Do we need to block any action for the time being? there is a config we can set to reject the webhook api 
3. 
