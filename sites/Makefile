all:
	grep "http" repositories.txt > rendered/repositories.txt
	grep "http" forums_qa.txt > rendered/forums_qa.txt
	grep "http" docs.txt > rendered/docs.txt
	grep "http" blogs.txt > rendered/blogs.txt
	> rendered/all.txt && grep -h "http" *.txt > rendered/all.txt && wc -l rendered/all.txt
