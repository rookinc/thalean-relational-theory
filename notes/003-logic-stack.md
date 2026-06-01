# Logic Stack for Thalean Relational Theory

Status: working theory note
Date: 2026-06-01
Scope: formal stack for existential relativity, discrete action theory, admissibility, and field effect

## 1. Purpose

This note builds the logic stack for Thalean Relational Theory.

The foundation note defines the umbrella. The glossary stabilizes the vocabulary. This note begins the formal architecture.

The goal is to make the following thesis expressible:

Identity is not isolated substance. Identity is relational invariance under admissible change.

A second thesis completes the active loop:

A thing is what its relations make possible, and what its presence makes possible for others.

Together, these require more than ordinary graph language and more than ordinary modal logic. TRT needs a layered logic stack that can speak about:

relations,
frames,
possibility,
necessity,
typed access,
time,
action,
admissibility,
invariance,
and frame update.

The guiding question is:

What formal language can describe a thing as a relational position that receives constraint, acts through admissible transformations, and changes the possibility-space around itself?

## 2. Informal overview

The stack is:

1. Relational graph base
2. Basic modal logic
3. Typed modal logic
4. Temporal logic
5. Dynamic logic
6. Admissibility logic
7. Update or graph-transformation semantics

Each layer adds one missing capability.

The graph base gives discrete relational structure.

Modal logic gives possibility and necessity relative to a frame.

Typed modal logic distinguishes different kinds of relation.

Temporal logic adds ordered persistence.

Dynamic logic makes actions explicit.

Admissibility logic separates lawful transformation from arbitrary mutation.

Update semantics allows actions to change the relational frame itself.

The result is not yet a single finished calculus. It is a design target:

Thalean Relational Theory wants typed dynamic modal logic over updateable relational frames.

## 3. Layer 0: relational graph base

Start with a labeled relational structure:

G = (V, E, L)

where:

V is a set of vertices, states, entities, or positions.
E is a set of relations, edges, incidences, adjacencies, or constraints.
L is a labeling function or label store for vertices, edges, and possibly higher structures.

At this layer, a graph is not treated as a picture. It is treated as a finite relational object.

A vertex is not merely a dot. It is a relational position.

The identity of a vertex depends on its relational profile.

A relational profile may include:

labels,
neighbors,
incident edges,
typed relations,
paths,
cycles,
distances,
cuts,
symmetries,
quotient behavior,
admissible actions,
and effects on surrounding structure.

A minimal profile notation:

Profile_G(x)

This means the relational profile of entity x inside graph or frame G.

The first identity approximation is:

Id_G(x) = Profile_G(x)

This is not yet a final metaphysical claim. It is a working formal posture:

To identify x inside G is to identify x by its position and role in the relational structure of G.

## 4. Layer 1: basic modal logic

A modal frame is usually given as:

F = (W, R)

where:

W is a set of worlds, states, or positions.
R is an accessibility relation on W.

A modal model adds valuation:

M = (W, R, V)

where V assigns propositions to worlds.

TRT reads this graph-theoretically:

W is a set of possible relational positions or states.
R says which positions are accessible from which others.
V labels positions with facts or properties.

The basic modal operators are:

Diamond p: p is possible from here.
Box p: p is necessary from here.

ASCII notation:

<>p means there exists an accessible state where p holds.
[]p means p holds in every accessible state.

In graph language:

<>p means p holds somewhere reachable by the relevant relation.
[]p means p holds everywhere reachable by the relevant relation.

This gives TRT a first formal expression of frame-relative truth.

A proposition is not evaluated in isolation. It is evaluated at a world, state, vertex, or frame-position.

Informal TRT reading:

Meaning is not free-floating. It is evaluated from somewhere inside a relational frame.

## 5. Layer 2: typed modal logic

One accessibility relation is too blunt.

TRT needs different relation types.

For example:

