load('//sys/src/FLAGS', "LIB_COMPILER_FLAGS", "CMD_LINK_OPTS")
load('//sys/src/harvey.BUILD', "harvey_binary")

CMD_SRCS = [
	"9pvpxy.c",
	"aan.c",
	"ar.c",
	"archfs.c",
	"ascii.c",
	"awd.c",
	"basename.c",
	"bind.c",
	"bsplit.c",
	"cal.c",
	"calendar.c",
	"calls.c",
	"cat.c",
	"chgrp.c",
	"chmod.c",
	"cleanname.c",
	"clock.c",
	"cmp.c",
	"col.c",
	"colors.c",
	"comm.c",
	"cp.c",
	"cpu.c",
	"crop.c",
	"date.c",
	"dc.c",
	"dd.c",
	"deroff.c",
	"du.c",
	"echo.c",
	"ecp.c",
	"factor.c",
	"fcp.c",
	"field.c",
	"file.c",
	"fmt.c",
	"fortune.c",
	"freq.c",
	"getmap.c",
	"gview.c",
	"hget.c",
	"histogram.c",
	"history.c",
	"html2ms.c",
	"iconv.c",
	"idiff.c",
	"import.c",
	"init.c",
	"join.c",
	"kbmap.c",
	"kiss.c",
	"ktrace.c",
	"lens.c",
	"lnfs.c",
	"lock.c",
	"look.c",
	"mc.c",
	"mclock.c",
	"md5sum.c",
	"mkdir.c",
	"mntgen.c",
	"ms2html.c",
	"ms.c",
	"mtime.c",
	"mug.c",
	"mv.c",
	"netstat.c",
	"news.c",
	"nm.c",
	"nntpfs.c",
	"ns.c",
	"pbd.c",
	"p.c",
	"pipefile.c",
	"pr.c",
	"primes.c",
	"pump.c",
	"pwd.c",
	"ramfs.c",
	"read.c",
	"resample.c",
	"rm.c",
	"rx.c",
	"screenlock.c",
	"seconds.c",
	"sed.c",
	"seq.c",
	"sha1sum.c",
	"size.c",
	"sleep.c",
	"sort.c",
	"split.c",
	"srvfs.c",
	"stats.c",
	"strace.c",
	"strings.c",
	"strip.c",
	"sum.c",
	"swap.c",
	"tail.c",
	"tar.c",
	"tee.c",
	"testalarm.c",
	"test.c",
	"time.c",
	"tlsclient.c",
	"tlssrv.c",
	"touch.c",
	"trace.c",
	"tr.c",
	"tweak.c",
	"unicode.c",
	"uniq.c",
	"unlnfs.c",
	"unmount.c",
	"wc.c",
	"webcookies.c",
	"webfsget.c",
	"winwatch.c",
	"xd.c",
	"yacc.c",
]

[harvey_binary(
	name=c[:-2],
	srcs=[c],
	deps=[
		"//sys/src/lib9p:lib9p",
		"//sys/src/libauth:libauth",
		"//sys/src/libauthsrv:libauthsrv",
		"//sys/src/libcomplete:libcomplete",
		"//sys/src/libcontrol:libcontrol",
		"//sys/src/libdisk:libdisk",
		"//sys/src/libdraw:libdraw",
		"//sys/src/libflate:libflate",
		"//sys/src/libframe:libframe",
		"//sys/src/libgeometry:libgeometry",
		"//sys/src/libhttpd:libhttpd",
		"//sys/src/libip:libip",
		"//sys/src/liblex:liblex",
		"//sys/src/libmach:libmach",
		"//sys/src/libmemlayer:libmemlayer",
		"//sys/src/libmemdraw:libmemdraw",
		"//sys/src/libmp:libmp",
		"//sys/src/libndb:libndb",
		"//sys/src/libplumb:libplumb",
		"//sys/src/libregexp:libregexp",
		"//sys/src/libsec:libsec",
		"//sys/src/libstdio:libstdio",
		"//sys/src/libString:libString",
		"//sys/src/libthread:libthread",
		"//sys/src/libusb:libusb",
		"//sys/src/libventi:libventi",
		"//sys/src/liboventi:liboventi",
		"//sys/src/libbio:libbio",
		"//sys/src/libc:libc",
	],
	linkopts=CMD_LINK_OPTS
) for c in CMD_SRCS]

harvey_binary(
	name="mount",
	srcs=[
		"mount.c"
	],
	deps=[
		"//sys/src/libauth:libauth",
		"//sys/src/libc:libc",
	],
)

harvey_binary(
	name="srv",
	srcs=[
		"srv.c"
	],
	deps=[
		"//sys/src/libauth:libauth",
		"//sys/src/libc:libc",
	]
)

harvey_binary(
	name="ls",
	srcs=[
		"ls.c"
	],
	deps=[
		"//sys/src/libbio:libbio",
		"//sys/src/libc:libc",
	],
)

harvey_binary(
	name="ps",
	srcs=[
		"ps.c"
	],
	deps=[
		"//sys/src/libbio:libbio",
		"//sys/src/libc:libc",
	],
)

harvey_binary(
	name="ed",
	srcs=[
		"ed.c"
	],
	deps=[
		"//sys/src/libregexp:libregexp",
		"//sys/src/libbio:libbio",
		"//sys/src/libc:libc",
	],
	includes=[
		"//sys/include",
		"//amd64/include",
		"//sys/src/libregexp",
	],
)

