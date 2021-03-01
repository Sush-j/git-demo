# Ferma

Ferma server code

Configurations:
    Check below configurations, as needed, and update them in ‘sherlock/constants.py’
        - Spell Checker On / Off
        - Google logger sheets On / Off and Google Spreadsheets Id
        - PORT Number, if you want to run the server on different port (Default: 8080)


    ENVIRONMENT VARIABLES:

        GITLAB CREDS:
            -  GIT_USERNAME
            -  GIT_PASSWORD

        CLIENT NAME:
            - FC_CLIENT_NAME

        SQL CREDS:
            - FC_SQL_HOST  //ip
            - FC_SQL_USER  //username
            - FC_SQL_PWD   //password

        REDIS DB CREDS
            - FC_REDIS_HOST     //ip
            - FC_REDIS_PWD      //password
            - FC_REDIS_AUTH_IDX //Authorisation tokens index
            - FC_REDIS_SYN_IDX  //Synonyms index

        NEO4J CREDS
            - FC_NEO4J_HOST //ip
            - FC_NEO4J_USER //username
            - FC_NEO4J_PWD  //password

        ELASTIC SEARCH CREDS:
            - FC_ES_HOST //ip


Pre-Requisites:

[Poetry user guide](https://docs.google.com/document/d/1wMZtLQ3Yi1npmWIuse6JpF-bwgTg8PKTpUUn2LXs-bk/edit)

     Packages required : 
        - datastore
        - knowledge-base
        - auto-correct
        - autocomplete-state
        - helpers	

     Packages installation : 
	- Install all the required packages (included in pyproject.toml file) using :
     poetry install --no-root



     Spell Checker Pickles
        Files:  "../datastore/auto_correct/kb_autocorrect.pkl"
                "../datastore/auto_correct/stopwords_trie.pkl"
                "../datastore/auto_correct/english_auto_correct.pkl"
                "../datastore/auto_correct/valid_grams_trie.pkl"
        For more details, refer to the "auto-correct" & "datastore" modules

     Knowledge Base Pickles
        Files: 
          "../datastore/knowledge_base/knowledge_base.pkl" for core Ferma
          "../datastore/knowledge_base/knowledge_base_qual.pkl" for Qual Documents
          "../datastore/knowledge_base/knowledge_base_app.pkl" for Congress App
      For more details, refer to the "knowledge-base" module


    But don't worry you can generate all of them and load all dependencies including the python
packages required using one script.
    VOILA......;P 
        Run `sh ferma/setup_ferma.sh`

To Run the server:
    ‘python3 http_interface.py’


SIMPLE.....!
