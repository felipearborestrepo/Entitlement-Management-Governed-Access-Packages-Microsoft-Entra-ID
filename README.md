# Module Description
Designed and deployed a governed access management system using Microsoft Entra ID Entitlement Management. Built a catalog of department-based access packages with approval workflows, expiration policies, and self-service request capabilities through the My Access portal. Shifts access ownership from IT to department managers while maintaining full governance and audit trail.
**Step 1 — Created the Department Access Catalog**
- Navigated to Entra Portal → Identity Governance → Entitlement Management → Catalogs
- Created a new catalog named Department Access Catalog
- Set external visibility to No — internal users only
- Enabled the catalog for access package creation
- The catalog acts as the container that organizes all department access packages in one place

<img width="438" height="861" alt="Image 8-5-26 at 21 40" src="https://github.com/user-attachments/assets/1cf03a5e-fb7b-4d2c-90ee-d04afaada1df" />

**Step 2 — Added department groups as resources to the catalog**
- Opened the catalog → Resources tab → Add Resources → Groups and Teams
- Added the following security groups as resources:
- Engineering Team
- HR Team
- Sales Team
- Finance Team
- IT Team
- All Employees
- Adding groups as resources makes them available to be included in access packages
- Without adding them to the catalog first they cannot be assigned through access packages

<img width="1258" height="583" alt="Image 8-5-26 at 21 51" src="https://github.com/user-attachments/assets/42d7e77c-b645-492a-bfc4-f076c29e164a" />

**Step 3 — Created the Engineering Access Package**
- Navigated to Identity Governance → Entitlement Management → Access Packages → New Access Package
- Configured the package:
- Name        : Engineering Access Package
- Description : Access for Engineering department members
- Catalog     : Department Access Catalog

  <img width="1188" height="515" alt="Image 8-5-26 at 21 52" src="https://github.com/user-attachments/assets/fac392ad-7174-46bf-9642-32581ce396b3" />

- On the Resource Roles tab added:
- Resource    : Engineering Team group
- Role        : Member

<img width="1418" height="350" alt="Image 8-5-26 at 21 52 (1)" src="https://github.com/user-attachments/assets/9ed95585-2382-41ae-91ff-728d95176478" />

- On the Requests tab configured:
- Who can request : Users in your directory
- Require approval: Yes
- Approver        : Manager (requestor's direct manager)

<img width="1225" height="720" alt="Image 8-5-26 at 21 55" src="https://github.com/user-attachments/assets/30ab562d-e3e6-460f-911f-ea199fa4d5ac" />

<img width="830" height="844" alt="Image 8-5-26 at 21 56" src="https://github.com/user-attachments/assets/ad80844c-5c76-41b1-85f4-f6922ee0fd4e" />

- Expiration      : 365 days
- Approval is routed automatically to the requestor's manager in Entra ID — no IT intervention needed
- Access expires after 365 days — user must re-request if still needed

<img width="991" height="627" alt="Image 8-5-26 at 21 57" src="https://github.com/user-attachments/assets/8d797094-3716-4131-aa43-69972a5154ad" />
