# Privacy and Safety

A knowledge graph can become surprisingly personal over time.

Treat a public repository as permanently public information, even if you later delete a file.

## Never commit secrets

Do not add:

- passwords
- API keys
- access tokens
- private keys
- database credentials
- session cookies
- recovery codes
- environment files containing secrets

If a secret is committed, deleting the latest version of the file is not enough. Assume the secret may exist in Git history and rotate/revoke it.

## Avoid sensitive personal information

Think carefully before publishing:

- government identification numbers
- home addresses
- personal phone numbers
- private email addresses
- medical or health information
- financial/account information
- private relationship details
- confidential employment information

## Respect other people's privacy

Do not put private information about coworkers, clients, friends, family members, or other people into a public knowledge graph without appropriate permission.

## Work and client information

Do not publish:

- proprietary source code
- unreleased product plans
- internal credentials
- customer data
- private tickets or messages
- confidential architecture
- information covered by an NDA or employment agreement

Record the lesson, not the secret.

For example, prefer:

> Learned why idempotency matters when retrying payment operations.

instead of exposing a client's private payment implementation.

## Public vs private graphs

A public graph is useful for:

- technical knowledge
- public projects
- learning goals
- non-sensitive questions
- reusable principles
- public experiments

A private repository is safer for deeply personal reflection or information you would not want indexed, copied, or archived.

## Before every push

Ask:

1. Would I be comfortable with a stranger reading this?
2. Does this reveal information about somebody else?
3. Does it contain a secret or internal system detail?
4. Am I allowed to publish this?
5. Would a private note be more appropriate?

When uncertain, leave it out of the public repository.
