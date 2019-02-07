youtube-dl-api-server Changelog
===============================

Version 0.3
-----------

- Add ``/api/play`` endpoint. (Adapted from a patch by eadmaster in `PR #46 <https://github.com/jaimeMF/youtube-dl-api-server/pull/46>`_)
- Add ``/api/version`` endpoint. (Added by Carlos Ramos in `PR #43 <https://github.com/jaimeMF/youtube-dl-api-server/pull/43>`_)
- Pass the ``format`` parameter to the ``YoutubeDL`` object.
- Add ``--number-processes`` option for choosing the number of processes the server will use, defaults to 5. (Added by Carlos Ramos in `PR #42 <https://github.com/jaimeMF/youtube-dl-api-server/pull/42>`_)
- Provide a ``Blueprint`` for the API.

Version 0.2
-----------

- ``/api/`` no longer redirects to ``/api/info``.
- Change default value of the ``flatten`` parameter to ``False`` and deprecate it.
- Add ``--host`` option for choosing the server address. (Added by Alexandr Korsak in `PR #26 <https://github.com/jaimeMF/youtube-dl-api-server/pull/26>`_)
- Add instructions and sample file for deploying to Heroku. (Thanks to Ronald Ip, see `PR #28 <https://github.com/jaimeMF/youtube-dl-api-server/pull/28>`_)
- Force the youtube-dl ``format`` parameter to ``best``. Since version ``2015.04.26`` it uses ``bestvideo+bestaudio/best`` if ffmpeg/libav is installed.
- Allow passing some extra parameters directly to the ``YoutubeDL`` object.

Version 0.1.2
-------------

- Fix disabling the youtube-dl's cache in latest versions.

Version 0.1.1
-------------

- Fix access to the version string of youtube-dl in the last versions.

Version 0.1
-----------
- The endpoint for getting the video information is now ``/api/info``.
  ``/api/`` redirects now to it, but it's deprecated and will be removed in a future version.
- The server can be run now with ``python -m youtube_dl_server``.
- Added ``flatten`` option to ``/api/info`` to select between a single dictionary result or a list of videos, it's ``True`` by default.
