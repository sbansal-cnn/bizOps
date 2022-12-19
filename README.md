## Watch Next Dashboard Definitions:

- **Watch Next Impressions** - COUNTD(if [Watch Next Impressions]>0 then [Zion Anon Id] end)
- __Watch Next Video Started__ - count(case when a.component_type = 'video_detail' and a.view_name = 'watch_next_videos_top_news' then a.video_id end)
- __Watch Next Users with an Impression__ - COUNTD(if [Watch Next Impressions]>0 then [Zion Anon Id] end)
- __Watch Next Users__ - countd(if [Watch Next Video Started] > 0 then [Zion Anon Id] end)
- __Watch Next 2nd Video Users__ - COUNTD(if [Watch Next Video Started] >= 2 then [Zion Anon Id] end)

## Watch Next Dashboard Aggregation Definitions:


- __Watch Next Adoption Rate__ - countd(if [Watch Next Video Started]>0 then [Zion Anon Id] END) / COUNTD([Zion Anon Id])
- __Watch Next Conversion Rate__ - sum([Watch Next Video Started])/sum([Watch Next Impressions])
- __Watch Next Customer Conversion Rate__ - COUNTD(if [Watch Next Video Started] >0 then [Zion Anon Id] end)/COUNTD(if [Watch Next Impressions]>0 then [Zion Anon Id] end)
- __% Users w/2nd Video Started__ - COUNTD(if [Watch Next Video Started] >= 2 then [Zion Anon Id] end)/ COUNTD(if [Watch Next Video Started] >= 1 then [Zion Anon Id] end)
- __Watch Next Timespent per User__ - sum(if [Watch Next Video Started] > 0 then [Video Timespent] end) /COUNTD(if [Watch Next Video Started] >0 then [Zion Anon Id]   end)
- __Watch Next Video Starts per User__ - SUM([Watch Next Video Started])/COUNTD( if [Watch Next Video Started] >0 then [Zion Anon Id] end)


