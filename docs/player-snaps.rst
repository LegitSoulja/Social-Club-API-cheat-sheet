Player snaps
============

.. http:get:: /member/(nickname)/games/gtav/snapmatic/ajax/search?[SearchQuery=(search_query)&]Filter=(filter)&page=(page_number)

  Returns 12 snapmatic pictures of the specific player. Make sure to increase ``page_number`` to browse through the pagination.

  **Example request**:

  .. sourcecode:: http

    GET /member/restlessnarwhal/games/gtav/snapmatic/ajax/search?Filter=MostRecent&page=1 HTTP/1.1
    Host: socialclub.rockstargames.com

  **Example response** `(full) <_static/responses/snapmatic_player.txt>`_:

  .. include:: _static/responses/snapmatic_player.txt
    :literal:
    :code: json
    :end-line: 30

  :param nickname: target player
  :query optional search_query: a specific term to search for
  :query filter: allowed values: ``mostrecent``, ``trending``, ``popular`` (all-time), ``myfriends``, ``myphotos``, ``mythumbsup``
  :query page_number: page number, starting with ``1``
