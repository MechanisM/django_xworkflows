ChangeLog
=========

0.5.0 (14/07/2012)
------------------

*New:*

    * Add rebuild_transitionlog_states management command to refill :attr:`~django_xworkflows.models.BaseTransitionLog.from_state`
      and :attr:`~django_xworkflows.models.BaseTransitionLog.to_state`.
    * Add indexes on various :class:`django_xworkflows.models.BaseTransitionLog` fields

*Bugfix:*

    * Fix :class:`django_xworkflows.models.WorkflowEnabled` inheritance

0.4.5 (12/06/2012)
------------------

*Bugfix:*

    * Don't default to :class:`~django_xworkflows.models.TransactionalImplementationWrapper` when using
      a :class:`django_xworkflows.models.Workflow`.

0.4.4 (29/05/2012)
------------------

*Bugfix:*

    * Serialize unicode of :attr:`xworkflows.base.State.title` in south ORM freezing.

0.4.3 (29/05/2012)
------------------

*Bugfix:*

    * Include migrations in package

0.4.2 (29/05/2012)
------------------

*Bugfix:*

    * Fix log=False/save=False when calling transitions

0.4.1 (29/05/2012)
------------------

*Bugfix:*

    * Avoid circular import issues when resolving :attr:`~django_xworkflows.models.Workflow.log_model`
      to a :class:`~django.db.models.Model`
    * Log source and target state names in :class:`~django_xworkflows.models.BaseTransitionLog`

0.4.0 (29/04/2012)
------------------

*New:*

    * Improve south support (
    * Run transition implementations in a database transaction

0.3.1 (15/04/2012)
------------------

*New:*

    * Introduce :class:`~django_xworkflows.models.StateField` for adding a :class:`~django_xworkflows.models.Workflow`
      to a model
    * Adapt to xworkflows-0.3.0


.. vim:et:ts=4:sw=4:tw=79:ft=rst:
