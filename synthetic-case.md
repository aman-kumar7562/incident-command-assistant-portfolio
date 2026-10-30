# Fictional Evidence Set

All names, systems, dates, and figures below are invented for demonstration.

## Scope

Incident `DEMO-1042` affects a fictional appointment service in the North region. The review window is 09:00–10:00 UTC on 14 May 2030.

## Evidence

- **09:12 UTC — monitoring alert:** The appointment API returned elevated errors for requests that confirm new bookings in the North region.
- **09:18 UTC — support report:** Three customers say they can view available slots but receive an error when confirming a booking. No total customer count is available.
- **09:26 UTC — service owner update:** A database connection-pool change at 09:05 UTC is the leading hypothesis. The team is checking whether it explains the regional failures.
- **09:34 UTC — mitigation update:** The team reverted the connection-pool setting. The deployment is complete, but customer-path validation is still running.
- **09:41 UTC — test result:** A synthetic booking succeeds in the North region. The error chart is improving, but there is no confirmed observation period and no update on the three customer reports.
- **Priority policy:** Not supplied.
- **Action register:** No formal actions or owners supplied.
