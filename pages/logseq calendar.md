---
title: Logseq Calendar
---

## #contents span.opacity-50 {
    opacity: 0;
}

#contents .logseq-tools-calendar:first-child h2 {
    margin-top: -25px;
}

.cp__sidebar-main-content .logseq-tools-multiple-calendars {
    display: flex;
    flex-wrap: wrap;
    padding: 0 15px;
}

.cp__sidebar-main-content .logseq-tools-multiple-calendars .logseq-tools-calendar {
    flex: 0 50%;
    box-sizing: border-box;
    padding: 0 15px;
}

.logseq-tools-calendar tr {
    background: none !important;
}

.logseq-tools-calendar th,
.logseq-tools-calendar td,
.logseq-tools-calendar tr {
    border: none;
}

.logseq-tools-calendar th,
.logseq-tools-calendar td {
    text-align: center;
}


/* Calendar - pages from other months */

.logseq-tools-calendar .outofmonth {
    opacity: .3;
}

/* If you're using Lupin.
   otherwise you can remove this: */

/* 
.logseq-tools-calendar .today {
    font-weight: 900;
    color: var(--ls-link-text-color);
}

.logseq-tools-calendar .page-exists {
    border-bottom: 1px solid var(--ls-link-ref-text-color);
}

.logseq-tools-calendar .today.page-exists {
    border-bottom-color: var(--ls-link-text-color);
}

.logseq-tools-calendar .page-ref:not(.page-exists):not(.today) {
    color: violet;
}
*/
