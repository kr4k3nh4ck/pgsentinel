REGRESS_OPTS =--temp-config=./pgsentinel.conf --temp-instance=./tmp_check
REGRESS = pgsentinel-test

MODULE_big = pgsentinel
OBJS = pgsentinel.o get_parsedinfo.o

EXTENSION = pgsentinel
DATA = pgsentinel--1.0.sql
PGFILEDESC = "pgsentinel - active session history"

LDFLAGS_SL += $(filter -lm, $(LIBS))

PG_CONFIG = pg_config
PGXS := $(shell $(PG_CONFIG) --pgxs)
include $(PGXS)
