# Oracle Health Millennium Platform FHIR API Reference

This document provides a reference to the Oracle Health Millennium Platform FHIR R4 APIs used in this project.

## Official Documentation

- **Interactive Swagger UI**: [https://app.swaggerhub.com/apis-docs/cbhconsulingllc/fhir-r4-apis-for-oracle-health-millennium-platform/2025.08.21](https://app.swaggerhub.com/apis-docs/cbhconsulingllc/fhir-r4-apis-for-oracle-health-millennium-platform/2025.08.21)
- **Original Swagger JSON**: [https://docs.oracle.com/en/industries/health/millennium-platform-apis/mfrap/swagger.json](https://docs.oracle.com/en/industries/health/millennium-platform-apis/mfrap/swagger.json)
- **Local Copy**: `./oracle-fhir-swagger.json`

## API Information

- **Title**: FHIR R4 APIs for Oracle Health Millennium Platform
- **Version**: 2025.08.21
- **Base URL**: `https://fhir-ehr-code.cerner.com/r4/ec2458f2-1e24-41c8-b71b-0e701af7583d`
- **Description**: These HL7 FHIR R4 APIs allow a registered user to access the Oracle Health EHR data in Oracle Health Millennium Platform for which they are authorized.

## Supported Resources

Based on the Swagger specification, the following FHIR resources are supported:

### Core Resources
- **Patient** - Patient demographics and information
- **Observation** - Clinical observations and vital signs
- **Condition** - Patient conditions and diagnoses
- **Encounter** - Patient encounters and visits
- **Practitioner** - Healthcare providers

### Medication Resources
- **MedicationStatement** - Patient medication statements
- **MedicationRequest** - Medication prescriptions and requests
- **MedicationAdministration** - Medication administration records
- **MedicationDispense** - Medication dispensing records

### Other Resources
- **ServiceRequest** - Service requests and orders
- **QuestionnaireResponse** - Questionnaire responses
- **AllergyIntolerance** - Patient allergies
- **Immunization** - Immunization records
- **DocumentReference** - Document references
- **Binary** - Binary resources

## Common Query Parameters

| Parameter | Description | Example |
|-----------|-------------|---------|
| `_id` | The logical resource ID | `_id=12345` |
| `patient` | The specific patient | `patient=12345` |
| `subject` | The specific subject | `subject=Patient/12345` |
| `_lastUpdated` | Date/time range for updates | `_lastUpdated=ge2023-01-01` |
| `_count` | Number of results | `_count=10` |
| `status` | Resource status | `status=active` |
| `category` | Resource category | `category=vital-signs` |

## Authorization

The API requires OAuth 2.0 authorization with the following scopes:

- `launch` - Launch context
- `openid` - OpenID Connect
- `fhirUser` - FHIR user information
- `patient/Patient.read` - Read patient data
- `patient/Observation.read` - Read observations
- `patient/Condition.read` - Read conditions
- `online_access` - Online access

## Usage in This Project

Access the interactive API documentation through the following methods:

### From the Application
1. **Navbar Link**: Click "API Docs" in the top navigation
2. **Quick Access Card**: Click "Oracle FHIR API (SwaggerHub)" button
3. **Direct URL**: [https://app.swaggerhub.com/apis-docs/cbhconsulingllc/fhir-r4-apis-for-oracle-health-millennium-platform/2025.08.21](https://app.swaggerhub.com/apis-docs/cbhconsulingllc/fhir-r4-apis-for-oracle-health-millennium-platform/2025.08.21)

### SwaggerHub Features
- **Interactive API Testing**: Try endpoints directly in the browser
- **Request/Response Examples**: See actual data structures
- **Schema Documentation**: Understand data models and validation rules
- **Authentication Testing**: Test with your actual FHIR credentials
- **Code Generation**: Generate client SDKs in multiple languages
- **Version Management**: Track API changes and updates

## Integration with Existing Code

The current `app.html` already implements FHIR client functionality. The Swagger reference can be used to:

1. **Validate API calls** - Ensure requests match the documented API
2. **Add new endpoints** - Use the Swagger spec to implement additional resources
3. **Handle errors** - Reference error codes and responses documented in the spec
4. **Understand data structures** - Use the schema definitions for proper data handling

## Updates

To keep the API reference current:

1. Periodically download the latest Swagger JSON
2. Update the configuration in `swagger-config.js`
3. Review changes in the Oracle documentation
4. Update this reference document as needed
