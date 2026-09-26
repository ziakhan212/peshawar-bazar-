# Realtime Chat

Peshawar Bazar chat now refreshes conversations every 1.5 seconds while the Inbox is open, so incoming messages appear automatically without manually reopening the chat.

The server also exposes an authenticated `/api/messages/stream` SSE endpoint for future native realtime clients.

Messages remain protected by user authentication and are only returned to the sender/recipient.