harvey_binary(
	name="ratrace",
	srcs=[
		"ratrace.c"
	],
	deps=[
		"//sys/src/libthread:libthread",
		"//sys/src/libc:libc",
	]
)
group(
	name="cmds",
	deps=[
		"//sys/src/cmd/aux:cmds",
		"//sys/src/cmd/ndb:cmds",
		"//sys/src/cmd/ip/ipconfig:ipconfig",
		"//sys/src/cmd/auth/factotum:factotum",
		"//sys/src/cmd/acme:acme",
		"//sys/src/cmd/rc:rc",
		"//sys/src/cmd/rio:rio",
		"//sys/src/cmd/plumb:plumb",
		"//sys/src/cmd/plumb:plumber",
		"//sys/src/cmd/grep:grep",
		"//sys/src/cmd/acpi:irq",
		"//sys/src/cmd:ascii",
		"//sys/src/cmd:awd",
		"//sys/src/cmd:basename",
		"//sys/src/cmd:bind",
		"//sys/src/cmd:bsplit",
		"//sys/src/cmd:cal",
		"//sys/src/cmd:calendar",
		"//sys/src/cmd:calls",
		"//sys/src/cmd:cat",
		"//sys/src/cmd:chgrp",
		"//sys/src/cmd:chmod",
		"//sys/src/cmd:cleanname",
		"//sys/src/cmd:clock",
		"//sys/src/cmd:cmp",
		"//sys/src/cmd:col",
		"//sys/src/cmd:colors",
		"//sys/src/cmd:comm",
		"//sys/src/cmd:cp",
		"//sys/src/cmd:cpu",
		"//sys/src/cmd:crop",
		"//sys/src/cmd:date",
		"//sys/src/cmd:dc",
		"//sys/src/cmd:dd",
		"//sys/src/cmd:deroff",
		"//sys/src/cmd:du",
		"//sys/src/cmd:echo",
		"//sys/src/cmd:ecp",
		"//sys/src/cmd:ed",
		"//sys/src/cmd:factor",
		"//sys/src/cmd:fcp",
		"//sys/src/cmd:field",
		"//sys/src/cmd:file",
		"//sys/src/cmd:fmt",
		"//sys/src/cmd:fortune",
		"//sys/src/cmd:freq",
		"//sys/src/cmd:getmap",
		"//sys/src/cmd:gview",
		"//sys/src/cmd:hget",
		"//sys/src/cmd:histogram",
		"//sys/src/cmd:history",
		"//sys/src/cmd:html2ms",
		"//sys/src/cmd:iconv",
		"//sys/src/cmd:idiff",
		"//sys/src/cmd:import",
		"//sys/src/cmd:init",
		"//sys/src/cmd:join",
		"//sys/src/cmd:kbmap",
		"//sys/src/cmd:kiss",
		"//sys/src/cmd:ktrace",
		"//sys/src/cmd:lens",
		"//sys/src/cmd:lnfs",
		"//sys/src/cmd:lock",
		"//sys/src/cmd:look",
		"//sys/src/cmd:ls",
		"//sys/src/cmd:mc",
		"//sys/src/cmd:mclock",
		"//sys/src/cmd:md5sum",
		"//sys/src/cmd:mkdir",
		"//sys/src/cmd:mntgen",
		"//sys/src/cmd:mount",
		"//sys/src/cmd:ms2html",
		"//sys/src/cmd:ms",
		"//sys/src/cmd:mtime",
		"//sys/src/cmd:mug",
		"//sys/src/cmd:mv",
		"//sys/src/cmd:netstat",
		"//sys/src/cmd:news",
		"//sys/src/cmd:nm",
		"//sys/src/cmd:nntpfs",
		"//sys/src/cmd:ns",
		"//sys/src/cmd:pbd",
		"//sys/src/cmd:p",
		"//sys/src/cmd:pipefile",
		"//sys/src/cmd:pr",
		"//sys/src/cmd:primes",
		"//sys/src/cmd:ps",
		"//sys/src/cmd:pump",
		"//sys/src/cmd:pwd",
		"//sys/src/cmd:ramfs",
		"//sys/src/cmd:ratrace",
		"//sys/src/cmd:read",
		"//sys/src/cmd:resample",
		"//sys/src/cmd:rm",
		"//sys/src/cmd:rx",
		"//sys/src/cmd:screenlock",
		"//sys/src/cmd:seconds",
		"//sys/src/cmd:sed",
		"//sys/src/cmd:seq",
		"//sys/src/cmd:sha1sum",
		"//sys/src/cmd:size",
		"//sys/src/cmd:sleep",
		"//sys/src/cmd:sort",
		"//sys/src/cmd:split",
		"//sys/src/cmd:srv",
		"//sys/src/cmd:srvfs",
		"//sys/src/cmd:stats",
		"//sys/src/cmd:strace",
		"//sys/src/cmd:strings",
		"//sys/src/cmd:strip",
		"//sys/src/cmd:sum",
		"//sys/src/cmd:swap",
		"//sys/src/cmd:tail",
		"//sys/src/cmd:tar",
		"//sys/src/cmd:tee",
		"//sys/src/cmd:testalarm",
		"//sys/src/cmd:test",
		"//sys/src/cmd:time",
		"//sys/src/cmd:tlsclient",
		"//sys/src/cmd:tlssrv",
		"//sys/src/cmd:touch",
		"//sys/src/cmd:trace",
		"//sys/src/cmd:tr",
		"//sys/src/cmd:tweak",
		"//sys/src/cmd:unicode",
		"//sys/src/cmd:uniq",
		"//sys/src/cmd:unlnfs",
		"//sys/src/cmd:unmount",
		"//sys/src/cmd:wc",
		"//sys/src/cmd:webcookies",
		"//sys/src/cmd:webfsget",
		"//sys/src/cmd:winwatch",
		"//sys/src/cmd:xd",
		"//sys/src/cmd:yacc",
	],
)
