.PHONY: all build install-libs clean

INSTALL_FILE = mvn install:install-file
GGJAVA_DIR = local/ggjava
GOLDENGATE_VERSION = 12.2.0.1.2.001

all: build

build:
	mvn clean package

install-libs:
	$(INSTALL_FILE) -Dfile=$(GGJAVA_DIR)/resources/lib/ggdbutil-$(GOLDENGATE_VERSION).jar -DgroupId=com.oracle.goldengate -DartifactId=ggdbutil -Dversion=$(GOLDENGATE_VERSION) -Dpackaging=jar
	$(INSTALL_FILE) -Dfile=$(GGJAVA_DIR)/resources/lib/gguserexitapi-$(GOLDENGATE_VERSION).jar -DgroupId=com.oracle.goldengate -DartifactId=gguserexitapi -Dversion=$(GOLDENGATE_VERSION) -Dpackaging=jar
	$(INSTALL_FILE) -Dfile=$(GGJAVA_DIR)/resources/lib/ggutil-$(GOLDENGATE_VERSION).jar -DgroupId=com.oracle.goldengate -DartifactId=ggutil -Dversion=$(GOLDENGATE_VERSION) -Dpackaging=jar

clean:
	mvn clean
