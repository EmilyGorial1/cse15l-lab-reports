**Part 1- Bugs**

The bug I have chosen from week 4 is the bug in the reverseInPlace() method

1.) A failure-inducing input as a JUnit test

```
public class ArrayTests 
{
  @Test
  public void testReverseInPlace()
  {
    int[] input1 = {1,2};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{2,1}, input1};
   }
}
```

2.) An input that does not induce a failure

```
public class ArrayTests 
{
  @Test
  public void testReverseInPlace()
  {
    int[] input1 = {1};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{1}, input1};
   }
}
```

3.) Screenshots of the symptom as the output of running the tests for each input above

Below are two screenshots that prove that whenn input1= {1}, testReverseInPlace() does not fail. Therefore, {1} is not a failure-inducing input.

![testReverseInPlace-nf1](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/7f2e25af-fc1e-44e3-83a4-bcf4bf897afa)

![testReverseInPlace-nf2](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/e5cee4b4-b5de-4b31-b495-2ac89029e06d)

Below is a screenshot that proves that when input1= {1,2}, testReverseInPlace() does fail. Therefore, {1,2} is a failure-inducing input.

![testReverseInPlace-f](https://github.com/EmilyGorial1/cse15l-lab-reports/assets/146862114/37e95678-175b-49f6-ba7e-d5a43aae606c)


4.) The before and after code

The code before

```static void reverseInPlace(int[] arr)
{
   for(int i = 0; i< arr.length; i+=1)
{
   arr[i]=arr[arr.length-i-1];
}
}
```

The code after

```static void reverseInPlace(int[] arr)
{
    for(int i = 0; i < arr.length/2; i += 1)
{
      int temporary = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1]= temporary;
}
}
```

5.) Briefly describe why the fix addresses the issue

The fix addresses the issue because, initally, the first half of the array was not being recorded, so the second half of the array was not properly reversed. For this reason, we created a temporary array to store the first half of the elements. Additionally, because we are swapping elements, we do not need the loop to run through the entire array, so we run through only half of the elements.

**Part 2- Researching Commands**

I have chosen the grep command

Command line options

1.) ``` grep -i ``` (searches upper and lower case)
     https://zwischenzugs.com/2022/02/02/grep-flags-the-good-stuff/

a.) ```grep -i``` on a file
```
Owner@DESKTOP-CF3LOP8 MINGW64 ~/Documents/GitHub/docsearch/technical (main)
$ grep -i "threat" 911report/chapter-8.txt


 THE SUMMER OF THREAT
                reports about threats. Indeed, there appeared to be possible threats almost
            To understand how the escalation in threat reporting was handled in the summer of
                2001, it is useful to understand how threat information in general is collected and
                disseminated to state and local law enforcement agencies. Threat reporting must be
                disseminated, either through individual reports or through threat advisories. Such
                advisories, intended to alert their recipients, may address a specific threat or be
                Central Intelligence GeorgeTenet was briefed regularly regarding threats and other
                reporting on terrorist threats and planned attacks increased dramatically to its
                community disseminated a terrorist threat advisory, indicating a heightened threat
            In response to these threats, the FBI sent a message to all its field offices on
                that there was a domestic threat.

```
Here, we can see that the -i flag on grep searches for a string in an un-case sensitive manner. We searched for the string "threat" and we can see that "threat" is displayed both in lower and upper case.

b.) ```grep -i``` on a directory

```
$ grep -i "targeted" *.txt

1471-2121-3-15.txt:          that SNIP1 is targeted to proteasome for degradation
1471-2121-3-15.txt:        ODC is the only protein known to be targeted by Az to
1471-2121-3-15.txt:        targeted by Az to proteasome has been suspected [ 20 ] . We
1471-2121-3-15.txt:        Smad1 is targeted to proteasome for degradation, a process
1471-2121-3-15.txt:        targeted, together with Smad1, to proteasome for
1471-2121-3-15.txt:        report, we showed that Smad1 itself is targeted to
1471-2121-3-15.txt:        Third, SNIP1 is co-targeted into the proteasome with Smad1,
1471-2121-3-15.txt:        that the Smad1/Smad4 bound SNIP1 can be further targeted to
1471-2121-3-25.txt:          Rab24/Rab1B chimera, the protein was no longer targeted
1471-2121-3-25.txt:        e.g. , D123I and T120A), are targeted
1471-2121-3-6.txt:          longer targeted to the peri-centromeric DNA (Fig. 5B).
1471-2121-3-6.txt:          still targeted to peri-centromeric chromatin, did not
1471-213X-1-1.txt:        non-neural tissues. Targeted mutations of the 
1471-213X-1-1.txt:        defect seen in mice with a deletion or targeted mutation in

```
In this output, we can see that all of the .txt files within our current working directory (/docsearch/technical/biomed) have been searched for the given string. Additionally, we see upper and lower case outputs which proves that the -i flag searches for both upper and lower case.

2.) ``` grep -c ``` (gives the number of lines that match the given string)
 https://developer.mozilla.org/en-US/blog/searching-code-with-grep/

a.) ```grep -c``` on a file
```
$ grep -c "FBI" chapter-3.txt
114

```
Here our output is 114 because the given string "FBI" is found in exactly 114 lines in the given file ("chapter-3.txt") in the working directory, 911reports.

