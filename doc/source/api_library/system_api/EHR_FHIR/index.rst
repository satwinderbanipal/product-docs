EHR FHIR System API
!!!!!!!!!!!!!!!!!!!

We have created System APIs which will be exposed as REST interface to provide information based upon ID provided to get information.

Currently these APIs has been enabled for Patient, Condition and Appointment. Mule Server has been setup on EC2 instance, we are accessing RDS instance to get EHR data based on provided ID's.

Base URI for template-healthcare-ehr2fhir-system-api-3.8 application running on Mule Server is http://ec2-34-208-134-225.us-west-2.compute.amazonaws.com:8081/api/

Fetch Patient Information:-

Method-: GET

Path:- Patient/{ID}

Example :-ID and corresponding fetch JSON response for Patient Resource.

curl -X GET http://ec2-34-208-134-225.us-west-2.compute.amazonaws.com:8081/api/Patient/Patient-1125

{
    "resourceType": "Patient",
    "id": "Patient-1125",
    "address": {
        "postalCode": "Manchester",
        "country": null,
        "city": "48158",
        "line": "220 S Almond Court",
        "state": "MI"
    },
    "birthDate": "1978-03-19",
    "careProvider": null,
    "gender": "male",
    "name": {
        "use": null,
        "family": "Paulson",
        "given": "Ryan"
    },
    "telecom": {
        "use": "home",
        "system": "phone",
        "value": "586.555.8242"
    }
}

