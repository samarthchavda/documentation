==============
Batch payments
==============

Batch payments act as an organizational tool that allows you to group multiple individual payments
(either from customers or to vendors) into a single file. Rather than managing dozens of
transactions one by one, you can consolidate them to generate a detailed deposit slip or a single
electronic payment file. The primary advantage of this method is the simplification of the bank
reconciliation process; when a single bulk sum appears on your bank statement, Odoo uses the batch
reference to automatically match and reconcile all the underlying payments at once.

For customer batch payments, the feature is most commonly used for handling physical assets like
checks or cash. For example, if you receive several checks throughout the day, you can group them
into a single batch to print a deposit slip for the bank, ensuring your internal records mirror the
total amount shown on your bank statement. On the vendor side, batch payments are essential for bulk
electronic transfers. Instead of manually processing each supplier invoice, you can select multiple
bills and generate a single outgoing payment file—such as SEPA or NACHA—to be uploaded directly to
your banking portal.

The format of these payment files varies depending on your region and bank requirements. In Europe,
most businesses utilize the SEPA (Single Euro Payments Area) standard for seamless cross-border
transfers. However, outside of Europe, many countries adopt the broader ISO 20022 standard or
maintain their own unique national systems. Because these requirements are region-specific, it is
important to consult the Odoo Fiscal Localization page for your specific country to see which
formats are supported.

Batch payments allow grouping payments from multiple customers or vendors into a single batch and
generating a detailed deposit slip or payment file with a batch reference. This reference can be
used during :doc:`reconciliation <../bank/reconciliation>` to match bank transactions with the
corresponding payments. This feature is particularly useful for submitting :doc:`SEPA payments
<sepa_payments>`, depositing cash payments or :doc:`checks <checks>`, or generating outgoing payment
files, such as :ref:`SEPA <accounting/sepa_payments/sct>` or :ref:`NACHA <l10n_us/nacha>`.

.. seealso::
   - :doc:`sepa_payments`
   - :ref:`l10n_us/nacha`
   - :doc:`../../fiscal_localizations`

Configuration
=============

(Missing vendor batch payment?)

To enable batch payments, go to :menuselection:`Accounting --> Configuration --> Settings`, scroll
down to the :guilabel:`Customer Payments` section, and enable :guilabel:`Batch Payments`.

.. _accounting/batch/creation:

Batch creation
==============

(How to create batch customer/vendor payments), how to create them from the payment list view,
how to create them from vendors/customers --> batch payments and explain the fields there)

To create a batch payment, follow these steps:

#. Make sure all payments to be included in the batch have been :ref:`registered
   <accounting/payments/from-invoice-bill>`.
#. Go to :menuselection:`Accounting --> Customers --> Payments`.
#. Select the payments to include in the batch.

   .. note::
      All payments in the batch must use the same payment method. If needed, payments can be grouped
      using the :guilabel:`Payment Method Line`.

#. Click :guilabel:`Create batch` or click :icon:`fa-cog` :guilabel:`Actions` and select
   :guilabel:`Create batch payment`.
#. In the batch payment form, review the selected payments. If any individual payments were missed,
   click :guilabel:`Add a line` and select the missing payments to be included in the batch.
#. Once all relevant payments are included, click :guilabel:`Validate` to finalize the batch.

.. note::
   Once validated, no additional payments can be added to a batch.

.. tip::
   - Click :guilabel:`Print` to download a list of the included payments.
   - To view existing batch payments, go to :menuselection:`Accounting --> Customers --> Batch
     Payments`.

Bank reconciliation
-------------------

Once the bank transactions :doc:`have been created <../bank/transactions>` in your database, you can
:ref:`reconcile them with the batch payment <reconciliation/batch-payments>`.

.. image:: batch/batch-reconciliation.png
   :alt: Reconciling the batch payment with all its transactions

.. note::
   If a specific payment could not be processed by the bank or is missing, remove the related line
   from the resulting entry section of the reconciliation view using the :icon:`fa-trash`
   (:guilabel:`delete`) button before validating the reconciliation.

.. seealso::
   - :doc:`../payments`
   - :doc:`sepa_payments`
