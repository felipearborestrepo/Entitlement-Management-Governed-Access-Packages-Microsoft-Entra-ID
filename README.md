# Module Description
Designed and deployed a governed access management system using Microsoft Entra ID Entitlement Management. Built a catalog of department-based access packages with approval workflows, expiration policies, and self-service request capabilities through the My Access portal. Shifts access ownership from IT to department managers while maintaining full governance and audit trail.
# Step 1 — Created the Department Access Catalog
- Navigated to Entra Portal → Identity Governance → Entitlement Management → Catalogs
- Created a new catalog named Department Access Catalog
- Set external visibility to No — internal users only
- Enabled the catalog for access package creation
- The catalog acts as the container that organizes all department access packages in one place

<img width="438" height="861" alt="Image 8-5-26 at 21 40" src="https://github.com/user-attachments/assets/1cf03a5e-fb7b-4d2c-90ee-d04afaada1df" />

# Step 2 — Added department groups as resources to the catalog
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

# Step 3 — Created the Engineering Access Package
- Navigated to Identity Governance → Entitlement Management → Access Packages → New Access Package
- Configured the package:
- Name        : Engineering Access Package
- Description : Access for Engineering department members
- Catalog     : Department Access Catalog
- On the Resource Roles tab added:
- Resource    : Engineering Team group
- Role        : Member
- On the Requests tab configured:
- Who can request : Users in your directory
- Require approval: Yes
- Approver        : Manager (requestor's direct manager)
- Expiration      : 365 days
- Approval is routed automatically to the requestor's manager in Entra ID — no IT intervention needed
- Access expires after 365 days — user must re-request if still needed

<img width="1188" height="515" alt="Image 8-5-26 at 21 52" src="https://github.com/user-attachments/assets/1d67b2b7-6b16-4cf4-a715-e88b2bd5be35" />

<img width="1418" height="350" alt="Image 8-5-26 at 21 52 (1)" src="https://github.com/user-attachments/assets/6b942c87-81a1-40f7-b4da-b60cba57f763" />

<img width="1225" height="720" alt="Image 8-5-26 at 21 55" src="https://github.com/user-attachments/assets/88fbe633-52aa-4afc-aa39-c3049cfe9b18" />

<img width="830" height="844" alt="Image 8-5-26 at 21 56" src="https://github.com/user-attachments/assets/cac6ffcb-277b-4871-8ba8-a72d27cb4517" />

<img width="991" height="627" alt="Image 8-5-26 at 21 57" src="https://github.com/user-attachments/assets/a1779915-844a-4329-afc4-191c693abe7a" />

# Step 4 — Created access packages for all remaining departments
- Repeated the same configuration for each department:
- HR Access Package      → HR Team group → Manager approval → 365 days
- Sales Access Package   → Sales Team group → Manager approval → 365 days
- Finance Access Package → Finance Team group → Manager approval → 365 days
- IT Access Package      → IT Team group → Manager approval → 365 days
- All packages follow the same governed model — self-service request, manager approval, automatic expiration

<img width="1421" height="551" alt="Image 8-5-26 at 22 04" src="https://github.com/user-attachments/assets/712acd5f-541b-4a3a-92ee-c59e23bcca6f" />

# Step 5 — Requested access as Carlos Rivera
- Signed in to the My Access portal as Carlos Rivera:
- https://myaccess.microsoft.com
- Browsed available access packages
- Selected Engineering Access Package
- Submitted the access request
- Request entered pending approval state — access not yet granted
- Carlos Rivera cannot access Sales Team resources until manager approves

<img width="1414" height="385" alt="Image 8-5-26 at 22 07" src="https://github.com/user-attachments/assets/e512f22d-a4c8-4874-a67f-45b03cebbfdd" />

<img width="876" height="287" alt="Image 8-5-26 at 22 08" src="https://github.com/user-attachments/assets/6f90e1f1-b70a-47b9-9205-1ba11727ced3" />

# Step 6 — Approved the request as admin
- Signed in to My Access portal as the admin account — Carlos Rivera's manager
- Navigated to Approvals tab
- Found Carlos Rivera's pending Engineering Access Package request
- Reviewed the request details
- Clicked Approve
- Access granted automatically — Carlos Rivera added to Engineering Team group
- Full audit trail created — who requested, who approved, when, what access was granted

<img width="1409" height="439" alt="Image 8-5-26 at 22 09" src="https://github.com/user-attachments/assets/e9602790-1526-4ba8-bce6-38ac73d5e3ed" />

<img width="331" height="838" alt="Image 8-5-26 at 22 13" src="https://github.com/user-attachments/assets/1c9bccc4-3bf6-4b50-a8a4-d53652259f15" />

<img width="1149" height="452" alt="Image 8-6-26 at 19 54" src="https://github.com/user-attachments/assets/55bf1c32-f913-440b-a78a-d42a71ee37d5" />
