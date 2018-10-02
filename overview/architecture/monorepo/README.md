# Monorepo

This approach provide us the modularity we need to develop across a growing team, but also eliminates the networking overhead there would have been if each service is deployed independently.

To learn more about this approach, read this article by DHH

{% embed data="{\"url\":\"https://m.signalvnoise.com/the-majestic-monolith-29166d022228\",\"type\":\"link\",\"title\":\"The Majestic Monolith\",\"description\":\"Some patterns are just about the code. If your code looks like this, and you need it to do that, here’s what to do. You’d do well to study…\",\"icon\":{\"type\":\"icon\",\"url\":\"https://cdn-images-1.medium.com/fit/c/304/304/1\*UUpa5mFtnLRLlT3nzi4FjQ.png\",\"width\":152,\"height\":152,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://cdn-images-1.medium.com/max/2000/1\*C0WR8CjuV3MCbuukjOqeUg.png\",\"width\":2000,\"height\":1120,\"aspectRatio\":0.56}}" %}

We are using lerna with yarn workspaces to orchestrate the monorepo

{% embed data="{\"url\":\"https://github.com/lerna/lerna\",\"type\":\"link\",\"title\":\"lerna/lerna\",\"description\":\"lerna - :dragon: A tool for managing JavaScript projects with multiple packages.\",\"icon\":{\"type\":\"icon\",\"url\":\"https://github.com/fluidicon.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://avatars2.githubusercontent.com/u/19333396?s=400&v=4\",\"width\":400,\"height\":400,\"aspectRatio\":1}}" %}

