SASS = sassc
POSTCSS = postcss -u autoprefixer -r
BUILD_DIR = .

%.min.css : %.scss
	$(SASS) -t compressed -I ./ $< $@
	$(POSTCSS) $@
	mv $@ $(BUILD_DIR)/$(@F)

all: ./@material/components/components.min.css

.PHONY: all
