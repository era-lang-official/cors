# Era CORS (`github.com/era-lang-official/cors`)

Cross-Origin Resource Sharing (CORS) preflight validation and header generator for Era web applications.

## Features
- **Permissive & Strict Profiles**: Support wildcards or explicit origin whitelists.
- **Preflight Support**: Handles HTTP `OPTIONS` requests and sets Max-Age and Allowed-Methods.
- **Credentials Support**: Handles `Access-Control-Allow-Credentials`.

## Usage
```era
import "github.com/era-lang-official/cors";

fn main() {
    let conf = CorsConfig::permissive();
    let res = handle_cors(&conf, "https://example.com".to_string(), "GET".to_string());
    println(res.headers[0].val); // "*"
}
```

