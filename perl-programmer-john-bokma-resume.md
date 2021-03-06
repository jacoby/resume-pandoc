---
name: John Bokma
keywords: perl, modern perl, cpan, cgi, nginx, apache, algorithms,
    freelance, msc, senior perl developer, xml, xslt, mysql, crawling, 
	scraping, remote, parsing
left-column:
  - 'Senior Perl Programmer'
  - 'Remote Only'
right-column:
  - 'Email: [contact@johnbokma.com](mailto:contact@johnbokma.com)'
  - 'Homepage: [http://johnbokma.com/](http://johnbokma.com/)'
  - 'Last Updated: \today'
...

# Summary

I am a freelance Senior Perl Developer with over 20 years' experience,
including exposure to MySQL, Nginx, Apache HTTP Server, Python, XSLT,
XML, RelaxNG, HTML, and CSS.

I'm an active proponent of Modern Perl. I like writing technical
documentation and unit tests; both have saved my customers and me a
lot of time over the years. I prefer to reuse code as much as
possible, hence I often start a project with researching available
(partial) solutions on CPAN.

My personal development projects include a blog that's generated from
XML files using Perl. I am currently working on a new version using
Markdown for input instead.

# Skills

## Perl

Web Scraping

: Over the years many projects I've been working on involved parsing
  crawled data and storing the required result. I like challenges like
  how to make web crawlers robust. I prefer strict parsing of HTML,
  with many checks and extensive logging using Log::Log4perl. This way
  changes to HTML, which often occur in my experience, are detected
  early and collecting invalid data or missing additional data might
  be avoided.

Parsing

: Besides parsing HTML I’ve also experience with parsing XML, several
  custom formats and domain specific languages (DSLs).

Data Munging

: Another task that often is assigned to me up is the conversion of
  data from one format to another; including data cleaning and
  verification. For example, modifying the text output of a legacy
  application in such a way that it’s suitable to be printed on newly
  designed labels. Often the input format has to be reverse
  engineered, a challenge I like.

Testing

: I prefer to use extensive testing of the custom modules and scripts
  I write. My favorite module is Test::Most because the module
  provides the most commonly used testing functions with a single
  line, avoiding a lot of boilerplate.

## Systems Administration

My main development environment is currently Ubuntu 15.10 running in a
virtual machine on OS X. My router runs OpenWrt, and I use a fanless
computer to study FreeBSD. I also use two different VPS providers for
hosting my websites. I do the administration of each of those systems,
e.g. updates, firewall rules and other security related tasks,
installing and configuring software e.g. Apache HTTP server, nginx,
Postfix, Dovecot, OpenSSH, MySQL.

## Documentation

I like to write technical documentation. I prefer to use mark up
languages like Org Mode (Emacs), Markdown, LaTeX. This makes version
control and searching from the command line easy. Plain text also
makes it very easy to generate code from documentation, and vice
versa. Where required, PDF versions can be generated using tools like
Emacs, Pandoc, pdflatex.

## Remote Work

I exclusively work remotely. Over the past years I have worked with
customers in Japan, USA, The Netherlands, and Canada. Working from
home provides me with a very productive environment with a minimal
number of interruptions. I use the Internet to stay in touch with
peers and my craft. I prefer to communicate using email. I have
experience with encrypted email using GnuPG, SSH with public key
encryption, Git, Subversion, and Github.

## Other Skills

I would be happy to discuss my experience with and exposure to: Python,
MySQL, XML, XSLT, XSL-FO, RelaxNG, Apache HTTP Server, nginx, HTML, CSS,
SEO.

# Recent Projects

## RedSocks - Malicious Threat Detection

Senior Perl Developer; February 2013 - December 2015; remote, part-time

Skills used:

: Modern Perl, LWP::UserAgent, Log::Log4perl, HTML::TreeBuilder,
    Test::Most, Test::More, Test::Output, JSON::XS, DBI, Try::Tiny,
    XML::Parser, XML::Writer, Email::Sender, Text::CSV_XS,
    MaxMind::DB::Reader, Dancer2, MySQL, RelaxNG, XSLT, Apache Ant,
    git, VirtualBox, nginx, cron, Emacs Org Mode, OpenSSL, iptables,
    HTML, CSS, GNU Privacy Guard (GPG).

Role overview:

:   -   Developing several web crawling Perl programs for gathering
        security related data, each crawler exporting downloaded data as
        a CSV file.

    -   Developing a Perl program that downloads security related data
        from several sources, verifies, cleans, and normalizes the data,
        and export it as an XML file.

    -   Developing a Perl program that post-processes the exported XML
        data to remove duplicate entries and overlapping ranges using a
        binary search algorithm.

    -   Developing a Perl program that parses the log files (Log4Perl)
        generated by aforementioned programs, generates reports, and
        emails those reports.

    -   Developing a Dancer2 web application to manually enter such data
        and store it into a MySQL database.

    -   Configuring and documenting virtual machines for each of the
        Perl programs, including designing firewall rules, and allowing
        access via rsync and HTTPs in a secure manner where required.

    -   Writing documentation on how to create certificates to allow
        client side certificate authentication in nginx (HTTPS), and
        configuring nginx accordingly.

    -   Writing extensive tests for all developed custom Perl modules
        and scripts.

    -   Designing and documentating file format specifications (XML,
        CSV) in Org Mode format (Emacs).

    -   Designing Relax NG schemata to validate XML files.
	
	-   Writing XSLT to transform XML output to older formats in order
	    to support client programs that require an older format prior
	    to being safely updated.

    -   Writing extensive technical documentation in Org Mode format
        (Emacs).

