# BaiTapHeDIeuHanh
Project 1: Thread

Bài 1:
Chỉnh sửa hàm timer_sleep() trong timer.c để block hàm trong thời gian ngủ.
Tạo Hàm Wakeup để gọi các thread đang ngủ dậy. 
Chỉnh sửa hàm timer_interrupt () bằng cách gọi hàm Wakeup thông qua foreach để duyệt ready_list và đánh thức các hàm cần thức dậy
Chỉnh sửa struct thread trong hàm thread.h: thêm vào biến tick_blocked . Giá trị này thay đổi khi gọi timer_sleep và giảm đi 1 mỗi khi timer_interrupt xảy ra.
Khi giá trị này giảm xuống 0 thì gọi hàm Wakeup

Bài 2:
Chỉnh sửa file thread.c: Thêm các hàm thread_cmp_priority(), thread_donate_priority(), thread_hold_lock(), thread_remove_lock(), lock_cmp_priority(), thread_update_priority(). 
Sửa hàm thread_create(),thread_unblock(),thread_set_priority(),thread_get_priority(),thread_yield(),init_thread()
Chỉnh sửa file synch.c: Chỉnh sửa các hàm sema_up(),sema_down(),lock_acquire(),lock_release(), cond_cmp_priority()
Chính sửa file thread.h: Thêm các biến base_priority, struct lock_holding va struct lock_seeking vào trong struct thread
Chỉnh sửa file synch.h: thêm struct elem và biến lock_priority vào trong struct lock, thêm hàm cond_cmp_priority()

Bài 3:

Chỉnh sửa file thread.c: Thêm các hàm thread_get_nice(),thread_set_nice(), thread_get_recent_cpu(),thread_get_load_avg(),
mlfqs_inc_recent_cpu(),mlfqs_update_load_avg_and_recent_cpu(),mlfqs_update_priority()
thêm biến toàn cục load_avg
Tạo mới file fixed_point.h trong thư mục thread.h
