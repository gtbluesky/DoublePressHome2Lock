# DoublePressHome2Lock
1.
PhoneWindowManager.smali的
.method public constructor <init>()V的最后面的return-void之前加上
    new-instance v0, Lcom/android/internal/policy/impl/PhoneWindowManager$Injector;

    invoke-direct {v0, p0}, Lcom/android/internal/policy/impl/PhoneWindowManager$Injector;-><init>(Lcom/android/internal/policy/impl/PhoneWindowManager;)V

    iput-object v0, p0, Lcom/android/internal/policy/impl/PhoneWindowManager;->mHomeKeyTap:Ljava/lang/Runnable;
2.
  通过ContentResolver获取并设置"double_press_home_lock_screen"的值来写开关。
