===========
Event slots
===========

In Odoo **Events**, users can create multiple time-slots for an event, giving attendees the
flexibility to register for a specific time or session.

Configuration
=============

To create slots for an event, the feature must be enabled on an event form. To do this, open the
**Events** app, then navigate to an existing event or :doc:`create a new one
<../event_setup/create_events>`.

On the event form, select the :guilabel:`Multiple Slots` checkbox. A :guilabel:`# Slot(s)` link
appears next to the field, displaying the total number of slots for the event.

Under the *Tickets* tab, a :guilabel:`Maximum per slot` column appears on event registration lines.
This option allows the user to specify the maximum number of registrations allowed for a slot. If a
slot reaches the maximum registration count, it is marked as *Sold Out* on the registration webpage.

Viewing slots
=============

To access a dashboard of slots, click the :guilabel:`# Slot(s)` link. This opens a
:icon:`oi-view-calendar` :guilabel:`(Calendar)` view with clickable entries, allowing users to
interactively create and delete slots on valid dates of the event.

Alternatively, users can also see a list of all created slots via the :icon:`oi-view-list`
:guilabel:`(List)` view.

Create slots
============

.. tabs::

   .. tab:: Calendar

      To create slots in the calendar view, click on a calendar entry, or click and drag to select
      multiple entries. A :guilabel:`# Selected` appears above the calendar, displaying the selected
      dates for which to create slots.

      Then, click the :guilabel:`Add` button. On the resulting popover, select the start and end
      time of the slot. Next, specify the :guilabel:`Timezone` and the display :guilabel:`Color` of
      the slot. Click :guilabel:`Add` to add the slot to the calendar entry.

   .. tab:: List

      To create a slot in the list view, click :guilabel:`New`. This creates a new line to configure
      slot options.

      In the calendar popover, select the :guilabel:`Date` of the slot. Then, under the
      :guilabel:`From` and :guilabel:`To` columns, specify the respective start and end times.
      Finally, select a display :guilabel:`Color` representing the slot.

      Click :guilabel:`Save` to create the slot.

      .. warning::
         If the configured date and time is outside the valid date range of the event, Odoo returns
         an error.

Delete slots
============

.. tabs::

   .. tab:: Calendar

      To delete all records for a particular date, click the corresponding calendar entry and click
      :icon:`fa-trash` :guilabel:`(Delete)` at the top of the calendar.

      Alternatively, to delete a specific slot, click the specific slot item. On the resulting popover,
      click :icon:`fa-trash` :guilabel:`(Delete)`.

   .. tab:: List

      To delete all slots, click the checkbox next to the :guilabel:`Date` column. Or, to delete a
      specific slot, click the checkbox next to the slot. Then, click the :icon:`fa-cog`
      :guilabel:`Actions` button and select the :icon:`fa-trash` :guilabel:`Delete` option.

Slot registration
=================

Similar to registering for an event, attendees can register for slots from the event website. When
a visitor arrives on the event website, they can click the :guilabel:`Register` button to select
the desired slot and purchase a ticket.
