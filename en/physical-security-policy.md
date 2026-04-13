# Physical Security Policy

> **Document control**  
> Owner: [POLICY_OWNER_ROLE, e.g. Information Security Officer]  
> Approved by: [APPROVER_NAME_AND_ROLE]  
> Version: [VERSION]  
> Effective date: [EFFECTIVE_DATE]  
> Next review: [NEXT_REVIEW_DATE]

## 1. Legal/Regulatory Basis

ISO/IEC 27001:2022 / ISO/IEC 27002:2022, Annex A — Physical Controls:

- A 7.1 — Physical Security Perimeters
- A 7.2 — Physical Entry
- A 7.3 — Securing Offices, Rooms and Facilities
- A 7.4 — Physical Security Monitoring
- A 7.5 — Protecting Against Physical and Environmental Threats
- A 7.6 — Working in Secure Areas
- A 7.7 — Clear Desk and Clear Screen
- A 7.8 — Equipment Siting and Protection
- A 7.9 — Security of Assets Off-Premises
- A 7.10 — Storage Media
- A 7.11 — Supporting Utilities
- A 7.12 — Cabling Security
- A 7.13 — Equipment Maintenance
- A 7.14 — Secure Disposal or Re-use of Equipment

BSI IT-Grundschutz:

- INF.1 (Generic Building)
- INF.2 (Data Centre and Server Room)
- ORP.4 (Identity and Access Management)
- INF.7 (Office Workplace)
- INF.5 (Room or Cabinet for Technical Infrastructure)
- SYS.2.1 (General Client)
- INF.8 (Working from Home)
- INF.9 (Mobile Workplace)
- CON.7 (Information Security on Trips Abroad)
- SYS.4.5 (Removable Media)
- CON.6 (Deleting and Destroying Data and Devices)
- INF.12 (Cabling)
- INF.11 (General Vehicle)
- INF.13 (Technical Building Management)

Additional jurisdiction-specific laws — in particular workplace safety law, building codes, fire safety regulations, data protection law (for CCTV and access logging) and works council co-determination rules — are listed in the Legal Register and incorporated by reference.

## 2. Purpose & Scope

This policy defines the physical and environmental security controls that protect the premises, facilities, equipment and information assets of **[YOUR_ORGANISATION_NAME]**. It covers physical security perimeters, entry controls, office and room security, monitoring, environmental threat protection, secure area working rules, clear desk and clear screen practices, equipment siting, off-premises asset security, storage media management, supporting utilities, cabling, equipment maintenance and secure disposal.

The policy applies to all buildings, rooms and facilities owned, leased or operated by the organisation that house information processing systems, storage media or personnel handling classified information. It is binding on all employees, contractors, visitors and third-party service providers with physical access to the organisation's premises.

## 3. Physical Security Perimeters (A 7.1)

Security perimeters are defined and used to protect areas that contain information and other associated assets. Building security planning covers the entire lifecycle of a facility, from site selection through design, construction, operation and decommissioning. Perimeter boundaries are documented and reviewed whenever facility layouts change. For data centres and server rooms, dedicated fire compartments with appropriate fire resistance ratings are maintained.

- **Perimeter Definition & Siting:** Security perimeters are defined based on a risk assessment. The siting and strength of each perimeter reflect the information security and privacy requirements of the assets located within that perimeter. Perimeter boundaries are documented in the facility security plan and reviewed annually.
- **Physical Soundness:** All buildings and sites containing information processing facilities have physically sound perimeters with no gaps or areas vulnerable to break-in. Exterior roofs, walls, ceilings and floors are of solid construction. All external doors are protected against unauthorised access through control mechanisms such as bars, alarms and locks. Doors and windows are locked when unattended, and external protection is applied to ground-level windows. Ventilation points are assessed and secured against unauthorised entry.
- **Fire Door Security:** All fire doors on a security perimeter are alarmed, monitored and tested in conjunction with the adjacent walls to confirm the required level of resistance in accordance with applicable fire safety standards. Fire doors operate in a failsafe manner, maintaining both fire containment and security integrity.

## 4. Physical Entry Controls (A 7.2)