adjacency,
incidence,
transport,
memory,
observation,
projection,
quotient,
constraint,
action,
and context.

So replace one relation R with a family of relations:

R_i for i in I

A typed modal model becomes:

M = (W, {R_i}_{i in I}, V)

For each relation type i, we get modal operators:

<>_i p
[]_i p

Meaning:

<>_i p means p is possible by relation type i.
[]_i p means p holds across every i-accessible alternative.

This matters because a thing can be stable under one relation type and unstable under another.

A structure may survive relabeling but fail perturbation.
It may survive projection but fail lifting.
It may be locally stable but globally incoherent.
It may be reachable by transport but not by symmetry.
It may be visible in a quotient but not faithful to the full object.

Typed relations prevent false equivalence.

Core TRT rule:

Do not collapse distinct relation types unless the collapse itself is justified.

## 6. Layer 3: temporal logic

Modal logic says what is possible from a position. Temporal logic adds order.

Useful temporal operators include:

X p: p holds in the next state.
F p: p eventually holds.
G p: p always holds.
p U q: p holds until q holds.

ASCII notation:

X p
F p
G p
p U q

TRT needs temporal language because identity is not merely a snapshot.

Identity is coherence through transformation.

An entity may remain recognizable through a sequence of admissible changes. Or it may lose its defining profile after a certain transition.

Temporal logic lets us ask:

What persists?
What eventually emerges?
What always remains constrained?
What holds until collapse?
What changes after a specific action?
What returns after a cycle?

In TGT language, this connects naturally to walks, cycles, transport, recurrence, quotient traces, and sign-closing versus identity-closing behavior.

Informal TRT reading:

A thing is not only what it is at one moment. It is what remains legible through ordered change.

## 7. Layer 4: dynamic logic

Dynamic logic makes actions explicit.

Instead of only asking what is possible from here, dynamic logic asks what happens after action a.

Common dynamic operators:

<a>p means there exists an execution of action a after which p holds.
[a]p means after every execution of action a, p holds.

ASCII notation:

<a>p
[a]p

TRT reading:

<a>p means action a can bring about p.
[a]p means action a necessarily preserves or produces p.

This is central for Discrete Action Theory.

An action is not merely motion. It is a lawful finite transformation inside a relational structure.

An action has:

a before-state,
an after-state,
a local context,
a rule of admissibility,
a trace,
and an effect.

At this layer, identity can be defined as action-invariant over an action family A.

Informal definition:

x remains itself under action family A when all relevant actions in A preserve the defining profile of x.

Sketch:

Inv_A(x, P) iff for every a in A, [a]P(x)

This still needs admissibility. Not every action should count. That leads to the next layer.

## 8. Layer 5: admissibility logic

TRT does not care about arbitrary mutation as a test of identity.

It cares about lawful transformation.

So we introduce admissibility.

Adm(a, S) means action a is admissible in state or frame S.

Adm(a, S, x) means action a is admissible for entity x in state or frame S.

We may also define:

A_S = the set of actions admissible in S
A_S(x) = the set of actions admissible for x in S

Now identity should be tested only against admissible actions.

Refined invariant:

Inv_A(x, P, S) iff for every a in A, if Adm(a, S, x), then [a]P(x)

Plain English:

P is an invariant of x in S under A when every admissible action in A preserves P.

This is a crucial boundary.

Without admissibility, any structure can be destroyed by arbitrary mutation. That proves nothing.

Admissibility separates meaningful transformation from noise.

Core TRT rule:

Only admissible transformations count as lawful tests of identity.

## 9. Layer 6: update semantics

The previous layers can still be read as movement inside a fixed frame.

But TRT also requires field effect.

A thing is shaped by its relations, but it also changes the relational field around it.

Therefore an action may change not only the current state, but the frame itself.

Let a frame or model be:

S = (W, R, V)

or in typed form:

S = (W, {R_i}_{i in I}, V)

An update action maps one frame to another:

