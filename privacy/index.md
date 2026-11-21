# ClaimBack — Privacy Notice

**Version:** 1.2  
**Effective date:** November 21, 2026

ClaimBack helps you organise receipts, track product warranties and prepare
warranty claims. Your saved items and claims are stored on your device.
Receipt analysis can send documents to a processing server and an AI provider.
Gmail import is optional and starts when you choose to connect and search.

## 1. Who provides ClaimBack

ClaimBack is provided by Vincenzo Vitale, an individual developer based in the
Netherlands, under the project name **Smanettu**. Smanettu is not a separate
legal entity. For processing controlled by the developer, Vincenzo Vitale is
the data controller.

Support, privacy questions and data requests:
**[smanettu@gmail.com](mailto:smanettu@gmail.com)**.

## 2. Information stored on your device

The app stores saved receipt copies, product names, retailers, purchase dates,
prices, warranty dates, claim drafts and history, preferences, and receipt
discovery progress locally. Documents can contain additional personal data,
such as names, addresses, order numbers or partial payment information.
Connected Google account identifiers, mailbox message references and import
checkpoints help keep Gmail searches associated with the correct account.
Google sign-in credentials are handled by Google's sign-in software; ClaimBack
does not ask for or receive your Google password.

Camera and photo-library access is used for receipt capture and selection.
Selected files and shared documents can also be imported. Permission can be
changed in your device settings. The app does not need access to your contacts
or precise location. The current app has no advertising or standalone usage
analytics or crash-reporting integration.