Secure areas are protected by appropriate entry controls to ensure that only authorised personnel are permitted access. Physical access rights are provisioned, reviewed periodically, updated and revoked in accordance with the access management process (see the *Access Control Policy*). A comprehensive key management process governs the issuance, tracking and return of all physical keys and authentication tokens. Fire drills and evacuation exercises are conducted at planned intervals.

### 4.1 General Access Controls

- **Authorised Personnel Only:** Access to sites and buildings is restricted to authorised personnel only. Physical access rights are provisioned through a formal authorisation process, reviewed periodically, updated when roles change and revoked upon termination or role change (see the *Access Control Policy*).
- **Access Logging:** A physical logbook or electronic audit trail records all access events. Logs are maintained securely, monitored for anomalies and protected against tampering, unauthorised access and deletion (see the *IT Operations Security Policy*).
- **Authentication Mechanisms:** A documented process and technical mechanisms govern access to areas where information is processed or stored. Authentication mechanisms include access cards, biometrics or two-factor authentication such as an access card combined with a secret PIN. Double security doors (mantraps) are used for access to sensitive areas such as data centres.
- **Reception & Monitoring:** A reception area staffed by personnel, or equivalent means, controls physical access to each site and building. Reception personnel verify identity before granting entry.
- **Belongings Inspection:** Personal belongings of personnel and interested parties are inspected and examined upon entry and exit where the risk assessment warrants it.
- **Visible Identification:** All personnel and interested parties wear visible identification at all times on the premises. Security personnel are immediately notified upon encountering unescorted visitors or anyone without visible identification. Easily distinguishable badges differentiate permanent employees, suppliers and visitors.
- **Supplier Access:** Supplier personnel receive restricted access to secure areas or information processing facilities only when operationally required. Such access is formally authorised and monitored throughout the visit.
- **Multi-Tenant Buildings:** Where a building houses assets for multiple organisations, physical access security receives special attention. Access controls prevent personnel from one tenant from accessing another tenant's secure areas.
- **Scalable Security Measures:** Physical security measures are designed so that they can be strengthened when the likelihood of physical incidents increases, such as during elevated threat levels or after security incidents.
- **Emergency Exit Security:** Emergency exits and other secondary entry points such as fire escapes, loading bays and basement accesses are secured against unauthorised use while remaining operable for emergency egress in compliance with fire safety regulations.
- **Key Management:** A key management process governs all physical keys and authentication information, including lock codes and combination locks for offices, rooms, facilities and key cabinets. A key logbook or annual key audit tracks issuance, return and current holders. Access to physical keys and authentication information is controlled.

### 4.2 Visitor Management

- **Visitor Identity Verification:** The identity of every visitor is authenticated by an appropriate means before access is granted. Valid government-issued identification is checked and recorded.
- **Visitor Log:** The date and time of entry and departure of every visitor is recorded in a visitor log. Records are retained in accordance with the organisation's retention schedule.
- **Authorised Purpose & Briefing:** Visitors are granted access only for specific, authorised purposes. Each visitor receives instructions on the security requirements of the area being visited and on emergency procedures before entering.
- **Visitor Supervision:** All visitors are supervised at all times unless an explicit, documented exception has been granted by an authorised person.

### 4.3 Delivery & Loading Areas

- **Restricted External Access:** Access to delivery and loading areas from outside the building is restricted to identified and authorised personnel. Delivery drivers do not access internal building areas.
- **Area Design:** Delivery and loading areas are designed so that deliveries can be loaded and unloaded without delivery personnel gaining unauthorised access to other parts of the building.
- **Door Interlocking:** The external doors of delivery and loading areas are secured when doors to restricted internal areas are opened, preventing simultaneous opening of both sets of doors.
- **Incoming Delivery Inspection:** Incoming deliveries are inspected and examined for explosives, chemicals or other hazardous materials before they are moved from delivery and loading areas into the building.
- **Delivery Registration:** Incoming deliveries are registered in accordance with asset management procedures upon entry to the site. Records include sender, contents, date and recipient.
- **Shipment Segregation:** Incoming and outgoing shipments are physically segregated where possible to prevent commingling and reduce the risk of substitution or theft.
- **Tampering Detection:** Incoming deliveries are inspected for evidence of tampering during transit. Any detected tampering is immediately reported to security personnel for investigation.

