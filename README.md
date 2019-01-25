TypeScript "tsc" Option "files" Demo
====================================

这个demo主要是为了证明：当我们调用tsc并且指定了ts文件的时候，
它会忽略掉`tsconfig.json`中的`files`中的内容，在某些情况下
可能会出错（比如缺少某些`.d.ts`文件，并且这些`.d.ts`文件没有被`import`）。

所以在使用`.d.ts`文件的时候，使用tsc要特别注意，要么全都写在`files`中，
要么在命令行中把相应的`.d.ts`文件也加上。

还有一点需要注意：为了使得hello.ts中的代码执行，在tsconfig.json中需要把`strict`设为`false`

```
npm install
npm run demo
npm run demo-cmd
npm run demo-cmd-invalid
```

