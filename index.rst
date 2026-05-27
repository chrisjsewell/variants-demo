Variant demonstration
=====================

.. req:: Multi OS support
   :id: OS1

   The platform shall support

.. if:: var.platform == "linux"

    .. req:: A Requirement for Linux
        :id: LINUX1
        :link: OS1

        Here is the content


.. if:: var.platform == "windows"

    .. req:: A Requirement for Windows
        :id: WINDOWS1
        :link: OS1

        Here is the content
