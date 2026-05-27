Variant demonstration
=====================

.. req:: Multi OS support
   :id: OS1

   The platform shall support following OS

   .. needtable::
      :filter: "OS1" in links_back

.. if:: var.platform == "linux"

    .. req:: A Requirement for Linux
        :id: LINUX1
        :links: OS1

        The platform shall support Linux


.. if:: var.platform == "windows"

    .. req:: A Requirement for Windows
        :id: WINDOWS1
        :links: OS1

        The platform shall support Windows


.. needpie::

.. needtable::
