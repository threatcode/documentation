---
Title: instaloader
Homepage: https://github.com/instaloader/instaloader
Repository: https://salsa.debian.org/debian/instaloader
Architectures: all
Version: 4.10.1+ds-1
Metapackages: kali-linux-everything 
Icon: /images/kali-tools-icon-missing.svg
PackagesInfo: |
 ### instaloader
 
  Instaloader downloads photos from Instagram, including public
  and private profiles, hashtags, user stories, feeds and saved
  media. How as well as comments, geotags and captions for each
  post.
   
  It automatically detects profile name changes and renames the
  target directory accordingly. It also allows for refined
  customization of filters and where to store downloaded media
  be able to detect automatically stop previously interrupted
  download interactions.
 
 **Installed size:** `294 KB`  
 **How to install:** `sudo apt install instaloader`  
 
 {{< spoiler "Dependencies:" >}}
 * python3
 * python3-requests
 {{< /spoiler >}}
 
 ##### instaloader
 
 Instagram automatic photo downloader
 
 ```
 root@kali:~# instaloader -h
 usage: 
 instaloader [--comments] [--geotags]
             [--stories] [--highlights] [--tagged] [--igtv]
             [--login YOUR-USERNAME] [--fast-update]
             profile | "#hashtag" | %location_id | :stories | :feed | :saved
 instaloader --help
 
 Download pictures (or videos) along with their captions and other metadata
 from Instagram.
 
 What to Download:
   Specify a list of targets. For each of these, Instaloader creates a folder
   and downloads all posts. The following targets are supported:
 
   profile               Download profile. If an already-downloaded profile has
                         been renamed, Instaloader automatically finds it by
                         its unique ID and renames the folder likewise.
   @profile              Download all followees of profile. Requires --login.
                         Consider using :feed rather than @yourself.
   "#hashtag"            Download #hashtag.
   %location_id          Download %location_id. Requires --login.
   :feed                 Download pictures from your feed. Requires --login.
   :stories              Download the stories of your followees. Requires
                         --login.
   :saved                Download the posts that you marked as saved. Requires
                         --login.
   -- -shortcode         Download the post with the given shortcode
   filename.json[.xz]    Re-Download the given object.
   +args.txt             Read targets (and options) from given textfile.
 
 What to Download of each Post:
   --slide SLIDE         Set what image/interval of a sidecar you want to
                         download.
   --no-pictures         Do not download post pictures. Cannot be used together
                         with --fast-update. Implies --no-video-thumbnails,
                         does not imply --no-videos.
   -V, --no-videos       Do not download videos.
   --no-video-thumbnails
                         Do not download thumbnails of videos.
   -G, --geotags         Download geotags when available. Geotags are stored as
                         a text file with the location's name and a Google Maps
                         link. This requires an additional request to the
                         Instagram server for each picture. Requires --login.
   -C, --comments        Download and update comments for each post. This
                         requires an additional request to the Instagram server
                         for each post, which is why it is disabled by default.
   --no-captions         Do not create txt files.
   --post-metadata-txt POST_METADATA_TXT
                         Template to write in txt file for each Post.
   --storyitem-metadata-txt STORYITEM_METADATA_TXT
                         Template to write in txt file for each StoryItem.
   --no-metadata-json    Do not create a JSON file containing the metadata of
                         each post.
   --no-compress-json    Do not xz compress JSON files, rather create pretty
                         formatted JSONs.
 
 What to Download of each Profile:
   --no-posts            Do not download regular posts.
   --no-profile-pic      Do not download profile picture.
   -s, --stories         Also download stories of each profile that is
                         downloaded. Requires --login.
   --highlights          Also download highlights of each profile that is
                         downloaded. Requires --login.
   --tagged              Also download posts where each profile is tagged.
   --igtv                Also download IGTV videos.
 
 Which Posts to Download:
   -F, --fast-update     For each target, stop when encountering the first
                         already-downloaded picture. This flag is recommended
                         when you use Instaloader to update your personal
                         Instagram archive.
   --latest-stamps [STAMPSFILE]
                         Store the timestamps of latest media scraped for each
                         profile. This allows updating your personal Instagram
                         archive even if you delete the destination
                         directories. If STAMPSFILE is not provided, defaults
                         to /root/.config/instaloader/latest-stamps.ini
   --post-filter filter, --only-if filter
                         Expression that, if given, must evaluate to True for
                         each post to be downloaded. Must be a syntactically
                         valid python expression. Variables are evaluated to
                         instaloader.Post attributes. Example: --post-
                         filter=viewer_has_liked.
   --storyitem-filter filter
                         Expression that, if given, must evaluate to True for
                         each storyitem to be downloaded. Must be a
                         syntactically valid python expression. Variables are
                         evaluated to instaloader.StoryItem attributes.
   -c COUNT, --count COUNT
                         Do not attempt to download more than COUNT posts.
                         Applies to #hashtag, %location_id, :feed, and :saved.
 
 Login (Download Private Profiles):
   Instaloader can login to Instagram. This allows downloading private
   profiles. To login, pass the --login option. Your session cookie (not your
   password!) will be saved to a local file to be reused next time you want
   Instaloader to login.
 
   -l YOUR-USERNAME, --login YOUR-USERNAME
                         Login name (profile name) for your Instagram account.
   -f SESSIONFILE, --sessionfile SESSIONFILE
                         Path for loading and storing session key file.
                         Defaults to
                         /root/.config/instaloader/session-<login_name>
   -p YOUR-PASSWORD, --password YOUR-PASSWORD
                         Password for your Instagram account. Without this
                         option, you'll be prompted for your password
                         interactively if there is not yet a valid session
                         file.
 
 How to Download:
   --dirname-pattern DIRNAME_PATTERN
                         Name of directory where to store posts. {profile} is
                         replaced by the profile name, {target} is replaced by
                         the target you specified, i.e. either :feed, #hashtag
                         or the profile name. Defaults to '{target}'.
   --filename-pattern FILENAME_PATTERN
                         Prefix of filenames for posts and stories, relative to
                         the directory given with --dirname-pattern. {profile}
                         is replaced by the profile name,{target} is replaced
                         by the target you specified, i.e. either :feed#hashtag
                         or the profile name. Defaults to '{date_utc}_UTC'
   --title-pattern TITLE_PATTERN
                         Prefix of filenames for profile pics, hashtag profile
                         pics, and highlight covers. Defaults to
                         '{date_utc}_UTC_{typename}' if --dirname-pattern
                         contains '{target}' or '{dirname}', or if --dirname-
                         pattern is not specified. Otherwise defaults to
                         '{target}_{date_utc}_UTC_{typename}'.
   --resume-prefix PREFIX
                         Prefix for filenames that are used to save the
                         information to resume an interrupted download.
   --sanitize-paths      Sanitize paths so that the resulting file and
                         directory names are valid on both Windows and Unix.
   --no-resume           Do not resume a previously-aborted download iteration,
                         and do not save such information when interrupted.
   --user-agent USER_AGENT
                         User Agent to use for HTTP requests. Defaults to
                         'Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36
                         (KHTML, like Gecko) Chrome/92.0.4515.131
                         Safari/537.36'.
   --max-connection-attempts N
                         Maximum number of connection attempts until a request
                         is aborted. Defaults to 3. If a connection fails, it
                         can be manually skipped by hitting CTRL+C. Set this to
                         0 to retry infinitely.
   --request-timeout N   Seconds to wait before timing out a connection
                         request. Defaults to 300.
   --abort-on STATUS_CODES
                         Comma-separated list of HTTP status codes that cause
                         Instaloader to abort, bypassing all retry logic.
   --no-iphone           Do not attempt to download iPhone version of images
                         and videos.
 
 Miscellaneous Options:
   -q, --quiet           Disable user interaction, i.e. do not print messages
                         (except errors) and fail if login credentials are
                         needed but not given. This makes Instaloader suitable
                         as a cron job.
   -h, --help            Show this help message and exit.
   --version             Show version number and exit.
 
 The complete documentation can be found at https://instaloader.github.io/.
 ```
 
 - - -
 
---
{{% hidden-comment "<!--Do not edit anything above this line-->" %}}
