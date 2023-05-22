# Random Windows Commands That Might Be Useful


# Event Logs

## wevtutil

### Switches used explained:
- `qe` - Query events
- `/q:` - XML formatted query for event log information
- `/c:` - Most recent x number of events to return
- `/rd:` - Read direction (true = most recent first)
- `/f` - Format 

### Query Windows Terminal Services log for last 5 events showing user and source IP for connection
`wevtutil qe Microsoft-Windows-TerminalServices-LocalSessionManager/operational "/q:*[System [(EventID=21)]]" /c:5 /rd:true /f:text`

### Query SentinelOne for "malware detected" events
`wevtutil qe sentinelone/operational "/q:*[System [(EventID=31)]]" /c:5 /rd:true /f:text`

