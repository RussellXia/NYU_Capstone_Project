# NYU_Capstone_Project
Contributors: Amy Tang, Vivian Yan, Russell Xia
Mentors: Enes Avcu, Nick Landi, Yavuz Idug

### Project Overview: Lifetime Value Model
In this project, we will predict the total value a customer will bring to a business over the entire duration of their relationship. 
Develop a Customer Lifetime Value (LTV) model for a client: XYZ Networks.

### Dataset Overview
XYZ network has 5 brands (linear channels): LimeLight (Reality TV, lifestyle, and entertainment), Pulse (Action, thriller, and adventure), ChillStream (Documentaries, nature, and travel), RetroReel (Classic films and TV shows), CineQuest (Premium films and original scripted series). Under each brand, there are 10 content titles.

Also, there are 3 free brands of this XYZ networks (fast brands): Adrenaline (Action movies, extreme sports, and stunts), DarkMatter (Psychological thrillers, crime dramas, and mysteries), SilverScreen Classics (Hollywood's golden era films), TimeCapsule TV (Classic TV series and sitcoms), TasteMakers (Cooking competitions and food travel shows), DesignLab (Home improvement and interior design shows), PopCulture Now (Celebrity news, fashion, and trends). For each brand, there are 10 content titles.

**Subscription Data**: customer subscription status (monthly, annual)
**Viewership Data**: customer viewing sessions
**Online Content Data**: customer clicking online content for all the shows that XYZ Networks has from 2022-01-01 to 2024-01-01.

### Assumptions
The only Monetary Values come from user subscribing to the channels.

### Modeling Approaches
**Goal**: Takes customers' first 6 months RFM related behaviors as the input to predict whether they will generate low mid or high values in the next 6 months in 2023.

1. We conduct data preprocessing and feature engineering to generate RFM related features such as Recency, Frequency, Monetary Values, Tenure, Total Watch Time.
2. For each dataset’s RFM feature,  apply K Means and Elbow Methods to determine the optimal clusters. After calculating RFM clusters of the 3 datasets, adding all the cluster score together to get final score and group them into 3 final segments.
3. Build an XGBoost classifier to predict the users’ future lifetime value clusters, apply a 80 to 20 train test split.
4. Shapley values analysis for feature impact.
5. Customer Segmentation Analysis

### Related Project links
1. https://github.com/mukulsinghal001/customer-lifetime-prediction-using-python
2. https://github.com/adiag321/Customer-Lifetime-Value-Prediction-and-Segmentation-for-Online-Retail-Business (Reviewed by Amy)
3. https://github.com/basel-ay/Customer-Lifetime-Value-Prediction (Reviewed by Vivian)
4. https://www.kaggle.com/code/richardnnamdi/customer-segmentation-ltv
5. https://www.kaggle.com/code/shailaja4247/customer-lifetime-value-prediction (Reviewed by Russell)

### Related Paper
1. https://arxiv.org/abs/1912.07753 (Reviewed by Vivian)
2. https://www.sciencedirect.com/science/article/pii/S2405844023005911
3. https://www.sciencedirect.com/science/article/pii/S1877050910003868 (Reviewed by Amy)
4. https://www.brucehardie.com/papers/rfm_clv_2004-07-02.pdf
5. https://arxiv.org/pdf/1703.02596 (Reviewed by Russell)
