# Cloning Caveat: 
must include --recursive option while cloning repo, otherwise submodule folders are empty:
git clone https://github.com/guidovin/dialogSocialDemo.git --recursive

# Execution intructions:

cd dialogSocialDemo && cd challenge_backend && yarn install && yarn start; 
cd dialogSocialDemo && cd challenge_frontend && yarn install && yarn start;

Npm can be used instead of yarn.
Built with Node v12.18.2.

# curl for api call
curl 'http://localhost:4000/graphql' -H 'Accept-Encoding: gzip, deflate, br' -H 'Content-Type: application/json' -H 'Accept: application/json' -H 'Connection: keep-alive' -H 'DNT: 1' -H 'Origin: http://localhost:4000' --data-binary '{"query":"# Write your query or mutation here\n{\n  list {\n\t\tid\n\t\tindex\n\t\tpicture\n\t\tage\n    eyeColor\n\t\tname\n\t\tcompany\n\t\temail\n\t\tphone\n\t\tgreeting\n      \n  }\n}"}' --compressed

# curl for api call with name parameter
'http://localhost:4000/graphql' -H 'Accept-Encoding: gzip, deflate, br' -H 'Content-Type: application/json' -H 'Accept: application/json' -H 'Connection: keep-alive' -H 'DNT: 1' -H 'Origin: http://localhost:4000' --data-binary '{"query":"# Write your query or mutation here\n{\n  list(name:\"Cecilia\"){\n\t\tid\n\t\tindex\n\t\tpicture\n\t\tage\n    eyeColor\n\t\tname\n\t\tcompany\n\t\temail\n\t\tphone\n\t\tgreeting\n      \n  }\n}"}' --compressed

Obs: The loading time of the user images from the mock is pretty large. Added a placeholder spinner while they load.
