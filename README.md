# -
持っているちいかわご当地キーホルダー靴下ぬいぐるみ情報
<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ちいかわ ご当地コレクション帳</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Zen+Maru+Gothic:wght@400;700;900&display=swap');
*{box-sizing:border-box;margin:0;padding:0}
:root{
  --p:#FF8FAB;--pb:#FFB7C5;--ps:#FFF0F5;
  --t:#00ACC1;--tb:#B2EBF2;--ts:#E8FAFB;
  --y:#FFB300;--yb:#FFE082;--ys:#FFFDE7;
  --g:#43A047;--gb:#A5D6A7;--gs:#F1F8E9;
  --pu:#9575CD;--pub:#D1C4E9;--pus:#EDE7F6;
  --br:#5D4037;--bg:#FFF8F0;--tx:#3E2723;
  --sh:rgba(93,64,55,.12);--sh2:rgba(93,64,55,.2);
  --cat-color:var(--p); --cat-border:var(--pb); --cat-bg:var(--ps);
}
body{font-family:'Zen Maru Gothic',sans-serif;background:var(--bg);color:var(--tx);min-height:100vh}
body::before{content:'';position:fixed;inset:0;pointer-events:none;z-index:0;
  background:radial-gradient(circle at 10% 15%,rgba(255,183,197,.22) 0%,transparent 45%),
             radial-gradient(circle at 90% 80%,rgba(178,235,242,.18) 0%,transparent 45%)}
.wrap{position:relative;z-index:1;max-width:940px;margin:0 auto;padding:12px 12px 50px}

/* ── ヘッダー ── */
.hdr{background:#fff;border-radius:22px;box-shadow:0 4px 20px var(--sh);
  border:3px solid var(--cat-border);padding:14px 16px;text-align:center;
  margin-bottom:10px;position:relative;overflow:hidden;transition:border-color .3s}
.hdr::after{content:'';position:absolute;bottom:0;left:0;right:0;height:4px;
  background:linear-gradient(90deg,var(--pb),var(--yb),var(--tb),var(--pub),var(--pb));
  transition:background .4s}
.hdr h1{font-size:clamp(1rem,4vw,1.65rem);font-weight:900;color:var(--cat-color);
  margin-bottom:3px;transition:color .3s}
.hdr-sub{font-size:.71rem;color:#bbb;display:flex;justify-content:center;
  align-items:center;gap:7px;flex-wrap:wrap}
.chip{font-weight:700;font-size:.69rem;padding:2px 10px;border-radius:99px;
  cursor:pointer;border:1.5px solid;transition:all .2s}
