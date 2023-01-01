---
title: "Supernova"
date: 2021-05-01T13:06:18+08:00
description: MS208 homework in ACM 2019 class, a completely hand-made compiler for a toy language with multiple optimizations.
authors: [ziyi-cai]
tags: [compiler, LLVM, RISCV, course projects]
categories: [projects]
draft: false
---
This huge project is assigned in MS208 course. We built a compiler from scratch, from the backend to the frontend ([ANTLR 4](https://github.com/antlr/antlr4) used for parsing) and added multiple optimizing strategies to reach the `-O1` baseline. It was really an Odyssey both for mind and body.

The tutorial repo is [here](https://github.com/ACMClassCourses/Compiler-Design-Implementation). And my code is [here](https://github.com/acrazyczy/Supernova).

The bloated project structure looks like this:
```plain
src
├── Assembly
│  ├── asmBlock.java
│  ├── asmEntry.java
│  ├── asmFunction.java
│  ├── Instruction
│  │  ├── brInst.java
│  │  ├── callInst.java
│  │  ├── inst.java
│  │  ├── ITypeInst.java
│  │  ├── jumpInst.java
│  │  ├── laInst.java
│  │  ├── liInst.java
│  │  ├── loadInst.java
│  │  ├── luiInst.java
│  │  ├── mvInst.java
│  │  ├── retInst.java
│  │  ├── RTypeInst.java
│  │  ├── storeInst.java
│  │  └── szInst.java
│  ├── Operand
│  │  ├── globalData.java
│  │  ├── Imm.java
│  │  ├── intImm.java
│  │  ├── operand.java
│  │  ├── physicalReg.java
│  │  ├── reg.java
│  │  ├── relocationImm.java
│  │  └── virtualReg.java
│  └── stackFrame.java
├── AST
│  ├── arrayLiteralNode.java
│  ├── assignExprNode.java
│  ├── ASTNode.java
│  ├── ASTVisitor.java
│  ├── binaryExprNode.java
│  ├── breakStmtNode.java
│  ├── classDefNode.java
│  ├── classLiteralNode.java
│  ├── cmpExprNode.java
│  ├── constExprNode.java
│  ├── continueStmtNode.java
│  ├── exprStmtNode.java
│  ├── forStmtNode.java
│  ├── funcCallExprNode.java
│  ├── funcDefNode.java
│  ├── ifStmtNode.java
│  ├── logicExprNode.java
│  ├── memberAccessExprNode.java
│  ├── newExprNode.java
│  ├── programUnitNode.java
│  ├── returnStmtNode.java
│  ├── rootNode.java
│  ├── stmtNode.java
│  ├── subscriptionExprNode.java
│  ├── suiteStmtNode.java
│  ├── thisExprNode.java
│  ├── typeNode.java
│  ├── unaryExprNode.java
│  ├── varDefStmtNode.java
│  ├── varExprNode.java
│  └── whileStmtNode.java
├── Backend
│  ├── asmPrinter.java
│  ├── asmVisitor.java
│  ├── instructionSelector.java
│  ├── IRBuilder.java
│  ├── IRPrinter.java
│  ├── livenessAnalyser.java
│  ├── pass.java
│  ├── registerAllocator.java
│  ├── SSAConstructor.java
│  └── SSADestructor.java
├── Builtin
│  ├── builtin.c
│  ├── builtin.ll
│  └── builtin.s
├── Frontend
│  ├── ASTBuilder.java
│  ├── classGenerator.java
│  ├── semanticChecker.java
│  └── symbolCollector.java
├── LLVMIR
│  ├── basicBlock.java
│  ├── function.java
│  ├── Instruction
│  │  ├── _move.java
│  │  ├── binary.java
│  │  ├── bitcast.java
│  │  ├── br.java
│  │  ├── call.java
│  │  ├── getelementptr.java
│  │  ├── icmp.java
│  │  ├── load.java
│  │  ├── phi.java
│  │  ├── ret.java
│  │  ├── statement.java
│  │  ├── store.java
│  │  └── terminalStmt.java
│  ├── IREntry.java
│  ├── IRLoop.java
│  ├── Operand
│  │  ├── booleanConstant.java
│  │  ├── constant.java
│  │  ├── entity.java
│  │  ├── globalVariable.java
│  │  ├── integerConstant.java
│  │  ├── nullPointerConstant.java
│  │  ├── register.java
│  │  └── undefinedValue.java
│  └── TypeSystem
│     ├── LLVMAggregateType.java
│     ├── LLVMArrayType.java
│     ├── LLVMFirstClassType.java
│     ├── LLVMIntegerType.java
│     ├── LLVMPointerType.java
│     ├── LLVMSingleValueType.java
│     ├── LLVMStructureType.java
│     └── LLVMType.java
├── Main.java
├── Optimization
│  ├── asm
│  │  ├── asmOptimizer.java
│  │  ├── CFGSimplifier.java
│  │  └── peephole.java
│  └── IR
│     ├── ADCE.java
│     ├── algebraicSimplifier.java
│     ├── Analyser
│     │  ├── callingAnalyser.java
│     │  ├── dominanceAnalyser.java
│     │  ├── loopAnalyzer.java
│     │  └── sideEffectAnalyzer.java
│     ├── CFGSimplifier.java
│     ├── copyPropagation.java
│     ├── CSE.java
│     ├── inlineExpansion.java
│     ├── IROptimizer.java
│     ├── LICM.java
│     ├── OSR.java
│     ├── SCCP.java
│     └── TCO.java
├── Parser
│  ├── MxStar.g4
│  ├── MxStar.interp
│  ├── MxStar.tokens
│  ├── MxStarBaseListener.java
│  ├── MxStarBaseVisitor.java
│  ├── MxStarLexer.interp
│  ├── MxStarLexer.java
│  ├── MxStarLexer.tokens
│  ├── MxStarListener.java
│  ├── MxStarParser.java
│  └── MxStarVisitor.java
└── Util
   ├── disjointSet.java
   ├── error
   │  ├── error.java
   │  ├── internalError.java
   │  ├── semanticError.java
   │  └── syntaxError.java
   ├── MxStarErrorListener.java
   ├── position.java
   ├── Scope
   │  ├── aggregateScope.java
   │  ├── functionScope.java
   │  ├── globalScope.java
   │  ├── loopScope.java
   │  └── Scope.java
   ├── TriFunction.java
   ├── TriPredicate.java
   ├── Type
   │  ├── arrayType.java
   │  ├── classType.java
   │  ├── functionType.java
   │  └── Type.java
   └── typeCalculator.java
```
