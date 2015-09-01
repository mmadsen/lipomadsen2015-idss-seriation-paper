
all:
	mkdir -p output
	idss-seriation.py --inputfile=./pfg-cpl.txt --shapefile=1 --frequency=1 --xyfile=./pfgXY.txt --excel=1 --atlas=1 --debug 0 --graphs=1 --bootstrapCI=1 --bootstrapSignificance=0.95 --outputdirectory output

clean:
	rm -rf output
