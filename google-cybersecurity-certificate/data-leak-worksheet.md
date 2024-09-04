# Data leak worksheet

**Incident summary**: A sales manager shared access to a folder of internal-only documents with their
team during a meeting. The folder contained files associated with a new product that has not been
publicly announced. It also included customer analytics and promotional materials. After the meeting,
the manager did not revoke access to the internal folder, but warned the team to wait for approval
before sharing the promotional materials with others.

During a video call with a business partner, a member of the sales team forgot the warning from their
manager. The sales representative intended to share a link to the promotional materials so that the
business partner could circulate the materials to their customers. However, the sales representative
accidentally shared a link to the internal folder instead. Later, the business partner posted the link on
their company's social media page assuming that it was the promotional materials.

| Control | Least privilege |
| --- | --- |
| Issue(s) | The internal-only folder should not be accessible by those outside the organization (business partner). The manager should not give employees access to documents until it's needed. The promotional materials (public information) was not separated from the internal-only folder. |
| Review | NIST SP 800-53: AC-6 specifies that users should be given the least amount of access and authorization in order to complete their task. This follows the principle of least privilege. | 
| Recommendation(s) | AC-6(1) Authorize access for users to access internal documents. AC-6(7) Review of user privileges. |
| Justification | AC-6(1) was chosen because users outside the organization, should not be able to access internal-only documents. AC-6(7) to ensure all users in the organizations only has access to the resources they need to do their job. |
