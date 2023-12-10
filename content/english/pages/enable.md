---
title: "Enable Dialpine"
# meta title
meta_title: ""
# meta description
description: "This is meta description"
# save as draft
draft: false
---

 <script>
    function redirectToUrl(isProd) {
      // Get the selected timezone value
    //   var selectedTimezone = document.getElementById('timezone').value;

    // Construct the URL with the timezone as a query parameter

    // alert('"'+document.getElementById('timezone').value+'"')
    // alert('TOS : "'+document.getElementById('tos').checked+'"')
    var ALERT_HDR = 'Headsup \u2022 Please fix these before proceeding\n'
    var errorAlert = ALERT_HDR
    if(document.getElementById('timezone').value === "")
    {
        errorAlert +='\nYou need to select your timezone before moving forward'
    }

    if(document.getElementById('tos').checked === false)
    {
        
        errorAlert +='\nYou need to agree to Dialpine TOS before moving forward'
    }
    if(errorAlert !== ALERT_HDR)
    {
        
        alert(errorAlert)
        return false   
    }
    // alert(errorAlert)


      var url = ''

      if(isProd)
      {
        url = 'https://accounts.google.com/o/oauth2/v2/auth?client_id=791779533011-soqa9gdjtvt7l2kb7vuv1pnfvt8uan9t.apps.googleusercontent.com&access_type=offline&scope=https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fuserinfo.email%20https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fuserinfo.profile%20https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fcontacts%20https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fcalendar&response_type=code&redirect_uri=https%3A%2F%2Fwww.dialpine.com%2Fgredr&state='
        // ?timezone=' + encodeURIComponent(selectedTimezone);
        
      }
      else
      {
        // url = 'https://f1vawp0e5b.execute-api.us-west-2.amazonaws.com/develop/lam-bk-googlework-api/init?state='

        url = 'https://accounts.google.com/o/oauth2/v2/auth?access_type=offline&scope=https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fuserinfo.email%20https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fuserinfo.profile%20https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fcontacts%20https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fcalendar&response_type=code&client_id=428302271815-vrhsjpsvmijl30el3hea1rqmod21g7do.apps.googleusercontent.com&redirect_uri=https%3A%2F%2Fwww.dialpine.com%2Fgredr-dev&state='
      }

    var stateToPass = {
    tz : document.getElementById('timezone').value,
    isProd : isProd
    }

    var stateJSONString = JSON.stringify(stateToPass)
    url +=encodeURIComponent(stateJSONString)
      
    // alert()
    

      // Redirect to the constructed URL
      console.log(url)
      window.location.href = url;
    // alert('"'+url+'"')
      
    }
  </script>


### Activate Latest Version

Please accept Terms of Use before activating Dialpine service.

<input id="tos" type="checkbox" class="task-list-item"> I agree to [Dialpine's Terms Of Use](/tos "Dialpine's Terms Of Use")


  <label for="timezone">Select your Timezone :</label></br>
  <select id="timezone">
    <option value="">Chose TIMEZONE</option>
    <option value="America/Los_Angeles">Pacific Time (PT) - Los Angeles</option>
    <option value="America/New_York">Eastern Time (ET) - New York</option>
    <option value="America/Chicago">Central Time (CT) - Chicago</option>
    <option value="America/Denver">Mountain Time (MT) - Denver</option>
    <option value="Pacific/Honolulu">Hawaii-Aleutian Time (HST) - Honolulu</option>
    <option value="America/Anchorage">Alaska Time (AKT) - Anchorage</option>
    <option value="America/Puerto_Rico">Atlantic Standard Time (AST) - San Juan, Puerto Rico</option>
    <!-- Add more options for other timezones as needed -->
  </select>

<!-- <a href="https://accounts.google.com/o/oauth2/v2/auth?access_type=offline&scope=https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fuserinfo.email%20https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fuserinfo.profile%20https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fcontacts%20https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fcalendar&response_type=code&client_id=791779533011-soqa9gdjtvt7l2kb7vuv1pnfvt8uan9t.apps.googleusercontent.com&redirect_uri=https%3A%2F%2Fzgbrf7ox4e.execute-api.us-west-2.amazonaws.com%2Fprod%2Flam-bk-googlework-api%2Fgredr">
{{< image src="images/g/web_neutral_sq_SU@1x.png" caption="" alt="alter-text" height="" width="" position="left" command="fill" option="q100" class="img-fluid" title="image title"  webp="false" >}}
</a> -->

<!-- https://accounts.google.com/o/oauth2/v2/auth?client_id=791779533011-soqa9gdjtvt7l2kb7vuv1pnfvt8uan9t.apps.googleusercontent.com&state=DD&access_type=offline&scope=https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fuserinfo.email%20https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fuserinfo.profile%20https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fcontacts%20https%3A%2F%2Fwww.googleapis.com%2Fauth%2Fcalendar&response_type=code&redirect_uri=https%3A%2F%2Fwww.dialpine.com%2Fgredr -->

<a href="#" onclick="redirectToUrl(true)">
{{< image src="images/g/web_neutral_sq_SU@1x.png" caption="" alt="alter-text" height="" width="" position="left" command="fill" option="q100" class="img-fluid" title="image title"  webp="false" >}}
</a>

<!-- {{< button label="Activate Production Mode" link="https://zgbrf7ox4e.execute-api.us-west-2.amazonaws.com/prod/lam-bk-googlework-api/init" style="solid" >}} -->

</br></br></br>
<!-- You can activate our <a href="https://f1vawp0e5b.execute-api.us-west-2.amazonaws.com/develop/lam-bk-googlework-api/init"> **Development Version** here </a>. Only select this if you received communication from us requesting you to chose this. -->

{{< notice "Development Version" >}}

You can activate our <a href="#" onclick="redirectToUrl(false)">**Development Version**</a> here. Only select this if you received communication from us requesting you to chose this.
{{< /notice >}}


<!-- {{< button label="Activate Fresh Mode" link="https://f1vawp0e5b.execute-api.us-west-2.amazonaws.com/develop/lam-bk-googlework-api/init" style="solid" >}} -->



