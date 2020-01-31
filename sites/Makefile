all:
	cat repositories.txt | grep "http" > rendered/repositories.txt
	cat forums_qa.txt | grep "http" > rendered/forums_qa.txt
	cat docs.txt | grep "http" > rendered/docs.txt
	cat blogs.txt | grep "http" > rendered/blogs.txt
	> rendered/all.txt && cat *.txt | grep "http" > rendered/all.txt && wc -l rendered/all.txt
