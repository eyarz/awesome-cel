# awesome-cel 🕶️

```
 █████╗ ██╗    ██╗███████╗███████╗ ██████╗ ███╗   ███╗███████╗    ███████╗███████╗██╗  
██╔══██╗██║    ██║██╔════╝██╔════╝██╔═══██╗████╗ ████║██╔════╝    ██╔════╝██╔════╝██║ 
███████║██║ █╗ ██║█████╗  ███████╗██║   ██║██╔████╔██║█████╗      ██║     █████╗  ██║ 
██╔══██║██║███╗██║██╔══╝  ╚════██║██║   ██║██║╚██╔╝██║██╔══╝      ██║     ██╔══╝  ██║ 
██║  ██║╚███╔███╔╝███████╗███████║╚██████╔╝██║ ╚═╝ ██║███████╗    ███████╗███████╗███████╗
╚═╝  ╚═╝ ╚══╝╚══╝ ╚══════╝╚══════╝ ╚═════╝ ╚═╝     ╚═╝╚══════╝    ╚══════╝╚══════╝╚══════╝
```                                                                          


The Common Expression Language (CEL) is a simple language built on protocol buffer types. CEL can be used on its own, or embedded into a larger product.  

Popular products that implemented CEL support:

* **Envoy RBAC**
* **Caddy server standard matcher**
* **Kubernetes validation and policy rules**
* **KrakenD conditional requests and responses**
* **Cloud Firestore / Cloud Storage security rules**
  
CEL evaluates expressions that are similar to single-line functions or lambda expressions. While CEL is commonly used for boolean decisions, it can also be used to construct more complex objects like JSON or protobuf messages.

Here are some CEL syntax examples:

| CEL Expression | Purpose | 
| -------------- | ------- |
| `names.isSorted()` | Verify that a list of names is kept in alphabetical order |
| `items.map(x, x.weight).sum() == 1.0` | Verify that the "weights" of a list of objects sum to 1.0 |
| `lowPriorities.map(x, x.priority).max() < highPriorities.map(x, x.priority).min()` | Verify that two sets of priorities do not overlap |
| `names.indexOf('should-be-first') == 1` | Require that the first name in a list is a specific value |
      
## Table of Contents

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Packages](#packages)
- [Resources](#resources)
- [Tools](#tools)
- [Kubernetes](#kubernetes)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

---

### Packages

* [cel-go](https://pkg.go.dev/github.com/google/cel-go) - Go implementations of CEL
* [cel-c++](https://github.com/google/cel-cpp) - C++ implementations of CEL
* [cel-java](https://github.com/google/cel-java) - Java implementations of CEL
* [cel-python](https://pypi.org/project/cel-python/) - Python implementations of CEL
* [cel-rust](https://github.com/thesayyn/cel-rust) - Rust implementations of CEL

### Resources

* [CEL-Go Codelab](https://codelabs.developers.google.com/codelabs/cel-go#0) - a codelab for developers who would like to learn CEL in order to use services that already support CEL
* [cel-spec](https://github.com/google/cel-spec) - Common Expression Language specification

### Tools

* [vscode-cel](https://marketplace.visualstudio.com/items?itemName=hmarr.cel) - CEL support for Visual Studio Code
* [CEL Playground](https://playcel.undistro.io/) - an interactive WebAssembly (Wasm) powered environment to explore and experiment with the CEL

### Kubernetes

* [Webhook Fatigue? You're Not Alone: Introducing the CEL](https://www.youtube.com/watch?v=gJWMvsC7Mzo) - overview of Kubernetes 1.23 CEL support for simplifying CRD validation and reducing reliance on webhooks for extensibility
* [Common Expression Language in Kubernetes](https://kubernetes.io/docs/reference/using-api/cel/) - the Common Expression Language in Kubernetes API