b.) ```grep -c``` on a directory
```
$ grep -c "culture" *.txt
chapter-1.txt:0
chapter-10.txt:1
chapter-11.txt:0
chapter-12.txt:4
chapter-13.1.txt:6
chapter-13.2.txt:0
chapter-13.3.txt:0
chapter-13.4.txt:1
chapter-13.5.txt:2
chapter-2.txt:5
chapter-3.txt:4
chapter-5.txt:2
chapter-6.txt:0
chapter-7.txt:0
chapter-8.txt:0
chapter-9.txt:1
preface.txt:0
```
This output proves that grep -c gives us the number of times a given string ("culture") is found within all .txt files of our given directory (911reports). We can see each .txt file in 911reports listed with the number of lines containing our specified string next to it. 

3.) ``` grep -v ``` (shows all lines that do not contain specified word)
    https://zwischenzugs.com/2022/02/02/grep-flags-the-good-stuff/

a.) ```grep -v``` on a file

```
$ grep -v "threats" chapter-8.txt


            "THE SYSTEM WAS BLINKING RED"
            THE SUMMER OF THREAT
            As 2001 began, counterterrorism officials were receiving frequent but fragmentary
                everywhere the United States had interests-including at home.
            To understand how the escalation in threat reporting was handled in the summer of
                2001, it is useful to understand how threat information in general is collected and
                conveyed. Information is collected through several methods, including signals
                intelligence and interviews of human sources, and gathered into intelligence
                reports. Depending on the source and nature of the reporting, these reports may be
                highly classified-and therefore tightly held-or less sensitive and widely
```
Here, we can see that the grep -v command printed all lines in the specified file ("chapter-8.txt) that do not contain our given string ("threats).

b.) ```grep -v``` on a directory

```
grep -v "the" *.txt

chapter-9.txt:            The same three factors worked against successful communication among FDNY personnel.
chapter-9.txt:
chapter-9.txt:                that greatly repeats and enhances radio signal strength.
chapter-9.txt:
chapter-9.txt:                to prepare ourselves to meet it.
chapter-9.txt:                Because no one believes that every conceivable form of attack can be prevented,
chapter-9.txt:
chapter-9.txt:
preface.txt:
preface.txt:
preface.txt:
preface.txt:            PREFACE
preface.txt:                Democrats chosen by elected leaders from our nation's capital at a time of great
preface.txt:                avoid such tragedy again?
preface.txt:                27, 2002).
preface.txt:            Our mandate was sweeping. The law directed us to investigate "facts and circumstances
preface.txt:                to intelligence agencies, law enforcement agencies, diplomacy, immigration issues
preface.txt:                reviewed more than 2.5 million pages of documents and interviewed more than 1,200
preface.txt:                current and previous administrations who had responsibility for topics covered in
preface.txt:                our mandate. We have sought to be independent, impartial, thorough, and nonpartisan.        
preface.txt:                public testimony from 160 witnesses.

```

Due to the large output, I was only able to include a snippet that captures what is necessary. Here we can see that multiple files within a directory are being checked using grep-v. This is because we specified that we wanted all of the .txt files within the current directory (911reports) to be checked. If you look, you will notice that the lines printed do not contain the string "the" because the grep- v command is supposed to return all of the lines that do not contain the specified string, so all of the lines in the output do not contain this string.

4.) ``` grep -B ``` (shows lines before match)
https://zwischenzugs.com/2022/02/02/grep-flags-the-good-stuff/

a.) ```grep -B``` on a file

```
$ grep -B2 "culture" technical/911report/chapter-10.txt
                9/11 attacks, hold states and other actors responsible for providing sanctuary to
                terrorists, work with a coalition to eliminate terrorist groups and networks, and
                avoid malice toward any people, religion, or culture.
```
Here we can see that the grep-B (we put 2 after the B to have the command print the 2 lines before the line with the specified string) command prints the lines before the line containing the specified string. In our case, the specified string is "culture" and we want the 2 lines before to print, hence the 2 after the B. In the output, we can see that the thrid line contains our specified string and the the two lines above are simply the lines that come before this line.

b.) ```grep-B``` on a directory

```
$ grep -B2 "culture" *.txt
chapter-10.txt-                9/11 attacks, hold states and other actors responsible for providing sanctuary to
chapter-10.txt-                terrorists, work with a coalition to eliminate terrorist groups and networks, and
chapter-10.txt:                avoid malice toward any people, religion, or culture.
--
chapter-12.txt-                charity- functioning also as a form of income tax, educational assistance, foreign
chapter-12.txt-                aid, and a source of political influence. The Western notion of the separation of
chapter-12.txt:                civic and religious duty does not exist in Islamic cultures. Funding charitable
chapter-12.txt-                works is an integral function of the governments in the Islamic world. It is so
chapter-12.txt:                ingrained in Islamic culture that in Saudi Arabia, for example, a department within

```

Once again, only a snippet of the output is included, due to its size. However, in this snippet we can see that the command works on the directory just as it should. The flag -B2 specifies that the 2 lines preceding the line containing our string ("culture") are to be printed. The *.txt tells us that we need to look through every .txt file in the current directory and for every instance where we find "culture", we will print it, along with the 2 lines that precede it. We see this demonstrated for chapter-10.txt and chapter-12.txt (and more that are not included in this snippet).
