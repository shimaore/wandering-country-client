    PouchDB = require 'pouchdb-browser'

    location = (name) ->
      [window.location.protocol,'//',window.location.host,'/',name].join ''

    browser = (month) ->
      name = ['reference',month].join '-'
      new PouchDB location name

    module.exports = {browser}
