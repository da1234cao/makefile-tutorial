build_msg_var_fn = @echo "@@@@ $(1) @@@@"

define build_msg_fn
	@echo "@@@@ $(1) @@@@"
endef

all:
	$(call build_msg_var_fn, Using variables as functions)
	$(call build_msg_fn, Using real functions)
	$(call MY_FUNC,yes,This is a test message)