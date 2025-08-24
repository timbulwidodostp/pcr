# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Principal Component Regression Model Use pcr (analogue) With (In) R Software
install.packages("analogue")
library("analogue")
pcr = read.csv("https://raw.githubusercontent.com/timbulwidodostp/pcr/main/pcr/pcr.csv",sep = ";")
# Estimation Principal Component Regression Model Use pcr (analogue) With (In) R Software
pcr <- pcr(hipcenter ~ Age + Weight + HtShoes + Ht + Seated + Arm +Thigh + Leg, data = pcr, ncomp =8, validation='CV', segments = 10)
pcr
head(fitted(pcr, comps = 1:4))
head(resid(pcr, comps = 1:4))
coef(pcr, comps = 1:4)
eigenvals(pcr)
screeplot(pcr)
# Principal Component Regression Model Use pcr (analogue) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished