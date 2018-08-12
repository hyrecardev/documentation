# Monorepo

This approach provide us the modularity we need to develop across a growing team, but also eliminates the networking overhead there would have been if each service is deployed independently.

To learn more about this approach, read this article by DHH

{% embed data="{\"url\":\"https://m.signalvnoise.com/the-majestic-monolith-29166d022228\",\"type\":\"link\",\"title\":\"The Majestic Monolith\",\"description\":\"Some patterns are just about the code. If your code looks like this, and you need it to do that, here’s what to do. You’d do well to study…\",\"icon\":{\"type\":\"icon\",\"url\":\"https://cdn-images-1.medium.com/fit/c/304/304/1\*UUpa5mFtnLRLlT3nzi4FjQ.png\",\"width\":152,\"height\":152,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://cdn-images-1.medium.com/max/2000/1\*C0WR8CjuV3MCbuukjOqeUg.png\",\"width\":2000,\"height\":1120,\"aspectRatio\":0.56}}" %}

## Services

Each `service` is a self-contained code base with its own dependencies and configuration. These services can "install" other services in the monorepo just like npm packages. See how to do this [here](https://hyrecar.gitbook.io/graphql/~/edit/drafts/-LJf_GXWrC5Cy7JKhyns/tutorials/installing-other-packages-from-the-monorepo).

### Gateway

The gateway service is the glue which binds all of the other services together. It determines how, say, the users schema relates to the files schema. We use what is called "[schema stitching](https://hyrecar.gitbook.io/graphql/~/edit/drafts/-LJf_GXWrC5Cy7JKhyns/architecture/schema-stitching)" to accomplish this.