## 5. Securing Offices, Rooms & Facilities (A 7.3)

Physical security for offices, rooms and facilities is designed and implemented to protect information and associated assets against unauthorised access, damage and interference. Room selection considers the sensitivity of activities performed within, and rooms housing information processing equipment are separated from public areas. Technical infrastructure rooms (server rooms, network distribution rooms) receive enhanced protection including reinforced doors, climate control and restricted access.

- **Critical Facility Siting:** Critical facilities are sited to avoid access by the public. Locations are selected to minimise exposure to unauthorised observation, casual foot traffic and external threats.
- **Unobtrusive Buildings:** Where applicable, buildings are unobtrusive and give no indication of their purpose. No obvious signs outside or inside the building identify the presence of information processing activities.
- **Visibility & Audibility Prevention:** Facilities are configured to prevent confidential information or activities from being visible and audible from the outside. Electromagnetic shielding is applied where the risk assessment warrants it.
- **Directory & Map Restrictions:** Directories, internal telephone books and online maps identifying the locations of confidential information processing facilities are not made readily available to unauthorised persons. Access to such information is restricted to personnel with a demonstrated need to know.

## 6. Physical Security Monitoring (A 7.4)

Premises are continuously monitored for unauthorised physical access. Monitoring systems are designed, installed and maintained in accordance with applicable data protection regulations and workplace privacy requirements. Video recordings and alarm logs are retained for a defined period and reviewed following security incidents.

- **Video Surveillance:** Closed-circuit television (CCTV) or equivalent video monitoring systems are installed to view and record access to sensitive areas both within and outside the organisation's premises. Camera placement, recording retention and access to footage are documented and comply with applicable privacy legislation.
- **Intrusion Detection:** Contact, sound or motion detectors are installed in accordance with relevant standards and tested periodically. These include door and window contact detectors, infrared motion detectors and glass-break sensors that trigger intruder alarms to alert security personnel.
- **Alarm Coverage:** Alarms cover all external doors and accessible windows. Unoccupied areas are alarmed at all times. Additional coverage extends to critical areas such as computer rooms, communications rooms and archive storage.

## 7. Protection Against Physical & Environmental Threats (A 7.5)

Protection against physical and environmental threats is designed and implemented based on a risk assessment that considers the geographic location, building characteristics and surrounding environment. Fire protection follows applicable building codes and includes smoke detection, handheld extinguishers and fire suppression systems. Data centres incorporate dedicated fire compartments, uninterruptible power supplies and emergency shutdown procedures.

### 7.1 Site Selection & Risk Assessment

- **Topographic Risks:** Site selection and risk assessments consider local topography, including appropriate elevation above flood plains, proximity to bodies of water and distance from tectonic fault lines.
- **Urban & Location Risks:** Site selection and risk assessments evaluate urban threats, including whether the location has a high profile that could attract political unrest, criminal activity or terrorist attacks. Locations with elevated threat profiles receive additional physical countermeasures.

### 7.2 Threat-Specific Controls

- **Fire Protection:** Fire detection systems are installed and configured to detect fires at an early stage and to send alarms or trigger fire suppression systems. Suppression uses the most appropriate substance for the environment — gas-based suppression in confined spaces such as server rooms, water-based systems in general areas. Handheld fire extinguishers are placed at accessible locations throughout all buildings. Fire drills are conducted at planned intervals.
- **Flood Protection:** Flood detection systems are installed under the floors of areas containing storage media or information processing systems. Water pumps or equivalent drainage means are readily available. Critical equipment is elevated above floor level where flood risk is identified.
- **Electrical Surge Protection:** Surge protection systems protect both server and client information systems against electrical surges and similar events. Lightning protection is applied to all buildings, and lightning protection filters are fitted to all incoming power and communications lines.
- **Explosives & Weapons:** Random inspections for the presence of explosives or weapons are performed on personnel, vehicles or goods entering sensitive information processing facilities.
- **Crime Prevention:** Crime prevention through environmental design (CPTED) principles are applied when designing and selecting controls to secure the organisation's environment. This includes natural surveillance, access control through landscaping, territorial reinforcement and maintenance to reduce urban threats.

