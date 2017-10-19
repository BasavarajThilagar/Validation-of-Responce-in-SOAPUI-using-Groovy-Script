# Validation-of-Responce-in-SOAPUI-using-Groovy-Script
# This code will compare whether status=success and name=ABCD.

import groovy.json.JsonSlurper 
def response = messageExchange.response.responseContent
def slurper = new JsonSlurper()
def json = slurper.parseText response
assert json.status=="SUCCESS"
assert json.inpor=="ABCD"
