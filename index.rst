Variant demonstration
=====================

.. req:: Multi OS support
   :id: OSSUP1
   :architect: <<[1 in var.nested.other]: yes, no>>

   The platform shall support following OS: :need_incoming:`OSSUP1`

.. if:: var.platform == "linux"

    .. req:: A Requirement for Linux
        :id: LINUX1
        :links: OSSUP1

        The platform shall support Linux


.. if:: var.platform == "windows"

    .. req:: A Requirement for Windows
        :id: WINDOWS1
        :links: OSSUP1

        The platform shall support Windows

.. needimport:: import.json
    :filter: status == var.status

.. needtable::