## 8. Working in Secure Areas (A 7.6)

Security measures for working in secure areas are designed and implemented to protect information and associated assets within those areas. Secure areas include data centres, server rooms, archive rooms and any area designated as restricted due to the sensitivity of the information or equipment it contains.

- **Need-to-Know Awareness:** Personnel are made aware of the existence of, or activities within, a secure area only on a need-to-know basis. The location and purpose of secure areas are not disclosed to personnel who have no operational requirement to access them.
- **Supervised Work:** Unsupervised work in secure areas is avoided both for safety reasons and to reduce the opportunity for malicious activities. At least two authorised persons are present during work in high-security areas.
- **Vacant Area Inspection:** Vacant secure areas are physically locked and periodically inspected to detect unauthorised access, tampering or environmental anomalies.
- **Recording Equipment Restrictions:** Photographic, video, audio or other recording equipment — including cameras built into user endpoint devices — is not permitted in secure areas unless explicitly authorised by the facility security manager.
- **Endpoint Device Controls:** The carrying and use of user endpoint devices in secure areas is controlled. Devices are either prohibited, placed in secure storage at the entrance or subject to inspection and usage restrictions.
- **Emergency Procedures:** Emergency procedures — including evacuation routes, assembly points and emergency contact numbers — are posted in a readily visible or accessible manner within all secure areas.

## 9. Clear Desk & Clear Screen (A 7.7)

Clear desk rules for papers and removable storage media and clear screen rules for information processing facilities are defined and enforced. These rules minimise the risk of unauthorised access to, loss of or damage to information during and outside normal working hours. For home workplaces, the same clear desk and clear screen standards apply.

- **Secure Storage of Sensitive Information:** Sensitive or critical business information — whether on paper or electronic storage media — is locked away in a safe, cabinet or other security furniture when not actively required, especially when the office is vacated.
- **Endpoint Device Locking:** User endpoint devices are protected by key locks or other physical security means when not in use or unattended. Laptops are secured with cable locks or stored in locked drawers or cabinets.
- **Screen Lock & Auto-Logout:** User endpoint devices are logged off or protected with a screen and keyboard locking mechanism controlled by user authentication when unattended. All computers and systems are configured with a session timeout or automatic logout feature that activates after a defined period of inactivity.
- **Printer Output Collection:** Originators collect outputs from printers or multi-function devices immediately. Printers with authentication functions are used so that only the originator can retrieve printouts, and only when physically present at the printer.
- **Document & Media Disposal:** Documents and removable storage media containing sensitive information are stored securely when in use and, when no longer required, discarded using secure disposal mechanisms such as cross-cut shredding or degaussing.
- **Screen Pop-Up Configuration:** Rules and guidance are established and communicated for the configuration of pop-ups on screens. New email and messaging notification pop-ups are turned off during presentations, screen sharing sessions or when working in public areas.
- **Whiteboard & Display Clearing:** Sensitive or critical information on whiteboards and other display surfaces is erased or removed when no longer required. Meeting rooms are inspected after use.
- **Final Sweep:** A final sweep is conducted prior to leaving or vacating facilities to ensure that organisational assets — particularly documents — are not left behind, including items that may have fallen behind drawers or furniture.

## 10. Equipment Siting & Protection (A 7.8)

Equipment is sited and protected to reduce the risks from physical and environmental threats and to prevent unauthorised access, damage and interference. Data centre equipment is placed in climate-controlled environments with redundant cooling and fire suppression. Office workplace equipment is positioned to minimise unauthorised viewing and is secured against theft.

