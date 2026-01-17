---
title: "On the Supremacy of Rio over Modern Toolkits"
date: 2026-01-17
tags: ["PLAN 9", "UX", "SUCKLESS"]
---

In the Plan 9 operating system, **rio** isn’t just a window manager; it is a filesystem service. It represents the logical conclusion of “everything is a file.” Modern desktops like GNOME or KDE have become bloated monoliths that treat the user as a consumer of widgets rather than a manipulator of data.

<h3 class="section-header">The Threefold Path</h3>
<ul class="list-disc list-inside space-y-1 text-xs">
    <li><strong>Isolation:</strong> Each window is its own namespace.</li>
    <li><strong>Plumbing:</strong> Data moves between applications without complex APIs.</li>
    <li><strong>Textual Control:</strong> Everything can be driven by simple strings.</li>
</ul>

<p>Consider the simplicity of opening a window in a script compared to the nightmare of DBus or X11 protocols:</p>

<div class="code-block">
<pre># Plan 9 Shell: Opening a window is just writing to a file
mount /srv/rio /n/rio
echo 'window 100 100 500 500' > /n/rio/new</pre>
</div>

<h3 class="section-header">The Political Parallel</h3>
<p>Just as we advocate for the reduction of state interference in the economy, we must advocate for the reduction of "middleware" interference in computing. A computer should be a tool of absolute sovereignty. Every layer of abstraction you don't understand is a tax on your productivity and freedom.</p>

<p>When you use software that adheres to the <strong>suckless</strong> philosophy, you are performing an act of intellectual secession. You are saying "No" to the planned obsolescence of modern software ecosystems.</p>

<blockquote class="bg-gray-100 p-4 text-xs italic border-l-4 border-black mt-6">
    "Programs should do one thing and do it well. But more importantly, they should get out of the way when they are done."
    <br>— Uriel (cat-v.org)
</blockquote>
