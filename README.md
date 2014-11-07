kent_student_lookup
===================

Using the ldap server provided by the University of Kent, this
software will dig and find the entry of a student associated to
the uid or last name given.

* ldapsearch is needed for the software to run properly. It is
often provided in the package `openldap'

usage: 

    $ kent_student_lookup Gayot

<stdout>

```
# extended LDIF
#
# LDAPv3
# base <ou=students,o=kent.ac.uk,o=uni> with scope subtree
# filter: (|(sn=Gayot)(uid=Gayot))
# requesting: ALL
#

# ojgg2, students, kent.ac.uk, uni
dn: uid=ojgg2,ou=students,o=kent.ac.uk,o=uni
mail: ojgg2@kent.ac.uk
objectClass: top
objectClass: person
objectClass: organizationalPerson
objectClass: dspswuser
objectClass: unikentuser
objectClass: inetorgperson
objectClass: inetUser
objectClass: posixaccount
objectClass: eduPerson
objectClass: account
objectClass: mailRecipient
givenName: O.J.G.
sn: Gayot
uid: ojgg2
cn: O.J.G.Gayot
displayName: O.J.G.Gayot
unikentaccountType: pgtstudent
unikentdepartment: comp

# search result
search: 2
result: 0 Success
```