- **Work Area Access Minimisation:** Equipment is sited to minimise unnecessary access into work areas and to prevent unauthorised physical access. Server and network equipment is placed in dedicated, access-controlled rooms.
- **Viewing Angle Protection:** Information processing facilities handling sensitive data are carefully positioned to reduce the risk of information being viewed by unauthorised persons during use. Screens face away from windows, corridors and public areas; privacy filters are applied where necessary.
- **Physical & Environmental Threat Controls:** Controls minimise the risk of potential physical and environmental threats including theft, fire, explosives, smoke, water and water supply failure, dust, vibration, chemical effects, electrical supply interference, communications interference, electromagnetic radiation and vandalism.
- **Food & Drink Guidelines:** Guidelines prohibit eating, drinking and smoking in proximity to information processing facilities, particularly in server rooms, data centres and technical infrastructure rooms.
- **Environmental Monitoring:** Environmental conditions — including temperature and humidity — are monitored in real time for conditions that can adversely affect the operation of information processing facilities. Alerts are generated when thresholds are exceeded. Data centre environments maintain temperature and humidity within manufacturer-specified ranges.
- **Lightning Protection:** Lightning protection is applied to all buildings. Lightning protection filters are fitted to all incoming power and communications lines to prevent damage from electrical surges.
- **Special Protection Methods:** Special protection methods — such as keyboard membranes, sealed enclosures and ruggedised housings — are used for equipment deployed in industrial, manufacturing or other harsh environments.
- **Electromagnetic Emanation Protection:** Equipment processing confidential information is protected to minimise the risk of information leakage due to electromagnetic emanation. Shielding, filtering and emission reduction techniques are applied based on the classification of the information processed.
- **Facility Separation:** Information processing facilities managed by the organisation are physically separated from those not managed by the organisation. Co-located equipment from different organisations does not share the same physical enclosures or racks without documented risk acceptance.

## 11. Security of Assets Off-Premises (A 7.9)

Off-site assets are protected in accordance with the risk assessment. Equipment and storage media taken outside the organisation's premises remain subject to the same level of protection as on-site assets, adjusted for the higher risk of the off-premises environment. Personnel travelling with organisational assets follow the information security travel guidelines. Home workplaces meet defined security standards, and mobile workplaces are used only in environments that provide adequate privacy and physical protection.

### 11.1 General Off-Premises Protection

- **No Unattended Equipment in Public:** Equipment and storage media taken off premises are never left unattended in public and unsecured places. Devices are kept under personal supervision or secured in locked containers, hotel safes or vehicle boots.
- **Manufacturer Protection Instructions:** Manufacturer instructions for protecting equipment are observed at all times, including protection against exposure to strong electromagnetic fields, water, heat, humidity and dust.
- **Chain of Custody:** When off-premises equipment is transferred among different individuals or interested parties, a log defines the chain of custody including the names and organisations of those responsible for the equipment at each point. Information that does not need to be transferred with the asset is securely deleted before the transfer.
- **Removal Authorisation:** Where necessary and practical, authorisation is required for equipment and media to be removed from the organisation's premises. A record of such removals is maintained to provide an audit trail (see the *Information Transfer Policy*).
- **Shoulder Surfing Prevention:** Information displayed on device screens is protected against viewing by unauthorised persons on public transport and in public spaces. Privacy filters are used on laptops and mobile devices, and screen brightness is adjusted to minimise readability from adjacent seating.
- **Location Tracking & Remote Wipe:** Location tracking and remote wiping capabilities are implemented on mobile devices and laptops. Remote wipe is activated immediately upon confirmed loss or theft of a device.

### 11.2 Permanent External Installations

- **Physical Security Monitoring:** Permanent external installations — such as remote offices, co-location facilities and external storage sites — are subject to physical security monitoring equivalent to on-premises standards.
- **Environmental Threat Protection:** Permanent external installations are protected against physical and environmental threats using the same risk-based approach applied to the main premises.
- **Tamper Proofing:** Physical access controls and tamper-proofing mechanisms protect external installations against unauthorised physical access and evidence of tampering triggers an immediate investigation.
- **Logical Access Controls:** Logical access controls at external installations meet the same requirements as those applied on-premises, including authentication, authorisation and audit logging.

## 12. Storage Media (A 7.10)

