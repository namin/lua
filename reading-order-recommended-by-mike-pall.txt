Recommended reading order

 1. lmathlib.c, lstrlib.c
   
    Get familiar with the external C API. Don't bother with the pattern
    matcher though. Just the easy functions.

 2. lapi.c
   
    Check how the API is implemented internally. Only skim this to get
    a feeling for the code. Cross-reference to lua.h and luaconf.h as
    needed.

 3. lobject.h

    Tagged values and object representation. Skim through this
    first. You'll want to keep a window with this file open all the
    time.

 4. lstate.h

    State objects. Ditto.

 5. lopcodes.h

    Bytecode instruction format and opcode definitions. Easy.

 6. lvm.c

    Scroll down to luaV_execute, the main interpreter loop. See how
    all of the instructions are implemented. Skip the details for
    now. Reread later.

 7. ldo.c

    Calls, stacks, exceptions, coroutines. Tough read.

 8. lstring.c

    String interning. Cute, huh?

 9. ltable.c

    Hash tables and arrays. Tricky code.

10. ltm.c

    Metamethod handling. Reread all of lvm.c now. You may want to reread lapi.c now.

11. ldebug.c

    Surprise waiting for you. Abstract interpretation is used to find
    object names for tracebacks. Does bytecode verification, too.

12. lparser.c, lcode.c
    
    Recursive descent parser, targetting a register-based VM. Start
    from chunk() and work your way through. Read the expression parser
    and the code generator parts last.

13. lgc.c

    Incremental garbage collector. Take your time.

Read all the other files as you see references to them. Don't let your
stack get too deep though.

source: [Reddit comment](http://www.reddit.com/comments/63hth/ask_reddit_which_oss_codebases_out_there_are_so/c02pxbp)