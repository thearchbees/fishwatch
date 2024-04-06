# Use of Edge Computing

## Context
In the context of FishWatch, rapid and reliable data processing is critical due to the remote nature of aquatic farms and their varying internet connectivity. These farms require an immediate response to environmental data to maintain the health of the livestock. Edge computing emerges as a solution to process data locally, ensuring minimal latency and less reliance on stable internet connectivity.

## Decision
We will implement edge computing within our system architecture. Edge devices will be equipped with the necessary computational power to process data on-site, providing near-instant analytics and enabling real-time decision-making and actions.

## Considered Options
1. **Centralized Cloud Processing**: All data is sent to a centralized cloud for processing.
2. **Hybrid Processing**: A combination of local processing for time-sensitive analysis and cloud processing for less critical data.
3. **Full Edge Processing**: All data is processed on local edge devices, with synchronization to the cloud as needed.

## Rationale
Edge processing was selected to:
- Ensure real-time actionability in response to data inputs.
- Conserve bandwidth by reducing the volume of data transmitted to the cloud.
- Provide continuous operation, even during internet outages.

## Implications
- Edge devices will need to be more robust and may incur higher costs.
- Deployment strategies must include edge device management for updates.
- Data synchronization mechanisms must be established to maintain cloud consistency.

## Status
Accepted

## Consequences
Local data processing at the edge will enable the system to react promptly to environmental changes, providing a robust response mechanism for fish farm operations. This choice, however, implies a higher initial investment in edge infrastructure and more complex system management.

## Mapped Requirements
This decision supports several key FishWatch requirements:
- **Real-time Analysis/Data Processing**: Enabling immediate local processing and actions based on environmental conditions.
- **Reliability**: Ensuring that monitoring and control systems remain operational regardless of internet connectivity quality.
- **System Accessibility and Compatibility**: Allowing for the system's operation in varied environments, including those where connectivity is a challenge.
- **Scalability and Extensibility**: Facilitating the future integration of more advanced processing capabilities at the edge as technology evolves.
