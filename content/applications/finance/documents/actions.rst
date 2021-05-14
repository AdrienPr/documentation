================
Workflow actions
================

Workflow actions are automated actions, such as adding tags to a file moving it to another
workspace, you can create and customize at the level of each workspace. They appear next to a file
whenever it meets the criteria you set. They can help you streamline the management of your
documents and your overall business operations.

Create workflow actions
=======================

To create workflow actions, go to :menuselection:`Configuration --> Workspaces`, select the
workspace where the action should apply, click on the *Actions* smart button, and click on *Create*.

.. image:: actions/access-workflow-actions.png
   :align: center
   :alt: Workflow actions smart button in Odoo Documents

.. note::
   An action applies to all *Child Workspaces* under the *Parent Workspace* you selected (i.e. to
   all sub-folders under the selected folder).

.. tip::
   If you use the :doc:`developer mode <../../general/developer_mode/activate>`, you can access
   directly all your actions by going to :menuselection:`Configuration --> Actions`.

Set the conditions
------------------

After having named your workflow action, you can set the conditions that trigger the appearance
of the action button on the right-side panel when selecting a file.

There are three basic types of conditions you can set:

#. **Tags**: you can both use the *Contains* and *Does not contain* conditions, meaning the files
   *must have* or *mustn't have* the tags you set here.

#. **Contact**: the files must be associated with the contact you set here.

#. **Owner**: the files must be associated with the owner you set here.

.. image:: actions/workflow-action-basic-conditions.png
   :align: center
   :alt: Example of a workflow action's basic condition in Odoo Documents

.. tip::
   If you don't set any condition, the action button appears for all files located inside the
   workspace you selected.

Advanced condition type: domain
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. important:: It is recommended to have some knowledge of Odoo development to configure properly
   *Domain* filters.

To access the *Domain* condition, the :doc:`developer mode <../../general/developer_mode/activate>`
needs to be activated. Once that's done, select the *Domain* condition type, and click on *Add
Filter*.

.. image:: actions/activate-domain-condition-type.png
   :align: center
   :alt: Activating the domain condition type in Odoo Documents

To create a rule, you typically select a field, an operator, and a value. For example, if you want
to add a workflow action to all the PDF files inside a workspace, set the field to: *Mime Type*, the
operator to *contains*, and the value to *pdf*.

.. image:: actions/domain-filter-example.png
   :align: center
   :alt: Example of a workflow action's domain condition in Odoo Documents

Click on *Add node* (plus circle icon) and *Add branch* (ellipsis icon) to add conditions and
sub-conditions. You can then specify if your rule should match *ALL* or *ANY* conditions. You can
also edit the rule directly using the *Code editor*.

.. image:: actions/add-branch-node-domain-condition.png
   :align: center
   :alt: Add a node or a branch to a workflow action's condition in Odoo Documents

Configure the actions
---------------------

Select the *Actions* tab to set up your action. You can simultaneously:

#. **Set Contact**: add a contact to the file, or replace an already existing contact with a new
   one.

#. **Set Owner**: add an owner to the file, or replace an already existing owner with a new one.

#. **Move to Workspace**: move the file to any workspace.

#. **Create**: create in your database one of the following items, which will be attached
   to the file:

   1. **Product template** (creates a product you can edit directly)
   2. **Task** (creates a Project task you can edit directly)
   3. **Signature request** (creates a new Sign template to send out)
   4. **Sign directly** (creates a Sign template to sign directly)
   5. **Vendor bill** (creates a vendor bill, based on the file content, using OCR and AI)
   6. **Customer invoice** (creates a customer invoice, based on the file content, using OCR and AI)
   7. **Vendor credit note** (creates a vendor credit note, based on the file content, using OCR
      and AI)
   8. **Credit note** (creates a customer credit note, based on the file content, using OCR
      and AI)
   9. **Applicant** (create a new HR application you can edit directly)

#. **Set Tags**: add, remove, and replace any number of tags

#. **Activities: Mark all as Done**: mark all activities linked to the file as done

#. **Activities: Schedule Activity**: create a new activity linked to the file as configured in the
   action. You can choose to set the activity on the document owner.

.. image:: actions/workflow-action-example.png
   :align: center
   :alt: Example of a workflow action Odoo Documents