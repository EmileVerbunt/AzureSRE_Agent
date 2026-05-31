The Octopets backend is experiencing a deterministic HTTP 500 caused by the `oopsException` diagnostic endpoint.

Application context:

- Azure subscription: `<subscription-id>`
- Resource group: `<octopets-resource-group>`
- Container App name: `octopetsapi`
- Application Insights resource: `octopets-appinsights`
- GitHub repository: `EmileVerbunt/AzureSRE_Agent`
- Failing endpoint: `GET /api/oopsException`
- Expected exception message: `oopsException demo failure: venue lookup returned an empty result while building a pet-friendly recommendation.`

Important:

- Start the Azure SRE Agent if it is stopped, then run a deep investigation for recent HTTP 500 responses from `GET /api/oopsException`.
- Query Application Insights traces, exceptions, and requests for the failing operation and correlate the stack trace to the backend source code.
- Identify the most likely root cause and include the relevant file path, method name, exception type, and stack trace in the investigation summary.
- Create a GitHub issue in `EmileVerbunt/AzureSRE_Agent` with the title `Diagnose oopsException HTTP 500 in Octopets backend`.
- If the GitHub connector is not connected or lacks issue creation permission, stop and report that connector setup must be fixed before completing the alert.
- If the agent is in Review mode, request approval for the GitHub issue creation action.
- Include reproduction steps, Application Insights query evidence, the stack trace, suspected source location, and recommended remediation in the GitHub issue body.
- Complete the alert only after the GitHub issue has been created and linked in your final response.