.dev-chip{background:var(--cat-bg);color:var(--cat-color);border-color:var(--cat-border)}
.dev-chip:hover{background:var(--cat-border);color:#fff}
.sync-chip.on{background:var(--ts);color:var(--t);border-color:var(--tb)}
.sync-chip.off{background:#f5f5f5;color:#bbb;border-color:#eee}

/* ── カテゴリタブ ── */
.cat-bar{background:#fff;border-radius:16px;box-shadow:0 3px 14px var(--sh);
  padding:10px 12px;margin-bottom:10px;display:flex;gap:7px;align-items:center;flex-wrap:wrap}
.cat-tab{display:flex;align-items:center;gap:5px;padding:8px 16px;border-radius:12px;
  border:2.5px solid #eee;background:#f9f9f9;cursor:pointer;font-family:inherit;
  font-size:.8rem;font-weight:700;color:#aaa;transition:all .22s;white-space:nowrap}
.cat-tab .cat-emo{font-size:1.1rem}
.cat-tab.active-key{border-color:var(--pb);background:var(--ps);color:var(--p)}
.cat-tab.active-sock{border-color:var(--pub);background:var(--pus);color:var(--pu)}
.cat-tab.active-nuig{border-color:var(--gb);background:var(--gs);color:var(--g)}
.cat-tab:hover:not([class*=active]){background:#f0f0f0;color:#777;transform:translateY(-1px)}
.cat-desc{flex:1;font-size:.69rem;color:#bbb;text-align:right;white-space:nowrap}

/* ── 統計バー ── */
.stats{background:#fff;border-radius:14px;box-shadow:0 3px 12px var(--sh);
  border:2px solid var(--yb);padding:10px 14px;margin-bottom:10px;
  display:flex;flex-wrap:wrap;gap:8px;align-items:center}
.si{flex:1;min-width:50px;text-align:center}
.sn{font-size:1.3rem;font-weight:900;line-height:1;display:block}
.sn.o{color:var(--cat-color)}.sn.m{color:#ccc}.sn.t{color:var(--t)}
.sl{font-size:.62rem;color:#bbb;margin-top:1px;display:block}
.prog{flex:3;min-width:120px}
.prog-bg{height:11px;background:#f0f0f0;border-radius:99px;overflow:hidden}
.prog-fill{height:100%;border-radius:99px;transition:width .5s,background .4s;
  background:linear-gradient(90deg,var(--cat-color),var(--y))}
.prog-pct{font-size:.7rem;font-weight:700;color:var(--cat-color);text-align:right;margin-top:2px}

/* ── コントロール ── */
.ctrl{background:#fff;border-radius:14px;box-shadow:0 3px 12px var(--sh);
  padding:9px 12px;margin-bottom:10px;display:flex;flex-wrap:wrap;gap:6px;align-items:center}
.filt{padding:5px 11px;border-radius:99px;border:2px solid transparent;
  font-family:inherit;font-size:.72rem;font-weight:700;cursor:pointer;
  background:#f5f5f5;color:#aaa;transition:all .18s}
.filt.on{background:var(--cat-color);color:#fff;border-color:var(--cat-border)}
.filt:hover:not(.on){background:#E1BEE7;color:var(--tx)}
.sw{flex:1;min-width:100px}
.sw input{width:100%;padding:6px 12px;border:2px solid #eee;border-radius:99px;
  font-family:inherit;font-size:.78rem;outline:none;transition:border-color .2s}
.sw input:focus{border-color:var(--cat-border)}
.ibtn{padding:5px 12px;border-radius:99px;border:none;font-family:inherit;
  font-size:.71rem;font-weight:700;cursor:pointer;transition:transform .12s;white-space:nowrap}
.ibtn:hover{transform:translateY(-1px)}
.ibtn.green{background:linear-gradient(135deg,#34A853,#0F9D58);color:#fff;box-shadow:0 2px 7px rgba(52,168,83,.3)}
.ibtn.teal{background:linear-gradient(135deg,var(--t),#00838F);color:#fff;box-shadow:0 2px 7px rgba(0,172,193,.3)}
.ibtn.purple{background:linear-gradient(135deg,var(--pu),#7B1FA2);color:#fff;box-shadow:0 2px 7px rgba(149,117,205,.25)}
.ibtn.gray{background:#f5f5f5;color:#888}

/* ── カードグリッド ── */
.region{margin-bottom:14px}
.rlabel{font-size:.76rem;font-weight:900;color:#fff;background:var(--br);
  display:inline-block;padding:2px 13px;border-radius:99px;margin-bottom:7px}
.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(116px,1fr));gap:7px}
.card{background:#fff;border-radius:13px;padding:8px 6px 10px;box-shadow:0 2px 9px var(--sh);
  border:2.5px solid transparent;cursor:pointer;transition:all .2s;text-align:center;
  position:relative;user-select:none;animation:cIn .3s ease both}
@keyframes cIn{from{opacity:0;transform:translateY(8px)}to{opacity:1;transform:none}}
.card:hover{transform:translateY(-3px);box-shadow:0 7px 18px var(--sh2)}
.card.owned{background:linear-gradient(145deg,var(--ps),#fff);border-color:var(--pb)}
.card.owned.sock{background:linear-gradient(145deg,var(--pus),#fff);border-color:var(--pub)}
.card.owned.nuig{background:linear-gradient(145deg,var(--gs),#fff);border-color:var(--gb)}
.card.wanted{background:linear-gradient(145deg,var(--ys),#fff);border-color:var(--yb)}
.card.trade{border-color:var(--t);background:linear-gradient(145deg,var(--ts),#fff)}
.card.none{opacity:.44}
.card.hidden{display:none}
.cemo{font-size:1.75rem;display:block;margin-bottom:2px}
.carea{font-size:.57rem;font-weight:700;color:#bbb;background:#f5f5f5;
  border-radius:99px;padding:1px 7px;display:inline-block;margin-bottom:3px}
.cname{font-size:.68rem;font-weight:700;line-height:1.3;color:var(--tx)}
.cvenue{font-size:.53rem;color:#ccc;margin-top:3px;line-height:1.3}
.badgeown{position:absolute;top:5px;right:5px;width:17px;height:17px;border-radius:50%;
  background:var(--cat-color);color:#fff;font-size:.54rem;font-weight:900;
  display:flex;align-items:center;justify-content:center}
.badgetag{position:absolute;top:5px;left:5px;font-size:.5rem;font-weight:700;
  padding:1px 5px;border-radius:99px;color:#fff;line-height:1.4}
.badgetag.tr{background:var(--t)}.badgetag.wt{background:var(--y)}

/* ── オーバーレイ共通 ── */
.ov{position:fixed;inset:0;background:rgba(0,0,0,.4);display:flex;
  align-items:center;justify-content:center;z-index:200;padding:14px;animation:fI .15s}
.ov.hide{display:none}
@keyframes fI{from{opacity:0}to{opacity:1}}
.box{background:#fff;border-radius:22px;padding:20px;max-width:400px;width:100%;
  box-shadow:0 20px 50px rgba(0,0,0,.22);animation:sU .2s;max-height:92vh;overflow-y:auto}
.box.wide{max-width:580px}.box.xwide{max-width:680px}
@keyframes sU{from{transform:translateY(16px);opacity:0}to{transform:translateY(0);opacity:1}}
.bhdr{display:flex;justify-content:space-between;align-items:center;
  padding-bottom:11px;border-bottom:2px solid #f5f5f5;margin-bottom:13px}
.bhdr h2{font-size:.95rem;font-weight:900}
.xbtn{background:none;border:none;font-size:1.3rem;cursor:pointer;color:#ccc;line-height:1}
.xbtn:hover{color:var(--tx)}
.field{margin-bottom:11px}
.field label{font-size:.71rem;font-weight:700;color:#888;display:block;margin-bottom:4px}
.field input,.field textarea,.field select{width:100%;padding:7px 12px;border:2px solid #eee;
  border-radius:11px;font-family:inherit;font-size:.82rem;outline:none;transition:border-color .2s}
.field input:focus,.field textarea:focus{border-color:var(--cat-border)}
.field textarea{resize:none;height:56px}
.row{display:flex;gap:7px}
.btn{flex:1;padding:9px;border:none;border-radius:11px;font-family:inherit;
  font-size:.82rem;font-weight:900;cursor:pointer;transition:transform .1s}
.btn:hover{transform:translateY(-1px)}
.btn.pri{background:linear-gradient(135deg,var(--p),#FF5E84);color:#fff;box-shadow:0 3px 9px rgba(255,143,171,.3)}
.btn.sec{background:#f5f5f5;color:#888;border:2px solid #eee}
.btn.dan{background:#FFEBEE;color:#E53935;border:2px solid #FFCDD2}
.smbtn{padding:5px 11px;border-radius:99px;border:none;font-family:inherit;
  font-size:.68rem;font-weight:700;cursor:pointer;white-space:nowrap;transition:opacity .18s}
.smbtn:hover{opacity:.8}
.smbtn.teal{background:var(--t);color:#fff}.smbtn.pu{background:var(--pu);color:#fff}
.smbtn.red{background:#EF5350;color:#fff}.smbtn.og{background:#EF6C00;color:#fff}
.hint{font-size:.64rem;color:#aaa;line-height:1.6;margin-top:5px}

/* ── カードモーダル ── */
.card-mo .box{border-top:5px solid var(--cat-color)}
.cemo2{font-size:2.5rem;text-align:center;margin-bottom:7px}
.csub{font-size:.7rem;color:#bbb;text-align:center;margin-bottom:10px}
.vbox{background:var(--ys);border:1.5px solid var(--yb);border-radius:11px;
  padding:8px 12px;margin-bottom:10px}
.vbox h4{font-size:.69rem;font-weight:900;color:#E65100;margin-bottom:5px}
.vtags{display:flex;flex-wrap:wrap;gap:4px}
.vtag{background:#fff;border:1.5px solid var(--yb);color:#E65100;
  font-size:.62rem;font-weight:700;padding:2px 8px;border-radius:99px}
.mapsec{margin-bottom:10px}
.mapsec-title{font-size:.69rem;font-weight:900;color:#2E7D32;margin-bottom:5px;display:flex;align-items:center;gap:4px}
.maplink{display:flex;align-items:center;gap:6px;padding:7px 12px;border-radius:10px;
  background:linear-gradient(135deg,#34A853,#1B8040);color:#fff;text-decoration:none;
  font-size:.73rem;font-weight:700;margin-bottom:5px;transition:all .18s}
.maplink:hover{transform:translateY(-1px);box-shadow:0 4px 12px rgba(52,168,83,.3)}
.maplink .mi{font-size:.95rem;flex-shrink:0}.maplink .mt{flex:1;text-align:left;line-height:1.3}
.trow{display:flex;gap:6px;margin-bottom:11px}
.tgl{flex:1;padding:7px 3px;border-radius:11px;border:2.5px solid #eee;
  font-family:inherit;font-size:.7rem;font-weight:700;cursor:pointer;
  background:#fafafa;color:#bbb;text-align:center;line-height:1.4;transition:all .15s}
.tgl.on-own{background:var(--cat-color);border-color:var(--cat-border);color:#fff}
.tgl.on-want{background:var(--ys);border-color:var(--yb);color:#E65100}
.tgl.on-trade{background:var(--ts);border-color:var(--t);color:var(--t)}
.forsec{background:#FFF8E1;border:1.5px solid var(--yb);border-radius:11px;
  padding:9px 12px;margin-bottom:10px}
.forsec h4{font-size:.69rem;font-weight:900;color:#E65100;margin-bottom:7px}
.fortags{display:flex;flex-wrap:wrap;gap:5px;margin-bottom:6px}
.ftag{display:flex;align-items:center;gap:4px;padding:4px 10px;border-radius:99px;
  border:2px solid #eee;background:#fff;cursor:pointer;font-family:inherit;
  font-size:.7rem;font-weight:700;color:#aaa;transition:all .15s}
.ftag.on{border-color:var(--y);background:var(--ys);color:#E65100}
.fadd{display:flex;gap:5px;margin-top:4px}
.fadd input{flex:1;padding:5px 10px;border:2px solid #eee;border-radius:9px;
  font-family:inherit;font-size:.75rem;outline:none;transition:border-color .2s;background:#fff}
.fadd input:focus{border-color:var(--y)}
.fadd button{padding:5px 10px;border:none;border-radius:9px;background:var(--y);
  color:#fff;font-family:inherit;font-size:.72rem;font-weight:700;cursor:pointer}

/* ── シェアモーダル ── */
.share-mo .box{border-top:5px solid var(--t)}
.stabs{display:flex;gap:5px;flex-wrap:wrap;margin-bottom:10px}
.stab{padding:4px 10px;border-radius:99px;border:2px solid #eee;background:#f5f5f5;
  color:#aaa;font-family:inherit;font-size:.69rem;font-weight:700;cursor:pointer;transition:all .2s}
.stab.on{background:var(--ts);border-color:var(--t);color:var(--t)}
.spre{font-size:.68rem;background:#f8f8f8;border-radius:9px;padding:10px;
  white-space:pre-wrap;word-break:break-all;max-height:230px;overflow-y:auto;
  font-family:monospace;color:var(--tx);border:1px solid #eee;line-height:1.7}
.cpbtn{margin-top:7px;padding:5px 16px;border-radius:99px;border:none;
  background:var(--t);color:#fff;font-family:inherit;font-size:.72rem;font-weight:700;cursor:pointer}

/* ── 旅行プランナー ── */
.trip-mo .box{border-top:5px solid #43A047}
.trip-steps{display:flex;gap:8px;margin-bottom:12px;font-size:.72rem;color:#888;flex-wrap:wrap}
.trip-step{display:flex;align-items:center;gap:4px}
.trip-step .sn2{width:20px;height:20px;border-radius:50%;background:#43A047;color:#fff;
  font-size:.62rem;font-weight:900;display:flex;align-items:center;justify-content:center;flex-shrink:0}
/* エリア選択グリッド */
.area-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(82px,1fr));gap:5px;margin-bottom:10px}
.abtn{padding:6px 5px;border-radius:10px;border:2px solid #eee;background:#fafafa;
  cursor:pointer;font-family:inherit;font-size:.7rem;font-weight:700;color:#888;
  text-align:center;transition:all .18s;position:relative}
.abtn:hover{border-color:#81C784;background:var(--gs);color:#2E7D32}
.abtn.sel{border-color:#43A047;background:var(--gs);color:#2E7D32;box-shadow:0 0 0 2px rgba(67,160,71,.25)}
.abtn .acnt{font-size:.56rem;display:block;color:#aaa;margin-top:1px}
.abtn.sel .acnt{color:#81C784}
.abtn .acheck{position:absolute;top:3px;right:3px;font-size:.6rem;color:#43A047}
/* 選択中チップ */
.sel-chips{display:flex;flex-wrap:wrap;gap:5px;margin-bottom:10px;min-height:28px;
  background:#f9f9f9;border-radius:10px;padding:6px 8px;border:1.5px solid #eee}
.sel-chip{display:flex;align-items:center;gap:4px;padding:3px 9px;border-radius:99px;
  background:#43A047;color:#fff;font-size:.72rem;font-weight:700}
.sel-chip .sc-x{cursor:pointer;opacity:.7;font-size:.75rem}
.sel-chip .sc-x:hover{opacity:1}
.sel-empty{color:#ccc;font-size:.72rem;align-self:center}
/* 旅行結果 */
.trip-res{background:var(--gs);border-radius:13px;padding:12px;border:1.5px solid var(--gb)}
.trip-res h3{font-size:.82rem;font-weight:900;color:#2E7D32;margin-bottom:8px;display:flex;align-items:center;gap:5px}
.trip-summary{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:10px}
.trip-stat{background:#fff;border-radius:9px;padding:5px 11px;font-size:.7rem;
  font-weight:700;color:#555;border:1px solid #C8E6C9;text-align:center}
.trip-stat span{display:block;font-size:1rem;font-weight:900;color:#2E7D32}
.ttabs{display:flex;gap:5px;margin-bottom:9px;flex-wrap:wrap}
.ttab{padding:4px 11px;border-radius:99px;border:2px solid #eee;background:#fff;
  color:#aaa;font-family:inherit;font-size:.69rem;font-weight:700;cursor:pointer;transition:all .2s}
.ttab.on{background:var(--gs);border-color:#43A047;color:#2E7D32}
.trip-item{display:flex;align-items:center;gap:7px;padding:7px 9px;background:#fff;
  border-radius:10px;margin-bottom:5px;border:1.5px solid #E8F5E9;cursor:pointer;transition:all .15s}
.trip-item:hover{border-color:#81C784;transform:translateX(2px)}
.ti-emo{font-size:1.1rem;min-width:24px;text-align:center}
.ti-info{flex:1}
.ti-name{font-size:.76rem;font-weight:700}
.ti-area{font-size:.59rem;color:#888;margin-top:1px}
.ti-venue{font-size:.59rem;color:#888}
.tistatus{font-size:.61rem;font-weight:700;padding:2px 7px;border-radius:99px;white-space:nowrap}
.tistatus.owned_{background:var(--ps);color:var(--p)}
.tistatus.wanted_{background:var(--ys);color:#E65100}
.tistatus.none_{background:#f5f5f5;color:#bbb}
.trip-mapbtns{margin-top:8px}
.tmapbtn{display:flex;align-items:center;gap:6px;padding:8px 12px;border-radius:10px;
  background:linear-gradient(135deg,#34A853,#1B8040);color:#fff;text-decoration:none;
  font-size:.74rem;font-weight:700;margin-bottom:5px;transition:all .18s;justify-content:center}
.tmapbtn:hover{transform:translateY(-1px);box-shadow:0 4px 12px rgba(52,168,83,.3)}
.friend-list-sec{background:#E8F5E9;border-radius:10px;padding:10px 12px;margin-top:9px;border:1px solid var(--gb)}
.friend-list-sec h4{font-size:.72rem;font-weight:900;color:#2E7D32;margin-bottom:6px}
.friend-row{font-size:.74rem;padding:4px 0;border-bottom:1px solid #C8E6C9}
.friend-row:last-child{border-bottom:none}
.trip-empty{text-align:center;color:#aaa;font-size:.8rem;padding:20px}
.trip-ctrl{display:flex;gap:7px;align-items:center;flex-wrap:wrap;margin-bottom:10px}
.trip-clear{padding:4px 11px;border-radius:99px;border:1.5px solid #ffcdd2;
  background:#fff;color:#E57373;font-family:inherit;font-size:.69rem;font-weight:700;cursor:pointer}

/* ── 設定・管理モーダル ── */
.set-mo .box,.manage-mo .box{border-top:5px solid var(--pu);max-width:450px}
.sec{background:#fafafa;border-radius:12px;padding:11px;margin-bottom:11px;border:1.5px solid #f0f0f0}
.sec h3{font-size:.77rem;font-weight:900;color:var(--br);margin-bottom:9px}
.keyarea{display:flex;gap:7px;align-items:center;flex-wrap:wrap}
.keydis{background:#f0f0f0;border-radius:8px;padding:6px 11px;font-family:monospace;
  font-size:.78rem;word-break:break-all;flex:1;min-width:80px;color:var(--tx)}
.item-search{width:100%;padding:7px 12px;border:2px solid #eee;border-radius:11px;
  font-family:inherit;font-size:.8rem;outline:none;margin-bottom:9px}
.item-search:focus{border-color:var(--pu)}
.ilist{max-height:240px;overflow-y:auto;border:1.5px solid #eee;border-radius:11px;margin-bottom:10px}
.irow{display:flex;align-items:center;gap:6px;padding:7px 9px;border-bottom:1px solid #f5f5f5;flex-wrap:wrap}
.irow:last-child{border-bottom:none}.irow:hover{background:#fafafa}
.ir-emo{font-size:1.1rem;min-width:22px}.ir-area{font-size:.6rem;color:#bbb;font-weight:700;min-width:36px}
.ir-name{font-size:.75rem;font-weight:700;flex:1}
.ir-venue{font-size:.58rem;color:#ccc;max-width:90px;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.ir-e{padding:2px 7px;border-radius:99px;border:1.5px solid #ddd;background:#fff;color:#888;
  font-family:inherit;font-size:.63rem;font-weight:700;cursor:pointer}
.ir-d{padding:2px 7px;border-radius:99px;border:1.5px solid #ffcdd2;background:#fff;
  color:#E57373;font-family:inherit;font-size:.63rem;font-weight:700;cursor:pointer}
.iform{background:#fafafa;border-radius:12px;padding:11px;border:1.5px solid #eee}
.iform h4{font-size:.77rem;font-weight:900;margin-bottom:9px;color:var(--br)}
.frow{display:flex;gap:7px;margin-bottom:7px;flex-wrap:wrap}
.frow input{padding:6px 10px;border:2px solid #eee;border-radius:9px;
  font-family:inherit;font-size:.77rem;outline:none;flex:1;min-width:68px}
.frow input:focus{border-color:var(--pu)}
.vchecks{display:flex;flex-wrap:wrap;gap:5px;margin-bottom:8px}
.vchecks label{display:flex;align-items:center;gap:3px;font-size:.68rem;color:#666;cursor:pointer}
.vchecks input[type=checkbox]{accent-color:var(--t)}
.inote{background:var(--ts);border-radius:8px;padding:7px 11px;font-size:.67rem;
  color:var(--t);margin-top:8px;border:1px solid var(--tb)}

/* ── 初回セットアップ ── */
.setup-mo .box{border-top:5px solid var(--p);text-align:center}
.setup-emo{font-size:3rem;margin-bottom:10px}

/* ── トースト ── */
.toast{position:fixed;bottom:22px;left:50%;transform:translateX(-50%) translateY(60px);
  background:var(--br);color:#fff;padding:8px 22px;border-radius:99px;
  font-size:.79rem;font-weight:700;transition:transform .3s;z-index:500;pointer-events:none}
.toast.show{transform:translateX(-50%) translateY(0)}

/* ── 閲覧モードバナー ── */
.view-banner{background:linear-gradient(135deg,#1565C0,#0D47A1);color:#fff;
  border-radius:14px;padding:11px 16px;margin-bottom:10px;
  display:flex;align-items:center;gap:10px;box-shadow:0 4px 14px rgba(21,101,192,.3)}
.view-banner .vb-icon{font-size:1.5rem;flex-shrink:0}
.view-banner .vb-info{flex:1}
.view-banner .vb-name{font-size:.9rem;font-weight:900}
.view-banner .vb-sub{font-size:.68rem;opacity:.8;margin-top:2px}
.view-banner .vb-back{padding:6px 14px;border-radius:99px;border:2px solid rgba(255,255,255,.5);
  background:rgba(255,255,255,.15);color:#fff;font-family:inherit;
  font-size:.72rem;font-weight:700;cursor:pointer;white-space:nowrap;transition:all .2s}
.view-banner .vb-back:hover{background:rgba(255,255,255,.3)}
.view-mode .card{cursor:default}
.view-mode .card:hover{transform:none;box-shadow:0 2px 9px var(--sh)}
/* 閲覧コード発行セクション */
.viewcode-sec{background:#E3F2FD;border:1.5px solid #90CAF9;border-radius:11px;padding:10px 12px;margin-top:11px}
.viewcode-sec h3{font-size:.77rem;font-weight:900;color:#1565C0;margin-bottom:8px}
.viewcode-area{display:flex;gap:7px;align-items:center;flex-wrap:wrap;margin-bottom:7px}
.viewcode-dis{background:#fff;border:1.5px solid #90CAF9;border-radius:8px;
  padding:6px 11px;font-family:monospace;font-size:.82rem;flex:1;min-width:80px;
  color:#1565C0;font-weight:700;letter-spacing:.08em}
.viewcode-hint{font-size:.64rem;color:#1976D2;line-height:1.6}
.friend-input-sec{margin-top:10px;padding-top:10px;border-top:1px solid #BBDEFB}
.friend-input-sec h3{font-size:.77rem;font-weight:900;color:#1565C0;margin-bottom:8px}

@media(max-width:480px){
  .grid{grid-template-columns:repeat(auto-fill,minmax(94px,1fr))}
  .trow{gap:4px}.tgl{font-size:.65rem;padding:6px 2px}
  .area-grid{grid-template-columns:repeat(auto-fill,minmax(70px,1fr))}
}
</style>
</head>
<body>
<div class="wrap">

<div class="hdr">
  <h1 id="hdr-title">🗝️ ちいかわ ご当地キーホルダー</h1>
  <div class="hdr-sub">
    <span id="item-cnt">全0種類</span>
    <button class="chip dev-chip" id="dev-btn" onclick="openSet()">📱 未設定</button>
    <button class="chip sync-chip off" id="sync-chip" onclick="openSet()">🔒 ローカル</button>
  </div>
</div>

<!-- 閲覧モードバナー（閲覧中のみ表示） -->
<div class="view-banner hide" id="view-banner">
  <span class="vb-icon">👁️</span>
  <div class="vb-info">
    <div class="vb-name" id="vb-name">友達のコレクション</div>
    <div class="vb-sub">読み取り専用で閲覧中です</div>
  </div>
  <button class="vb-back" onclick="exitViewMode()">自分のリストに戻る</button>
</div>

<!-- カテゴリタブ -->
<div class="cat-bar">
  <button class="cat-tab active-key" data-cat="key" onclick="switchCat('key')">
    <span class="cat-emo">🗝️</span> キーホルダー
  </button>
  <button class="cat-tab" data-cat="sock" onclick="switchCat('sock')">
    <span class="cat-emo">🧦</span> 靴下
  </button>
  <button class="cat-tab" data-cat="nuig" onclick="switchCat('nuig')">
    <span class="cat-emo">🧸</span> ぬいぐるみ
  </button>
  <span class="cat-desc" id="cat-desc">カテゴリを切り替えて管理</span>
</div>

<!-- 統計 -->
<div class="stats">
  <div class="si"><span class="sn o" id="s-own">0</span><span class="sl">所持</span></div>
  <div class="si"><span class="sn m" id="s-mis">0</span><span class="sl">未所持</span></div>
  <div class="si"><span class="sn t" id="s-tot">0</span><span class="sl">合計</span></div>
  <div class="prog">
    <div class="prog-bg"><div class="prog-fill" id="pfill" style="width:0%"></div></div>
    <div class="prog-pct" id="ppct">0%</div>
  </div>
</div>

<!-- コントロール -->
<div class="ctrl">
  <button class="filt on" data-f="all">すべて</button>
  <button class="filt" data-f="owned">✅ 持ってる</button>
  <button class="filt" data-f="wanted">⭐ ほしい</button>
  <button class="filt" data-f="trade">🔄 交換用</button>
  <button class="filt" data-f="none">🔲 未所持</button>
  <div class="sw"><input type="text" id="search" placeholder="🔍 検索…"></div>
  <button class="ibtn green" id="trip-btn">🗺️ 旅行プラン</button>
  <button class="ibtn teal" id="share-btn">📋 シェア</button>
  <button class="ibtn purple" id="manage-btn">✏️ 管理</button>
  <button class="ibtn gray" id="set-btn">⚙️</button>
</div>

<div id="cards"></div>
</div>

<!-- ① セットアップ -->
<div class="ov hide setup-mo" id="setup-mo">
  <div class="box">
    <div class="setup-emo">🎀</div>
    <div class="bhdr" style="justify-content:center;border:none;margin-bottom:8px">
      <h2 style="color:var(--p);font-size:1.1rem">ようこそ！</h2>
    </div>
    <p style="font-size:.78rem;color:#888;text-align:center;margin-bottom:16px;line-height:1.7">
      この端末の名前を設定してください。<br>家族で共有するとき「誰の端末か」がわかります。
    </p>
    <div class="field">
      <label>端末名（例：パパ、ママ、自分）</label>
      <input type="text" id="setup-name" placeholder="端末名を入力" maxlength="20">
    </div>
    <button class="btn pri" id="setup-save" style="width:100%">はじめる 🐾</button>
  </div>
</div>

<!-- ② カードモーダル -->
<div class="ov hide card-mo" id="card-mo">
  <div class="box" id="card-box">
    <div class="cemo2" id="cm-emo">🗾</div>
    <div class="bhdr" style="margin-bottom:10px">
      <div><h2 id="cm-name"></h2><div class="csub" id="cm-area"></div></div>
      <button class="xbtn" onclick="close_('card-mo')">✕</button>
    </div>
    <div class="vbox" id="cm-vbox" style="display:none">
      <h4>🛍️ どこで買える？</h4>
      <div class="vtags" id="cm-vtags"></div>
    </div>
    <div class="mapsec" id="cm-mapsec" style="display:none">
      <div class="mapsec-title">🗺️ Google Maps で売り場を探す</div>
      <div id="cm-mapbtns"></div>
    </div>
    <div class="trow">
      <button class="tgl" id="tgl-own" onclick="tog('own')">✅<br><small>持ってる</small></button>
      <button class="tgl" id="tgl-want" onclick="tog('want')">⭐<br><small>ほしい</small></button>
      <button class="tgl" id="tgl-trade" onclick="tog('trade')">🔄<br><small>交換用</small></button>
    </div>
    <div class="forsec">
      <h4>🎁 誰かに買う・買ってもらう</h4>
      <div class="fortags" id="cm-fortags"></div>
      <div class="fadd">
        <input type="text" id="for-inp" placeholder="名前（例：〇〇ちゃん）" maxlength="15">
        <button onclick="addForPerson()">＋追加</button>
      </div>
      <div style="font-size:.61rem;color:#aaa;margin-top:4px">💡 タップでON/OFF・シェアテキストに反映</div>
    </div>
    <div class="field"><label>メモ</label>
      <textarea id="cm-memo" placeholder="入手場所・交換コメントなど"></textarea>
    </div>
    <div class="row">
      <button class="btn pri" id="cm-save">保存する</button>
      <button class="btn sec" onclick="close_('card-mo')">閉じる</button>
    </div>
  </div>
</div>

<!-- ③ 旅行プランナー -->
<div class="ov hide trip-mo" id="trip-mo">
  <div class="box xwide">
    <div class="bhdr">
      <h2>🗺️ 旅行プランナー</h2>
      <button class="xbtn" onclick="close_('trip-mo')">✕</button>
    </div>
    <div class="trip-steps">
      <div class="trip-step"><span class="sn2">1</span>行き先を選ぶ（複数OK）</div>
      <div class="trip-step"><span class="sn2">2</span>買えるものを確認</div>
      <div class="trip-step"><span class="sn2">3</span>Google Mapsで売り場を探す</div>
    </div>
    <!-- 選択中エリアチップ -->
    <div class="sel-chips" id="sel-chips">
      <span class="sel-empty">↓ 下からエリアを選んでください</span>
    </div>
    <div class="trip-ctrl">
      <button class="trip-clear" onclick="clearTripSel()">✕ 選択をクリア</button>
      <div style="font-size:.69rem;color:#aaa">現在のカテゴリ：<b id="trip-cat-label" style="color:var(--g)">キーホルダー</b></div>
    </div>
    <!-- エリア選択グリッド -->
    <div class="area-grid" id="area-grid"></div>
    <!-- 結果 -->
    <div id="trip-result"></div>
  </div>
</div>

<!-- ④ シェアモーダル -->
<div class="ov hide share-mo" id="share-mo">
  <div class="box wide">
    <div class="bhdr">
      <h2>📋 シェア・お土産リスト</h2>
      <button class="xbtn" onclick="close_('share-mo')">✕</button>
    </div>
    <div class="stabs">
      <button class="stab on" data-st="status">📦 所持状況</button>
      <button class="stab" data-st="omiyage">🛍️ お土産リクエスト</button>
      <button class="stab" data-st="trade">🔄 交換リスト</button>
      <button class="stab" data-st="buy4">🎁 誰かに買う</button>
    </div>
    <div class="spre" id="spre"></div>
    <button class="cpbtn" id="cpbtn">📋 コピーする</button>
  </div>
</div>

<!-- ⑤ 設定 -->
<div class="ov hide set-mo" id="set-mo">
  <div class="box set-mo">
    <div class="bhdr"><h2>⚙️ 設定</h2><button class="xbtn" onclick="close_('set-mo')">✕</button></div>
    <div class="sec">
      <h3>📱 この端末の名前</h3>
      <div class="field" style="margin-bottom:7px">
        <input type="text" id="set-devname" placeholder="例：パパ、ママ、自分" maxlength="20">
      </div>
      <button class="smbtn teal" onclick="saveDevName()">保存</button>
    </div>
    <div class="sec">
      <h3>🔗 共有設定</h3>
      <div style="font-size:.72rem;color:#666;line-height:1.8;margin-bottom:9px">
        <b>①</b> このHTMLファイルをLINEなどで家族に送る<br>
        <b>②</b> 「生成」ボタンで共有キーを作成してコピー<br>
        <b>③</b> もう一方の端末で「入力」する<br>
        <b>④</b> 同じキーの端末が同じデータを共有！
      </div>
      <div class="keyarea">
        <div class="keydis" id="key-dis">（未設定）</div>
        <button class="smbtn teal" onclick="genKey()">🔑 生成</button>
        <button class="smbtn pu" onclick="inputKey()">✏️ 入力</button>
        <button class="smbtn red" onclick="clearKey()" id="clr-key" style="display:none">🗑 解除</button>
      </div>
      <div class="hint" id="key-hint">キーを生成か入力してください</div>
    </div>
    <div class="sec">
      <h3>💾 バックアップ</h3>
      <div style="display:flex;gap:7px;flex-wrap:wrap">
        <button class="smbtn teal" onclick="exportData()">📤 書き出し</button>
        <button class="smbtn pu" onclick="importData()">📥 取り込み</button>
        <button class="smbtn red" onclick="resetData()">🗑 リセット</button>
      </div>
      <div class="hint">バックアップを保存しておくと機種変更時に安心です</div>
    </div>

    <!-- 閲覧コード -->
    <div class="viewcode-sec">
      <h3>👁️ 友達とコレクションを見せ合う</h3>
      <div style="font-size:.72rem;color:#1976D2;line-height:1.7;margin-bottom:9px">
        <b>①</b> 「閲覧コード生成」でコードを作りLINEで友達に送る<br>
        <b>②</b> 友達のコードを入力すると読み取り専用で見られる<br>
        <b>③</b> 自分のデータは変わりません
      </div>
      <div style="font-size:.72rem;font-weight:900;color:#1976D2;margin-bottom:5px">📤 自分の閲覧コード</div>
      <div class="viewcode-area">
        <div class="viewcode-dis" id="viewcode-dis">（未発行）</div>
        <button class="smbtn teal" onclick="genViewCode()">🔑 発行</button>
        <button class="smbtn" style="background:#90CAF9;color:#0D47A1" onclick="copyViewCode()" id="copy-viewcode" style="display:none">📋 コピー</button>
        <button class="smbtn red" onclick="clearViewCode()" id="clr-viewcode" style="display:none">🗑 削除</button>
      </div>
      <div class="viewcode-hint" id="viewcode-hint">発行するとコードをLINEなどで友達に送れます</div>
      <div class="friend-input-sec">
        <h3>👥 友達のコードを入力して閲覧</h3>
        <div style="display:flex;gap:7px;align-items:center;flex-wrap:wrap">
          <input type="text" id="friend-code-inp" placeholder="友達の閲覧コードを入力"
            style="flex:1;min-width:120px;padding:7px 11px;border:2px solid #90CAF9;border-radius:10px;
            font-family:inherit;font-size:.8rem;outline:none;text-transform:uppercase;letter-spacing:.05em">
          <button class="smbtn" style="background:#1565C0;color:#fff" onclick="enterViewMode()">👁 閲覧する</button>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- ⑥ キーホルダー管理 -->
<div class="ov hide manage-mo" id="manage-mo">
  <div class="box manage-mo wide">
    <div class="bhdr">
      <h2>✏️ <span id="manage-cat-label">キーホルダー</span>管理 <span id="manage-cnt" style="font-size:.72rem;color:#bbb;font-weight:400"></span></h2>
      <button class="xbtn" onclick="close_('manage-mo')">✕</button>
    </div>
    <input class="item-search" id="iq" placeholder="🔍 検索…" oninput="renderIList()">
    <div class="ilist" id="ilist"></div>
    <div class="iform">
      <h4 id="iform-title">➕ 新しいアイテムを追加</h4>
      <input type="hidden" id="edit-id">
      <div class="frow">
        <input type="text" id="f-emo" placeholder="絵文字" maxlength="2" style="max-width:60px;text-align:center;font-size:1.1rem">
        <input type="text" id="f-area" placeholder="エリア（例：静岡）">
        <input type="text" id="f-name" placeholder="名前（例：桜えび）">
      </div>
      <div style="font-size:.69rem;font-weight:700;color:#888;margin-bottom:5px">🛍️ 買える場所</div>
      <div class="vchecks" id="vchecks"></div>
      <div class="row" style="gap:7px">
        <button class="btn pri" id="iform-save" onclick="saveItem()" style="max-width:150px">追加する</button>
        <button class="btn sec" onclick="cancelEdit()" style="max-width:90px">リセット</button>
      </div>
    </div>
    <div class="inote">💡 新しいご当地グッズが出たら「➕ 追加」で簡単に追記できます。</div>
    <div style="display:flex;gap:7px;margin-top:9px;flex-wrap:wrap">
      <button class="smbtn og" onclick="exportItems()">📤 リスト書き出し</button>
      <button class="smbtn teal" onclick="importItems()">📥 リスト取り込み</button>
    </div>
  </div>
</div>

<div class="toast" id="toast"></div>

<script>
// ══════════════════════════════════════════════
//  定数
// ══════════════════════════════════════════════
const VENUES = {
  sa:'SA・PA', do_:'道の駅', air:'空港', st:'駅・駅ビル',
  obs:'観光地・施設', shop:'おみやげ店', temp:'神社・寺', theme:'テーマパーク'
};

const REGIONS = [
  {l:'🗾 北海道・東北', ar:['北海道','青森','岩手','宮城','秋田','山形','福島']},
  {l:'🗾 関東',         ar:['茨城','栃木','群馬','埼玉','千葉','東京','神奈川']},
  {l:'🗾 中部・北陸',  ar:['新潟','富山','石川','福井','山梨','長野','岐阜','静岡','愛知']},
  {l:'🗾 近畿',         ar:['三重','滋賀','京都','大阪','兵庫','奈良','和歌山']},
  {l:'🗾 中国・四国',  ar:['鳥取','島根','岡山','広島','山口','徳島','香川','愛媛','高知']},
  {l:'🗾 九州・沖縄',  ar:['福岡','佐賀','長崎','熊本','大分','宮崎','鹿児島','沖縄']},
  {l:'🌍 海外・その他', ar:['海外','その他']},
];

// カテゴリ定義
const CATS = {
  key:  { label:'キーホルダー', emo:'🗝️', color:'var(--p)', border:'var(--pb)', bg:'var(--ps)', headGrad:'linear-gradient(90deg,var(--pb),var(--yb),var(--tb),var(--pub),var(--pb))' },
  sock: { label:'靴下',         emo:'🧦', color:'var(--pu)',border:'var(--pub)',bg:'var(--pus)', headGrad:'linear-gradient(90deg,var(--pub),var(--pb),var(--tb),var(--pub))' },
  nuig: { label:'ぬいぐるみ',   emo:'🧸', color:'var(--g)', border:'var(--gb)', bg:'var(--gs)', headGrad:'linear-gradient(90deg,var(--gb),var(--yb),var(--tb),var(--gb))' },
};

const VENUE_QUERIES = {
  sa:'サービスエリア パーキングエリア', do_:'道の駅', air:'空港', st:'駅 みやげ',
  obs:'ちいかわ キーホルダー', shop:'おみやげ 土産店', temp:'神社 寺 みやげ', theme:'テーマパーク',
};

// デフォルトキーホルダーデータ
const DEF_KEY = [
  {id:'h1',a:'北海道',n:'北海道（道内全域）',e:'🏔️',v:['sa','air','shop']},
  {id:'h2',a:'北海道',n:'ラベンダー',e:'💜',v:['sa','air','shop']},
  {id:'h3',a:'北海道',n:'メロン',e:'🍈',v:['sa','air','shop']},
  {id:'h4',a:'北海道',n:'シマエナガ',e:'🐦',v:['sa','air','shop']},
  {id:'h5',a:'北海道',n:'くま',e:'🐻',v:['sa','air','shop']},
  {id:'h6',a:'北海道',n:'小樽運河',e:'⛵',v:['obs','shop']},
  {id:'h7',a:'北海道',n:'さっぽろテレビ塔（札幌限定）',e:'🗼',v:['obs']},
  {id:'h8',a:'北海道',n:'函館の夜景（函館限定）',e:'🌃',v:['obs','shop']},
  {id:'a1',a:'青森',n:'りんご',e:'🍎',v:['sa','shop','st']},
  {id:'a2',a:'青森',n:'ねぶた祭',e:'🎆',v:['shop','obs']},
  {id:'i1',a:'岩手',n:'わんこそば',e:'🍜',v:['shop','sa']},
  {id:'i2',a:'岩手',n:'銀河鉄道',e:'🚂',v:['shop','obs']},
  {id:'m1',a:'宮城',n:'伊達政宗',e:'⚔️',v:['obs','sa','st']},
  {id:'m2',a:'宮城',n:'笹かま',e:'🍢',v:['obs','sa','st']},
  {id:'m3',a:'宮城',n:'こけし',e:'🪆',v:['obs','shop']},
  {id:'ak1',a:'秋田',n:'秋田犬',e:'🐕',v:['shop','do_','st']},
  {id:'ak2',a:'秋田',n:'なまはげ',e:'👹',v:['shop','do_','st']},
  {id:'ak3',a:'秋田',n:'竿燈まつり',e:'🏮',v:['shop','do_','st']},
  {id:'y1',a:'山形',n:'さくらんぼ',e:'🍒',v:['sa','shop','st']},
  {id:'y2',a:'山形',n:'米沢牛',e:'🐄',v:['obs','shop']},
  {id:'y3',a:'山形',n:'花笠まつり',e:'🌺',v:['shop','st']},
  {id:'y4',a:'山形',n:'だだちゃ豆',e:'🫘',v:['shop','sa']},
  {id:'f1',a:'福島',n:'赤べこ',e:'🐮',v:['sa','shop','obs']},
  {id:'f2',a:'福島',n:'ハワイアン',e:'🌺',v:['obs']},
  {id:'f3',a:'福島',n:'白虎隊',e:'🐯',v:['obs','shop']},
  {id:'f4',a:'福島',n:'桃',e:'🍑',v:['sa','shop']},
  {id:'ib1',a:'茨城',n:'黄門様',e:'👴',v:['sa','shop']},
  {id:'ib2',a:'茨城',n:'水戸納豆',e:'🍱',v:['do_','shop']},
  {id:'to1',a:'栃木',n:'スカイベリー',e:'🍓',v:['do_','sa','shop']},
  {id:'to2',a:'栃木',n:'藤の花',e:'🌸',v:['obs','shop']},
  {id:'to3',a:'栃木',n:'三猿',e:'🐒',v:['obs','temp']},
  {id:'to4',a:'栃木',n:'栃木レモン牛乳',e:'🍋',v:['sa','do_']},
  {id:'g1',a:'群馬',n:'草津温泉',e:'♨️',v:['obs','shop']},
  {id:'g2',a:'群馬',n:'だるま',e:'🎎',v:['shop','sa']},
  {id:'g3',a:'群馬',n:'焼きまんじゅう',e:'🍡',v:['shop','obs']},
  {id:'s1',a:'埼玉',n:'さつまいも',e:'🍠',v:['sa','do_','shop']},
  {id:'s2',a:'埼玉',n:'深谷ねぎ',e:'🧅',v:['do_','shop']},
  {id:'c1',a:'千葉',n:'落花生',e:'🥜',v:['sa','shop','st']},
  {id:'c2',a:'千葉',n:'梨（市川市限定）',e:'🍐',v:['shop']},
  {id:'c3',a:'千葉',n:'行徳みこし（市川市限定）',e:'🎊',v:['shop']},
  {id:'tk1',a:'東京',n:'雷門',e:'⛩️',v:['obs','shop','temp']},
  {id:'tk2',a:'東京',n:'東京パンダ',e:'🐼',v:['obs','theme']},
  {id:'tk3',a:'東京',n:'スカイツリー',e:'🗼',v:['obs','shop']},
  {id:'tk4',a:'東京',n:'東京タワー',e:'🗼',v:['obs','shop']},
  {id:'tk5',a:'東京',n:'東京駅丸の内駅舎',e:'🚉',v:['st','shop']},
  {id:'k1',a:'神奈川',n:'箱根温泉まんじゅう',e:'♨️',v:['obs','shop']},
  {id:'k2',a:'神奈川',n:'横浜 金の豚',e:'🐷',v:['obs','shop']},
  {id:'k3',a:'神奈川',n:'鎌倉 大仏さま',e:'🙏',v:['obs','temp']},
  {id:'k4',a:'神奈川',n:'寄木細工',e:'🪵',v:['obs','shop']},
  {id:'k5',a:'神奈川',n:'カンフー（横濱限定）',e:'🥋',v:['obs']},
  {id:'k6',a:'神奈川',n:'黒たまご（大涌谷限定）',e:'🥚',v:['obs']},
  {id:'ni1',a:'新潟',n:'笹団子',e:'🎋',v:['sa','shop','st']},
  {id:'ni2',a:'新潟',n:'トキ',e:'🦢',v:['obs','shop']},
  {id:'ty1',a:'富山',n:'ホタルイカ',e:'🦑',v:['sa','shop','st']},
  {id:'is1',a:'石川',n:'兼六園',e:'🌿',v:['obs','shop']},
  {id:'fi1',a:'福井',n:'恐竜',e:'🦕',v:['obs','shop','sa']},
  {id:'ym1',a:'山梨',n:'ぶどう',e:'🍇',v:['sa','do_','shop']},
  {id:'ym2',a:'山梨',n:'富士山',e:'🗻',v:['obs','sa','shop']},
  {id:'ng1',a:'長野',n:'信州りんご',e:'🍎',v:['sa','shop','st']},
  {id:'ng2',a:'長野',n:'信州オコジョ',e:'🐾',v:['obs','shop']},
  {id:'gi1',a:'岐阜',n:'合掌造り',e:'🏠',v:['obs','shop']},
  {id:'gi2',a:'岐阜',n:'さるぼぼ',e:'🐒',v:['obs','shop','sa']},
  {id:'sz1',a:'静岡',n:'お茶',e:'🍵',v:['sa','shop','st']},
  {id:'sz2',a:'静岡',n:'みかん',e:'🍊',v:['sa','do_','shop']},
  {id:'sz3',a:'静岡',n:'うなぎ',e:'🐟',v:['sa','shop','st']},
  {id:'sz4',a:'静岡',n:'いちご',e:'🍓',v:['sa','do_','shop']},
  {id:'sz5',a:'静岡',n:'次郎長',e:'⚔️',v:['obs','shop']},
  {id:'sz6',a:'静岡',n:'富士山',e:'🗻',v:['obs','sa','shop']},
  {id:'sz7',a:'静岡',n:'桜えび',e:'🦐',v:['sa','shop','st']},
  {id:'ai1',a:'愛知',n:'しゃちほこ',e:'🐟',v:['obs','shop','st']},
  {id:'ai2',a:'愛知',n:'小倉トースト',e:'🍞',v:['shop','st','sa']},
  {id:'mi1',a:'三重',n:'真珠',e:'💎',v:['obs','shop']},
  {id:'mi2',a:'三重',n:'伊勢エビ',e:'🦞',v:['obs','shop','sa']},
  {id:'sg1',a:'滋賀',n:'琵琶湖',e:'🏞️',v:['do_','obs','shop']},
  {id:'sg2',a:'滋賀',n:'彦根城',e:'🏯',v:['obs','shop']},
  {id:'sg3',a:'滋賀',n:'忍者',e:'🥷',v:['obs','shop']},
  {id:'sg4',a:'滋賀',n:'信楽たぬき',e:'🦝',v:['obs','do_','shop']},
  {id:'ky1',a:'京都',n:'八ツ橋',e:'🍡',v:['shop','obs','st']},
  {id:'ky2',a:'京都',n:'新撰組',e:'⚔️',v:['obs','shop']},
  {id:'ky3',a:'京都',n:'伏見稲荷',e:'⛩️',v:['temp','obs']},
  {id:'ky4',a:'京都',n:'抹茶ソフト',e:'🍦',v:['obs','shop']},
  {id:'ky5',a:'京都',n:'金閣寺（金閣寺限定）',e:'🏯',v:['temp']},
  {id:'ky6',a:'京都',n:'ニデック京都タワー',e:'🗼',v:['obs']},
  {id:'os1',a:'大阪',n:'たこ焼き',e:'🐙',v:['sa','shop','st']},
  {id:'os2',a:'大阪',n:'通天閣',e:'🗼',v:['obs','shop']},
  {id:'os3',a:'大阪',n:'大阪のおばちゃん',e:'👩',v:['shop','obs']},
  {id:'os4',a:'大阪',n:'大阪城',e:'🏯',v:['obs','shop']},
  {id:'os5',a:'大阪',n:'ミックスジュース',e:'🥤',v:['shop','obs']},
  {id:'hy1',a:'兵庫',n:'神戸セーラー',e:'⚓',v:['obs','shop']},
  {id:'hy2',a:'兵庫',n:'神戸中華街',e:'🐉',v:['obs','shop']},
  {id:'hy3',a:'兵庫',n:'淡路玉ねぎ',e:'🧅',v:['do_','obs','shop']},
  {id:'hy4',a:'兵庫',n:'神戸ポートタワー',e:'🗼',v:['obs']},
  {id:'hy5',a:'兵庫',n:'姫路千姫',e:'👘',v:['obs','shop']},
  {id:'hy6',a:'兵庫',n:'コウノトリ',e:'🦢',v:['obs','do_']},
  {id:'nr1',a:'奈良',n:'鹿',e:'🦌',v:['obs','shop','temp']},
  {id:'nr2',a:'奈良',n:'大仏',e:'🙏',v:['obs','temp']},
  {id:'wk1',a:'和歌山',n:'パンダ',e:'🐼',v:['obs','shop']},
  {id:'wk2',a:'和歌山',n:'みかん',e:'🍊',v:['sa','do_','shop']},
  {id:'tt1',a:'鳥取',n:'いなばの白うさぎ',e:'🐇',v:['obs','do_','shop']},
  {id:'sm1',a:'島根',n:'縁結び',e:'❤️',v:['obs','temp']},
  {id:'sm2',a:'島根',n:'いなばの白うさぎ',e:'🐇',v:['obs','shop']},
  {id:'ok1',a:'岡山',n:'桃太郎',e:'🍑',v:['shop','obs','st']},
  {id:'ok2',a:'岡山',n:'瀬戸内レモン',e:'🍋',v:['sa','shop','obs']},
  {id:'hr1',a:'広島',n:'もみじ饅頭',e:'🍁',v:['obs','shop','st','sa']},
  {id:'hr2',a:'広島',n:'お好み焼き',e:'🥞',v:['obs','shop','sa']},
  {id:'hr3',a:'広島',n:'宮島の鹿',e:'🦌',v:['obs','temp']},
  {id:'hr4',a:'広島',n:'しゃもじ',e:'🥄',v:['obs','shop']},
  {id:'hr5',a:'広島',n:'尾道ラーメン',e:'🍜',v:['obs','shop']},
  {id:'hr6',a:'広島',n:'瀬戸内レモン',e:'🍋',v:['sa','shop','obs']},
  {id:'yg1',a:'山口',n:'ふく',e:'🐡',v:['obs','shop']},
  {id:'yg2',a:'山口',n:'瀬戸内レモン',e:'🍋',v:['sa','shop']},
  {id:'ts1',a:'徳島',n:'うずしお',e:'🌊',v:['obs','shop']},
  {id:'ts2',a:'徳島',n:'阿波おどり',e:'💃',v:['obs','shop']},
  {id:'kg1',a:'香川',n:'さぬきうどん',e:'🍜',v:['shop','obs','sa']},
  {id:'kg2',a:'香川',n:'瀬戸内レモン',e:'🍋',v:['sa','shop']},
  {id:'eh1',a:'愛媛',n:'みかん',e:'🍊',v:['sa','do_','shop']},
  {id:'eh2',a:'愛媛',n:'道後温泉',e:'♨️',v:['obs','shop']},
  {id:'kc1',a:'高知',n:'坂本龍馬',e:'🗡️',v:['obs','shop']},
  {id:'fk1',a:'福岡',n:'あまおう',e:'🍓',v:['sa','shop','st']},
  {id:'fk2',a:'福岡',n:'明太子',e:'🐟',v:['sa','shop','st','air']},
  {id:'fk3',a:'福岡',n:'とんこつラーメン',e:'🍜',v:['sa','shop','st']},
  {id:'sg5',a:'佐賀',n:'バルーン',e:'🎈',v:['obs','shop']},
  {id:'ns1',a:'長崎',n:'カステラ',e:'🍰',v:['obs','shop','sa']},
  {id:'km1',a:'熊本',n:'熊本城',e:'🏯',v:['obs','shop']},
  {id:'km2',a:'熊本',n:'辛子れんこん',e:'🌶️',v:['shop','sa','obs']},
  {id:'km3',a:'熊本',n:'すいか',e:'🍉',v:['do_','shop']},
  {id:'oi1',a:'大分',n:'温泉（地獄めぐり）',e:'♨️',v:['obs','shop','sa']},
  {id:'mz1',a:'宮崎',n:'マンゴー',e:'🥭',v:['do_','shop','sa']},
  {id:'mz2',a:'宮崎',n:'サーフィン',e:'🏄',v:['obs','shop']},
  {id:'ks1',a:'鹿児島',n:'桜島',e:'🌋',v:['obs','shop']},
  {id:'ok3',a:'沖縄',n:'シーサー',e:'🦁',v:['shop','obs','air']},
  {id:'ok4',a:'沖縄',n:'ジンベイザメ',e:'🦈',v:['obs','shop']},
  {id:'ok5',a:'沖縄',n:'紅芋タルト',e:'🍠',v:['shop','air','obs']},
  {id:'ov1',a:'海外',n:'セントポール大聖堂（マカオ）',e:'⛪',v:['obs']},
  {id:'ov2',a:'海外',n:'エッグタルト（マカオ）',e:'🥧',v:['obs']},
  {id:'ov3',a:'海外',n:'アズレージョ（マカオ）',e:'🎨',v:['obs']},
  {id:'ov4',a:'海外',n:'エッグワッフル（香港）',e:'🧇',v:['obs']},
  {id:'ov5',a:'海外',n:'ビクトリアハーバー（香港）',e:'🌃',v:['obs']},
  {id:'ov6',a:'海外',n:'カンフー（香港）',e:'🥋',v:['obs']},
  {id:'ov7',a:'海外',n:'コアラ（オーストラリア）',e:'🐨',v:['obs']},
  {id:'ov8',a:'海外',n:'カンガルー（オーストラリア）',e:'🦘',v:['obs']},
  {id:'ot1',a:'その他',n:'温泉地',e:'♨️',v:['obs','sa']},
  {id:'ot2',a:'その他',n:'スキー',e:'⛷️',v:['obs','sa']},
  {id:'ot3',a:'その他',n:'スノボー',e:'🏂',v:['obs','sa']},
  {id:'ot4',a:'その他',n:'はやぶさ（新幹線）',e:'🚅',v:['st','shop']},
  {id:'ot5',a:'その他',n:'E7系（新幹線）',e:'🚅',v:['st','shop']},
  {id:'ot6',a:'その他',n:'N700S（新幹線）',e:'🚅',v:['st','shop']},
  {id:'ot7',a:'その他',n:'ドクターイエロー（新幹線）',e:'🚅',v:['st','shop']},
  {id:'ot8',a:'その他',n:'パイロット（空港限定）',e:'✈️',v:['air']},
  {id:'ot9',a:'その他',n:'ちいかわらんどTOKYO Station（1周年限定）',e:'🎂',v:['st']},
];

// 靴下デフォルト（主要エリアのみ初期収録・追加可能）
const DEF_SOCK = [
  // ─── 全国共通 ───
  {id:'sk_onsen',a:'その他',n:'温泉地限定（全国のお土産コーナー）',e:'♨️',v:['obs','sa','shop']},
  // ─── 北海道・東北 ───
  {id:'sk_hk1',a:'北海道',n:'北海道（地図柄）',e:'🗾',v:['sa','air','shop']},
  {id:'sk_hk2',a:'北海道',n:'ラベンダー',e:'💜',v:['sa','air','shop']},
  {id:'sk_hk3',a:'北海道',n:'シマエナガ',e:'🐦',v:['sa','air','shop']},
  {id:'sk_hk4',a:'北海道',n:'メロン',e:'🍈',v:['sa','air','shop']},
  {id:'sk_iw1',a:'岩手',n:'わんこそば',e:'🍜',v:['shop','sa']},
  {id:'sk_my1',a:'宮城',n:'伊達政宗',e:'⚔️',v:['obs','sa','st']},
  {id:'sk_my2',a:'宮城',n:'笹かま',e:'🍢',v:['obs','sa','st']},
  {id:'sk_my3',a:'宮城',n:'こけし',e:'🪆',v:['obs','shop']},
  {id:'sk_fk1',a:'福島',n:'赤べこ',e:'🐮',v:['sa','shop','obs']},
  {id:'sk_fk2',a:'福島',n:'ハワイアン（スパリゾートハワイアンズ）',e:'🌺',v:['obs']},
  {id:'sk_ak1',a:'秋田',n:'秋田犬',e:'🐕',v:['shop','do_','st']},
  {id:'sk_yg1',a:'山形',n:'さくらんぼ',e:'🍒',v:['sa','shop','st']},
  // ─── 関東 ───
  {id:'sk_tc1',a:'栃木',n:'スカイベリー（いちご）',e:'🍓',v:['do_','sa','shop']},
  {id:'sk_ib1',a:'茨城',n:'黄門様',e:'👴',v:['sa','shop']},
  {id:'sk_sa1',a:'埼玉',n:'深谷ねぎ',e:'🧅',v:['do_','shop','sa']},
  {id:'sk_sa2',a:'埼玉',n:'さつまいも',e:'🍠',v:['sa','do_','shop']},
  {id:'sk_tk1',a:'東京',n:'東京タワー',e:'🗼',v:['obs','shop']},
  {id:'sk_tk2',a:'東京',n:'スカイツリー',e:'🗼',v:['obs','shop']},
  {id:'sk_tk3',a:'東京',n:'雷門（浅草）',e:'⛩️',v:['obs','shop','temp']},
  {id:'sk_tk4',a:'東京',n:'パンダ（上野）',e:'🐼',v:['obs','theme']},
  {id:'sk_kn1',a:'神奈川',n:'黒たまご（大涌谷限定）',e:'🥚',v:['obs']},
  {id:'sk_kn2',a:'神奈川',n:'箱根温泉まんじゅう',e:'♨️',v:['obs','shop']},
  {id:'sk_kn3',a:'神奈川',n:'鎌倉 大仏さま',e:'🙏',v:['obs','temp']},
  {id:'sk_kn4',a:'神奈川',n:'神戸 中華街',e:'🐉',v:['obs','shop']},
  {id:'sk_gn1',a:'群馬',n:'だるま',e:'🎎',v:['shop','sa']},
  {id:'sk_gn2',a:'群馬',n:'草津温泉',e:'♨️',v:['obs','shop']},
  {id:'sk_gn3',a:'群馬',n:'焼きまんじゅう',e:'🍡',v:['shop','obs']},
  // ─── 中部・北陸 ───
  {id:'sk_sz1',a:'静岡',n:'みかん',e:'🍊',v:['sa','do_','shop']},
  {id:'sk_sz2',a:'静岡',n:'うなぎ',e:'🐟',v:['sa','shop','st']},
  {id:'sk_sz3',a:'静岡',n:'お茶',e:'🍵',v:['sa','shop','st']},
  {id:'sk_sz4',a:'静岡',n:'いちご',e:'🍓',v:['sa','do_','shop']},
  {id:'sk_sz5',a:'静岡',n:'富士山',e:'🗻',v:['obs','sa','shop']},
  {id:'sk_ni1',a:'新潟',n:'笹団子',e:'🎋',v:['sa','shop','st']},
  {id:'sk_ng1',a:'長野',n:'信州りんご',e:'🍎',v:['sa','shop','st']},
  {id:'sk_gi1',a:'岐阜',n:'さるぼぼ',e:'🐒',v:['obs','shop','sa']},
  {id:'sk_ty1',a:'富山',n:'ほたるいか',e:'🦑',v:['sa','shop','st']},
  {id:'sk_is1',a:'石川',n:'兼六園',e:'🌿',v:['obs','shop']},
  {id:'sk_fi1',a:'福井',n:'恐竜',e:'🦕',v:['obs','shop','sa']},
  {id:'sk_ai1',a:'愛知',n:'しゃちほこ（名古屋）',e:'🐟',v:['obs','shop','st']},
  // ─── 近畿 ───
  {id:'sk_ky1',a:'京都',n:'八ツ橋',e:'🍡',v:['shop','obs','st']},
  {id:'sk_ky2',a:'京都',n:'伏見稲荷',e:'⛩️',v:['temp','obs']},
  {id:'sk_ky3',a:'京都',n:'新選組',e:'⚔️',v:['obs','shop']},
  {id:'sk_ky4',a:'京都',n:'抹茶ソフト',e:'🍦',v:['obs','shop']},
  {id:'sk_ky5',a:'京都',n:'金閣寺（金閣寺限定）',e:'🏯',v:['temp']},
  {id:'sk_ky6',a:'京都',n:'舞妓',e:'👘',v:['obs','shop']},
  {id:'sk_hy1',a:'兵庫',n:'神戸 中華街',e:'🐉',v:['obs','shop']},
  {id:'sk_nr1',a:'奈良',n:'鹿',e:'🦌',v:['obs','shop','temp']},
  {id:'sk_wk1',a:'和歌山',n:'みかん',e:'🍊',v:['sa','do_','shop']},
  // ─── 中国・四国 ───
  {id:'sk_ok1',a:'岡山',n:'桃太郎',e:'🍑',v:['shop','obs','st']},
  {id:'sk_hr1',a:'広島',n:'もみじ饅頭',e:'🍁',v:['obs','shop','st','sa']},
  {id:'sk_hr2',a:'広島',n:'宮島の鹿',e:'🦌',v:['obs','temp']},
  {id:'sk_kg1',a:'香川',n:'さぬきうどん',e:'🍜',v:['shop','obs','sa']},
  // ─── 九州・沖縄 ───
  {id:'sk_fk3',a:'福岡',n:'あまおう',e:'🍓',v:['sa','shop','st']},
  {id:'sk_fk4',a:'福岡',n:'明太子',e:'🐟',v:['sa','shop','st','air']},
  {id:'sk_fk5',a:'福岡',n:'とんこつラーメン',e:'🍜',v:['sa','shop','st']},
  {id:'sk_sg1',a:'佐賀',n:'バルーン',e:'🎈',v:['obs','shop']},
  {id:'sk_km1',a:'熊本',n:'熊本城',e:'🏯',v:['obs','shop']},
  {id:'sk_mz1',a:'宮崎',n:'マンゴー',e:'🥭',v:['do_','shop','sa']},
  {id:'sk_ks1',a:'鹿児島',n:'桜島',e:'🌋',v:['obs','shop']},
  {id:'sk_ks2',a:'鹿児島',n:'黒豚',e:'🐷',v:['shop','sa']},
  {id:'sk_ks3',a:'鹿児島',n:'氷しろくま',e:'🍧',v:['shop','sa']},
  {id:'sk_ok2',a:'沖縄',n:'シーサー',e:'🦁',v:['shop','obs','air']},
  {id:'sk_ok3',a:'沖縄',n:'ジンベイザメ',e:'🦈',v:['obs','shop']},
  // ─── 海外 ───
  {id:'sk_mc1',a:'海外',n:'セントポール大聖堂（マカオ）',e:'⛪',v:['obs']},
  {id:'sk_mc2',a:'海外',n:'エッグタルト（マカオ）',e:'🥧',v:['obs']},
];

// ぬいぐるみ（マスコットキーチェーン）デフォルト
// ※各キャラ（ちいかわ・ハチワレ・うさぎ）が存在するものをまとめて管理
const DEF_NUIG = [
  // ─── 北海道・東北 ───
  {id:'nu_hk1',a:'北海道',n:'北海道（ちいかわ）',e:'🐻',v:['sa','air','shop']},
  {id:'nu_hk2',a:'北海道',n:'北海道（ハチワレ）',e:'🐻',v:['sa','air','shop']},
  {id:'nu_hk3',a:'北海道',n:'北海道（うさぎ）',e:'🐰',v:['sa','air','shop']},
  {id:'nu_hk4',a:'北海道',n:'メロン（ちいかわ）',e:'🍈',v:['sa','air','shop']},
  {id:'nu_hk5',a:'北海道',n:'メロン（ハチワレ）',e:'🍈',v:['sa','air','shop']},
  {id:'nu_hk6',a:'北海道',n:'メロン（うさぎ）',e:'🍈',v:['sa','air','shop']},
  {id:'nu_hk7',a:'北海道',n:'ラベンダー（うさぎ）',e:'💜',v:['sa','air','shop']},
  {id:'nu_iw1',a:'岩手',n:'わんこそば（ちいかわ）',e:'🍜',v:['shop','sa']},
  {id:'nu_ak1',a:'秋田',n:'秋田犬（ハチワレ）',e:'🐕',v:['shop','do_','st']},
  // ─── 関東 ───
  {id:'nu_tc1',a:'栃木',n:'藤の花・足利（ちいかわ）',e:'🌸',v:['obs','shop']},
  {id:'nu_tc2',a:'栃木',n:'藤の花・足利（ハチワレ）',e:'🌸',v:['obs','shop']},
  {id:'nu_sa1',a:'埼玉',n:'深谷ねぎ（ちいかわ）',e:'🧅',v:['do_','shop','sa']},
  {id:'nu_sa2',a:'埼玉',n:'深谷ねぎ（ハチワレ）',e:'🧅',v:['do_','shop','sa']},
  {id:'nu_sa3',a:'埼玉',n:'深谷ねぎ（うさぎ）',e:'🧅',v:['do_','shop','sa']},
  {id:'nu_tk1',a:'東京',n:'東京タワー（ちいかわ）',e:'🗼',v:['obs','shop']},
  {id:'nu_tk2',a:'東京',n:'東京タワー（ハチワレ）',e:'🗼',v:['obs','shop']},
  {id:'nu_tk3',a:'東京',n:'東京タワー（うさぎ）',e:'🗼',v:['obs','shop']},
  // ─── 中部・北陸 ───
  {id:'nu_gi1',a:'岐阜',n:'さるぼぼ（ちいかわ）',e:'🐒',v:['obs','shop','sa']},
  {id:'nu_ty1',a:'富山',n:'ほたるいか（ハチワレ）',e:'🦑',v:['sa','shop','st']},
  {id:'nu_sz1',a:'静岡',n:'みかん（ちいかわ）',e:'🍊',v:['sa','do_','shop']},
  {id:'nu_sz2',a:'静岡',n:'みかん（ハチワレ）',e:'🍊',v:['sa','do_','shop']},
  {id:'nu_sz3',a:'静岡',n:'みかん（うさぎ）',e:'🍊',v:['sa','do_','shop']},
  // ─── 近畿 ───
  {id:'nu_ky1',a:'京都',n:'八ツ橋（ハチワレ）',e:'🍡',v:['shop','obs','st']},
  {id:'nu_ky2',a:'京都',n:'伏見稲荷（ちいかわ）',e:'⛩️',v:['temp','obs']},
  {id:'nu_ky3',a:'京都',n:'伏見稲荷（ハチワレ）',e:'⛩️',v:['temp','obs']},
  {id:'nu_ky4',a:'京都',n:'新選組（ちいかわ）',e:'⚔️',v:['obs','shop']},
  {id:'nu_ky5',a:'京都',n:'抹茶ソフト（ちいかわ）',e:'🍦',v:['obs','shop']},
  {id:'nu_ky6',a:'京都',n:'舞妓（ちいかわ）',e:'👘',v:['obs','shop']},
  {id:'nu_sg1',a:'滋賀',n:'信楽たぬき（ちいかわ）',e:'🦝',v:['obs','do_','shop']},
  {id:'nu_sg2',a:'滋賀',n:'信楽たぬき（ハチワレ）',e:'🦝',v:['obs','do_','shop']},
  {id:'nu_sg3',a:'滋賀',n:'信楽たぬき（うさぎ）',e:'🦝',v:['obs','do_','shop']},
  {id:'nu_sg4',a:'滋賀',n:'忍者（ちいかわ）',e:'🥷',v:['obs','shop']},
  {id:'nu_sg5',a:'滋賀',n:'忍者（ハチワレ）',e:'🥷',v:['obs','shop']},
  {id:'nu_sg6',a:'滋賀',n:'忍者（うさぎ）',e:'🥷',v:['obs','shop']},
  {id:'nu_nr1',a:'奈良',n:'鹿（ちいかわ）',e:'🦌',v:['obs','shop','temp']},
  {id:'nu_nr2',a:'奈良',n:'鹿（うさぎ）',e:'🦌',v:['obs','shop','temp']},
  // ─── 九州 ───
  {id:'nu_mz1',a:'宮崎',n:'マンゴー（ちいかわ）',e:'🥭',v:['do_','shop','sa']},
  // ─── 海外 ───
  {id:'nu_mc1',a:'海外',n:'エッグタルト（ちいかわ/マカオ）',e:'🥧',v:['obs']},
  {id:'nu_mc2',a:'海外',n:'エッグタルト（ハチワレ/マカオ）',e:'🥧',v:['obs']},
  {id:'nu_mc3',a:'海外',n:'エッグタルト（うさぎ/マカオ）',e:'🥧',v:['obs']},
];

const DEF_BY_CAT = { key: DEF_KEY, sock: DEF_SOCK, nuig: DEF_NUIG };

// ══════════════════════════════════════════════
//  状態変数
// ══════════════════════════════════════════════
const LS = {
  g:(k,d)=>{ try{ const v=localStorage.getItem(k); return v!=null?JSON.parse(v):d }catch{return d} },
  s:(k,v)=>{ try{localStorage.setItem(k,JSON.stringify(v))}catch{} }
};

let cat = 'key';       // 現在のカテゴリ
let ITEMS = [];        // 現在カテゴリのアイテムリスト
let COLL = {};         // 現在カテゴリのコレクション {itemId:{owned,want,trade,memo,forPeople}}
let devName = '';
let shareKey = '';
let viewCode = '';     // 自分の閲覧コード（読み取り専用発行用）
let viewMode = false;  // 友達のリストを閲覧中か
let viewFriendCode = '';  // 閲覧中の友達コード
let viewFriendName = '';  // 閲覧中の友達名
let myBackupCOLL = {}; // 閲覧モード中に自分のデータを退避
let filterMode = 'all';
let searchQ = '';
let curItem = null, curState = {};
let editingId = null;
let tripSel = new Set();
let tripTab = 'want';

function getItems(c){ return LS.g('ck_items_'+c, null) || JSON.parse(JSON.stringify(DEF_BY_CAT[c])); }
function setItems(c, d){ LS.s('ck_items_'+c, d); }
function getColl(c){ return LS.g('ck_coll_'+c, {}); }
function setColl(c, d){ LS.s('ck_coll_'+c, d); }
function getS(id){ return COLL[id] || {owned:false,want:false,trade:false,memo:'',forPeople:{}}; }

// ══════════════════════════════════════════════
//  初期化・共有
// ══════════════════════════════════════════════
async function init() {
  devName  = LS.g('ck_devname','');
  shareKey = LS.g('ck_sharekey','');
  viewCode = LS.g('ck_viewcode','');
  if (!devName) { open_('setup-mo'); return; }
  await loadCat(cat);
}

async function loadCat(c) {
  cat = c;
  ITEMS = getItems(c);
  if (shareKey) {
    try {
      const r = await window.storage.get('ck_shared_'+shareKey+'_'+c, true);
      COLL = r ? JSON.parse(r.value) : getColl(c);
    } catch { COLL = getColl(c); }
  } else {
    COLL = getColl(c);
  }
  renderAll();
}

async function saveColl() {
  if (shareKey) {
    try {
      await window.storage.set('ck_shared_'+shareKey+'_'+cat, JSON.stringify(COLL), true);
    } catch { toast('⚠️ 同期失敗。ローカルに保存'); }
  }
  setColl(cat, COLL);
  // 閲覧コードがあれば最新データを自動反映
  if (viewCode) await pushMyDataForView();
}

// ══════════════════════════════════════════════
//  カテゴリ切り替え
// ══════════════════════════════════════════════
function switchCat(c) {
  if (viewMode) { loadViewCat(c); } else { loadCat(c); }
  // タブ見た目
  document.querySelectorAll('.cat-tab').forEach(b => {
    b.className = 'cat-tab' + (b.dataset.cat === c ? ' active-'+c : '');
  });
  // CSS変数切り替え
  const ct = CATS[c];
  const root = document.documentElement.style;
  root.setProperty('--cat-color', ct.color);
  root.setProperty('--cat-border', ct.border);
  root.setProperty('--cat-bg', ct.bg);
  // ヘッダー
  document.getElementById('hdr-title').textContent = ct.emo + ' ちいかわ ご当地' + ct.label;
  document.getElementById('cat-desc').textContent = `${ct.emo} ${ct.label}のコレクション`;
  document.querySelector('.hdr').style.borderColor = ct.border;
  document.querySelector('.hdr::after') // CSS変数で自動反映
  document.getElementById('trip-cat-label').textContent = ct.label;
  document.getElementById('manage-cat-label').textContent = ct.label;
  // フィルターのactiveクラスもリセット
  document.querySelectorAll('.filt').forEach(b => b.classList.toggle('on', b.dataset.f === filterMode));
}

// ══════════════════════════════════════════════
//  レンダリング
// ══════════════════════════════════════════════
function renderAll() {
  updateHeader();
  renderCards();
  updateStats();
}

function updateHeader() {
  const c = CATS[cat];
  document.getElementById('item-cnt').textContent = '全'+ITEMS.length+'種類';
  document.getElementById('dev-btn').textContent = '📱 '+(devName||'未設定');
  const sc = document.getElementById('sync-chip');
  sc.textContent = shareKey ? '🔗 共有中' : '🔒 ローカル';
  sc.className = 'chip sync-chip '+(shareKey?'on':'off');

  // 閲覧バナー
  const banner = document.getElementById('view-banner');
  if (viewMode) {
    banner.classList.remove('hide');
    document.getElementById('vb-name').textContent = viewFriendName
      ? `👤 ${viewFriendName} のコレクション` : '友達のコレクション';
    // 編集系ボタンを隠す
    document.getElementById('share-btn').style.display = 'none';
    document.getElementById('manage-btn').style.display = 'none';
    document.getElementById('set-btn').style.display = 'none';
    document.querySelector('.wrap').classList.add('view-mode');
  } else {
    banner.classList.add('hide');
    document.getElementById('share-btn').style.display = '';
    document.getElementById('manage-btn').style.display = '';
    document.getElementById('set-btn').style.display = '';
    document.querySelector('.wrap').classList.remove('view-mode');
  }
}

function getS_(id){ return COLL[id]||{owned:false,want:false,trade:false,memo:'',forPeople:{}}; }

function renderCards() {
  const cont = document.getElementById('cards');
  cont.innerHTML = '';
  let delay = 0;
  REGIONS.forEach(r => {
    const items = ITEMS.filter(x => r.ar.includes(x.a));
    if (!items.length) return;
    const sec = document.createElement('div'); sec.className = 'region';
    sec.innerHTML = `<div class="rlabel">${r.l}</div>`;
    const grid = document.createElement('div'); grid.className = 'grid';
    items.forEach(item => {
      const s = getS_(item.id);
      let cls = 'card';
      if (s.owned) cls += ' owned '+(cat==='sock'?'sock':cat==='nuig'?'nuig':'');
      else if (s.want) cls += ' wanted';
      else cls += ' none';
      if (s.trade) cls += ' trade';
      const card = document.createElement('div');
      card.className = cls.trim();
      card.dataset.id = item.id; card.dataset.a = item.a; card.dataset.n = item.n;
      card.style.animationDelay = (delay++ * 0.011) + 's';
      const vShort = (item.v||[]).slice(0,2).map(k=>VENUES[k]||k).join('・');
      const fp = s.forPeople||{};
      const forBadge = Object.values(fp).some(v=>v) ? '<span class="badgetag wt">🎁</span>' : '';
      card.innerHTML =
        (s.owned ? `<span class="badgeown">✓</span>` : '') +
        (s.trade ? `<span class="badgetag tr">交換</span>` :
          s.want&&!s.owned ? `<span class="badgetag wt">ほしい</span>` : '') +
        forBadge +
        `<span class="cemo">${item.e}</span>` +
        `<div class="carea">${item.a}</div>` +
        `<div class="cname">${item.n}</div>` +
        (vShort ? `<div class="cvenue">${vShort}</div>` : '');
      card.addEventListener('click', () => { if (!viewMode) openCard(item); });
      grid.appendChild(card);
    });
    sec.appendChild(grid); cont.appendChild(sec);
  });
  applyFilter();
}

function updateStats() {
  const total = ITEMS.length;
  const owned = ITEMS.filter(i => getS_(i.id).owned).length;
  const pct = total ? Math.round(owned/total*100) : 0;
  document.getElementById('s-own').textContent = owned;
  document.getElementById('s-mis').textContent = total-owned;
  document.getElementById('s-tot').textContent = total;
  document.getElementById('pfill').style.width = pct+'%';
  document.getElementById('ppct').textContent = pct+'%';
}

// フィルター
document.querySelectorAll('.filt').forEach(b => {
  b.addEventListener('click', () => {
    document.querySelectorAll('.filt').forEach(x=>x.classList.remove('on'));
    b.classList.add('on'); filterMode=b.dataset.f; applyFilter();
  });
});
document.getElementById('search').addEventListener('input', e => { searchQ=e.target.value.toLowerCase(); applyFilter(); });

function applyFilter() {
  document.querySelectorAll('.card').forEach(c => {
    const s = getS_(c.dataset.id);
    const mQ = !searchQ || (c.dataset.n+c.dataset.a).toLowerCase().includes(searchQ);
    let mF = true;
    if(filterMode==='owned')  mF = s.owned;
    if(filterMode==='wanted') mF = s.want&&!s.owned;
    if(filterMode==='trade')  mF = s.trade;
    if(filterMode==='none')   mF = !s.owned&&!s.want;
    c.classList.toggle('hidden', !mQ||!mF);
  });
  document.querySelectorAll('.region').forEach(r => {
    r.style.display = [...r.querySelectorAll('.card')].some(c=>!c.classList.contains('hidden')) ? '' : 'none';
  });
}

// ══════════════════════════════════════════════
//  カードモーダル
// ══════════════════════════════════════════════
function mapsUrl(area, vk) {
  const q = encodeURIComponent(area+' '+(VENUE_QUERIES[vk]||VENUES[vk]||vk)+' ちいかわ');
  return `https://www.google.com/maps/search/${q}`;
}

function openCard(item) {
  curItem = item;
  curState = JSON.parse(JSON.stringify(getS_(item.id)));
  if (!curState.forPeople) curState.forPeople = {};
  document.getElementById('cm-emo').textContent = item.e;
  document.getElementById('cm-name').textContent = item.n;
  document.getElementById('cm-area').textContent = '📍 '+item.a;
  document.getElementById('cm-memo').value = curState.memo||'';
  // 販売場所
  const vb = document.getElementById('cm-vbox');
  if (item.v&&item.v.length) {
    document.getElementById('cm-vtags').innerHTML = item.v.map(k=>`<span class="vtag">${VENUES[k]||k}</span>`).join('');
    vb.style.display='block';
  } else vb.style.display='none';
  // Google Mapsリンク（未所持のとき）
  const ms = document.getElementById('cm-mapsec');
  if (item.v&&item.v.length&&!curState.owned) {
    document.getElementById('cm-mapbtns').innerHTML = item.v.map(k =>
      `<a class="maplink" href="${mapsUrl(item.a,k)}" target="_blank" rel="noopener">
        <span class="mi">📍</span>
        <span class="mt">${item.a} の ${VENUES[k]||k} を地図で探す</span>→
      </a>`).join('');
    ms.style.display='block';
  } else ms.style.display='none';
  // 誰かに買う
  renderForTags();
  syncTgls();
  open_('card-mo');
}

function syncTgls() {
  document.getElementById('tgl-own').className = 'tgl'+(curState.owned?' on-own':'');
  document.getElementById('tgl-want').className = 'tgl'+(curState.want&&!curState.owned?' on-want':'');
  document.getElementById('tgl-trade').className = 'tgl'+(curState.trade?' on-trade':'');
}
function tog(t) {
  if(t==='own'){curState.owned=!curState.owned;if(!curState.owned)curState.trade=false;if(curState.owned)curState.want=false;}
  else if(t==='want'){curState.want=!curState.want;if(curState.want)curState.owned=false;}
  else if(t==='trade'){curState.trade=!curState.trade;if(curState.trade){curState.owned=true;curState.want=false;}}
  syncTgls();
  // 所持になったらマップリンク非表示
  document.getElementById('cm-mapsec').style.display = (!curState.owned&&curItem.v&&curItem.v.length)?'block':'none';
}

function renderForTags() {
  const fp = curState.forPeople||{};
  const kp = LS.g('ck_people',[]);
  const all = [...new Set([...kp,...Object.keys(fp)])];
  document.getElementById('cm-fortags').innerHTML = all.map(name =>
    `<button class="ftag ${fp[name]?'on':''}" onclick="toggleFor('${name}')">
      ${fp[name]?'🛒':'👤'} ${name}
    </button>`).join('');
}
function toggleFor(name) {
  if(!curState.forPeople) curState.forPeople={};
  curState.forPeople[name]=!curState.forPeople[name];
  renderForTags();
}
function addForPerson() {
  const inp=document.getElementById('for-inp');
  const name=inp.value.trim(); if(!name)return; inp.value='';
  const kp=LS.g('ck_people',[]); if(!kp.includes(name)){kp.push(name);LS.s('ck_people',kp);}
  if(!curState.forPeople)curState.forPeople={};
  curState.forPeople[name]=true; renderForTags();
}

document.getElementById('cm-save').addEventListener('click', async () => {
  curState.memo = document.getElementById('cm-memo').value;
  COLL[curItem.id] = curState;
  await saveColl();
  close_('card-mo'); renderCards(); updateStats(); toast('保存しました！');
});

// ══════════════════════════════════════════════
//  旅行プランナー（複数エリア選択）
// ══════════════════════════════════════════════
document.getElementById('trip-btn').addEventListener('click', () => {
  document.getElementById('trip-cat-label').textContent = CATS[cat].label;
  buildAreaGrid(); renderSelChips(); renderTripResult();
  open_('trip-mo');
});

function buildAreaGrid() {
  const areas = [...new Set(ITEMS.filter(i=>i.a!=='その他').map(i=>i.a))];
  document.getElementById('area-grid').innerHTML = areas.map(area => {
    const wantCnt = ITEMS.filter(i=>i.a===area&&getS_(i.id).want&&!getS_(i.id).owned).length;
    const noneCnt = ITEMS.filter(i=>i.a===area&&!getS_(i.id).owned).length;
    const isSel = tripSel.has(area);
    return `<button class="abtn ${isSel?'sel':''}" onclick="toggleArea('${area}')" data-area="${area}">
      ${isSel?'<span class="acheck">✓</span>':''}
      ${area}
      <span class="acnt">${wantCnt?'⭐'+wantCnt+' ':''}未${noneCnt}</span>
    </button>`;
  }).join('');
}

function toggleArea(area) {
  if(tripSel.has(area)) tripSel.delete(area); else tripSel.add(area);
  buildAreaGrid(); renderSelChips(); renderTripResult();
}

function clearTripSel() { tripSel.clear(); buildAreaGrid(); renderSelChips(); renderTripResult(); }

function renderSelChips() {
  const cont = document.getElementById('sel-chips');
  if(tripSel.size===0){
    cont.innerHTML='<span class="sel-empty">↓ 下からエリアを選んでください（複数OK）</span>'; return;
  }
  cont.innerHTML = [...tripSel].map(area =>
    `<span class="sel-chip">${area}<span class="sc-x" onclick="toggleArea('${area}')">✕</span></span>`
  ).join('');
}

function renderTripResult() {
  const cont = document.getElementById('trip-result');
  if(tripSel.size===0){ cont.innerHTML=''; return; }

  const areas = [...tripSel];
  // 選択エリアの全アイテム
  const allItems = ITEMS.filter(i=>areas.includes(i.a));
  const owned_ = allItems.filter(i=>getS_(i.id).owned);
  const wanted_ = allItems.filter(i=>getS_(i.id).want&&!getS_(i.id).owned);
  const none_ = allItems.filter(i=>!getS_(i.id).owned&&!getS_(i.id).want);
  const forFriend_ = allItems.filter(i=>{const fp=getS_(i.id).forPeople||{};return Object.values(fp).some(v=>v);});

  const showItems = tripTab==='want' ? [...wanted_,...none_] :
                    tripTab==='friend' ? forFriend_ : allItems;

  // 全選択エリアのマップリンク（エリア×販売場所の組み合わせ）
  const venueMap = {}; // {area: Set(vk)}
  allItems.forEach(i=>{
    if(!venueMap[i.a]) venueMap[i.a]=new Set();
    (i.v||[]).forEach(vk=>venueMap[i.a].add(vk));
  });

  const catLabel = CATS[cat].label;

  const mapLinks = areas.map(area => {
    if(!venueMap[area]) return '';
    return [...venueMap[area]].map(vk =>
      `<a class="tmapbtn" href="${mapsUrl(area,vk)}" target="_blank" rel="noopener">
        🗺️ ${area} の ${VENUES[vk]||vk} でちいかわ${catLabel}を探す →
      </a>`
    ).join('');
  }).join('');

  const friendSection = forFriend_.length ? `
    <div class="friend-list-sec">
      <h4>🎁 この旅行で買う予定（友達・家族へ）</h4>
      ${forFriend_.map(i=>{
        const fp=getS_(i.id).forPeople||{};
        const who=Object.entries(fp).filter(([,v])=>v).map(([k])=>k).join('、');
        return `<div class="friend-row">${i.e} <b>${i.a}</b>「${i.n}」 → 🎁 ${who}</div>`;
      }).join('')}
    </div>
  ` : '';

  cont.innerHTML = `
    <div class="trip-res">
      <h3>📍 ${areas.join('・')} のちいかわ${catLabel}</h3>
      <div class="trip-summary">
        <div class="trip-stat"><span>${allItems.length}</span>全アイテム</div>
        <div class="trip-stat"><span>${owned_.length}</span>所持済み</div>
        <div class="trip-stat"><span>${wanted_.length}</span>ほしい</div>
        <div class="trip-stat"><span>${none_.length}</span>未所持</div>
        ${forFriend_.length?`<div class="trip-stat"><span>${forFriend_.length}</span>🎁友達へ</div>`:''}
      </div>
      <div class="ttabs">
        <button class="ttab ${tripTab==='want'?'on':''}" onclick="tripTab='want';renderTripResult()">⭐ ほしい・未所持</button>
        <button class="ttab ${tripTab==='all'?'on':''}" onclick="tripTab='all';renderTripResult()">📋 全アイテム</button>
        ${forFriend_.length?`<button class="ttab ${tripTab==='friend'?'on':''}" onclick="tripTab='friend';renderTripResult()">🎁 友達へのお土産</button>`:''}
      </div>
      ${showItems.length===0 ?
        `<div class="trip-empty">🎉 このエリアのアイテムはすべて揃っています！</div>` :
        showItems.map(i=>{
          const s=getS_(i.id);
          const stCls=s.owned?'owned_':s.want?'wanted_':'none_';
          const stTxt=s.owned?'✅ 所持':s.want?'⭐ ほしい':'🔲 未所持';
          const vs=(i.v||[]).map(k=>VENUES[k]||k).join('・');
          const fp=s.forPeople||{};
          const forWho=Object.entries(fp).filter(([,v])=>v).map(([k])=>`🎁${k}`).join(' ');
          return `<div class="trip-item" onclick="openCard(ITEMS.find(x=>x.id==='${i.id}'));close_('trip-mo')">
            <span class="ti-emo">${i.e}</span>
            <div class="ti-info">
              <div class="ti-name">${i.n}${forWho?` <span style="color:#E65100;font-size:.62rem">${forWho}</span>`:''}
              </div>
              <div class="ti-area">${i.a}</div>
              <div class="ti-venue">${vs||'販売場所未登録'}</div>
            </div>
            <span class="tistatus ${stCls}">${stTxt}</span>
          </div>`;
        }).join('')
      }
      ${friendSection}
      <div class="trip-mapbtns">${mapLinks}</div>
    </div>
  `;
}

// ══════════════════════════════════════════════
//  シェアモーダル
// ══════════════════════════════════════════════
document.getElementById('share-btn').addEventListener('click', () => { open_('share-mo'); genShare('status'); });
document.querySelectorAll('.stab').forEach(b => {
  b.addEventListener('click', () => {
    document.querySelectorAll('.stab').forEach(x=>x.classList.remove('on'));
    b.classList.add('on'); genShare(b.dataset.st);
  });
});

function genShare(type) {
  const name = devName||'コレクター';
  const catLabel = CATS[cat].label;
  const owned_ = ITEMS.filter(i=>getS_(i.id).owned);
  const missing_= ITEMS.filter(i=>!getS_(i.id).owned&&!getS_(i.id).want);
  const wanted_ = ITEMS.filter(i=>getS_(i.id).want&&!getS_(i.id).owned);
  const trade_  = ITEMS.filter(i=>getS_(i.id).trade);
  const vs = i=>(i.v||[]).slice(0,2).map(k=>VENUES[k]||k).join('・');
  const memo_ = i=>getS_(i.id).memo?`（${getS_(i.id).memo}）`:'';
  let txt='';

  if(type==='status'){
    const pct=ITEMS.length?Math.round(owned_.length/ITEMS.length*100):0;
    txt=`🎀 ${name}のちいかわご当地${catLabel}\n`;
    txt+=`📦 ${owned_.length}個所持 / 全${ITEMS.length}個（${pct}%）\n`;
    if(trade_.length){txt+=`\n🔄【交換できます！】\n`;trade_.forEach(i=>txt+=`  ✅ ${i.a}「${i.n}」${memo_(i)}\n`);}
    if(wanted_.length){txt+=`\n⭐【ほしいもの】\n`;wanted_.forEach(i=>{const v=vs(i);txt+=`  □ ${i.a}「${i.n}」${v?' → '+v:''}\n`;});}
    txt+=`\n🔲【未所持（${missing_.length}個）】\n`;
    missing_.slice(0,30).forEach(i=>txt+=`  □ ${i.a}「${i.n}」\n`);
    if(missing_.length>30)txt+=`  …他${missing_.length-30}個\n`;
  } else if(type==='omiyage'){
    txt=`🛍️ ${name}のちいかわ${catLabel}\nお土産リクエスト 🙏\n\n`;
    if(wanted_.length){
      txt+=`⭐ 優先度高め\n`;
      wanted_.forEach(i=>{const v=vs(i);txt+=`  ⭐ ${i.a}「${i.n}」${v?'\n     📍 '+v+'で入手可能':''}\n`;});
      txt+='\n';
    }
    const byArea={};
    missing_.forEach(i=>{if(!byArea[i.a])byArea[i.a]=[];byArea[i.a].push(i);});
    txt+='🔲 持っていないもの\n';
    Object.entries(byArea).forEach(([area,items])=>{
      txt+=`\n【${area}】\n`;
      items.forEach(i=>{const v=vs(i);txt+=`  □ 「${i.n}」${v?' → '+v:''}\n`;});
    });
  } else if(type==='trade'){
    txt=`🔄 ${name}の交換リスト（${catLabel}）\n\n`;
    if(trade_.length){txt+='【交換できます！】\n';trade_.forEach(i=>txt+=`✅ ${i.a}「${i.n}」${memo_(i)}\n`);}
    else txt+='（交換用なし）\n';
    if(wanted_.length){txt+='\n【これと交換したい！】\n';wanted_.forEach(i=>txt+=`⭐ ${i.a}「${i.n}」\n`);}
  } else if(type==='buy4'){
    const buyMap={};
    ITEMS.forEach(i=>{
      const fp=getS_(i.id).forPeople||{};
      Object.entries(fp).forEach(([person,active])=>{
        if(active){if(!buyMap[person])buyMap[person]=[];buyMap[person].push(i);}
      });
    });
    txt=`🎁 ${name}の「誰かに買ってあげる」リスト（${catLabel}）\n\n`;
    if(!Object.keys(buyMap).length){txt+='（まだ登録なし）\nカードを開いて「誰かに買う」欄で追加してください！';}
    else{
      Object.entries(buyMap).forEach(([person,items])=>{
        txt+=`👤 ${person} へ（${items.length}個）\n`;
        items.forEach(i=>{const v=vs(i);txt+=`  🛒 ${i.a}「${i.n}」${v?' → '+v:''}\n`;});
        txt+='\n';
      });
    }
  }
  document.getElementById('spre').textContent=txt;
}

document.getElementById('cpbtn').addEventListener('click',()=>{
  const txt=document.getElementById('spre').textContent;
  navigator.clipboard.writeText(txt).then(()=>toast('コピーしました！')).catch(()=>{
    const ta=document.createElement('textarea');ta.value=txt;document.body.appendChild(ta);ta.select();document.execCommand('copy');document.body.removeChild(ta);toast('コピーしました！');
  });
});

// ══════════════════════════════════════════════
//  閲覧コード機能
// ══════════════════════════════════════════════

// 自分の閲覧コードを発行
function genViewCode() {
  viewCode = 'V' + Math.random().toString(36).slice(2,10).toUpperCase();
  LS.s('ck_viewcode', viewCode);
  renderViewCodeDisplay();
  // 自分の全カテゴリデータを共有ストレージに書き込む
  pushMyDataForView();
  toast('閲覧コードを発行しました！友達に送ってください👁');
}

async function pushMyDataForView() {
  if (!viewCode) return;
  const payload = { name: devName, ts: Date.now(), colls: {} };
  ['key','sock','nuig'].forEach(c => { payload.colls[c] = getColl(c); });
  try {
    await window.storage.set('ck_view_'+viewCode, JSON.stringify(payload), true);
  } catch { toast('⚠️ ストレージへの書き込みに失敗しました'); }
}

function clearViewCode() {
  if (!confirm('閲覧コードを削除しますか？\n友達がコードを使えなくなります。')) return;
  viewCode = ''; LS.s('ck_viewcode', '');
  renderViewCodeDisplay();
  toast('閲覧コードを削除しました');
}

function copyViewCode() {
  if (!viewCode) return;
  const msg = `【ちいかわコレクション帳】\n私のコレクションを見てね🎀\n閲覧コード：${viewCode}\n（設定 → 友達のコードを入力して閲覧）`;
  navigator.clipboard.writeText(msg).catch(()=>{
    const ta=document.createElement('textarea');ta.value=msg;document.body.appendChild(ta);ta.select();document.execCommand('copy');document.body.removeChild(ta);
  });
  toast('コードをコピーしました！LINEで送ってね📋');
}

function renderViewCodeDisplay() {
  const dis = document.getElementById('viewcode-dis');
  const hint = document.getElementById('viewcode-hint');
  const btnCopy = document.getElementById('copy-viewcode');
  const btnClr = document.getElementById('clr-viewcode');
  if (viewCode) {
    dis.textContent = viewCode;
    hint.textContent = '✅ このコードを友達に送ると、あなたのコレクションを読み取り専用で見られます';
    btnCopy.style.display = '';
    btnClr.style.display = '';
  } else {
    dis.textContent = '（未発行）';
    hint.textContent = '発行するとコードをLINEなどで友達に送れます';
    btnCopy.style.display = 'none';
    btnClr.style.display = 'none';
  }
}

// 友達のコードを入力して閲覧モードへ
async function enterViewMode() {
  const inp = document.getElementById('friend-code-inp');
  const code = inp.value.trim().toUpperCase();
  if (!code) { toast('コードを入力してください'); return; }

  toast('読み込み中…');
  try {
    const r = await window.storage.get('ck_view_'+code, true);
    if (!r) { toast('❌ コードが見つかりません。確認してください'); return; }
    const payload = JSON.parse(r.value);

    // 自分のデータを退避して友達データをロード
    myBackupCOLL = getColl(cat);
    viewMode = true;
    viewFriendCode = code;
    viewFriendName = payload.name || '友達';
    COLL = payload.colls?.[cat] || {};
    close_('set-mo');
    renderAll();
    toast(`👁 ${viewFriendName} のコレクションを閲覧中`);
  } catch(e) {
    toast('❌ 読み込みに失敗しました');
  }
}

// カテゴリ切り替え時に閲覧データも更新
async function loadViewCat(c) {
  cat = c;
  ITEMS = getItems(c);
  try {
    const r = await window.storage.get('ck_view_'+viewFriendCode, true);
    if (r) {
      const payload = JSON.parse(r.value);
      COLL = payload.colls?.[c] || {};
    }
  } catch { COLL = {}; }
  renderAll();
}

// 自分のリストに戻る
function exitViewMode() {
  viewMode = false;
  viewFriendCode = '';
  viewFriendName = '';
  COLL = myBackupCOLL;
  loadCat(cat); // 自分データで再ロード
  toast('自分のコレクションに戻りました');
}

// ══════════════════════════════════════════════
//  設定
// ══════════════════════════════════════════════
document.getElementById('set-btn').addEventListener('click', openSet);
function openSet(){
  document.getElementById('set-devname').value=devName;
  document.getElementById('friend-code-inp').value='';
  renderKeyDisplay();
  renderViewCodeDisplay();
  open_('set-mo');
}
function saveDevName(){
  const v=document.getElementById('set-devname').value.trim();
  if(!v){toast('名前を入力してください');return;}
  devName=v; LS.s('ck_devname',v); updateHeader(); toast('保存しました！');
}
function renderKeyDisplay(){
  const d=document.getElementById('key-dis');
  const h=document.getElementById('key-hint');
  const cb=document.getElementById('clr-key');
  if(shareKey){d.textContent=shareKey;h.textContent='✅ 家族の端末でこのキーを入力すると共有できます';cb.style.display='';}
  else{d.textContent='（未設定）';h.textContent='キーを生成か入力してください';cb.style.display='none';}
}
function genKey(){
  const k=Math.random().toString(36).slice(2,12).toUpperCase();
  shareKey=k; LS.s('ck_sharekey',k); renderKeyDisplay(); updateHeader();
  toast('キーを生成しました！家族の端末に送ってください🔑');
}
function inputKey(){
  const k=prompt('家族の端末の共有キーを入力してください：');
  if(!k||!k.trim())return;
  shareKey=k.trim().toUpperCase(); LS.s('ck_sharekey',shareKey);
  renderKeyDisplay(); updateHeader(); toast('キーを設定しました！同期中…');
  loadCat(cat);
}
function clearKey(){
  if(!confirm('共有を解除しますか？'))return;
  shareKey=''; LS.s('ck_sharekey',''); renderKeyDisplay(); updateHeader(); toast('共有を解除しました');
}
function exportData(){
  const d={devName,shareKey,collections:{},items:{}};
  ['key','sock','nuig'].forEach(c=>{d.collections[c]=getColl(c);d.items[c]=getItems(c);});
  const b=new Blob([JSON.stringify(d,null,2)],{type:'application/json'});
  const a=document.createElement('a');a.href=URL.createObjectURL(b);
  a.download=`chiikawa_backup_${devName||'data'}_${new Date().toISOString().slice(0,10)}.json`;
  a.click(); toast('書き出しました！');
}
function importData(){
  const inp=document.createElement('input');inp.type='file';inp.accept='.json';
  inp.onchange=e=>{
    const f=e.target.files[0];if(!f)return;
    const r=new FileReader();
    r.onload=async ev=>{
      try{
        const d=JSON.parse(ev.target.result);
        if(d.items)Object.entries(d.items).forEach(([c,v])=>setItems(c,v));
        if(d.collections)Object.entries(d.collections).forEach(([c,v])=>setColl(c,v));
        if(d.shareKey){shareKey=d.shareKey;LS.s('ck_sharekey',shareKey);}
        await loadCat(cat); toast('取り込みました！');
      }catch{toast('⚠️ 取り込み失敗');}
    };r.readAsText(f);
  };inp.click();
}
function resetData(){
  if(!confirm('全データをリセットしますか？'))return;
  ['key','sock','nuig'].forEach(c=>{setColl(c,{});setItems(c,JSON.parse(JSON.stringify(DEF_BY_CAT[c])));});
  close_('set-mo'); loadCat(cat); toast('リセットしました');
}

// ══════════════════════════════════════════════
//  キーホルダー管理
// ══════════════════════════════════════════════
document.getElementById('manage-btn').addEventListener('click', () => {
  document.getElementById('manage-cat-label').textContent = CATS[cat].label;
  buildVchecks(); renderIList(); open_('manage-mo');
});
function buildVchecks(){
  document.getElementById('vchecks').innerHTML=Object.entries(VENUES).map(([k,v])=>
    `<label><input type="checkbox" name="vc" value="${k}"> ${v}</label>`).join('');
}
function renderIList(){
  const q=(document.getElementById('iq').value||'').toLowerCase();
  const cont=document.getElementById('ilist');
  const filtered=ITEMS.filter(i=>!q||(i.n+i.a).toLowerCase().includes(q));
  document.getElementById('manage-cnt').textContent='（全'+ITEMS.length+'種類）';
  if(!filtered.length){cont.innerHTML='<div style="padding:18px;text-align:center;color:#bbb;font-size:.8rem">該当なし</div>';return;}
  cont.innerHTML=filtered.map(item=>`
    <div class="irow">
      <span class="ir-emo">${item.e}</span>
      <span class="ir-area">${item.a}</span>
      <span class="ir-name">${item.n}</span>
      <span class="ir-venue">${(item.v||[]).map(k=>VENUES[k]||k).join('・')}</span>
      <button class="ir-e" onclick="startEdit('${item.id}')">編集</button>
      <button class="ir-d" onclick="delItem('${item.id}')">削除</button>
    </div>`).join('');
}
function startEdit(id){
  const item=ITEMS.find(i=>i.id===id);if(!item)return;
  editingId=id;
  document.getElementById('iform-title').textContent='✏️ アイテムを編集';
  document.getElementById('f-emo').value=item.e;
  document.getElementById('f-area').value=item.a;
  document.getElementById('f-name').value=item.n;
  document.querySelectorAll('[name=vc]').forEach(cb=>cb.checked=(item.v||[]).includes(cb.value));
  document.getElementById('iform-save').textContent='更新する';
  document.getElementById('iform-title').scrollIntoView({behavior:'smooth'});
}
function cancelEdit(){
  editingId=null;
  document.getElementById('iform-title').textContent='➕ 新しいアイテムを追加';
  document.getElementById('f-emo').value='';document.getElementById('f-area').value='';document.getElementById('f-name').value='';
  document.querySelectorAll('[name=vc]').forEach(cb=>cb.checked=false);
  document.getElementById('iform-save').textContent='追加する';
}
function saveItem(){
  const emo=document.getElementById('f-emo').value.trim()||'🎀';
  const area=document.getElementById('f-area').value.trim();
  const name=document.getElementById('f-name').value.trim();
  if(!area||!name){toast('エリアと名前を入力してください');return;}
  const v=[...document.querySelectorAll('[name=vc]:checked')].map(cb=>cb.value);
  if(editingId){
    const item=ITEMS.find(i=>i.id===editingId);
    if(item){item.e=emo;item.a=area;item.n=name;item.v=v;}
    toast('更新しました！');
  }else{
    ITEMS.push({id:'c'+Date.now(),a:area,n:name,e:emo,v,custom:true});
    toast(`「${name}」を追加しました！`);
  }
  setItems(cat,ITEMS); cancelEdit(); renderIList(); renderAll();
}
function delItem(id){
  const item=ITEMS.find(i=>i.id===id);
  if(!confirm(`「${item?.n}」を削除しますか？`))return;
  ITEMS=ITEMS.filter(i=>i.id!==id); delete COLL[id];
  setItems(cat,ITEMS); saveColl(); renderIList(); renderAll(); toast('削除しました');
}
function exportItems(){
  const b=new Blob([JSON.stringify(ITEMS,null,2)],{type:'application/json'});
  const a=document.createElement('a');a.href=URL.createObjectURL(b);
  a.download=`chiikawa_${CATS[cat].label}_${new Date().toISOString().slice(0,10)}.json`;
  a.click(); toast('書き出しました！');
}
function importItems(){
  const inp=document.createElement('input');inp.type='file';inp.accept='.json';
  inp.onchange=e=>{
    const f=e.target.files[0];if(!f)return;
    const r=new FileReader();
    r.onload=ev=>{
      try{
        const d=JSON.parse(ev.target.result);
        if(!Array.isArray(d))throw new Error();
        ITEMS=d; setItems(cat,ITEMS); renderIList(); renderAll();
        toast(`${d.length}件を取り込みました！`);
      }catch{toast('⚠️ 形式が正しくありません（JSON配列）');}
    };r.readAsText(f);
  };inp.click();
}

// ══════════════════════════════════════════════
//  初回セットアップ
// ══════════════════════════════════════════════
document.getElementById('setup-save').addEventListener('click',()=>{
  const v=document.getElementById('setup-name').value.trim();
  if(!v){toast('名前を入力してください');return;}
  devName=v; LS.s('ck_devname',v); close_('setup-mo'); loadCat(cat);
});

// ══════════════════════════════════════════════
//  モーダル共通
// ══════════════════════════════════════════════
function open_(id){
  document.querySelectorAll('.ov').forEach(o=>{if(o.id!==id)o.classList.add('hide');});
  document.getElementById(id).classList.remove('hide');
}
function close_(id){document.getElementById(id).classList.add('hide');}
document.querySelectorAll('.ov').forEach(o=>{
  o.addEventListener('click',e=>{if(e.target===o)o.classList.add('hide');});
});

// ══════════════════════════════════════════════
//  トースト
// ══════════════════════════════════════════════
let _tt;
function toast(msg){
  const t=document.getElementById('toast');t.textContent=msg;t.classList.add('show');
  clearTimeout(_tt);_tt=setTimeout(()=>t.classList.remove('show'),2400);
}

init();
</script>
</body>
</html>