Storage media are managed throughout their lifecycle — from acquisition through use, transport, storage and disposal — in accordance with the organisation's classification scheme and handling procedures. Removable storage media policies address the specific risks of portable devices that can easily be lost or stolen. Information on storage media transported physically is protected against unauthorised access, misuse and corruption during transit. Secure deletion and destruction follow documented procedures.

### 12.1 Removable Media Management

- **Removable Media Policy:** A topic-specific policy on the management of removable storage media is established and communicated to all personnel who use or handle removable storage media.
- **Removal Authorisation:** Where necessary and practical, authorisation is required for storage media to be removed from the organisation. A record of such removals is maintained to provide an audit trail.
- **Secure Storage Environment:** All storage media are stored in a safe, secure environment according to their information classification and protected against environmental threats such as heat, moisture, humidity, electromagnetic fields and ageing, in accordance with manufacturer specifications.
- **Encryption:** When information confidentiality or integrity is a consideration, cryptographic techniques protect information on removable storage media. Encryption algorithms and key lengths follow the cryptography policy.
- **Media Refresh:** To mitigate the risk of storage media degrading while stored information is still needed, information is transferred to fresh storage media before the original media becomes unreadable. Media refresh schedules are documented per media type.
- **Redundant Copies:** Multiple copies of valuable information are stored on separate storage media to reduce the risk of coincidental information damage or loss.
- **Media Registration:** Removable storage media are registered in an inventory to limit the chance of information loss. The register records media type, classification level, custodian and location.
- **Port Control:** Removable storage media ports — including SD card slots and USB ports — are enabled only where there is a documented organisational reason for their use. Ports are disabled by default through endpoint management tools.
- **Transfer Monitoring:** Where there is a need to use removable storage media, the transfer of information to such media is monitored through data loss prevention (DLP) tools or manual logging procedures.
- **Physical Transport Protection:** Information on storage media during physical transport — including via postal service or courier — is protected against unauthorised access, misuse and corruption. Tamper-evident packaging and tracked delivery services are used for media classified above the baseline level.

### 12.2 Secure Reuse & Disposal

- **Secure Reuse:** Storage media containing confidential information that need to be reused within the organisation are securely deleted or formatted before reuse using approved tools (see the *Data Deletion, Masking & DLP Policy*).
- **Secure Disposal:** Storage media containing confidential information are disposed of securely when no longer needed, through destruction, shredding or secure deletion of content. The disposal method matches the classification level of the information.
- **Disposal Identification Procedures:** Procedures are in place to identify items that require secure disposal. These procedures cover all media types — hard drives, SSDs, USB devices, optical media, tapes and paper documents.
- **External Disposal Services:** When external collection and disposal services are used, the external party supplier is selected with adequate controls and experience. Contracts include confidentiality clauses, certification requirements and audit rights.
- **Disposal Logging:** The disposal of sensitive items is logged to maintain an audit trail. Records include the item description, disposal method, date, responsible person and confirmation of destruction.
- **Aggregation Effect:** When accumulating storage media for disposal, consideration is given to the aggregation effect, whereby a large quantity of individually non-sensitive information can become sensitive when combined. Accumulated media awaiting disposal are stored securely.
- **Damaged Device Assessment:** A risk assessment is performed on damaged devices containing sensitive data to determine whether the items are physically destroyed rather than sent for repair or discarded (see secure disposal, Section 16).

## 13. Supporting Utilities (A 7.11)

Information processing facilities are protected from power failures and other disruptions caused by failures in supporting utilities such as electricity, gas, water, sewage, heating/ventilation, air conditioning and telecommunications. Utility infrastructure is designed with redundancy to meet availability requirements. Uninterruptible power supplies (UPS) and diesel generators provide backup power for data centres and critical systems. Emergency switches and valves are installed near emergency exits and equipment rooms.