Interesting challenges:

:   Because the generated XML file is used in security related
    applications great care had to be taken to verify the downloaded
    data and make sure that malformed data wouldn’t end up in the final
    XML file. Because the generated data is used in programs written and
    maintained by other programmers high quality specifications and
    documentation was mandatory. In order to keep this documentation
    under version control Emacs’ Org Mode was used to write in plain
    text and convert it to, for example, PDF. Due to the asynchonous
    nature of the various programs avoiding race conditions is
    mandatory.

## SF Metrics

Senior Perl Developer; August 2015 - Present; remote, part-time

Skills used:

:   Modern Perl, LWP::UserAgent, Log::Log4perl, Test::Most, Text::Diff,
    XML::Parser, DBI, Config::Tiny, Try::Tiny, URI, JSON, git, MySQL,
    GitHub, Emacs Org Mode, Markdown, SEO.

Role overview:

:   - The development of a web crawler that downloads
      XML data, verifies this data, gathers some statistics, and stores
      desired data and statistics in a MySQL database. I am also
      reponsible for writing all the technical documentation,
      specifications, and example SQL queries. (current)

    - Developing a program to import a "JSON per line" database dump
	  into a MySQL database. Reverse engineering of the file format,
	  design of the 70+ MySQL database tables, logic to avoid
	  duplicate code.

Interesting challenges:

:   Because the web crawler program downloads data from the Internet it
    must be able to handle timeouts, partial downloads, etc. Moreover
    the XML parser must be able to distinguish between errors that can
    be safely ignored because they won’t affect the desired data much,
    and fatal errors. As a single crawl can gather a lot of data the
    MySQL database must be designed to deal with querying tens of
    millions of rows of data in mind.
:   The database dump program required several refactoring steps to
    avoid code repetition. Great care had to be taken to verify the
    types of JSON data and to verify all IDs had the correct type and
    were present in the dump.

## Eyeforyou

Senior Perl Developer; November 2011 - Present; remote, part-time

Skills used:

:   Modern Perl, CGI, DBI, Image::Magic, Test::Most, Util::Image, Apache
    HTTP server, HTML, CSS. MySQL, git, subversion.

Role overview:

:   Maintenance of several legacy Perl CGI programs. Adding new
    functionality like scaling of photos and adding watermarks to
    photos. MySQL database optimizations to improve search query time.
    Adding new search options.

Interesting challenges:

:   The Perl CGI program is mostly legacy code which makes extending
    and/or modifying it quite a challenge. Custom Perl modules are used
    to group both new functionality and factored out code logically and
    to support testing.

# Education

TH “Rijswijk”

:   Computer Science, BSc; 1991.

Utrecht University

:   Design of Algorithms, MSc; 1994.

# Courses

DelftX: FP101x Introduction to Functional Programming

: Haskell, Monads; final grade: 98%; December 2014;
  [course info](https://courses.edx.org/courses/DelftX/FP101x/3T2014/info);
  [verified certificate (PDF)](https://s3.amazonaws.com/verify.edx.org/downloads/6d4d4270a06545ecbdc12f4a9c5cafa4/Certificate.pdf).

Introduction to Big Data with Apache Spark

: Apache Spark, Python, Vagrant; final grade: 100%; July 2015;
  [course info](https://courses.edx.org/courses/BerkeleyX/CS100.1x/1T2015/info)
  ;
  [verified certificate (PDF)](https://s3.amazonaws.com/verify.edx.org/downloads/f94790bd236c48ca9e943fa50c5d8c48/Certificate.pdf).

Scalable Machine Learning

: Apache Spark, Python, Vagrant; final grade: 100%; August 2015;
  [course info](https://courses.edx.org/courses/BerkeleyX/CS190.1x/1T2015/info)
  ;
  [verified certificate (PDF)](https://s3.amazonaws.com/verify.edx.org/downloads/90d3c61ff8bb49d080c914dbfa1aa1e7/Certificate.pdf).

# GitHub

resume-pandoc

 : LaTeX resume template for Pandoc based on a LaTeX resume by Jason
R. Blevins. The template can be used to create either a LaTeX or PDF
file given a Markdown file as input. The template was used to create
this resume. Repository:
[resume-pandoc](https://github.com/john-bokma/resume-pandoc).

# Miscellaneous

Developing Web Applications with Apache, MySQL, memcached, and Perl

: Technical Editor; ISBN-13: 978-0470414644; 2009.

Modern Perl

: I did some voluntarily reviewing, and am listed in the Credits
  section. [Electronic versions](http://onyxneon.com/books/modern_perl/).

A Retrospective Study of Polyallergy as A Marker of Non-Epileptic Seizures in the Epilepsy Monitoring Unit
	  
: I provided the Perl program used in this study; article in
  Psychosomatics 55(6); June 2014;
  [abstract](https://www.researchgate.net/publication/262923044_A_Retrospective_Study_of_Polyallergy_as_A_Marker_of_Non-Epileptic_Seizures_in_the_Epilepsy_Monitoring_Unit).

Optimization of molecular methods and statistical procedures for forensic fingerprinting of microbial soil communities

: I assisted with Perl programming; article in International Research
  Journal of Microbiology (IRJM); ISSN: 2141-5463; Vol. 3(11) pp.
  363-372; November 2012;
  [full length research paper (PDF)](http://www.interesjournals.org/full-articles/optimization-of-molecular-methods-and-statistical-procedures-for-forensic-fingerprinting-of-microbial-soil-communities.pdf?view=inline)

Languages

: Dutch (native), English (fluent).
