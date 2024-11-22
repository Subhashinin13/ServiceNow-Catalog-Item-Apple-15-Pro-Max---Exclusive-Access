# ServiceNow Catalog Item: Apple 15 Pro Max - Exclusive Access

## Project Overview

This project implements a **Service Catalog item** in **ServiceNow** for requesting the newly released **Apple 15 Pro Max** smartphone. Due to budget constraints and strategic distribution, this device is restricted to **Senior Management** and **specific Project Leaders** within TechGlobal's organization. The catalog item will be configured such that it is **not visible or accessible** to the general employee population.

## Goals

- Create a new catalog item for the Apple 15 Pro Max smartphone.
- Restrict access to only senior management and select project leaders.
- Ensure the catalog item is hidden from the general employee base.
  
## Skills and Tools Required

- **ServiceNow** instance access with Administrator rights.
- **Service Catalog** knowledge.
- **User Role Management** in ServiceNow.
- **Access Control** configuration (Access Control Rules, Business Rules).
  
## Project Configuration Steps

### 1. **Create the Catalog Item**
   - **Navigate to:** Service Catalog > Catalog Definitions > Maintain Items.
   - Click on **New** to create a new catalog item.
   - Fill in the following details:
     - **Name:** Apple 15 Pro Max
     - **Short Description:** Apple 15 Pro Max smartphone.
     - **Catalog:** Employee Devices
     - **Category:** Smartphones
   - Optionally, provide a detailed description, price, and any other relevant details.
   - Set the **Order Guide** and **Item type** as appropriate.

### 2. **Create User Criteria for Restricted Access**
   - **Navigate to:** Service Catalog > User Criteria.
   - Create new User Criteria to define who can see the catalog item:
     - Name: Senior Management and Project Leaders Access
     - Criteria:
       - **Role:** Add the role(s) of Senior Management and Project Leaders.
         - E.g., `senior_management`, `project_leader_role`.
     - Use filters based on **User Roles** or **Groups** to restrict visibility to the right users.

### 3. **Assign the User Criteria to the Catalog Item**
   - Go back to the catalog item created in Step 1.
   - Under the **Available for** tab, select the User Criteria you created in Step 2.
   - This ensures only users with the designated roles can see and request the Apple 15 Pro Max.

### 4. **Test User Access**
   - Test with users who have the required roles (Senior Management or Project Leaders).
   - Ensure that they can see and access the catalog item.
   - Test with a user who does not have the appropriate role to ensure they cannot see the catalog item.

### 5. **Configure Access Control (Optional)**
   - If necessary, configure **Access Control Rules** to further restrict access at the record level.
   - This might include ensuring that users without the correct roles cannot access the catalog item's data.

### 6. **Set Up Notifications (Optional)**
   - Set up any required **notifications** (e.g., approval workflows, order confirmation) that should trigger when a request for the Apple 15 Pro Max is submitted.
   - This may include notifying managers or the IT department.

### 7. **Approval Workflow (Optional)**
   - You can implement an approval workflow, where requests for the Apple 15 Pro Max must be approved by senior management or another specific role before being processed.

## Testing & Validation

1. **Test with eligible users:**
   - Verify that users with roles like `senior_management` and `project_leader_role` can view and order the catalog item.
  
2. **Test with ineligible users:**
   - Ensure that users without the required roles cannot see the catalog item or submit requests for the Apple 15 Pro Max.

3. **Test notification and approval workflows:**
   - Ensure all notifications and approval workflows trigger correctly when a request is placed.

## Potential Enhancements

- **Approval Groups**: Use dynamic approval groups to route requests to specific senior management or project leaders.
- **Limit Request Quantities**: Limit the number of devices an individual can request, especially in cases of supply chain restrictions.
- **Custom Form Fields**: Add custom fields to capture more details when requesting the Apple 15 Pro Max (e.g., department, project name).

## Deployment Instructions

1. **Deploy the Catalog Item**:
   - Ensure the catalog item is created in a **development** environment.
   - Perform testing and validation.
   - Promote changes to **production** once confirmed.

2. **Backup**:
   - Before making changes, ensure that a backup of relevant configurations (e.g., Service Catalog Items, User Criteria) is taken.

## Known Issues

- The catalog item is only accessible to users with the correct roles. If roles are not properly configured, users may not see the catalog item.
  
## Contributing

Feel free to fork the repository, submit pull requests, or raise issues for any bugs or suggestions for improvements.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

---

## Conclusion

This README provides a comprehensive guide to implementing a ServiceNow Service Catalog item for exclusive access to the Apple 15 Pro Max. By using **User Criteria** and **Role-based restrictions**, we can ensure the device is only available to specific groups within the organization.