- **Manufacturer Compliance:** Equipment supporting the utilities is configured, operated and maintained in accordance with the relevant manufacturer's specifications and applicable safety standards.
- **Capacity Planning:** Utilities are appraised regularly for their capacity to meet business growth and are assessed for interactions with other supporting utilities that could create cascading failures.
- **Inspection & Testing:** Equipment supporting the utilities is inspected and tested regularly to ensure proper functioning. UPS systems are load-tested at planned intervals, and diesel generators undergo regular start-up and runtime tests.
- **Malfunction Alarms:** Where necessary, alarms detect utility malfunctions — including power failures, cooling system anomalies and water leaks — and notify responsible personnel immediately.
- **Multiple Feeds & Diverse Routing:** Where necessary, utilities have multiple feeds with diverse physical routing to eliminate single points of failure. Power is supplied from at least two independent sources for critical facilities.
- **Separate Network:** Equipment supporting the utilities is on a separate network from the information processing facilities if connected to a network, preventing compromise of building management systems from affecting IT systems and vice versa.
- **Secure Internet Connectivity:** Equipment supporting the utilities is connected to the internet only when operationally needed and only through a secured, monitored connection.
- **Emergency Lighting & Communications:** Emergency lighting and emergency communications systems are provided in all occupied areas and are tested at planned intervals to confirm readiness.
- **Emergency Shutoff Controls:** Emergency switches and valves to cut off power, water, gas or other utilities are located near emergency exits and equipment rooms and are clearly labelled and accessible.
- **Network Connectivity Redundancy:** Redundancy for network connectivity is obtained by means of multiple routes from more than one utility provider, ensuring that the failure of a single provider does not disrupt communications.
- **Emergency Contact Records:** Emergency contact details for utility providers and internal emergency response personnel are recorded and made available to all relevant personnel in the event of an outage.

## 14. Cabling Security (A 7.12)

Cables carrying power or data, or supporting information services, are protected from interception, interference, damage or tampering. Cabling infrastructure follows primary and secondary cabling standards, and cable documentation is maintained to enable rapid fault identification and infrastructure changes. All cabling installations use fire-resistant materials in compliance with applicable fire codes. Cable rooms are access-controlled and regularly inspected.

- **Underground or Protected Routing:** Power and telecommunications lines into information processing facilities are routed underground where possible, or subject to adequate alternative protection such as floor cable protectors and utility poles. Underground cables are protected against accidental cuts with armoured conduits or presence-signalling markers.
- **Cable Segregation:** Power cables are segregated from communications cables to prevent electromagnetic interference. Minimum separation distances follow applicable cabling standards.
- **Armoured Conduit & Secured Endpoints:** Armoured conduit, locked rooms and lockable enclosures with alarms are installed at inspection and termination points for sensitive or critical systems.
- **Electromagnetic Shielding:** Electromagnetic shielding is applied to protect the cables carrying data for sensitive or critical systems against emanation and interference.
- **Sweep & Inspection:** Periodical technical sweeps and physical inspections detect unauthorised devices attached to the cables for sensitive or critical systems. Inspection frequency is based on the risk assessment.
- **Patch Panel & Cable Room Access:** Access to patch panels and cable rooms is controlled through mechanical keys, PINs or electronic access control. Access is restricted to authorised maintenance and network personnel.
- **Fibre-Optic Cables:** Fibre-optic cables are used for sensitive or critical systems where the risk of electromagnetic interception or interference warrants their use.
- **Cable Labelling:** Cables are labelled at each end with sufficient source and destination details to enable physical identification and inspection. Labelling follows a documented naming convention and is kept current with infrastructure changes.

## 15. Equipment Maintenance (A 7.13)

Equipment is maintained correctly to ensure its continued availability, integrity and information security. Maintenance programmes are planned, documented and monitored to keep equipment in the condition specified by the manufacturer. Maintenance of data centre infrastructure follows a structured programme with documented service intervals. Technical building management systems are included in the maintenance schedule.

