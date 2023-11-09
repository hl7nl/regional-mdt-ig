Regionaal MDO ondersteuning FHIR Implementation Guide

https://confluence.hl7.org/display/HNETH/MDO+Implementatie+Gids

```
> curl -L https://github.com/HL7/fhir-ig-publisher/releases/latest/download/publisher.jar -o publisher.jar
> java -jar publisher.jar -ig ig.ini
```

Trigger FHIR auto-ig builder
```
curl -X POST  "https://us-central1-fhir-org-starter-project.cloudfunctions.net/ig-commit-trigger" \
  -H "Content-type: application/json" \
  --data '{"ref": "refs/heads/main", "repository": {"full_name": "HL7nl/regional-mdt-ig"}}'
```