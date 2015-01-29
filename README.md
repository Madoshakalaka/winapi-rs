# winapi-rs [![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/retep998/winapi-rs) #

[Documentation](https://retep998.github.io/doc/winapi/)

This crate provides types and constants for WinAPI FFI bindings. They are gathered by hand using the very latest official SDK from Microsoft. I aim to replace all existing Windows FFI in other crates with this set of crates through the "[Embrace, extend, and extinguish](http://en.wikipedia.org/wiki/Embrace,_extend_and_extinguish)" technique.

If this crate is missing something you need, feel free to create an issue, open a pull request, or contact me via [other means](http://www.rustaceans.org/retep998).

## Example ##

Cargo.toml:
```toml
[dependencies]
winapi = "*"
winmm-sys = "*"
```
example.rs:
```Rust
extern crate winapi;
extern crate "winmm-sys" as winmm;
fn func() {
    winmm::PlaySoundA(...);
}
```

## Functions ##

Bindings to library functions are in separate crates. The source to each crate is in the relevant subdirectory. Crossed out crates are currently empty and reserved for future use. Feel free to get in touch with me if you are interested in any of these crates.
* ~~[aclui-sys](https://crates.io/crates/aclui-sys)~~
* ~~[activeds-sys](https://crates.io/crates/activeds-sys)~~
* ~~[adsiid-sys](https://crates.io/crates/adsiid-sys)~~
* [advapi32-sys](https://crates.io/crates/advapi32-sys)
* ~~[advpack-sys](https://crates.io/crates/advpack-sys)~~
* ~~[ahadmin-sys](https://crates.io/crates/ahadmin-sys)~~
* ~~[alink-sys](https://crates.io/crates/alink-sys)~~
* ~~[amstrmid-sys](https://crates.io/crates/amstrmid-sys)~~
* ~~[api-ms-win-net-isolation-l1-1-0-sys](https://crates.io/crates/api-ms-win-net-isolation-l1-1-0-sys)~~
* ~~[apidll-sys](https://crates.io/crates/apidll-sys)~~
* ~~[appmgmts-sys](https://crates.io/crates/appmgmts-sys)~~
* ~~[appmgr-sys](https://crates.io/crates/appmgr-sys)~~
* ~~[appnotify-sys](https://crates.io/crates/appnotify-sys)~~
* ~~[asycfilt-sys](https://crates.io/crates/asycfilt-sys)~~
* ~~[audiobaseprocessingobject-sys](https://crates.io/crates/audiobaseprocessingobject-sys)~~
* ~~[audioeng-sys](https://crates.io/crates/audioeng-sys)~~
* ~~[audiomediatypecrt-sys](https://crates.io/crates/audiomediatypecrt-sys)~~
* ~~[authz-sys](https://crates.io/crates/authz-sys)~~
* ~~[aux_ulib-sys](https://crates.io/crates/aux_ulib-sys)~~
* ~~[avifil32-sys](https://crates.io/crates/avifil32-sys)~~
* ~~[avrt-sys](https://crates.io/crates/avrt-sys)~~
* ~~[basesrv-sys](https://crates.io/crates/basesrv-sys)~~
* ~~[bcrypt-sys](https://crates.io/crates/bcrypt-sys)~~
* ~~[bits-sys](https://crates.io/crates/bits-sys)~~
* ~~[bluetoothapis-sys](https://crates.io/crates/bluetoothapis-sys)~~
* ~~[bthprops-sys](https://crates.io/crates/bthprops-sys)~~
* ~~[bufferoverflow-sys](https://crates.io/crates/bufferoverflow-sys)~~
* ~~[bufferoverflowu-sys](https://crates.io/crates/bufferoverflowu-sys)~~
* ~~[cabinet-sys](https://crates.io/crates/cabinet-sys)~~
* ~~[certadm-sys](https://crates.io/crates/certadm-sys)~~
* ~~[certca-sys](https://crates.io/crates/certca-sys)~~
* ~~[certcli-sys](https://crates.io/crates/certcli-sys)~~
* ~~[certidl-sys](https://crates.io/crates/certidl-sys)~~
* ~~[certpoleng-sys](https://crates.io/crates/certpoleng-sys)~~
* ~~[cfgmgr32-sys](https://crates.io/crates/cfgmgr32-sys)~~
* ~~[clfsmgmt-sys](https://crates.io/crates/clfsmgmt-sys)~~
* ~~[clfsw32-sys](https://crates.io/crates/clfsw32-sys)~~
* ~~[clusapi-sys](https://crates.io/crates/clusapi-sys)~~
* ~~[comctl32-sys](https://crates.io/crates/comctl32-sys)~~
* ~~[comdlg32-sys](https://crates.io/crates/comdlg32-sys)~~
* ~~[comppkgsup-sys](https://crates.io/crates/comppkgsup-sys)~~
* ~~[compstui-sys](https://crates.io/crates/compstui-sys)~~
* ~~[comsvcs-sys](https://crates.io/crates/comsvcs-sys)~~
* ~~[corguids-sys](https://crates.io/crates/corguids-sys)~~
* ~~[correngine-sys](https://crates.io/crates/correngine-sys)~~
* ~~[credui-sys](https://crates.io/crates/credui-sys)~~
* ~~[crypt32-sys](https://crates.io/crates/crypt32-sys)~~
* ~~[cryptdll-sys](https://crates.io/crates/cryptdll-sys)~~
* ~~[cryptnet-sys](https://crates.io/crates/cryptnet-sys)~~
* ~~[cryptui-sys](https://crates.io/crates/cryptui-sys)~~
* ~~[cryptxml-sys](https://crates.io/crates/cryptxml-sys)~~
* ~~[cscapi-sys](https://crates.io/crates/cscapi-sys)~~
* ~~[cscdll-sys](https://crates.io/crates/cscdll-sys)~~
* ~~[d2d1-sys](https://crates.io/crates/d2d1-sys)~~
* ~~[d3d10-sys](https://crates.io/crates/d3d10-sys)~~
* ~~[d3d10_1-sys](https://crates.io/crates/d3d10_1-sys)~~
* ~~[d3d11-sys](https://crates.io/crates/d3d11-sys)~~
* ~~[d3d9-sys](https://crates.io/crates/d3d9-sys)~~
* ~~[d3dcompiler-sys](https://crates.io/crates/d3dcompiler-sys)~~
* ~~[d3dcsx-sys](https://crates.io/crates/d3dcsx-sys)~~
* ~~[d3dcsxd-sys](https://crates.io/crates/d3dcsxd-sys)~~
* ~~[davclnt-sys](https://crates.io/crates/davclnt-sys)~~
* ~~[dbgeng-sys](https://crates.io/crates/dbgeng-sys)~~
* ~~[dbghelp-sys](https://crates.io/crates/dbghelp-sys)~~
* ~~[dciman32-sys](https://crates.io/crates/dciman32-sys)~~
* ~~[dcomp-sys](https://crates.io/crates/dcomp-sys)~~
* ~~[ddraw-sys](https://crates.io/crates/ddraw-sys)~~
* ~~[devenum-sys](https://crates.io/crates/devenum-sys)~~
* ~~[deviceaccess-sys](https://crates.io/crates/deviceaccess-sys)~~
* ~~[devmgr-sys](https://crates.io/crates/devmgr-sys)~~
* ~~[dflayout-sys](https://crates.io/crates/dflayout-sys)~~
* ~~[dhcpcsvc-sys](https://crates.io/crates/dhcpcsvc-sys)~~
* ~~[dhcpcsvc6-sys](https://crates.io/crates/dhcpcsvc6-sys)~~
* ~~[dhcpsapi-sys](https://crates.io/crates/dhcpsapi-sys)~~
* ~~[difxapi-sys](https://crates.io/crates/difxapi-sys)~~
* ~~[dinput8-sys](https://crates.io/crates/dinput8-sys)~~
* ~~[dloadhelper-sys](https://crates.io/crates/dloadhelper-sys)~~
* ~~[dmoguids-sys](https://crates.io/crates/dmoguids-sys)~~
* ~~[dnsapi-sys](https://crates.io/crates/dnsapi-sys)~~
* ~~[dnscrcli-sys](https://crates.io/crates/dnscrcli-sys)~~
* ~~[dnslib-sys](https://crates.io/crates/dnslib-sys)~~
* ~~[dnsperf-sys](https://crates.io/crates/dnsperf-sys)~~
* ~~[dnsrpc-sys](https://crates.io/crates/dnsrpc-sys)~~
* ~~[dnsrslvr-sys](https://crates.io/crates/dnsrslvr-sys)~~
* ~~[dpx-sys](https://crates.io/crates/dpx-sys)~~
* ~~[drt-sys](https://crates.io/crates/drt-sys)~~
* ~~[drtprov-sys](https://crates.io/crates/drtprov-sys)~~
* ~~[drttransport-sys](https://crates.io/crates/drttransport-sys)~~
* ~~[dsound-sys](https://crates.io/crates/dsound-sys)~~
* ~~[dsprop-sys](https://crates.io/crates/dsprop-sys)~~
* ~~[dssec-sys](https://crates.io/crates/dssec-sys)~~
* ~~[dststlog-sys](https://crates.io/crates/dststlog-sys)~~
* ~~[dsuiext-sys](https://crates.io/crates/dsuiext-sys)~~
* ~~[dtchelp-sys](https://crates.io/crates/dtchelp-sys)~~
* ~~[dwmapi-sys](https://crates.io/crates/dwmapi-sys)~~
* ~~[dwrite-sys](https://crates.io/crates/dwrite-sys)~~
* ~~[dxgi-sys](https://crates.io/crates/dxgi-sys)~~
* ~~[dxguid-sys](https://crates.io/crates/dxguid-sys)~~
* ~~[dxtmsft-sys](https://crates.io/crates/dxtmsft-sys)~~
* ~~[dxtrans-sys](https://crates.io/crates/dxtrans-sys)~~
* ~~[dxva2-sys](https://crates.io/crates/dxva2-sys)~~
* ~~[eappcfg-sys](https://crates.io/crates/eappcfg-sys)~~
* ~~[eappprxy-sys](https://crates.io/crates/eappprxy-sys)~~
* ~~[easregprov-sys](https://crates.io/crates/easregprov-sys)~~
* ~~[efswrt-sys](https://crates.io/crates/efswrt-sys)~~
* ~~[ehstorguids-sys](https://crates.io/crates/ehstorguids-sys)~~
* ~~[elfapi-sys](https://crates.io/crates/elfapi-sys)~~
* ~~[els-sys](https://crates.io/crates/els-sys)~~
* ~~[elscore-sys](https://crates.io/crates/elscore-sys)~~
* ~~[esent-sys](https://crates.io/crates/esent-sys)~~
* ~~[evr-sys](https://crates.io/crates/evr-sys)~~
* ~~[evr_vista-sys](https://crates.io/crates/evr_vista-sys)~~
* ~~[faultrep-sys](https://crates.io/crates/faultrep-sys)~~
* ~~[feclient-sys](https://crates.io/crates/feclient-sys)~~
* ~~[fhsvcctl-sys](https://crates.io/crates/fhsvcctl-sys)~~
* ~~[fileextd-sys](https://crates.io/crates/fileextd-sys)~~
* ~~[fltlib-sys](https://crates.io/crates/fltlib-sys)~~
* ~~[fontsub-sys](https://crates.io/crates/fontsub-sys)~~
* ~~[format-sys](https://crates.io/crates/format-sys)~~
* ~~[framedyd-sys](https://crates.io/crates/framedyd-sys)~~
* ~~[framedyn-sys](https://crates.io/crates/framedyn-sys)~~
* ~~[fwpuclnt-sys](https://crates.io/crates/fwpuclnt-sys)~~
* ~~[fxsutility-sys](https://crates.io/crates/fxsutility-sys)~~
* [gdi32-sys](https://crates.io/crates/gdi32-sys)
* ~~[gdiplus-sys](https://crates.io/crates/gdiplus-sys)~~
* ~~[glmf32-sys](https://crates.io/crates/glmf32-sys)~~
* ~~[glu32-sys](https://crates.io/crates/glu32-sys)~~
* ~~[gpedit-sys](https://crates.io/crates/gpedit-sys)~~
* ~~[gpmuuid-sys](https://crates.io/crates/gpmuuid-sys)~~
* ~~[hbaapi-sys](https://crates.io/crates/hbaapi-sys)~~
* ~~[hhsetup-sys](https://crates.io/crates/hhsetup-sys)~~
* ~~[hid-sys](https://crates.io/crates/hid-sys)~~
* ~~[hlink-sys](https://crates.io/crates/hlink-sys)~~
* ~~[htmlhelp-sys](https://crates.io/crates/htmlhelp-sys)~~
* ~~[httpapi-sys](https://crates.io/crates/httpapi-sys)~~
* ~~[iashlpr-sys](https://crates.io/crates/iashlpr-sys)~~
* ~~[icm32-sys](https://crates.io/crates/icm32-sys)~~
* ~~[icmui-sys](https://crates.io/crates/icmui-sys)~~
* ~~[iepmapi-sys](https://crates.io/crates/iepmapi-sys)~~
* ~~[iesetup-sys](https://crates.io/crates/iesetup-sys)~~
* ~~[imagehlp-sys](https://crates.io/crates/imagehlp-sys)~~
* ~~[imgutil-sys](https://crates.io/crates/imgutil-sys)~~
* ~~[imm32-sys](https://crates.io/crates/imm32-sys)~~
* ~~[infocardapi-sys](https://crates.io/crates/infocardapi-sys)~~
* ~~[inseng-sys](https://crates.io/crates/inseng-sys)~~
* ~~[int64-sys](https://crates.io/crates/int64-sys)~~
* ~~[iphlpapi-sys](https://crates.io/crates/iphlpapi-sys)~~
* ~~[iprop-sys](https://crates.io/crates/iprop-sys)~~
* ~~[irprops-sys](https://crates.io/crates/irprops-sys)~~
* ~~[iscsidsc-sys](https://crates.io/crates/iscsidsc-sys)~~
* ~~[jetoledb-sys](https://crates.io/crates/jetoledb-sys)~~
* ~~[jsrt-sys](https://crates.io/crates/jsrt-sys)~~
* ~~[kerbcli-sys](https://crates.io/crates/kerbcli-sys)~~
* [kernel32-sys](https://crates.io/crates/kernel32-sys)
* ~~[ksproxy-sys](https://crates.io/crates/ksproxy-sys)~~
* ~~[ksuser-sys](https://crates.io/crates/ksuser-sys)~~
* ~~[ktmw32-sys](https://crates.io/crates/ktmw32-sys)~~
* ~~[loadperf-sys](https://crates.io/crates/loadperf-sys)~~
* ~~[locationapi-sys](https://crates.io/crates/locationapi-sys)~~
* ~~[lz32-sys](https://crates.io/crates/lz32-sys)~~
* ~~[magnification-sys](https://crates.io/crates/magnification-sys)~~
* ~~[mapi32-sys](https://crates.io/crates/mapi32-sys)~~
* ~~[mbnapi_uuid-sys](https://crates.io/crates/mbnapi_uuid-sys)~~
* ~~[mciole32-sys](https://crates.io/crates/mciole32-sys)~~
* ~~[mdmregistration-sys](https://crates.io/crates/mdmregistration-sys)~~
* ~~[mf-sys](https://crates.io/crates/mf-sys)~~
* ~~[mf_vista-sys](https://crates.io/crates/mf_vista-sys)~~
* ~~[mfcore-sys](https://crates.io/crates/mfcore-sys)~~
* ~~[mfplat-sys](https://crates.io/crates/mfplat-sys)~~
* ~~[mfplat_vista-sys](https://crates.io/crates/mfplat_vista-sys)~~
* ~~[mfplay-sys](https://crates.io/crates/mfplay-sys)~~
* ~~[mfreadwrite-sys](https://crates.io/crates/mfreadwrite-sys)~~
* ~~[mfsrcsnk-sys](https://crates.io/crates/mfsrcsnk-sys)~~
* ~~[mfuuid-sys](https://crates.io/crates/mfuuid-sys)~~
* ~~[mgmtapi-sys](https://crates.io/crates/mgmtapi-sys)~~
* ~~[mi-sys](https://crates.io/crates/mi-sys)~~
* ~~[mincore-sys](https://crates.io/crates/mincore-sys)~~
* ~~[mincore_downlevel-sys](https://crates.io/crates/mincore_downlevel-sys)~~
* ~~[mmc-sys](https://crates.io/crates/mmc-sys)~~
* ~~[mmdevapi-sys](https://crates.io/crates/mmdevapi-sys)~~
* ~~[mpr-sys](https://crates.io/crates/mpr-sys)~~
* ~~[mprapi-sys](https://crates.io/crates/mprapi-sys)~~
* ~~[mprsnap-sys](https://crates.io/crates/mprsnap-sys)~~
* ~~[mqoa-sys](https://crates.io/crates/mqoa-sys)~~
* ~~[mqrt-sys](https://crates.io/crates/mqrt-sys)~~
* ~~[msaatext-sys](https://crates.io/crates/msaatext-sys)~~
* ~~[msacm32-sys](https://crates.io/crates/msacm32-sys)~~
* ~~[mscms-sys](https://crates.io/crates/mscms-sys)~~
* ~~[mscoree-sys](https://crates.io/crates/mscoree-sys)~~
* ~~[mscorsn-sys](https://crates.io/crates/mscorsn-sys)~~
* ~~[msctfmonitor-sys](https://crates.io/crates/msctfmonitor-sys)~~
* ~~[msdasc-sys](https://crates.io/crates/msdasc-sys)~~
* ~~[msdelta-sys](https://crates.io/crates/msdelta-sys)~~
* ~~[msdmo-sys](https://crates.io/crates/msdmo-sys)~~
* ~~[msdrm-sys](https://crates.io/crates/msdrm-sys)~~
* ~~[msi-sys](https://crates.io/crates/msi-sys)~~
* ~~[msimg32-sys](https://crates.io/crates/msimg32-sys)~~
* ~~[mspatcha-sys](https://crates.io/crates/mspatcha-sys)~~
* ~~[mspatchc-sys](https://crates.io/crates/mspatchc-sys)~~
* ~~[mspbase-sys](https://crates.io/crates/mspbase-sys)~~
* ~~[msports-sys](https://crates.io/crates/msports-sys)~~
* ~~[msrating-sys](https://crates.io/crates/msrating-sys)~~
* ~~[mstask-sys](https://crates.io/crates/mstask-sys)~~
* ~~[msv1_0-sys](https://crates.io/crates/msv1_0-sys)~~
* ~~[msvfw32-sys](https://crates.io/crates/msvfw32-sys)~~
* ~~[mswsock-sys](https://crates.io/crates/mswsock-sys)~~
* ~~[msxml2-sys](https://crates.io/crates/msxml2-sys)~~
* ~~[msxml6-sys](https://crates.io/crates/msxml6-sys)~~
* ~~[mtx-sys](https://crates.io/crates/mtx-sys)~~
* ~~[mtxdm-sys](https://crates.io/crates/mtxdm-sys)~~
* ~~[muiload-sys](https://crates.io/crates/muiload-sys)~~
* ~~[ncrypt-sys](https://crates.io/crates/ncrypt-sys)~~
* ~~[nddeapi-sys](https://crates.io/crates/nddeapi-sys)~~
* ~~[ndfapi-sys](https://crates.io/crates/ndfapi-sys)~~
* ~~[ndproxystub-sys](https://crates.io/crates/ndproxystub-sys)~~
* ~~[netapi32-sys](https://crates.io/crates/netapi32-sys)~~
* ~~[netlib-sys](https://crates.io/crates/netlib-sys)~~
* ~~[netsh-sys](https://crates.io/crates/netsh-sys)~~
* ~~[newdev-sys](https://crates.io/crates/newdev-sys)~~
* ~~[ninput-sys](https://crates.io/crates/ninput-sys)~~
* ~~[normaliz-sys](https://crates.io/crates/normaliz-sys)~~
* ~~[nt-sys](https://crates.io/crates/nt-sys)~~
* ~~[ntdll-sys](https://crates.io/crates/ntdll-sys)~~
* ~~[ntdsa-sys](https://crates.io/crates/ntdsa-sys)~~
* ~~[ntdsapi-sys](https://crates.io/crates/ntdsapi-sys)~~
* ~~[ntdsatq-sys](https://crates.io/crates/ntdsatq-sys)~~
* ~~[ntdsetup-sys](https://crates.io/crates/ntdsetup-sys)~~
* ~~[ntfrsapi-sys](https://crates.io/crates/ntfrsapi-sys)~~
* ~~[ntlanman-sys](https://crates.io/crates/ntlanman-sys)~~
* ~~[ntmarta-sys](https://crates.io/crates/ntmarta-sys)~~
* ~~[ntquery-sys](https://crates.io/crates/ntquery-sys)~~
* ~~[ntstc_libcmt-sys](https://crates.io/crates/ntstc_libcmt-sys)~~
* ~~[ntstc_msvcrt-sys](https://crates.io/crates/ntstc_msvcrt-sys)~~
* ~~[ntvdm-sys](https://crates.io/crates/ntvdm-sys)~~
* ~~[objsel-sys](https://crates.io/crates/objsel-sys)~~
* ~~[odbc32-sys](https://crates.io/crates/odbc32-sys)~~
* ~~[odbcbcp-sys](https://crates.io/crates/odbcbcp-sys)~~
* ~~[odbccp32-sys](https://crates.io/crates/odbccp32-sys)~~
* ~~[oemlicense-sys](https://crates.io/crates/oemlicense-sys)~~
* [ole32-sys](https://crates.io/crates/ole32-sys)
* ~~[oleacc-sys](https://crates.io/crates/oleacc-sys)~~
* ~~[oleaut32-sys](https://crates.io/crates/oleaut32-sys)~~
* ~~[olecli32-sys](https://crates.io/crates/olecli32-sys)~~
* ~~[oledb-sys](https://crates.io/crates/oledb-sys)~~
* ~~[oledlg-sys](https://crates.io/crates/oledlg-sys)~~
* ~~[olepro32-sys](https://crates.io/crates/olepro32-sys)~~
* ~~[olesvr32-sys](https://crates.io/crates/olesvr32-sys)~~
* ~~[ondemandconnroutehelper-sys](https://crates.io/crates/ondemandconnroutehelper-sys)~~
* ~~[opengl32-sys](https://crates.io/crates/opengl32-sys)~~
* ~~[osptk-sys](https://crates.io/crates/osptk-sys)~~
* ~~[p2p-sys](https://crates.io/crates/p2p-sys)~~
* ~~[p2pgraph-sys](https://crates.io/crates/p2pgraph-sys)~~
* ~~[patchwiz-sys](https://crates.io/crates/patchwiz-sys)~~
* ~~[pathcch-sys](https://crates.io/crates/pathcch-sys)~~
* ~~[pdh-sys](https://crates.io/crates/pdh-sys)~~
* ~~[peerdist-sys](https://crates.io/crates/peerdist-sys)~~
* ~~[photoacquireuid-sys](https://crates.io/crates/photoacquireuid-sys)~~
* ~~[portabledeviceguids-sys](https://crates.io/crates/portabledeviceguids-sys)~~
* ~~[powrprof-sys](https://crates.io/crates/powrprof-sys)~~
* ~~[prntvpt-sys](https://crates.io/crates/prntvpt-sys)~~
* ~~[propsys-sys](https://crates.io/crates/propsys-sys)~~
* ~~[psapi-sys](https://crates.io/crates/psapi-sys)~~
* ~~[quartz-sys](https://crates.io/crates/quartz-sys)~~
* ~~[query-sys](https://crates.io/crates/query-sys)~~
* ~~[qutil-sys](https://crates.io/crates/qutil-sys)~~
* ~~[qwave-sys](https://crates.io/crates/qwave-sys)~~
* ~~[rasapi32-sys](https://crates.io/crates/rasapi32-sys)~~
* ~~[rasdlg-sys](https://crates.io/crates/rasdlg-sys)~~
* ~~[rasuser-sys](https://crates.io/crates/rasuser-sys)~~
* ~~[resutils-sys](https://crates.io/crates/resutils-sys)~~
* ~~[rometadata-sys](https://crates.io/crates/rometadata-sys)~~
* ~~[rpcexts-sys](https://crates.io/crates/rpcexts-sys)~~
* ~~[rpcns4-sys](https://crates.io/crates/rpcns4-sys)~~
* ~~[rpcproxy-sys](https://crates.io/crates/rpcproxy-sys)~~
* ~~[rpcrt4-sys](https://crates.io/crates/rpcrt4-sys)~~
* ~~[rpcutil-sys](https://crates.io/crates/rpcutil-sys)~~
* ~~[rstrtmgr-sys](https://crates.io/crates/rstrtmgr-sys)~~
* ~~[rtm-sys](https://crates.io/crates/rtm-sys)~~
* ~~[rtutils-sys](https://crates.io/crates/rtutils-sys)~~
* ~~[rtworkq-sys](https://crates.io/crates/rtworkq-sys)~~
* ~~[runtimeobject-sys](https://crates.io/crates/runtimeobject-sys)~~
* ~~[samlib-sys](https://crates.io/crates/samlib-sys)~~
* ~~[samsrv-sys](https://crates.io/crates/samsrv-sys)~~
* ~~[sapi-sys](https://crates.io/crates/sapi-sys)~~
* ~~[sas-sys](https://crates.io/crates/sas-sys)~~
* ~~[sbtsv-sys](https://crates.io/crates/sbtsv-sys)~~
* ~~[scarddlg-sys](https://crates.io/crates/scarddlg-sys)~~
* ~~[scecli-sys](https://crates.io/crates/scecli-sys)~~
* ~~[scesrv-sys](https://crates.io/crates/scesrv-sys)~~
* ~~[schannel-sys](https://crates.io/crates/schannel-sys)~~
* ~~[scrnsave-sys](https://crates.io/crates/scrnsave-sys)~~
* ~~[scrnsavw-sys](https://crates.io/crates/scrnsavw-sys)~~
* ~~[searchsdk-sys](https://crates.io/crates/searchsdk-sys)~~
* ~~[secur32-sys](https://crates.io/crates/secur32-sys)~~
* ~~[security-sys](https://crates.io/crates/security-sys)~~
* ~~[sens-sys](https://crates.io/crates/sens-sys)~~
* ~~[sensapi-sys](https://crates.io/crates/sensapi-sys)~~
* ~~[sensorsapi-sys](https://crates.io/crates/sensorsapi-sys)~~
* ~~[setupapi-sys](https://crates.io/crates/setupapi-sys)~~
* ~~[sfc-sys](https://crates.io/crates/sfc-sys)~~
* ~~[shcore-sys](https://crates.io/crates/shcore-sys)~~
* ~~[shdocvw-sys](https://crates.io/crates/shdocvw-sys)~~
* [shell32-sys](https://crates.io/crates/shell32-sys)
* ~~[shfolder-sys](https://crates.io/crates/shfolder-sys)~~
* ~~[shlwapi-sys](https://crates.io/crates/shlwapi-sys)~~
* ~~[sisbkup-sys](https://crates.io/crates/sisbkup-sys)~~
* ~~[slc-sys](https://crates.io/crates/slc-sys)~~
* ~~[slcext-sys](https://crates.io/crates/slcext-sys)~~
* ~~[slwga-sys](https://crates.io/crates/slwga-sys)~~
* ~~[snmpapi-sys](https://crates.io/crates/snmpapi-sys)~~
* ~~[spoolss-sys](https://crates.io/crates/spoolss-sys)~~
* ~~[sporder-sys](https://crates.io/crates/sporder-sys)~~
* ~~[srclient-sys](https://crates.io/crates/srclient-sys)~~
* ~~[ssdpapi-sys](https://crates.io/crates/ssdpapi-sys)~~
* ~~[sti-sys](https://crates.io/crates/sti-sys)~~
* ~~[strmbase-sys](https://crates.io/crates/strmbase-sys)~~
* ~~[strmiids-sys](https://crates.io/crates/strmiids-sys)~~
* ~~[strsafe-sys](https://crates.io/crates/strsafe-sys)~~
* ~~[structuredquery-sys](https://crates.io/crates/structuredquery-sys)~~
* ~~[svcguid-sys](https://crates.io/crates/svcguid-sys)~~
* ~~[swdevice-sys](https://crates.io/crates/swdevice-sys)~~
* ~~[synchronization-sys](https://crates.io/crates/synchronization-sys)~~
* ~~[t2embed-sys](https://crates.io/crates/t2embed-sys)~~
* ~~[tapi32-sys](https://crates.io/crates/tapi32-sys)~~
* ~~[tapi32l-sys](https://crates.io/crates/tapi32l-sys)~~
* ~~[taskschd-sys](https://crates.io/crates/taskschd-sys)~~
* ~~[tbs-sys](https://crates.io/crates/tbs-sys)~~
* ~~[tdh-sys](https://crates.io/crates/tdh-sys)~~
* ~~[thunk32-sys](https://crates.io/crates/thunk32-sys)~~
* ~~[tlbref-sys](https://crates.io/crates/tlbref-sys)~~
* ~~[traffic-sys](https://crates.io/crates/traffic-sys)~~
* ~~[transcodeimageuid-sys](https://crates.io/crates/transcodeimageuid-sys)~~
* ~~[tsec-sys](https://crates.io/crates/tsec-sys)~~
* ~~[tspubplugincom-sys](https://crates.io/crates/tspubplugincom-sys)~~
* ~~[twain_32-sys](https://crates.io/crates/twain_32-sys)~~
* ~~[twinapi-sys](https://crates.io/crates/twinapi-sys)~~
* ~~[txfw32-sys](https://crates.io/crates/txfw32-sys)~~
* ~~[ualapi-sys](https://crates.io/crates/ualapi-sys)~~
* ~~[uiautomationcore-sys](https://crates.io/crates/uiautomationcore-sys)~~
* ~~[umpdddi-sys](https://crates.io/crates/umpdddi-sys)~~
* ~~[unicows-sys](https://crates.io/crates/unicows-sys)~~
* ~~[urlmon-sys](https://crates.io/crates/urlmon-sys)~~
* [user32-sys](https://crates.io/crates/user32-sys)
* ~~[userenv-sys](https://crates.io/crates/userenv-sys)~~
* ~~[usp10-sys](https://crates.io/crates/usp10-sys)~~
* ~~[uuid-sys](https://crates.io/crates/uuid-sys)~~
* ~~[uxtheme-sys](https://crates.io/crates/uxtheme-sys)~~
* ~~[vccomsup-sys](https://crates.io/crates/vccomsup-sys)~~
* ~~[vdmdbg-sys](https://crates.io/crates/vdmdbg-sys)~~
* ~~[vds_uuid-sys](https://crates.io/crates/vds_uuid-sys)~~
* ~~[version-sys](https://crates.io/crates/version-sys)~~
* ~~[vfw32-sys](https://crates.io/crates/vfw32-sys)~~
* ~~[virtdisk-sys](https://crates.io/crates/virtdisk-sys)~~
* ~~[vscmgr-sys](https://crates.io/crates/vscmgr-sys)~~
* ~~[vss_uuid-sys](https://crates.io/crates/vss_uuid-sys)~~
* ~~[vssapi-sys](https://crates.io/crates/vssapi-sys)~~
* ~~[vstorinterface-sys](https://crates.io/crates/vstorinterface-sys)~~
* ~~[wbemuuid-sys](https://crates.io/crates/wbemuuid-sys)~~
* ~~[wcmapi-sys](https://crates.io/crates/wcmapi-sys)~~
* ~~[wcmguid-sys](https://crates.io/crates/wcmguid-sys)~~
* ~~[wdsbp-sys](https://crates.io/crates/wdsbp-sys)~~
* ~~[wdsclientapi-sys](https://crates.io/crates/wdsclientapi-sys)~~
* ~~[wdsmc-sys](https://crates.io/crates/wdsmc-sys)~~
* ~~[wdspxe-sys](https://crates.io/crates/wdspxe-sys)~~
* ~~[wdstptc-sys](https://crates.io/crates/wdstptc-sys)~~
* ~~[webservices-sys](https://crates.io/crates/webservices-sys)~~
* ~~[websocket-sys](https://crates.io/crates/websocket-sys)~~
* ~~[wecapi-sys](https://crates.io/crates/wecapi-sys)~~
* ~~[wer-sys](https://crates.io/crates/wer-sys)~~
* ~~[wevtapi-sys](https://crates.io/crates/wevtapi-sys)~~
* ~~[wiaguid-sys](https://crates.io/crates/wiaguid-sys)~~
* ~~[wiaservc-sys](https://crates.io/crates/wiaservc-sys)~~
* ~~[wiautil-sys](https://crates.io/crates/wiautil-sys)~~
* ~~[winbio-sys](https://crates.io/crates/winbio-sys)~~
* ~~[windows-data-pdf-sys](https://crates.io/crates/windows-data-pdf-sys)~~
* ~~[windows-networking-sys](https://crates.io/crates/windows-networking-sys)~~
* ~~[windows-ui-sys](https://crates.io/crates/windows-ui-sys)~~
* ~~[windowscodecs-sys](https://crates.io/crates/windowscodecs-sys)~~
* ~~[windowssideshowguids-sys](https://crates.io/crates/windowssideshowguids-sys)~~
* ~~[winfax-sys](https://crates.io/crates/winfax-sys)~~
* ~~[winhttp-sys](https://crates.io/crates/winhttp-sys)~~
* ~~[wininet-sys](https://crates.io/crates/wininet-sys)~~
* [winmm-sys](https://crates.io/crates/winmm-sys)
* ~~[winsatapi-sys](https://crates.io/crates/winsatapi-sys)~~
* ~~[winscard-sys](https://crates.io/crates/winscard-sys)~~
* ~~[winspool-sys](https://crates.io/crates/winspool-sys)~~
* ~~[winsta-sys](https://crates.io/crates/winsta-sys)~~
* ~~[winstrm-sys](https://crates.io/crates/winstrm-sys)~~
* ~~[wintrust-sys](https://crates.io/crates/wintrust-sys)~~
* ~~[winusb-sys](https://crates.io/crates/winusb-sys)~~
* ~~[wlanapi-sys](https://crates.io/crates/wlanapi-sys)~~
* ~~[wlanui-sys](https://crates.io/crates/wlanui-sys)~~
* ~~[wldap32-sys](https://crates.io/crates/wldap32-sys)~~
* ~~[wmcodecdspuuid-sys](https://crates.io/crates/wmcodecdspuuid-sys)~~
* ~~[wmdrmsdk-sys](https://crates.io/crates/wmdrmsdk-sys)~~
* ~~[wmip-sys](https://crates.io/crates/wmip-sys)~~
* ~~[wmiutils-sys](https://crates.io/crates/wmiutils-sys)~~
* ~~[wmvcore-sys](https://crates.io/crates/wmvcore-sys)~~
* ~~[wnvapi-sys](https://crates.io/crates/wnvapi-sys)~~
* ~~[workspaceax-sys](https://crates.io/crates/workspaceax-sys)~~
* ~~[wow32-sys](https://crates.io/crates/wow32-sys)~~
* ~~[ws2_32-sys](https://crates.io/crates/ws2_32-sys)~~
* ~~[wsbapp_uuid-sys](https://crates.io/crates/wsbapp_uuid-sys)~~
* ~~[wsbonline-sys](https://crates.io/crates/wsbonline-sys)~~
* ~~[wscapi-sys](https://crates.io/crates/wscapi-sys)~~
* ~~[wsclient-sys](https://crates.io/crates/wsclient-sys)~~
* ~~[wsdapi-sys](https://crates.io/crates/wsdapi-sys)~~
* ~~[wsmsvc-sys](https://crates.io/crates/wsmsvc-sys)~~
* ~~[wsnmp32-sys](https://crates.io/crates/wsnmp32-sys)~~
* ~~[wsock32-sys](https://crates.io/crates/wsock32-sys)~~
* ~~[wtsapi32-sys](https://crates.io/crates/wtsapi32-sys)~~
* ~~[wuguid-sys](https://crates.io/crates/wuguid-sys)~~
* ~~[xapobase-sys](https://crates.io/crates/xapobase-sys)~~
* ~~[xaswitch-sys](https://crates.io/crates/xaswitch-sys)~~
* ~~[xaudio2-sys](https://crates.io/crates/xaudio2-sys)~~
* ~~[xinput-sys](https://crates.io/crates/xinput-sys)~~
* ~~[xinput9_1_0-sys](https://crates.io/crates/xinput9_1_0-sys)~~
* ~~[xmllite-sys](https://crates.io/crates/xmllite-sys)~~
* ~~[xolehlp-sys](https://crates.io/crates/xolehlp-sys)~~
* ~~[xpsprint-sys](https://crates.io/crates/xpsprint-sys)~~