- **Manufacturer Service Schedule:** Equipment is maintained in accordance with the supplier's recommended service frequency and specifications. Maintenance intervals are documented and tracked.
- **Maintenance Programme:** A maintenance programme is implemented and monitored by the organisation. The programme covers all critical equipment, specifies responsible parties and tracks completion of scheduled maintenance activities.
- **Authorised Personnel Only:** Only authorised maintenance personnel carry out repairs and maintenance on equipment. Authorisation is verified before work begins.
- **Maintenance Records:** Records are kept of all suspected or actual faults, and of all preventive and corrective maintenance activities. Records include dates, work performed, parts replaced and the identity of the maintenance personnel.
- **Maintenance Security Controls:** Appropriate controls are implemented when equipment is scheduled for maintenance, taking into account whether maintenance is performed by on-site personnel or external service providers. External maintenance personnel sign a suitable confidentiality agreement.
- **On-Site Supervision:** Maintenance personnel are supervised when carrying out maintenance on site. Supervision includes escorting external technicians and verifying that only authorised work is performed.
- **Remote Maintenance Authorisation:** Access for remote maintenance is authorised and controlled. Remote sessions are logged, monitored and terminated when the maintenance task is completed.
- **Off-Premises Maintenance:** When equipment containing information is taken off premises for maintenance, security measures for assets off-premises apply. Information is removed from the equipment before it leaves the premises where feasible.
- **Insurance Compliance:** All maintenance requirements imposed by insurance policies are complied with. Maintenance records are made available to insurers upon request.
- **Post-Maintenance Inspection:** Before putting equipment back into operation after maintenance, the equipment is inspected to ensure it has not been tampered with and is functioning properly. Configuration baselines are re-verified.
- **End-of-Life Disposal:** When it is determined that equipment is to be disposed of rather than maintained, measures for secure disposal or re-use of equipment apply.

## 16. Secure Disposal or Re-use of Equipment (A 7.14)

Items of equipment containing storage media are verified to ensure that any sensitive data and licensed software has been removed or securely overwritten prior to disposal or re-use. Physical destruction of storage media follows documented procedures and is the preferred method for media that contained highly classified information. When facilities are vacated, a decommissioning process ensures that no residual information remains for subsequent occupants. This section provides the physical destruction controls referenced by the data deletion policy.

- **Facility Restoration:** When vacating a facility, the lease agreement requirements to return the facility to its original condition are observed. All information processing equipment, cabling, access control devices and monitoring systems are removed or rendered inoperable.
- **Residual Information Removal:** The risk of leaving systems with sensitive information for the next tenant is minimised. User access lists, video or image files, configuration data and any other information assets are securely deleted from all systems, storage media and network equipment before the facility is handed over.
- **Control Reusability:** The ability to reuse physical security controls — such as access control hardware, CCTV systems and alarm installations — at the next facility is assessed during decommissioning. Reusable controls are inventoried, tested and securely transported.

## 17. Roles & Responsibilities

- **Top Management:** Approves this policy, allocates resources for physical security infrastructure and ensures alignment with business objectives, legal requirements and workplace safety regulations.
- **Information Security Officer (ISO):** Maintains this policy, defines physical security requirements based on risk assessments, coordinates security perimeter reviews and oversees compliance with physical security controls across all facilities.
- **Facility Security Manager:** Implements and operates the physical security controls defined in this policy. Manages access control systems, visitor management, key management, alarm systems, CCTV and environmental monitoring. Coordinates with building management and external security service providers.
- **IT Operations / Data Centre Manager:** Ensures that data centre and server room environments meet the physical and environmental requirements defined in this policy, including climate control, fire suppression, power supply redundancy and access controls for technical areas.
- **Asset Owners:** Ensure that equipment and storage media under their responsibility are handled, transported, maintained and disposed of in accordance with this policy. Report physical security deficiencies to the Facility Security Manager.
- **All Personnel:** Follow clear desk and clear screen rules, wear visible identification on premises, report physical security incidents and suspicious activities, escort visitors when assigned and comply with secure area working rules.

## 18. Review & Maintenance

This policy is reviewed:

- At least annually, as part of the ISMS management review cycle.
- After significant physical security incidents (e.g. unauthorised access, break-in, fire, flooding, equipment theft).
- When the physical threat landscape changes significantly (e.g. changes in neighbourhood security profile, new construction affecting building access, elevated threat levels).
- Following significant changes to facilities, building layouts, data centre infrastructure or physical security systems.
- When new legal, regulatory or contractual requirements affecting physical security are identified.
