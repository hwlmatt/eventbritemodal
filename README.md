# eventbritemodal
Adding the eventbrite modal to a list of events on a single page

This takes an array of event objects and creates the buttons and modal for them. Used this in the footer code injection section of a squarespace site to add a list of events and have them all open with the eventbrite cart modal.

**An event object is:**

    { 
        city: "name of city",
        urlPart: "custom subdomain for event",
        id: "numerical id of event"
    }

**event.city** is used for button text, and for link text for the no JS fallback

**event.urlPart** is used for the no JS fallback href - this is set in the eventbrite dashboard when you create a custom url for the event, and follows the *https://[YOU CUSTOM ENTERED NAME].eventbrite.com* pattern

**event.id** is the numerical id of the event - this is appended to the end of event uri in the address bar when viewing event page

**To Add to a Squarespace site:**
After replacing the events array with one containing objects of your events, on your Squarespace page add a code block element and add this to it:
 
    <div id="eventsJS"></div>
 
 Then navigate to the main settings area, select the Code Injection setting for Footer, and add everything between and including the two sets of script tags. 
 
    <script src="..."></script>
    <sript type="text/javascript">
            ...
    </script>
