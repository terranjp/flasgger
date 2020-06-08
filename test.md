    ## Authenticate a q user.

    If **action**="checkin".
    The CompanySubscription table will be checked for the api_key, and that the
    record associated with teh api_key is True.

    The current date will be verified to between the subscription_start and subscription_end dates
    in the Subscription table, and the status will be validated to be 'active'.

    The SubscriptionModule table will be checked for the given module.

    The WhiteList table will be checked for the company_name, the module_name, and the user_name.

    The SeatsLogin table be checked to see if the user is currently checked in. If the user is logged in
    the updatetime will be updated to the current time, if user is not logged in the number of seats are checked to ensure
    there are seats open for the user. If seats are open the user is checked in.

    1. Test
    2. Test