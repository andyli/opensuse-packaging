# opensuse-packaging

A VSCode devcontainer setup for openSUSE packaging.

# Example steps for updating the Haxe package

1. cd projects

2. osc co devel:languages:haxe/haxe

3. cd devel\:languages\:haxe/haxe

4. Edit `haxe.spec`
    - Update `Version:`
    - Update the other build deps/rules if needed.

5. Update source archives
    - Download archives `rpmdev-spectool -g haxe.spec`
    - Remove old archives
    - `osc addremove`

6. Edit changelog by `osc vc`

7. `osc build`

8. `osc commit`
