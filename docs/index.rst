.. phe documentation master file, created by
   sphinx-quickstart on Wed Jun 11 15:00:09 2014.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

pyphe  docs
===========

A Python 3 library for **P**\ artially **H**\ omomorphic **E**\ ncryption using the
`Paillier crypto system <https://en.wikipedia.org/wiki/Paillier_cryptosystem>`_.

The homomorphic properties of the paillier crypto system are:

- Encrypted numbers can be multiplied by a non encrypted scalar.
- Encrypted numbers can be added together.
- Encrypted numbers can be added to non encrypted scalars.


.. toctree::
   :maxdepth: 2

   installation
   usage
   caveats
   phe


.. toctree::
   :maxdepth: 1

   alternatives


Example
-------

    >>> from phe import paillier
    >>> public_key, private_key = paillier.generate_paillier_keypair()
    >>> secret_number_list = [3.141592653, 300, -4.6e-12]
    >>> encrypted_number_list = [public_key.encrypt(x) for x in secret_number_list]
    >>> [private_key.decrypt(x) for x in encrypted_number_list]
    [3.141592653, 300, -4.6e-12]

See :ref:`usage` for more extensive examples taking advantage of the homomorphic
properties of the *paillier* cryptosystem.



.. admonition:: Documentation generated

    |today|
