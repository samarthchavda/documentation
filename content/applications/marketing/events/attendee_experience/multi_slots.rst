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
This option allows the user to specify the maximum number of registrations allowed for a slot.

Create and manage slots
=======================

To access a dashboard of slots, click the :guilabel:`# Slot(s)` link. This opens a calendar view,
allowing users to view, create, and delete slots for the event.

.. note::
   Alternatively, users can also see a list of all created slots via the :icon:`oi-view-list`
   :guilabel:`(List)` view.

Calendar entries within the event's date range are clickable by the user. To create a slot, click a
calendar entry. Above the calendar, click the :guilabel:`Add` button. On the hovering pop-up, select
the start and end time of the slot. Then, specify the :guilabel:`Timezone` and, optionally, a
:guilabel:`Color` with which to display the slot on the calendar. With these details specified,
click :guilabel:`Add` to add the slot to the date.

To delete all records for a particular date, click the corresponding calendar entry and click
:icon:`fa-trash` :guilabel:`(Delete)`. Or, to delete a specific slot, click the specific slot item,
then, on the resulting popover, click :icon:`fa-trash` :guilabel:`(Delete)`.

Slot registration
=================

Attendees can register for slots from the event website.
