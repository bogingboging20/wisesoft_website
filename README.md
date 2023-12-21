# wisesoft_website
wisesoft_website123

to avoid blank page on github

before upload build/web to github
1. keep the line: \<base href="$FLUTTER_BASE_HREF"\> in the index.html in web folder (not the index.html in the build/web folder)
2. compile with: $flutter build web --release --web-renderer html --base-href /your repository name/
3. after compile, the line: \<base href="$FLUTTER_BASE_HREF"\> in the index.html in build/web folter will be replaced to \<base href="/your repository name/"\>
4. so when the web app is loaded, the code will download (main.dart.js) from: github.com/youraccount/yourrepostoryname/main.dart.js, if yourrepostoryname is wrong, then it will never find it

for custom url
1. compile with: $flutter build web --release --web-renderer html --base-href /
