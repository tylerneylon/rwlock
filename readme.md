# rwlock
* A short and simple read-write lock in Python*

This is a concurrency lock that allows you to have many simultaneous readers of
an object, but only allows one writer at a time.

       Usage:

            from rwlock import RWLock

            my_obj_rwlock = RWLock()

            # When reading from my_obj:
            with my_obj_rwlock.r_locked():
                do_read_only_things_with(my_obj)

            # When writing to my_obj:
            with my_obj_rwlock.w_locked():
                mutate(my_obj)
