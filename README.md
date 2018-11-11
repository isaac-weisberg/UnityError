# UnityError

## Introduction

Modern GUI is like a projection of the whole programming domain to a smaller scale. That is in that there are too many ways to do it wrong.

The primary motivation for establishment of this standard is to constraint error handling and propagation approaches in GUI driven applications to make it more consistent, controllable and localizable.

UnityError as a standard can be classified as a "Generalized Handlable Errors Interface" or "GHEI", for short.

# Definition

UnityError is a standard of robust error halding in GUI driven software systems.

The standard introduces a number of concepts.

## UnityError Object

This definition correlates to an object that represents an error produced by a FAEI. An exception (an error) object of a given high-level programming language is said to be UnityError-compliant when it is produced by a FAEI.

## FAEI: Finite Abstraction Extent Interface

This definition correlates to a programming interface that covers precisely one level of a finite programming abstraction extent. The abstraction extent of a programming interface is said to be finite when there is a certain guarantee that each member of a set of concepts, processes and definitions, formed from the union of concepts, processes and definitions defined by the abstraction and concepts, processes and definitions defined by the interface, can be classified as "making sense in the context of that particular union of concepts, processes and definitions defined by the abstraction and concepts, processes and definitions defined by the interface". A programming interface is said to cover precisely one level of a finite programming abstraction extent when there exists precisely one union of concepts, processes and definitions defined by the abstraction and of concepts, processes and definitions defined by the interface. Guess what, this also means FAEI is guaranteed to be able of producing a finite number of UnityError objects.

## GUI emission

This definition correlates to an object whose interface allows for a non-ambiguous mapping into the GUI programming interface with a sole goal of notifying a GUI user of an erroneous event. Typicially, but not neccessarily, a minimal medium satisfying this requirement is a string of localized human readable text which is shown in the GUI to the user in case of an erroneous event. A GUI emission is a result of GUI emitter's activity. 

## GUI emitter

This definition correlates to a constant interface and an implementation in a given end-user application that is responsible for consistent production of GUI emissions.

# Common practices

- If a project declares it's compliance to UnityError, it is the developers' responsibility to ensure that every single interface used in the application that is capable of producing exception (error) objects is UnityError compliant.
- To simplify usage, a GUI emitter used in the application is advised to be ready for generalized error case that is not compliant to UnityError. GUI emitters implementer is advised to acknowledge the development platform's built in capabilities to be able to provide more detailed GUI emissions.
- UnityError objects are advised to be propagated via recommended development platforms' means of exception (error) propagation mechanisms.
- If FAEI uses another FAEI as an implementation detail, the UnityError object produced by the inner FAEI must be encapsulated into a UnityError object produced by the outher FAEI.

# Naming Rationale

Unity is in fact a terrible mistake-- just, what associations can you recall with the word "unity"? Huh? Yeah, I know, right. Well, now this time it's for a reason.
