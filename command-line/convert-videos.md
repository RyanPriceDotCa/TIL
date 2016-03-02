#Convert Videos with avconv

Command to convert mp4 to flv with avconv:

avconv -i source_file.mp4 -c:v libx264 -ar 22050 -crf 28 result_file.flv
