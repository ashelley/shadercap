ShaderCap 1.2 for Windows

-

15.04.17 - Release version 1.2
* Fix GUI limitation that prevented capture duration from exceeding 99 seconds.
* Upgrade to Qt 5.7 (from Qt 5.4)

-

Here is an example shader that uses a single texture:

uniform sampler2D iChannel0;
uniform float iGlobalTime;
uniform vec2 iResolution;
void main() {
  vec2 uv = gl_FragCoord.xy / iResolution * 2.0 - 1.0;
  vec3 tex = texture2D(iChannel0, uv).xyz;
  gl_FragColor = vec4(tex,1.0);
}