a: S -> S'

where:

S' = (W', {R'_i}_{i in I'}, V')

This means action a may change:

the available states,
the labels,
the accessibility relations,
the relation types,
the admissibility rules,
the local neighborhood,
or the global coherence structure.

This captures field effect.

A static question asks:

What is possible from here?

A dynamic relational update question asks:

What action is admissible from here, what does it preserve, and how does it change what becomes possible next?

This is the key formal move.

TRT cannot be fully captured by static modal logic alone. It needs dynamic update semantics over relational frames.

## 10. Field signature

If an action changes the frame, we need a way to describe its effect.

Let:

a(S) = S'

Then the field signature of a in S is the structured difference between S and S'.

FieldSig(a, S) = Delta(S, S')

At minimum, this may include:

changes to vertices or states,
changes to relations,
changes to labels,
changes to admissibility,
changes to reachability,
changes to invariants,
changes to local neighborhoods,
changes to global coherence.

A graph-specific version may track:

Delta V
Delta E
Delta L
Delta paths
Delta cycles
Delta distances
Delta automorphisms
Delta admissible actions

Plain English:

The field signature of an action is the difference it makes to what becomes possible, necessary, reachable, forbidden, or preserved around it.

This formalizes the slogan:

A thing is what its relations make possible, and what its presence makes possible for others.

## 11. Existential invariant

The most important concept in the stack is the existential invariant.

Definition:

An existential invariant is a property or relational profile of an entity that is preserved across a specified family of admissible frame transformations.

Formal sketch:

ExistInv(x, P, A, S) iff for every a in A, if Adm(a, S, x), then [a]P(x)

For frame updates:

ExistInv(x, P, A, S) iff for every a in A, if Adm(a, S, x) and a(S) = S', then P remains true of the corresponding trace of x in S'

This requires a correspondence rule because the updated frame may not contain x in exactly the same way.

So we need a trace or transport map.

Let:

tau_a,S(x) = the image, continuation, or trace of x after action a updates S to S'

Then:

ExistInv(x, P, A, S) iff for every a in A, if Adm(a, S, x), then P(tau_a,S(x)) holds in S'

Plain English:

P is an existential invariant of x when every relevant lawful transformation carries x into a continuation where P still holds.

## 12. Trace

A trace is the continuation or observable residue of an entity, action, or structure across transformation.

In static graph settings, a trace may be a projected image, quotient shadow, preserved label, path, signature, invariant, or mapped vertex.

In dynamic settings, a trace records what remains after action.

Trace is necessary because update semantics can change the frame.

If S becomes S', we need to ask:

What counts as the continuation of x?
What is preserved?
What is lost?
What is newly induced?
What witness shows the transformation?

Trace notation:

Trace_a,S(x)

or

tau_a,S(x)

The trace concept is important for avoiding sloppy identity claims.

If a thing changes, we should not simply assume it is the same thing. We should specify the trace relation that justifies continuity.

## 13. Witness discipline

Every formal layer should be connected to witness discipline.

A claim should identify:

the frame,
the relation types,
the admissible actions,
the property or profile being tested,
the transformation family,
the trace map,
and the invariant or failure.

A minimal TRT claim form:

In frame S, entity x has property P as an existential invariant under admissible action family A, witnessed by trace rule tau and verification artifact W.

Plain version:

Tell me the structure.
Tell me the thing.
Tell me the relation.
Tell me the allowed action.
Tell me what survives.
Tell me how you checked.

This connects directly to CoRI.

CoRI asks how apparent patterns become accountable structures. The logic stack gives a formal path for turning that question into a test.

## 14. Relation to coherence gap

The coherence-gap method fits naturally into the logic stack.

A surface can satisfy local tests while failing global coherence.

In modal terms:

A local neighborhood may satisfy p.

But p may fail across wider accessibility relations.

In dynamic terms:

A surface may survive easy actions.

But it may fail under adversarial admissible transformations.

In update terms:

A surface may look coherent in S.

But after a lawful frame update a: S -> S', the surface may lose its trace, break its invariants, or fail to integrate with the changed relational field.

A coherence gap occurs when local appearance and global relational accountability diverge.

TRT interpretation:

A coherence gap is a failure of existential invariance across the relevant admissible transformations of a relational frame.

## 15. Relation to Thalean Graph Theory

TGT gives the finite mathematical test bench for this stack.

A Thalean graph object can be studied as:

a finite relational frame,
a typed graph,
an admissible action space,
a quotient system,
a transport system,
a witness surface,
and an invariant-bearing object.

The G60/G30/G15 stack can be read through this lens:

G60 as fuller graph-level organism,
G30 as an intermediate quotient or transport-visible layer,
G15 as a compressed sector register or quotient-visible surface.

The incidence matrix M, quadratic form Q, sector geometry, chamber grammar, transport cocycle, and coherence tests are not just isolated artifacts. They are different witness surfaces for the same broader question:

Which relational identities survive admissible compression, transport, projection, and perturbation?

## 16. Minimal formal package

A working TRT model should eventually specify:

S = (W, R, L, A, Adm)

where:

W is a set of states, vertices, or positions.
R is a family of typed relations.
L is a labeling or valuation structure.
A is a set of actions.
Adm is an admissibility predicate.

A dynamic TRT model should allow:

a: S -> S'

for admissible actions a.

A full witness claim should specify:

x: entity or position
P: property or profile
A0: relevant action family
Adm: admissibility rule
tau: trace or continuation rule
Wit: witness artifact

Claim form:

ExistInv(x, P, A0, S, Adm, tau, Wit)

Plain reading:

The property P of x is an existential invariant in frame S under action family A0, restricted by admissibility rule Adm, carried by trace rule tau, and witnessed by artifact Wit.

This is too heavy for public prose, but useful for internal discipline.

## 17. Practical claim templates

Template 1: relational identity claim

In frame S, entity x is identified by relational profile Profile_S(x).

Template 2: admissible action claim

Action a is admissible for x in S because it satisfies rule Adm(a, S, x).

Template 3: preservation claim

Property P of x is preserved by action a in S.

Template 4: existential invariant claim

Property P of x is preserved across every admissible action in family A.

Template 5: field effect claim

Action a changes the relational field from S to S', with field signature FieldSig(a, S).

Template 6: coherence-gap claim

Surface U appears coherent under local relation family R_local but fails under wider relation family R_global or action family A_test.

Template 7: witness claim

Artifact W verifies claim C by making frame, action, trace, and invariant inspectable.

## 18. Current open problems

This note does not solve the formal system. It identifies the stack.

Open problems:

1. Choose the minimal notation that remains readable.

2. Decide whether TRT needs a custom calculus or can be expressed as a disciplined combination of existing dynamic modal, temporal, and graph-transformation logics.

3. Define trace maps rigorously enough for graph quotients and projections.

4. Define field signatures in computable form for finite graphs.

5. Relate coherence-gap invariants to modal failure conditions.

6. Specify how thalions, sectors, quotient surfaces, and transport structures map into this stack.

7. Develop small examples before attempting large theory claims.

8. Keep philosophical, formal, computational, and physical-analogy claims separated by proof status.

## 19. Summary

Thalean Relational Theory needs a logic stack because its central claims involve identity, relation, action, and field effect.

Static graph theory gives relation.

Modal logic gives possibility and necessity.

Typed modal logic distinguishes relation kinds.

Temporal logic gives persistence through ordered change.

Dynamic logic gives explicit action.

Admissibility logic distinguishes lawful transformation from arbitrary mutation.

Update semantics gives field effect.

Together, these layers support the working thesis:

Identity is relational invariance under admissible change.

And the active thesis:

A thing is what its relations make possible, and what its presence makes possible for others.

