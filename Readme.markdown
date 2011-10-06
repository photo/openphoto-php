Open Photo API / PHP Library
=======================
#### OpenPhoto, a photo service for the masses

----------------------------------------

<a name="commandline"></a>
### Using from the command line

Make sure that the `openphoto` file is executable.

    chown o+x openphoto
    
You'll then want to export your secrets to the environment. We suggest putting them in a file and sourcing it prior to running `openphoto` commands.

    # env.sh
    export consumerKey=your_consumer_key
    export consumerSecret=your_consumer_secret
    export token=your_access_token
    export tokenSecret=your_access_token_secret

You'll need to source that file once for each terminal session.
    
    source env.sh

These are the options you can pass to the shell program.

    -h hostname # default=localhost
    -e endpoint # default=/photos/list.json
    -X method # default=GET
    -F params # i.e. -F 'title=my title' -F 'tags=mytag1,mytag1'
    -p # pretty print the json
    -v # verbose output

Now you can run commands to the OpenPhoto API from your shell!

    ./openphoto -h current.openphoto.me -p -e /photo/62/view.json -F 'returnSizes=20x20'
    {
      "message" : "Photo 62",
      "code" : 200,
      "result" : {
        "tags" : [
          
        ],
        "id" : "62",
        "appId" : "current.openphoto.me",
        "pathBase" : "\/base\/201108\/1312956581-opmeqViHrD.jpg",
        "dateUploadedMonth" : "08",
        "dateTakenMonth" : "08",
        "exifCameraMake" : "",
        "dateTaken" : "1312956581",
        "title" : "Tomorrowland Main Stage 2011",
        "height" : "968",
        "description" : "",
        "creativeCommons" : "BY-NC",
        "dateTakenYear" : "2011",
        "dateUploadedDay" : "09",
        "longitude" : "4",
        "host" : "opmecurrent.s3.amazonaws.com",
        "hash" : "0455675a8c42148238b81ed1d8db655c45ae055a",
        "status" : "1",
        "width" : "1296",
        "dateTakenDay" : "09",
        "permission" : "1",
        "pathOriginal" : "\/original\/201108\/1312956581-opmeqViHrD.jpg",
        "size" : "325",
        "dateUploadedYear" : "2011",
        "views" : "0",
        "latitude" : "50.8333",
        "dateUploaded" : "1312956583",
        "exifCameraModel" : "",
        "Name" : "62",
        "path20x20" : "http:\/\/current.openphoto.me\/photo\/62\/create\/ceb90\/20x20.jpg"
      }
    }