Google ML Kit, used for on-device text recognition and scanning, can send
technical information to Google: device/app information, installation or device
identifiers, API-use events, performance measurements and error codes. Google
uses this for SDK diagnostics and usage analytics. The SDK's documented
technical reporting uses HTTPS; receipt images used for on-device recognition
are separate from the document uploads described below. See
[Google's ML Kit data-disclosure documentation](https://developers.google.com/ml-kit/android-data-disclosure).

## 3. Receipt processing and AI

When you use receipt analysis in Cloud mode, the app sends selected receipt
images, PDFs or extracted receipt text to the developer's processing service,
currently hosted on **Fly.io**. The service sends the document content needed
for extraction to **Anthropic's API** and returns purchase details to the app.
Receipts may include personal information beyond the fields being extracted.
Ordinary connection information, such as IP addresses, request times, job
identifiers, status, timing and model-usage information, is also processed to
deliver the service, troubleshoot failures and prevent abuse.

If you configure Local mode, processing uses the server you specify. A local
server can use a locally running model or a cloud provider depending on its
configuration. Local mode is not a guarantee that a separately configured
server keeps all processing offline.

AI results can be incomplete or incorrect. Review extracted details and claim
drafts before relying on or sharing them. Sharing a claim through your device's
share menu sends the content to the app or recipient you select; ClaimBack does
not automatically submit warranty claims or send emails on your behalf.

### Error reports and support codes

In versions that offer error reporting, a technical error displays a random support code.
You can share just that code with support. It identifies an operation and its retries.
The developer can use it to look up technical records on the processing server.

Automatic error reporting is enabled in supported builds. The phone sends the code,
app build, operating system and major version, named steps, timing, retry information,
HTTP status and a predefined failure category to ClaimBack on Fly.io when an error
appears. Email content, account identifiers, receipt details, filenames, credentials,
screenshots and raw error messages are excluded. Sharing a screenshot is your choice.
Google Firebase App Check uses Apple App Attest or Google Play Integrity to verify
that the report comes from ClaimBack. These services process app and device
verification information. Cloud reports go to ClaimBack even when you use a local
receipt-processing server.

You can switch off **Send error reports** in Settings. This clears waiting reports
and stops future uploads from the phone. Up to 20 reports can wait on the phone
for 48 hours. Diagnostic timelines expire from the live server database after seven
days. Hosting backups can retain earlier copies. The receipt service still records
operational information when processing a request. A code alone gives no access
to the private lookup. Include your code if you contact the developer about a report.

## 4. Optional Gmail import

If you connect Gmail, ClaimBack requests read-only Gmail access to find
purchase-related messages and attachments. It can inspect sender information,
subjects, dates, filenames, snippets, message bodies and attachments to identify
and analyse receipts. It does not use that permission to send, modify or delete
your Gmail messages.

During a search, candidate metadata such as sender, subject, filename and
snippet may be sent to the processing service and Anthropic to prioritise likely
receipts. Candidate receipt attachments or relevant email text may then be
sent for extraction. Gmail access tokens stay with the app's Google sign-in
flow and are not sent to the receipt-processing server. Search progress and
discovered documents can be saved on your device so you can resume or review.

ClaimBack uses information received from Google APIs only to provide the
receipt-discovery and import features you request. Its use and transfer of
that information will adhere to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy)
and [Google Workspace API User Data and Developer Policy](https://developers.google.com/workspace/workspace-api-user-data-developer-policy),
including the Limited Use requirements. Google user data is not sold, used for
advertising, or used to develop, improve or train general-purpose or
non-personalised AI or machine-learning models. Human access is limited to
what is permitted by those requirements, such as your explicit request for
support, security investigation or applicable law.

You can use manual receipt features without connecting Gmail. Disconnect
Gmail in the app or revoke access through your Google Account to stop future
access. This does not remove previously imported receipts or revoke a
document-processing request already submitted.

## 5. Providers, purposes and international processing

Data is used to provide requested app functions, maintain reliability and
security, respond to support and privacy requests, and meet legal obligations.
Depending on the processing, the legal basis is providing the service you
request, your consent where required, legitimate interests in operating and
protecting the service, or compliance with law. Optional permissions and Gmail
authorisation can be withdrawn; this may prevent the relevant feature working.

Providers include Google for sign-in, Gmail and on-device document-recognition
components; Fly.io for hosted processing; Anthropic for cloud AI; GitHub Pages
for these public pages; and Google for support email. Visiting this website
also discloses ordinary connection information to GitHub. Providers may process
information outside the Netherlands or European Economic Area, subject to their
applicable terms and safeguards. ClaimBack does not sell personal data or use
it for advertising. Data may also be disclosed where required by law or to
protect the service and users.

Provider information: [Google Privacy Policy](https://policies.google.com/privacy),
[Fly.io Privacy Policy](https://fly.io/legal/privacy-policy/),
[Anthropic Privacy Policy](https://www.anthropic.com/legal/privacy), and
[GitHub Privacy Statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).

## 6. Retention and deletion

- **On your device:** saved items, receipts and claims remain until you remove
  them, reset app data or uninstall. **Settings → Reset all data** removes app
  receipt records, claim records and Gmail discovery files. It does not remove
  original documents or messages from their source. Device backups may retain
  copies according to your operating-system and backup settings.
- **Processing server:** uploaded processing payloads are removed when a job
  completes or fails. Job records, results and any result previews normally
  expire seven days after submission; cleanup runs periodically. A pending job
  may retain its input until it completes, fails or expires. Resetting or
  uninstalling the app does not immediately erase these server records.
- **AI provider:** Anthropic's API has its own retention rules. Its published
  standard is deletion of inputs and outputs within 30 days, with exceptions
  for certain services, agreed arrangements, safety enforcement and law. See
  [Anthropic's current API retention explanation](https://privacy.claude.com/en/articles/7996866-how-long-do-you-store-my-organization-s-data).
  ClaimBack does not claim a zero-retention arrangement.
- **Operational logs and support:** technical logs rotate as they reach their
  size limits; hosting-provider records follow provider retention settings.
  Support messages are kept as needed to resolve and document your request,
  protect legal rights or comply with law.

Email the contact above for access, correction, deletion or other privacy
requests. A job identifier can help locate processing records; do not send
passwords or sign-in tokens. Removing Gmail access or app data does not delete
your Google Account. ClaimBack has no separate developer-operated user account.

## 7. Your choices and rights

You can decline camera or photo permissions, avoid Gmail import, disconnect
Gmail, choose what to share, and remove local app data. Depending on applicable
law, you may have rights to access, correct, erase, restrict or object to
processing, obtain a portable copy, and withdraw consent without affecting
earlier lawful processing. You can complain to your local data-protection
authority, including the Dutch
[Autoriteit Persoonsgegevens](https://www.autoriteitpersoonsgegevens.nl/).
The app is intended for adults and is not directed at children.

## 8. Changes

This notice describes the initial tester version. The version and date above
will change when the notice is updated. New data uses will be described before
they begin, with additional notice or choices where required. For help, see
[ClaimBack Support](../support/).
