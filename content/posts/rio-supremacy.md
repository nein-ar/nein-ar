---
title: "On the Supremacy of Rio over Modern Toolkits"
date: 2026-01-17
tags: ["PLAN 9", "UX", "SUCKLESS"]
---

In Plan 9, rio is a filesystem service. It also manages windows, but the file interface is the part that matters. Modern desktops like GNOME and KDE treat people as consumers of widgets. Plan 9 keeps people in charge of data.

<h3 class="section-header">How rio works</h3>

Each window has its own namespace. Applications exchange data through files instead of private APIs. A script can drive the whole session with ordinary strings.

Opening a window in a shell is short:

<div class="code-block">
<pre># Plan 9 shell: opening a window is writing to a file
mount /srv/rio /n/rio
echo 'window 100 100 500 500' > /n/rio/new</pre>
</div>

Compare that with the DBus or X11 setup behind a modern desktop.

<h3 class="section-header">Why this matters</h3>

Middleware sits between you and the machine. Each layer adds work you have to understand. A computer should be a tool you control.

Suckless software is small. It does one job and stops.

<blockquote class="bg-gray-100 p-4 text-xs italic border-l-4 border-black mt-6">
    "Programs should do one thing and do it well. But more importantly, they should get out of the way when they are done."
    <br>Uriel, cat-v.org
</blockquote>
