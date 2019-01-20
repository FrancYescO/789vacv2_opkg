Mirror of OpenWRT Packages repo for Technicolor 789vac v2 (brcm63xx-tch)
Actually mirrored from https://pietrotti97.com/repo/OpenWrt/repo/Tg-789vac_V2/ with just few fixes to Packages(.gz) files

Edit your `/etc/opkg/customfeeds.conf` to include these lines:

    src/gz base https://raw.githubusercontent.com/FrancYescO/789vacv2_opkg/master/base
    src/gz packages https://raw.githubusercontent.com/FrancYescO/789vacv2_opkg/master/packages
    src/gz luci https://raw.githubusercontent.com/FrancYescO/789vacv2_opkg/master/luci
    src/gz routing https://raw.githubusercontent.com/FrancYescO/789vacv2_opkg/master/routing
    src/gz telephony https://raw.githubusercontent.com/FrancYescO/789vacv2_opkg/master/telephony
    src/gz management https://raw.githubusercontent.com/FrancYescO/789vacv2_opkg/master/management
    
you can use it in conjunction with official OpenWRT repo appending this to your `/etc/opkg.conf`

    arch all 100
    arch brcm63xx 200
    arch brcm63xx-tch 300
    
and this in `/etc/opkg/customfeeds.conf`

    src/gz chaos_calmer_base http://archive.openwrt.org/chaos_calmer/15.05.1/brcm63xx/generic/packages/base
    src/gz chaos_calmer_packages http://archive.openwrt.org/chaos_calmer/15.05.1/brcm63xx/generic/packages/packages
    src/gz chaos_calmer_luci http://archive.openwrt.org/chaos_calmer/15.05.1/brcm63xx/generic/packages/luci
    src/gz chaos_calmer_routing http://archive.openwrt.org/chaos_calmer/15.05.1/brcm63xx/generic/packages/routing
    src/gz chaos_calmer_telephony http://archive.openwrt.org/chaos_calmer/15.05.1/brcm63xx/generic/packages/telephony
    src/gz chaos_calmer_management http://archive.openwrt.org/chaos_calmer/15.05.1/brcm63xx/generic/packages/management
    
 Then run `opkg update`
 
 ## Packages are untested! `opkg upgrade` can be a good way to brick your device!
