# Screen grab of shell session from class

```sh
⭐ ❯ python manage.py shell_plus
# Shell Plus Model Imports
from core.models import DailyRecord, Habit, User
from django.contrib.admin.models import LogEntry
from django.contrib.auth.models import Group, Permission
from django.contrib.contenttypes.models import ContentType
from django.contrib.sessions.models import Session
# Shell Plus Django Imports
from django.core.cache import cache
from django.conf import settings
from django.contrib.auth import get_user_model
from django.db import transaction
from django.db.models import Avg, Case, Count, F, Max, Min, Prefetch, Q, Sum, When
from django.utils import timezone
from django.urls import reverse
from django.db.models import Exists, OuterRef, Subquery
Python 3.10.7 (main, Nov  1 2022, 09:25:17) [Clang 14.0.0 (clang-1400.0.29.102)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
(InteractiveConsole)
>>> Habit.objects.all()
<QuerySet [<Habit: Walk steps>]>
>>> Habit.objects.get(pk=1)
<Habit: Walk steps>
>>> habit = Habit.objects.get(name="Walk steps")
>>> habit
<Habit: Walk steps>
>>> Habit.objects.get(pk=2)
Traceback (most recent call last):
  File "<console>", line 1, in <module>
  File "/Users/amygori/.local/share/virtualenvs/django-in-class-zqaVtQm9-python/lib/python3.10/site-packages/django/db/models/manager.py", line 85, in manager_method
    return getattr(self.get_queryset(), name)(*args, **kwargs)
  File "/Users/amygori/.local/share/virtualenvs/django-in-class-zqaVtQm9-python/lib/python3.10/site-packages/django/db/models/query.py", line 650, in get
    raise self.model.DoesNotExist(
core.models.Habit.DoesNotExist: Habit matching query does not exist.
>>> Habit.objects.filter(pk=2)
<QuerySet []>
>>> habit.name
'Walk steps'
>>> habit.pk
1
>>> habit2=Habit.objects.filter(pk=2)
>>> habit2
<QuerySet []>
>>> habit2.name
Traceback (most recent call last):
  File "<console>", line 1, in <module>
AttributeError: 'QuerySet' object has no attribute 'name'
>>> dir(habit)
['DoesNotExist', 'MultipleObjectsReturned', '__class__', '__delattr__', '__dict__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getstate__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__le__', '__lt__', '__module__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__setattr__', '__setstate__', '__sizeof__', '__str__', '__subclasshook__', '__weakref__', '_check_column_name_clashes', '_check_constraints', '_check_default_pk', '_check_field_name_clashes', '_check_fields', '_check_id_field', '_check_index_together', '_check_indexes', '_check_local_fields', '_check_long_column_names', '_check_m2m_through_same_relationship', '_check_managers', '_check_model', '_check_model_name_db_lookup_clashes', '_check_ordering', '_check_property_name_related_field_accessor_clashes', '_check_single_primary_key', '_check_swappable', '_check_unique_together', '_do_insert', '_do_update', '_get_FIELD_display', '_get_expr_references', '_get_field_value_map', '_get_next_or_previous_by_FIELD', '_get_next_or_previous_in_order', '_get_pk_val', '_get_unique_checks', '_meta', '_perform_date_checks', '_perform_unique_checks', '_prepare_related_fields_for_save', '_save_parents', '_save_table', '_set_pk_val', '_state', 'check', 'clean', 'clean_fields', 'date_error_message', 'delete', 'description', 'from_db', 'full_clean', 'get_constraints', 'get_deferred_fields', 'id', 'metric', 'name', 'objects', 'pk', 'prepare_database_save', 'records', 'refresh_from_db', 'save', 'save_base', 'serializable_value', 'unique_error_message', 'unit_of_measure', 'user', 'user_id', 'validate_constraints', 'validate_unique']
>>> user= User.objects.first()
>>> user
<User: admin>
>>> user.username
'admin'
>>> user.is_superuser
True
>>> Habit.objects.filter(user=user)
<QuerySet [<Habit: Walk steps>]>
>>> user.habits.all()
<QuerySet [<Habit: Walk steps>]>
>>> Habit.objects.filter(user=User.objects.first())
<QuerySet [<Habit: Walk steps>]>
>>> me=User.objects.first()
>>> Habit.objects.filter(user=me)
<QuerySet [<Habit: Walk steps>]>
>>> habit
<Habit: Walk steps>
>>> habit.records.all()
<QuerySet [<DailyRecord: Record for Walk steps>]>
>>> habit.records.all()
<QuerySet [<DailyRecord: Record for Walk steps>, <DailyRecord: Record for Walk steps>]>
>>>
```
