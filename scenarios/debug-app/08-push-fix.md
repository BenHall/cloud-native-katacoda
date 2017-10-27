Commit the bug fix to the Git repository.

```
git add src/main/java/com/redhat/cloudnative/inventory/InventoryResource.java
```{{execute T1}}

```
git commit -m "inventory returns zero for non-existing product id
```{{execute T1}}

```
git push origin master
```{{execute T1}}

As soon as you commit the changes to the Git repository, the **inventory-pipeline** gets
triggered to build and deploy a new Inventory container with the fix. Go to the
OpenShift Web Console and inside the **coolstore** project. On the sidebar
menu, Click on **Builds &rarr; Pipelines** to see its progress.

When the pipeline completes successfully, point your browser at the Web route and verify
that the inventory status is visible for all products. The suspect product should show
the inventory status as _Not in Stock_.

![Inventory Status Bug Fixed](https://katacoda.com/openshift-roadshow/assets/debug-coolstore-bug-fixed.png)

Well done and congratulations for completing all the scenarios.
