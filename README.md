GStreamer 1.x Scala Core (gst1-Scala-core)
========================================

*** not ready for releast yet, all information has not been verified ***

gst1-Scala-core is a set of Scala bindings for [GStreamer 1.x][gstreamer]. GStreamer
is an open-source, pipeline-based multimedia framework written in C. It allows a
programmer to create a wide variety of media-handling pipelines inside
applications, from simple media playback, to encoding, live-streaming, analysis,
machine learning, WebRTC, and more.

GStreamer is designed to be cross-platform, and binaries are provided for a range
of operating systems. gst1-Scala-core is actively tested on Linux (x86 and Arm),
Windows and macOS, but it should work on any OS with Scala, JNA, and GStreamer support.
The bindings are in use in a wide variety of commercial and open-source projects,
across desktop, server, and embedded.

## Usage

See the [examples repository][gst1-examples] for some self-contained projects to
get you started. Use the [Scaladoc][gst1-Scaladoc]! - all classes are documented,
and include links to the relevant native documentation where appropriate. Please use the
[GStreamer-Scala mailing list][gstreamer-Scala-group] to ask questions.

To try the examples you will need [GStreamer installed][gstreamer-download] on your
system. Other options for deployment are possible - see requirements below.

Please note that this is not an easy-to-use multimedia framework for beginners. It currently
requires people to know the Scala language and be familiar with the GStreamer framework
(and possibly be prepared to apply things from tutorials on GStreamer programming in
other languages to the Scala bindings).

## History and status

Releases are available via Maven Central (under the `org.freedesktop.gstreamer`
group ID), or can be downloaded from the GitHub [release page][gst1-releases].

Since v1.0.0, the bindings are functionally and API stable, but note that the low-level
packages are _effectively_ non-public and subject to change at any time.

The lead maintainer of the bindings is Joel Bushart at [HHM21C.com]. ***todo/ correct ***
The project began in 2024 as a fork of the java gstreamer bindings [GStreamer-Java][gtreamer-java]
bindings for GStreamer 0.10 started by Wayne Meissner. Numerous other people have made
valuable contributions to the original project and the 1.x fork over the years.

## Help and support

Help on getting started, and support for open-source projects, can be obtained
from the [GStreamer-Scala mailing list][gstreamer-Scala-group].

Commercial support and custom development is available, and sponsorship of additional
features is also welcome - please email info@codelerity.com to discuss.

## Requirements

The bindings are tested on Linux, Windows and macOS. Windows and macOS installers
for GStreamer are available from the [GStreamer project itself][gstreamer-download].
Linux users should be able to get GStreamer from their distribution repository if it
isn't already installed.

You will need to have the GStreamer 1.x native libraries available in your system path
in order to use the bindings, and may also need to set up environment variables
depending on how GStreamer is installed. See the `Utils` class in each example project
for one possible way to configure this inside your Scala code.

It is possible to ship GStreamer with your application should you want your users not
to have to install it separately. There are various ways to achieve this - see the
[upstream documentation][gstreamer-deploy]. Advice is also available via the support
options above.

The minimum supported version of GStreamer is 1.8.x. If you require access to features
related to later GStreamer versions (eg. WebRTC support), make sure to request the
version you need when calling `Gst.init(..)`

You will also need the [JNA (Java Native Access)][jna] library, minimum version 5.2.0.

The minimum required Java version is Java 8.

## Contributions

Contributions to the library are welcomed, either to fix/enhance current features,
or bring in new ones. There is also ongoing work to rework the low-level bindings.

**Before opening a Pull Request**, please raise an issue or discuss your contribution on
the mailing list. New features must have tests selectively applied if targeting
features in versions of GStreamer above 1.8. All Pull Requests will be automatically
tested via CI, and all tests must pass before merging will be considered.

If you are making a large contribution to benefit a commercial project, sponsorship
of integration and support time would be appreciated.


[gstreamer]: https://gstreamer.freedesktop.org/
[gstreamer-download]: https://gstreamer.freedesktop.org/download/
[gstreamer-deploy]: https://gstreamer.freedesktop.org/documentation/deploying/index.html
[gstreamer-Scala]: https://github.com/gstreamer-scala/gstreamer-scala
[gst1-examples]: https://github.com/gstreamer-scala/gst1-scala-examples
[gst1-scaladoc]: https://scaladoc.io/doc/org.freedesktop.gstreamer/gst1-scala-core
[gst1-releases]: https://github.com/gstreamer-scala/gst1-scala-core/releases
[gstreamer-scala-group]: https://groups.google.com/forum/#!forum/gstreamer-scala
[jna]: https://github.com/scala-native-access/jna
[codelerity]: https://www.codelerity.com
