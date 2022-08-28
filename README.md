# SupplierManagementApi
This is a simple API that will manage Suppliers in a simulated environment using in Memory DB and implementing CQRS pattern using MediatR

# Basic Functionality
Provides a simple API with CRUD operations to perform the following actions

1) Onboard a supplier to a simulated environment
Goals
  Create Suppliers, including a descriptive record for each and guarantee uniqueness across the system

2) Maintain existing suppliers
Goals
  Update / Delete, have mechanisms in place to evolve a suppliers metadata information as well as inactivating the lifecycle

3) List suppliers and search explicity metadata
Goals
  Read all supplier lists
  Read suppliers by properties
  
User Management
Goal
  The simulated environment is made up of several roles to perform specific actions using RBAC
  Role: Admin - Can do anything in the system
  Role: Approver - Can issue approval of anything related to suppliers/status/activation or otherwise
  Role: Supplier - Can manage its own information
  Role: Reader - Can only read information across all suppliers
  Role: Questionnaire Creator - Can create questionnaires

  
# Next functionalities
Each supplier might have several manufacturing facilities, manage the relationship across those where one supplier can have 'n' references to manufacturing centers and likewise, those manufacturing centers can be re-utilized by other suppliers, thus maintaing state/relationship between suppliers and manufacturing centers

Add capability to track a supplier certification/credentials thru its lifecycle, determine when those expire, alert or raise events when they do, inactivate the validity of a supplier when this happens

Add capability to create questionaires for suppliers to be evaluated by an approval authority

More functionality to come at a later phase
