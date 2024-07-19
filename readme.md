```console
sudo apt install -y git python-is-python3
git clone https://github.com/akhilnarang/scripts; cd scripts; sudo bash setup/android_build_env.sh; cd ..; mkdir Evolution-X; cd Evolution-X
repo init -u https://github.com/Evolution-X/manifest -b udc --git-lfs
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags

git clone https://github.com/moto-sm8550-Evo/.github -b udc .repo/local_manifests
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags

cd device/motorola/rtwo; ./extract-files.sh; cd ../../..
. build/envsetup.sh; lunch lineage_rtwo-user; m evolution
```
