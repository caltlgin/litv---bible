litv: litv.sh litv.awk litv.tsv
	cat litv.sh > $@

	echo 'exit 0' >> $@

	echo '#EOF' >> $@
	tar czf - litv.awk litv.tsv >> $@

	chmod +x $@

test: litv.sh
	shellcheck -s sh litv.sh

.PHONY: test
