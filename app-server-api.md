---


---

<h1 id="业务服务器接口">业务服务器接口</h1>
<h2 id="用户相关">1.用户相关</h2>
<h3 id="用户登录">1.1.用户登录</h3>
<p>URL: auth/login</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token string">"code"</span><span class="token punctuation">:</span><span class="token string">"test"</span><span class="token punctuation">}</span>   
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"user"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
        <span class="token string">"wxOpenId"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
        <span class="token string">"wxUnionId"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
        <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"test"</span><span class="token punctuation">,</span>
        <span class="token string">"headImgUrl"</span><span class="token punctuation">:</span> <span class="token string">"0"</span><span class="token punctuation">,</span>
        <span class="token string">"coin"</span><span class="token punctuation">:</span> <span class="token number">1004</span><span class="token punctuation">,</span>
        <span class="token string">"invitationCode"</span><span class="token punctuation">:</span> <span class="token string">"32131"</span><span class="token punctuation">,</span>
        <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-09T15:33:42.000Z"</span><span class="token punctuation">,</span>
        <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-15T13:54:20.000Z"</span>
    <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="用户登出">1.2.用户登出</h3>
<p>URL: users/logout</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"> <span class="token punctuation">{</span><span class="token punctuation">}</span>    
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span>
<span class="token punctuation">}</span>  
</code></pre>
<h3 id="获取用户信息">1.3.获取用户信息</h3>
<p>URL: users/getUserInfo</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"> <span class="token punctuation">{</span><span class="token punctuation">}</span>    
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"user"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
        <span class="token string">"wxOpenId"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
        <span class="token string">"wxUnionId"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
        <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"test"</span><span class="token punctuation">,</span>
        <span class="token string">"headImgUrl"</span><span class="token punctuation">:</span> <span class="token string">"0"</span><span class="token punctuation">,</span>
        <span class="token string">"coin"</span><span class="token punctuation">:</span> <span class="token number">1004</span><span class="token punctuation">,</span>
        <span class="token string">"invitationCode"</span><span class="token punctuation">:</span> <span class="token string">"32131"</span><span class="token punctuation">,</span>
        <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-09T15:33:42.000Z"</span><span class="token punctuation">,</span>
        <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-15T13:54:20.000Z"</span>
    <span class="token punctuation">}</span>
<span class="token punctuation">}</span>  
</code></pre>
<h3 id="添加邮寄地址">1.4.添加邮寄地址</h3>
<p>URL  : users/addAddress</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span> <span class="token string">"contact"</span><span class="token punctuation">:</span> <span class="token string">"user1"</span><span class="token punctuation">,</span> <span class="token string">"phone_number"</span><span class="token punctuation">:</span> <span class="token string">"1234567"</span><span class="token punctuation">,</span> <span class="token string">"province"</span><span class="token punctuation">:</span> <span class="token string">"北京市"</span><span class="token punctuation">,</span><span class="token string">"municipality"</span><span class="token punctuation">:</span><span class="token string">"北京市"</span><span class="token punctuation">,</span><span class="token string">"county"</span><span class="token punctuation">:</span><span class="token string">"朝阳区"</span><span class="token punctuation">,</span> <span class="token string">"address"</span><span class="token punctuation">:</span> <span class="token string">"XX小区X号楼212"</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"address_id"</span><span class="token punctuation">:</span> <span class="token number">2</span>
<span class="token punctuation">}</span>  
</code></pre>
<h3 id="更新邮寄地址">1.5.更新邮寄地址</h3>
<p>URL  : users/updateAddress</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span> <span class="token string">"address_id"</span><span class="token punctuation">:</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token string">"user_id"</span><span class="token punctuation">:</span><span class="token number">1</span><span class="token punctuation">,</span><span class="token string">"contact"</span><span class="token punctuation">:</span> <span class="token string">"user1"</span><span class="token punctuation">,</span> <span class="token string">"phone_number"</span><span class="token punctuation">:</span> <span class="token string">"1234567"</span><span class="token punctuation">,</span> <span class="token string">"province"</span><span class="token punctuation">:</span> <span class="token string">"北京市"</span><span class="token punctuation">,</span><span class="token string">"municipality"</span><span class="token punctuation">:</span><span class="token string">"北京市"</span><span class="token punctuation">,</span><span class="token string">"county"</span><span class="token punctuation">:</span><span class="token string">"朝阳区"</span><span class="token punctuation">,</span> <span class="token string">"address"</span><span class="token punctuation">:</span> <span class="token string">"XX小区X号楼212"</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span>
<span class="token punctuation">}</span>   
</code></pre>
<h3 id="删除邮寄地址">1.6.删除邮寄地址</h3>
<p>URL : users/deleteAddress</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span> <span class="token string">"address_id"</span><span class="token punctuation">:</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token string">"user_id"</span><span class="token punctuation">:</span><span class="token number">1</span><span class="token punctuation">}</span>    
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span>
<span class="token punctuation">}</span> 
</code></pre>
<h3 id="获取用户代币">1.7.获取用户代币</h3>
<p>URL  : users/getCoin</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token punctuation">}</span>  
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"coin"</span><span class="token punctuation">:</span> <span class="token number">1014</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="获取用户抓取娃娃排行">1.8.获取用户抓取娃娃排行</h3>
<p>URL  : users/tserRank</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token punctuation">}</span>  
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"rank"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
        <span class="token punctuation">{</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"用户A"</span><span class="token punctuation">,</span>
            <span class="token string">"img"</span><span class="token punctuation">:</span> <span class="token string">"/images/a.png"</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"用户B"</span><span class="token punctuation">,</span>
            <span class="token string">"img"</span><span class="token punctuation">:</span> <span class="token string">"/images/b.png"</span>
        <span class="token punctuation">}</span>
    <span class="token punctuation">]</span><span class="token punctuation">,</span>
    <span class="token string">"self_order"</span><span class="token punctuation">:</span> <span class="token number">18</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="获取app下载地址">1.9. 获取app下载地址</h3>
<p>URL  : users/getAppUrl</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token punctuation">}</span>  
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"url"</span><span class="token punctuation">:</span> <span class="token string">"https://github.com/wizardforcel/markdown-simple-world/blob/master/1.md"</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="兑换邀请码">1.10. 兑换邀请码</h3>
<p>URL  : users/useInvitationCode</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token string">"invitation_code"</span><span class="token punctuation">:</span><span class="token string">"12355"</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"add_coin"</span><span class="token punctuation">:</span> <span class="token number">15</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="获取用户周卡信息">1.11. 获取用户周卡信息</h3>
<p>URL  : users/getWeekCard</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"week_card"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
        <span class="token string">"userId"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span>
        <span class="token string">"cardType"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
        <span class="token string">"expireTime"</span><span class="token punctuation">:</span> <span class="token string">"2018-02-04T13:30:39.000Z"</span><span class="token punctuation">,</span>
        <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-12-06T13:30:39.000Z"</span><span class="token punctuation">,</span>
        <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-12-06T13:32:12.000Z"</span>
    <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="获取用户月卡信息">1.12. 获取用户月卡信息</h3>
<p>URL  : users/getMonthCard</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"week_card"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span>
        <span class="token string">"userId"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span>
        <span class="token string">"cardType"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span>
        <span class="token string">"expireTime"</span><span class="token punctuation">:</span> <span class="token string">"2018-02-04T13:30:39.000Z"</span><span class="token punctuation">,</span>
        <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-12-06T13:30:39.000Z"</span><span class="token punctuation">,</span>
        <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-12-06T13:32:12.000Z"</span>
    <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="领取周卡奖励">1.13. 领取周卡奖励</h3>
<p>URL  : users/receiveWeekCardReward</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"add_coin"</span><span class="token punctuation">:</span> <span class="token number">25</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="领取月卡卡奖励">1.14. 领取月卡卡奖励</h3>
<p>URL  : users/receiveMonthCardReward</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"add_coin"</span><span class="token punctuation">:</span> <span class="token number">25</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="获取我的积分">1.15. 获取我的积分</h3>
<p>URL  : users/getPoint</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"point"</span><span class="token punctuation">:</span> <span class="token number">0</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="获取我的积分变更记录">1.16. 获取我的积分变更记录</h3>
<p>URL  : users/getPointRecords</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token string">"pageindex"</span><span class="token punctuation">:</span><span class="token number">0</span><span class="token punctuation">,</span><span class="token string">"pagecount"</span><span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"claw_records"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"userId"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"point"</span><span class="token punctuation">:</span> <span class="token number">25</span><span class="token punctuation">,</span>
            <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"test add"</span><span class="token punctuation">,</span>
            <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-12-03T20:21:23.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-12-03T20:21:24.000Z"</span>
        <span class="token punctuation">}</span>
    <span class="token punctuation">]</span><span class="token punctuation">,</span>
    <span class="token string">"count"</span><span class="token punctuation">:</span> <span class="token number">1</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="获取我的抓娃娃记录">1.17. 获取我的抓娃娃记录</h3>
<p>URL  : users/getClawRecords</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token string">"pageindex"</span><span class="token punctuation">:</span><span class="token number">0</span><span class="token punctuation">,</span><span class="token string">"pagecount"</span><span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"claw_records"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"remoteGameId"</span><span class="token punctuation">:</span> <span class="token string">"0"</span><span class="token punctuation">,</span>
            <span class="token string">"userId"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"clawerId"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"spendCoin"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"dollTypeId"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"result"</span><span class="token punctuation">:</span> <span class="token keyword">null</span><span class="token punctuation">,</span>
            <span class="token string">"video"</span><span class="token punctuation">:</span> <span class="token keyword">null</span><span class="token punctuation">,</span>
            <span class="token string">"startTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-10T16:33:24.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"endTime"</span><span class="token punctuation">:</span> <span class="token keyword">null</span><span class="token punctuation">,</span>
            <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-10T16:33:24.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-10T16:33:24.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"user_id"</span><span class="token punctuation">:</span> <span class="token number">1</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span>
            <span class="token string">"remoteGameId"</span><span class="token punctuation">:</span> <span class="token string">"0"</span><span class="token punctuation">,</span>
            <span class="token string">"userId"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"clawerId"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"spendCoin"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"dollTypeId"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"result"</span><span class="token punctuation">:</span> <span class="token keyword">null</span><span class="token punctuation">,</span>
            <span class="token string">"video"</span><span class="token punctuation">:</span> <span class="token keyword">null</span><span class="token punctuation">,</span>
            <span class="token string">"startTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-10T16:34:39.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"endTime"</span><span class="token punctuation">:</span> <span class="token keyword">null</span><span class="token punctuation">,</span>
            <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-10T16:34:39.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-10T16:34:39.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"user_id"</span><span class="token punctuation">:</span> <span class="token number">1</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">3</span><span class="token punctuation">,</span>
            <span class="token string">"remoteGameId"</span><span class="token punctuation">:</span> <span class="token string">"0"</span><span class="token punctuation">,</span>
            <span class="token string">"userId"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"clawerId"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"spendCoin"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"dollTypeId"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"result"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"video"</span><span class="token punctuation">:</span> <span class="token keyword">null</span><span class="token punctuation">,</span>
            <span class="token string">"startTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-15T13:15:06.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"endTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-15T13:15:40.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-15T13:15:06.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-15T13:15:40.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"user_id"</span><span class="token punctuation">:</span> <span class="token number">1</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">4</span><span class="token punctuation">,</span>
            <span class="token string">"remoteGameId"</span><span class="token punctuation">:</span> <span class="token string">"0"</span><span class="token punctuation">,</span>
            <span class="token string">"userId"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"clawerId"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"spendCoin"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"dollTypeId"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"result"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"video"</span><span class="token punctuation">:</span> <span class="token keyword">null</span><span class="token punctuation">,</span>
            <span class="token string">"startTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-15T13:29:47.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"endTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-15T13:30:21.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-15T13:29:47.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-15T13:30:21.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"user_id"</span><span class="token punctuation">:</span> <span class="token number">1</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">5</span><span class="token punctuation">,</span>
            <span class="token string">"remoteGameId"</span><span class="token punctuation">:</span> <span class="token string">"0"</span><span class="token punctuation">,</span>
            <span class="token string">"userId"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"clawerId"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"spendCoin"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"dollTypeId"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"result"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
            <span class="token string">"video"</span><span class="token punctuation">:</span> <span class="token keyword">null</span><span class="token punctuation">,</span>
            <span class="token string">"startTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-15T13:32:19.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"endTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-15T13:32:41.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-15T13:32:19.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-15T13:32:41.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"user_id"</span><span class="token punctuation">:</span> <span class="token number">1</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">6</span><span class="token punctuation">,</span>
            <span class="token string">"remoteGameId"</span><span class="token punctuation">:</span> <span class="token string">"0"</span><span class="token punctuation">,</span>
            <span class="token string">"userId"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"clawerId"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"spendCoin"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"dollTypeId"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"result"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
            <span class="token string">"video"</span><span class="token punctuation">:</span> <span class="token keyword">null</span><span class="token punctuation">,</span>
            <span class="token string">"startTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-15T13:33:34.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"endTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-15T13:33:49.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-15T13:33:34.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-15T13:33:49.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"user_id"</span><span class="token punctuation">:</span> <span class="token number">1</span>
        <span class="token punctuation">}</span>
    <span class="token punctuation">]</span><span class="token punctuation">,</span>
    <span class="token string">"count"</span><span class="token punctuation">:</span> <span class="token number">261</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="获取我的全部地址">1.18. 获取我的全部地址</h3>
<p>URL  : users/getAddresses</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"addresses"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">6</span><span class="token punctuation">,</span>
            <span class="token string">"userId"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span>
            <span class="token string">"contact"</span><span class="token punctuation">:</span> <span class="token string">"user2"</span><span class="token punctuation">,</span>
            <span class="token string">"phoneNumber"</span><span class="token punctuation">:</span> <span class="token string">"1234567"</span><span class="token punctuation">,</span>
            <span class="token string">"province"</span><span class="token punctuation">:</span> <span class="token string">"北京市"</span><span class="token punctuation">,</span>
            <span class="token string">"municipality"</span><span class="token punctuation">:</span> <span class="token string">"北京市"</span><span class="token punctuation">,</span>
            <span class="token string">"county"</span><span class="token punctuation">:</span> <span class="token string">"朝阳区"</span><span class="token punctuation">,</span>
            <span class="token string">"address"</span><span class="token punctuation">:</span> <span class="token string">"XX小区X号楼212"</span><span class="token punctuation">,</span>
            <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-20T13:11:37.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-20T13:11:37.000Z"</span>
        <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="获取我的邀请码信息">1.19. 获取我的邀请码信息</h3>
<p>URL  : users/getInvitationCodeUsedInfo</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"total_reward_conis"</span><span class="token punctuation">:</span> <span class="token number">360</span><span class="token punctuation">,</span>
    <span class="token string">"use_count"</span><span class="token punctuation">:</span> <span class="token number">5</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="获取公告">1.20. 获取公告</h3>
<p>URL  : users/getBulletins</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"bulletins"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"title"</span><span class="token punctuation">:</span> <span class="token string">"1234"</span><span class="token punctuation">,</span>
            <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token string">"content"</span><span class="token punctuation">,</span>
            <span class="token string">"startTime"</span><span class="token punctuation">:</span> <span class="token string">"2018-01-22T12:00:00.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"endTime"</span><span class="token punctuation">:</span> <span class="token string">"2018-01-29T12:00:00.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"enable"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2018-01-21T16:09:17.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2018-01-22T02:59:56.000Z"</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span>
            <span class="token string">"title"</span><span class="token punctuation">:</span> <span class="token string">"1234"</span><span class="token punctuation">,</span>
            <span class="token string">"content"</span><span class="token punctuation">:</span> <span class="token string">"content"</span><span class="token punctuation">,</span>
            <span class="token string">"startTime"</span><span class="token punctuation">:</span> <span class="token string">"2018-01-22T12:00:00.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"endTime"</span><span class="token punctuation">:</span> <span class="token string">"2018-01-29T12:00:00.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"enable"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2018-01-22T02:48:55.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2018-01-22T02:48:55.000Z"</span>
        <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="获取每日登录奖励信息">1.21. 获取每日登录奖励信息</h3>
<p>URL  : users/getLoginRewards</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"loginRewards"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
            <span class="token string">"value"</span><span class="token punctuation">:</span> <span class="token number">10</span><span class="token punctuation">,</span>
            <span class="token string">"index"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
            <span class="token string">"imgUrl"</span><span class="token punctuation">:</span> <span class="token string">" "</span><span class="token punctuation">,</span>
            <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2018-01-24T16:21:56.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2018-01-24T16:21:57.000Z"</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span>
            <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"value"</span><span class="token punctuation">:</span> <span class="token number">10</span><span class="token punctuation">,</span>
            <span class="token string">"index"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"imgUrl"</span><span class="token punctuation">:</span> <span class="token string">" "</span><span class="token punctuation">,</span>
            <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2018-01-24T16:21:56.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2018-01-24T16:21:57.000Z"</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">3</span><span class="token punctuation">,</span>
            <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
            <span class="token string">"value"</span><span class="token punctuation">:</span> <span class="token number">20</span><span class="token punctuation">,</span>
            <span class="token string">"index"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span>
            <span class="token string">"imgUrl"</span><span class="token punctuation">:</span> <span class="token string">" "</span><span class="token punctuation">,</span>
            <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2018-01-24T16:21:56.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2018-01-24T16:21:57.000Z"</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">4</span><span class="token punctuation">,</span>
            <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"value"</span><span class="token punctuation">:</span> <span class="token number">20</span><span class="token punctuation">,</span>
            <span class="token string">"index"</span><span class="token punctuation">:</span> <span class="token number">3</span><span class="token punctuation">,</span>
            <span class="token string">"imgUrl"</span><span class="token punctuation">:</span> <span class="token string">" "</span><span class="token punctuation">,</span>
            <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2018-01-24T16:21:56.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2018-01-24T16:21:57.000Z"</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">5</span><span class="token punctuation">,</span>
            <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
            <span class="token string">"value"</span><span class="token punctuation">:</span> <span class="token number">30</span><span class="token punctuation">,</span>
            <span class="token string">"index"</span><span class="token punctuation">:</span> <span class="token number">4</span><span class="token punctuation">,</span>
            <span class="token string">"imgUrl"</span><span class="token punctuation">:</span> <span class="token string">" "</span><span class="token punctuation">,</span>
            <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2018-01-24T16:21:56.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2018-01-24T16:21:57.000Z"</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">6</span><span class="token punctuation">,</span>
            <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"value"</span><span class="token punctuation">:</span> <span class="token number">30</span><span class="token punctuation">,</span>
            <span class="token string">"index"</span><span class="token punctuation">:</span> <span class="token number">5</span><span class="token punctuation">,</span>
            <span class="token string">"imgUrl"</span><span class="token punctuation">:</span> <span class="token string">" "</span><span class="token punctuation">,</span>
            <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2018-01-24T16:21:56.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2018-01-24T16:21:57.000Z"</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">7</span><span class="token punctuation">,</span>
            <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
            <span class="token string">"value"</span><span class="token punctuation">:</span> <span class="token number">40</span><span class="token punctuation">,</span>
            <span class="token string">"index"</span><span class="token punctuation">:</span> <span class="token number">6</span><span class="token punctuation">,</span>
            <span class="token string">"imgUrl"</span><span class="token punctuation">:</span> <span class="token string">" "</span><span class="token punctuation">,</span>
            <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2018-01-24T16:21:56.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2018-01-24T16:21:57.000Z"</span>
        <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="领取每日登录奖励">1.22. 领取每日登录奖励</h3>
<p>URL  : users/receiveLoginReward</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span>
<span class="token punctuation">}</span>
</code></pre>
<hr>
<h2 id="娃娃机相关">2.娃娃机相关</h2>
<h3 id="获取娃娃列表">2.1.获取娃娃列表</h3>
<p>URL  : clawers/getDollTypesList<br>
输入</p>
<pre class=" language-json"><code class="prism  language-json"> <span class="token punctuation">{</span><span class="token string">"pageindex"</span><span class="token punctuation">:</span><span class="token number">0</span><span class="token punctuation">,</span><span class="token string">"pagecount"</span><span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">,</span><span class="token string">"tag"</span><span class="token punctuation">:</span><span class="token number">1</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"doll_types"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"doll1"</span><span class="token punctuation">,</span>
            <span class="token string">"price"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"convertCoinCount"</span><span class="token punctuation">:</span> <span class="token number">10</span><span class="token punctuation">,</span>
            <span class="token string">"img"</span><span class="token punctuation">:</span> <span class="token string">"images/item1.png"</span><span class="token punctuation">,</span>
            <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">"images/item1.png"</span><span class="token punctuation">,</span>
            <span class="token string">"tags"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
                <span class="token number">1</span><span class="token punctuation">,</span>
                <span class="token number">2</span><span class="token punctuation">,</span>
                <span class="token number">3</span>
            <span class="token punctuation">]</span><span class="token punctuation">,</span>
            <span class="token string">"status"</span><span class="token punctuation">:</span> <span class="token number">0</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"doll2"</span><span class="token punctuation">,</span>
            <span class="token string">"price"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span>
            <span class="token string">"convertCoinCount"</span><span class="token punctuation">:</span> <span class="token number">12</span><span class="token punctuation">,</span>
            <span class="token string">"img"</span><span class="token punctuation">:</span> <span class="token string">"images/item2.png"</span><span class="token punctuation">,</span>
            <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">"images/item2.png"</span><span class="token punctuation">,</span>
            <span class="token string">"tags"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
                <span class="token number">1</span><span class="token punctuation">,</span>
                <span class="token number">2</span><span class="token punctuation">,</span>
                <span class="token number">3</span>
            <span class="token punctuation">]</span><span class="token punctuation">,</span>
            <span class="token string">"status"</span><span class="token punctuation">:</span> <span class="token number">0</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">3</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"doll3"</span><span class="token punctuation">,</span>
            <span class="token string">"price"</span><span class="token punctuation">:</span> <span class="token number">3</span><span class="token punctuation">,</span>
            <span class="token string">"convertCoinCount"</span><span class="token punctuation">:</span> <span class="token number">13</span><span class="token punctuation">,</span>
            <span class="token string">"img"</span><span class="token punctuation">:</span> <span class="token string">"images/item3.png"</span><span class="token punctuation">,</span>
            <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">"images/item3.png"</span><span class="token punctuation">,</span>
            <span class="token string">"tags"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
                <span class="token number">1</span><span class="token punctuation">,</span>
                <span class="token number">2</span><span class="token punctuation">,</span>
                <span class="token number">3</span>
            <span class="token punctuation">]</span><span class="token punctuation">,</span>
            <span class="token string">"status"</span><span class="token punctuation">:</span> <span class="token number">0</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">4</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"doll4"</span><span class="token punctuation">,</span>
            <span class="token string">"price"</span><span class="token punctuation">:</span> <span class="token number">4</span><span class="token punctuation">,</span>
            <span class="token string">"convertCoinCount"</span><span class="token punctuation">:</span> <span class="token number">11</span><span class="token punctuation">,</span>
            <span class="token string">"img"</span><span class="token punctuation">:</span> <span class="token string">"images/item3.png"</span><span class="token punctuation">,</span>
            <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">"images/item4.png"</span><span class="token punctuation">,</span>
            <span class="token string">"tags"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
                <span class="token number">1</span><span class="token punctuation">,</span>
                <span class="token number">2</span><span class="token punctuation">,</span>
                <span class="token number">3</span>
            <span class="token punctuation">]</span><span class="token punctuation">,</span>
            <span class="token string">"status"</span><span class="token punctuation">:</span> <span class="token number">0</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">9</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"doll9"</span><span class="token punctuation">,</span>
            <span class="token string">"price"</span><span class="token punctuation">:</span> <span class="token number">9</span><span class="token punctuation">,</span>
            <span class="token string">"convertCoinCount"</span><span class="token punctuation">:</span> <span class="token number">33</span><span class="token punctuation">,</span>
            <span class="token string">"img"</span><span class="token punctuation">:</span> <span class="token string">"images/item9.png"</span><span class="token punctuation">,</span>
            <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">"images/item9.png"</span><span class="token punctuation">,</span>
            <span class="token string">"tags"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
                <span class="token number">1</span><span class="token punctuation">,</span>
                <span class="token number">3</span>
            <span class="token punctuation">]</span><span class="token punctuation">,</span>
            <span class="token string">"status"</span><span class="token punctuation">:</span> <span class="token number">0</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">10</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"doll10"</span><span class="token punctuation">,</span>
            <span class="token string">"price"</span><span class="token punctuation">:</span> <span class="token number">10</span><span class="token punctuation">,</span>
            <span class="token string">"convertCoinCount"</span><span class="token punctuation">:</span> <span class="token number">44</span><span class="token punctuation">,</span>
            <span class="token string">"img"</span><span class="token punctuation">:</span> <span class="token string">"images/item10.png"</span><span class="token punctuation">,</span>
            <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">"images/item10.png"</span><span class="token punctuation">,</span>
            <span class="token string">"tags"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
                <span class="token number">1</span>
            <span class="token punctuation">]</span><span class="token punctuation">,</span>
            <span class="token string">"status"</span><span class="token punctuation">:</span> <span class="token number">0</span>
        <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="获取娃娃机列表">2.2.获取娃娃机列表</h3>
<p>URL  : clawers/getClawersList</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token string">"doll_type_id"</span><span class="token punctuation">:</span><span class="token number">1</span><span class="token punctuation">,</span><span class="token string">"pageindex"</span><span class="token punctuation">:</span><span class="token number">0</span><span class="token punctuation">,</span><span class="token string">"pagecount"</span><span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">}</span>    
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"> <span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"clawers"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"c1"</span><span class="token punctuation">,</span>
            <span class="token string">"dollTypeId"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"ip"</span><span class="token punctuation">:</span> <span class="token string">"1"</span><span class="token punctuation">,</span>
            <span class="token string">"camera1"</span><span class="token punctuation">:</span> <span class="token string">"1"</span><span class="token punctuation">,</span>
            <span class="token string">"camera2"</span><span class="token punctuation">:</span> <span class="token string">"1"</span><span class="token punctuation">,</span>
            <span class="token string">"status"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
            <span class="token string">"dollType"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
                <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
                <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"doll1"</span><span class="token punctuation">,</span>
                <span class="token string">"price"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
                <span class="token string">"img"</span><span class="token punctuation">:</span> <span class="token string">"1"</span><span class="token punctuation">,</span>
                <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">"1"</span><span class="token punctuation">,</span>
                <span class="token string">"convertCoinCount"</span><span class="token punctuation">:</span> <span class="token number">10</span><span class="token punctuation">,</span>
                <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-09T16:40:31.000Z"</span><span class="token punctuation">,</span>
                <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-09T16:40:32.000Z"</span>
            <span class="token punctuation">}</span><span class="token punctuation">,</span>
            <span class="token string">"currentUser"</span><span class="token punctuation">:</span> <span class="token keyword">null</span><span class="token punctuation">,</span>
            <span class="token string">"currentClawRecord"</span><span class="token punctuation">:</span> <span class="token keyword">null</span><span class="token punctuation">,</span>
            <span class="token string">"timerId"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">1</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">11</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"c11"</span><span class="token punctuation">,</span>
            <span class="token string">"dollTypeId"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"ip"</span><span class="token punctuation">:</span> <span class="token string">"1"</span><span class="token punctuation">,</span>
            <span class="token string">"camera1"</span><span class="token punctuation">:</span> <span class="token string">"1"</span><span class="token punctuation">,</span>
            <span class="token string">"camera2"</span><span class="token punctuation">:</span> <span class="token string">"1"</span><span class="token punctuation">,</span>
            <span class="token string">"status"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
            <span class="token string">"dollType"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
                <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
                <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"doll1"</span><span class="token punctuation">,</span>
                <span class="token string">"price"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
                <span class="token string">"img"</span><span class="token punctuation">:</span> <span class="token string">"1"</span><span class="token punctuation">,</span>
                <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">"1"</span><span class="token punctuation">,</span>
                <span class="token string">"convertCoinCount"</span><span class="token punctuation">:</span> <span class="token number">10</span><span class="token punctuation">,</span>
                <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-09T16:40:31.000Z"</span><span class="token punctuation">,</span>
                <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-09T16:40:32.000Z"</span>
            <span class="token punctuation">}</span><span class="token punctuation">,</span>
            <span class="token string">"currentUser"</span><span class="token punctuation">:</span> <span class="token keyword">null</span><span class="token punctuation">,</span>
            <span class="token string">"currentClawRecord"</span><span class="token punctuation">:</span> <span class="token keyword">null</span><span class="token punctuation">,</span>
            <span class="token string">"timerId"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">1</span>
        <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
<span class="token punctuation">}</span>   
</code></pre>
<h3 id="获取娃娃机详情">2.3.获取娃娃机详情</h3>
<p>URL  : clawers/getClawerDetail</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"> <span class="token punctuation">{</span><span class="token string">"clawer_id"</span><span class="token punctuation">:</span><span class="token number">2</span><span class="token punctuation">}</span>   
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"> <span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"clawer"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span>
        <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"c2"</span><span class="token punctuation">,</span>
        <span class="token string">"dollTypeId"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span>
        <span class="token string">"ip"</span><span class="token punctuation">:</span> <span class="token string">"1"</span><span class="token punctuation">,</span>
        <span class="token string">"camera1"</span><span class="token punctuation">:</span> <span class="token string">"1"</span><span class="token punctuation">,</span>
        <span class="token string">"camera2"</span><span class="token punctuation">:</span> <span class="token string">"1"</span><span class="token punctuation">,</span>
        <span class="token string">"status"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
        <span class="token string">"dollType"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"doll2"</span><span class="token punctuation">,</span>
            <span class="token string">"price"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span>
            <span class="token string">"img"</span><span class="token punctuation">:</span> <span class="token string">"1"</span><span class="token punctuation">,</span>
            <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">"2"</span><span class="token punctuation">,</span>
            <span class="token string">"convertCoinCount"</span><span class="token punctuation">:</span> <span class="token number">12</span><span class="token punctuation">,</span>
            <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-09T16:40:31.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-09T16:40:32.000Z"</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token string">"currentUser"</span><span class="token punctuation">:</span> <span class="token keyword">null</span><span class="token punctuation">,</span>
        <span class="token string">"currentClawRecord"</span><span class="token punctuation">:</span> <span class="token keyword">null</span><span class="token punctuation">,</span>
        <span class="token string">"timerId"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">1</span>
    <span class="token punctuation">}</span>
<span class="token punctuation">}</span> 
</code></pre>
<h3 id="获取娃娃机成功抓取记录">2.4.获取娃娃机成功抓取记录</h3>
<p>URL  : clawers/getClawerSuccessRecord</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token string">"clawer_id"</span><span class="token punctuation">:</span><span class="token number">1</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"records"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">50</span><span class="token punctuation">,</span>
            <span class="token string">"userId"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"clawerId"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span>
            <span class="token string">"spendCoin"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span>
            <span class="token string">"dollTypeId"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span>
            <span class="token string">"result"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"video"</span><span class="token punctuation">:</span> <span class="token keyword">null</span><span class="token punctuation">,</span>
            <span class="token string">"startTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-17T04:58:01.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"endTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-17T04:58:34.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-17T04:58:01.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-17T04:58:34.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"user_id"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"user"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
                <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
                <span class="token string">"wxOpenId"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
                <span class="token string">"wxUnionId"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
                <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"test"</span><span class="token punctuation">,</span>
                <span class="token string">"headImgUrl"</span><span class="token punctuation">:</span> <span class="token string">"0"</span><span class="token punctuation">,</span>
                <span class="token string">"coin"</span><span class="token punctuation">:</span> <span class="token number">944</span><span class="token punctuation">,</span>
                <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-09T15:33:42.000Z"</span><span class="token punctuation">,</span>
                <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-17T12:26:53.000Z"</span>
            <span class="token punctuation">}</span>
        <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="开始抓娃娃游戏">2.5.开始抓娃娃游戏</h3>
<p>URL  : clawers/start</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token string">"clawer_id"</span><span class="token punctuation">:</span><span class="token number">1</span><span class="token punctuation">}</span> 
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"> <span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"claw_record_id"</span><span class="token punctuation">:</span> <span class="token number">6</span>
<span class="token punctuation">}</span>  
</code></pre>
<h3 id="抓取娃娃">2.6.抓取娃娃</h3>
<p>URL  : clawers/grab</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token string">"claw_record_id"</span><span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span>
<span class="token punctuation">}</span> 
</code></pre>
<h3 id="获取游戏结果">2.7.获取游戏结果</h3>
<p>抓取娃娃或者到达游戏结束时间后，调用此接口，可获取本次抓取娃娃的结果</p>
<p>URL  : clawers/gameResult</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token string">"claw_record_id"</span><span class="token punctuation">:</span><span class="token number">5</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"result"</span><span class="token punctuation">:</span> <span class="token number">0</span>
<span class="token punctuation">}</span>  
</code></pre>
<h3 id="获取所有娃娃类型">2.8.获取所有娃娃类型</h3>
<p>URL  : clawers/getAllDollType</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token punctuation">}</span>  
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"doll_types"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"傲娇布朗熊"</span><span class="token punctuation">,</span>
            <span class="token string">"price"</span><span class="token punctuation">:</span> <span class="token number">9</span><span class="token punctuation">,</span>
            <span class="token string">"convertCoinCount"</span><span class="token punctuation">:</span> <span class="token number">60</span><span class="token punctuation">,</span>
            <span class="token string">"img"</span><span class="token punctuation">:</span> <span class="token string">"images/item1.png"</span><span class="token punctuation">,</span>
            <span class="token string">"img70"</span><span class="token punctuation">:</span> <span class="token string">"images/doll/70/傲娇布朗熊.jpg"</span><span class="token punctuation">,</span>
            <span class="token string">"img250"</span><span class="token punctuation">:</span> <span class="token string">"images/doll/250/傲娇布朗熊.jpg"</span><span class="token punctuation">,</span>
            <span class="token string">"img300"</span><span class="token punctuation">:</span> <span class="token string">"images/doll/300/傲娇布朗熊.jpg"</span><span class="token punctuation">,</span>
            <span class="token string">"detailImages"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
                <span class="token punctuation">{</span>
                    <span class="token string">"width"</span><span class="token punctuation">:</span> <span class="token number">600</span><span class="token punctuation">,</span>
                    <span class="token string">"height"</span><span class="token punctuation">:</span> <span class="token number">810</span><span class="token punctuation">,</span>
                    <span class="token string">"url"</span><span class="token punctuation">:</span> <span class="token string">"images/doll/detail/傲娇布朗熊1.jpg"</span>
                <span class="token punctuation">}</span><span class="token punctuation">,</span>
                <span class="token punctuation">{</span>
                    <span class="token string">"width"</span><span class="token punctuation">:</span> <span class="token number">600</span><span class="token punctuation">,</span>
                    <span class="token string">"height"</span><span class="token punctuation">:</span> <span class="token number">1017</span><span class="token punctuation">,</span>
                    <span class="token string">"url"</span><span class="token punctuation">:</span> <span class="token string">"images/doll/detail/傲娇布朗熊2.jpg"</span>
                <span class="token punctuation">}</span><span class="token punctuation">,</span>
                <span class="token punctuation">{</span>
                    <span class="token string">"width"</span><span class="token punctuation">:</span> <span class="token number">600</span><span class="token punctuation">,</span>
                    <span class="token string">"height"</span><span class="token punctuation">:</span> <span class="token number">405</span><span class="token punctuation">,</span>
                    <span class="token string">"url"</span><span class="token punctuation">:</span> <span class="token string">"images/doll/detail/傲娇布朗熊3.jpg"</span>
                <span class="token punctuation">}</span><span class="token punctuation">,</span>
                <span class="token punctuation">{</span>
                    <span class="token string">"width"</span><span class="token punctuation">:</span> <span class="token number">600</span><span class="token punctuation">,</span>
                    <span class="token string">"height"</span><span class="token punctuation">:</span> <span class="token number">443</span><span class="token punctuation">,</span>
                    <span class="token string">"url"</span><span class="token punctuation">:</span> <span class="token string">"images/doll/detail/傲娇布朗熊4.jpg"</span>
                <span class="token punctuation">}</span><span class="token punctuation">,</span>
                <span class="token punctuation">{</span>
                    <span class="token string">"width"</span><span class="token punctuation">:</span> <span class="token number">600</span><span class="token punctuation">,</span>
                    <span class="token string">"height"</span><span class="token punctuation">:</span> <span class="token number">430</span><span class="token punctuation">,</span>
                    <span class="token string">"url"</span><span class="token punctuation">:</span> <span class="token string">"images/doll/detail/傲娇布朗熊5.jpg"</span>
                <span class="token punctuation">}</span>
            <span class="token punctuation">]</span><span class="token punctuation">,</span>
            <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">"images/item1.png"</span><span class="token punctuation">,</span>
            <span class="token string">"tags"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
                <span class="token number">1</span><span class="token punctuation">,</span>
                <span class="token number">2</span><span class="token punctuation">,</span>
                <span class="token number">3</span>
            <span class="token punctuation">]</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"蠢萌泰迪"</span><span class="token punctuation">,</span>
            <span class="token string">"price"</span><span class="token punctuation">:</span> <span class="token number">19</span><span class="token punctuation">,</span>
            <span class="token string">"convertCoinCount"</span><span class="token punctuation">:</span> <span class="token number">60</span><span class="token punctuation">,</span>
            <span class="token string">"img"</span><span class="token punctuation">:</span> <span class="token string">"images/item2.png"</span><span class="token punctuation">,</span>
            <span class="token string">"img70"</span><span class="token punctuation">:</span> <span class="token string">"images/doll/70/蠢萌泰迪.jpg"</span><span class="token punctuation">,</span>
            <span class="token string">"img250"</span><span class="token punctuation">:</span> <span class="token string">"images/doll/250/蠢萌泰迪.jpg"</span><span class="token punctuation">,</span>
            <span class="token string">"img300"</span><span class="token punctuation">:</span> <span class="token string">"images/doll/300/蠢萌泰迪.jpg"</span><span class="token punctuation">,</span>
            <span class="token string">"detailImages"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
                <span class="token punctuation">{</span>
                    <span class="token string">"width"</span><span class="token punctuation">:</span> <span class="token number">600</span><span class="token punctuation">,</span>
                    <span class="token string">"height"</span><span class="token punctuation">:</span> <span class="token number">810</span><span class="token punctuation">,</span>
                    <span class="token string">"url"</span><span class="token punctuation">:</span> <span class="token string">"images/doll/detail/蠢萌泰迪1.jpg"</span>
                <span class="token punctuation">}</span><span class="token punctuation">,</span>
                <span class="token punctuation">{</span>
                    <span class="token string">"width"</span><span class="token punctuation">:</span> <span class="token number">600</span><span class="token punctuation">,</span>
                    <span class="token string">"height"</span><span class="token punctuation">:</span> <span class="token number">638</span><span class="token punctuation">,</span>
                    <span class="token string">"url"</span><span class="token punctuation">:</span> <span class="token string">"images/doll/detail/蠢萌泰迪2.jpg"</span>
                <span class="token punctuation">}</span><span class="token punctuation">,</span>
                <span class="token punctuation">{</span>
                    <span class="token string">"width"</span><span class="token punctuation">:</span> <span class="token number">600</span><span class="token punctuation">,</span>
                    <span class="token string">"height"</span><span class="token punctuation">:</span> <span class="token number">436</span><span class="token punctuation">,</span>
                    <span class="token string">"url"</span><span class="token punctuation">:</span> <span class="token string">"images/doll/detail/蠢萌泰迪3.jpg"</span>
                <span class="token punctuation">}</span><span class="token punctuation">,</span>
                <span class="token punctuation">{</span>
                    <span class="token string">"width"</span><span class="token punctuation">:</span> <span class="token number">600</span><span class="token punctuation">,</span>
                    <span class="token string">"height"</span><span class="token punctuation">:</span> <span class="token number">442</span><span class="token punctuation">,</span>
                    <span class="token string">"url"</span><span class="token punctuation">:</span> <span class="token string">"images/doll/detail/蠢萌泰迪4.jpg"</span>
                <span class="token punctuation">}</span>
            <span class="token punctuation">]</span><span class="token punctuation">,</span>
            <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">"images/item2.png"</span><span class="token punctuation">,</span>
            <span class="token string">"tags"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
                <span class="token number">1</span><span class="token punctuation">,</span>
                <span class="token number">2</span><span class="token punctuation">,</span>
                <span class="token number">3</span>
            <span class="token punctuation">]</span>
        <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>    
<span class="token punctuation">}</span>
</code></pre>
<h3 id="控制娃娃机移动">2.9.控制娃娃机移动</h3>
<p><em>方向键按下时，调用对应方向的移动接口，抬起时，调用stop接口。快速单击按键时调用对应的轻微移动接口，如（forwardLight、backwardLight，leftLight，rightLight）</em></p>
<p>URL  : clawers/forward  (backward,left,right,forwardLight,backwardLight,leftLight,rightLight,stop)</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token string">"claw_record_id"</span><span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span>
<span class="token punctuation">}</span> 
</code></pre>
<h3 id="获取所有娃娃类型标签">2.10.获取所有娃娃类型标签</h3>
<p>URL  : clawers/getAllDollTypeTag</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"doll_type_tags"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"新品"</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"特价"</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">3</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"积分"</span>
        <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="获取抓娃娃成功通知">2.11. 获取抓娃娃成功通知</h3>
<p>URL  : clawers/getClawSuccessNotices</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"notices"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
		<span class="token punctuation">{</span> <span class="token string">"userId"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span> <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span> <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"用户A抓到了娃娃！"</span><span class="token punctuation">,</span> <span class="token string">"time"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-15T13:54:20.000Z"</span><span class="token punctuation">}</span><span class="token punctuation">,</span>
		<span class="token punctuation">{</span> <span class="token string">"userId"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span> <span class="token string">"type"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span> <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"用户B抓到了娃娃！"</span><span class="token punctuation">,</span> <span class="token string">"time"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-15T13:54:20.000Z"</span><span class="token punctuation">}</span><span class="token punctuation">,</span>
	<span class="token punctuation">]</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="领取分享奖励娃娃币">2.12. 领取分享奖励娃娃币</h3>
<p>URL  : clawers/receiveCoinsAfterShare</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token string">"claw_record_id"</span><span class="token punctuation">:</span><span class="token number">1</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"add_coin"</span><span class="token punctuation">:</span> <span class="token number">19</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="提交申诉">2.13. 提交申诉</h3>
<p>URL  : clawers/submitComplaint</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token string">"claw_record_id"</span><span class="token punctuation">:</span><span class="token number">1</span><span class="token punctuation">,</span><span class="token string">"reason"</span><span class="token punctuation">:</span><span class="token string">"抓到了没奖励"</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="进入娃娃机直播间">2.14. 进入娃娃机直播间</h3>
<p>URL  : clawers/enterClawerLive</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>"clawer_id<span class="token punctuation">:</span><span class="token number">1</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="离开娃娃机直播间">2.15. 离开娃娃机直播间</h3>
<p>URL  : clawers/leaveClawerLive</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>"clawer_id<span class="token punctuation">:</span><span class="token number">1</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="获取娃娃机直播间所有用户信息">2.16. 获取娃娃机直播间所有用户信息</h3>
<p>URL  : clawers/getUsersInClawLive</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token string">"clawer_id"</span><span class="token punctuation">:</span><span class="token number">1</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"users"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"hc421078278"</span><span class="token punctuation">,</span>
            <span class="token string">"headImgUrl"</span><span class="token punctuation">:</span> <span class="token string">""</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">5</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"彭昆"</span><span class="token punctuation">,</span>
            <span class="token string">"headImgUrl"</span><span class="token punctuation">:</span> <span class="token string">"http://wx.qlogo.cn/mmopen/vi_32/DYAIOgq83ep94v8hrFeC8bo89kevu6X1iaIQ70nTawxUp6diaC0husUdkPOxQ2HsnOU6CgibkXH9Su9oI5uvThibXA/0"</span>
        <span class="token punctuation">}</span>
    <span class="token punctuation">]</span><span class="token punctuation">,</span>
    <span class="token string">"count"</span><span class="token punctuation">:</span> <span class="token number">2</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="获取娃娃类型的图片列表">2.17. 获取娃娃类型的图片列表</h3>
<p>URL  : clawers/getDollTypeImages</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token string">"doll_type_id"</span><span class="token punctuation">:</span><span class="token number">1</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"images"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
        <span class="token punctuation">{</span>
            <span class="token string">"width"</span><span class="token punctuation">:</span> <span class="token number">128</span><span class="token punctuation">,</span>
            <span class="token string">"height"</span><span class="token punctuation">:</span> <span class="token number">128</span><span class="token punctuation">,</span>
            <span class="token string">"url"</span><span class="token punctuation">:</span> <span class="token string">"images/item1.png"</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"width"</span><span class="token punctuation">:</span> <span class="token number">128</span><span class="token punctuation">,</span>
            <span class="token string">"height"</span><span class="token punctuation">:</span> <span class="token number">128</span><span class="token punctuation">,</span>
            <span class="token string">"url"</span><span class="token punctuation">:</span> <span class="token string">"images/item2.png"</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"width"</span><span class="token punctuation">:</span> <span class="token number">128</span><span class="token punctuation">,</span>
            <span class="token string">"height"</span><span class="token punctuation">:</span> <span class="token number">128</span><span class="token punctuation">,</span>
            <span class="token string">"url"</span><span class="token punctuation">:</span> <span class="token string">"images/item3.png"</span>
        <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="获取娃娃机状态">2.18. 获取娃娃机状态</h3>
<p>URL  : clawers/getClawerStatus</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token string">"clawer_id"</span><span class="token punctuation">:</span><span class="token number">1</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"status"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"current_user"</span><span class="token punctuation">:</span> <span class="token keyword">null</span>
<span class="token punctuation">}</span>
</code></pre>
<hr>
<h2 id="代币相关">3.代币相关</h2>
<h3 id="获取代币变更记录">3.1.获取代币变更记录</h3>
<p>URL  : coins/getCoinRecords</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token string">"pageindex"</span><span class="token punctuation">:</span><span class="token number">1</span><span class="token punctuation">,</span><span class="token string">"pagecount"</span><span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"coin_records"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">7</span><span class="token punctuation">,</span>
            <span class="token string">"userId"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"coin"</span><span class="token punctuation">:</span> <span class="token number">10</span><span class="token punctuation">,</span>
            <span class="token string">"text"</span><span class="token punctuation">:</span> <span class="token string">"convertPrize"</span><span class="token punctuation">,</span>
            <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-15T13:54:20.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-11-15T13:54:20.000Z"</span>
        <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
<span class="token punctuation">}</span>  
</code></pre>
<h3 id="获取充值项">3.2.获取充值项</h3>
<p>URL  : coins/getPayItems</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"pay_items"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"充值6元娃娃币"</span><span class="token punctuation">,</span>
            <span class="token string">"amount"</span><span class="token punctuation">:</span> <span class="token number">6</span><span class="token punctuation">,</span>
            <span class="token string">"coins"</span><span class="token punctuation">:</span> <span class="token number">36</span><span class="token punctuation">,</span>
            <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
            <span class="token string">"imgurl"</span><span class="token punctuation">:</span> <span class="token string">""</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"首次充值6元娃娃币"</span><span class="token punctuation">,</span>
            <span class="token string">"amount"</span><span class="token punctuation">:</span> <span class="token number">6</span><span class="token punctuation">,</span>
            <span class="token string">"coins"</span><span class="token punctuation">:</span> <span class="token number">66</span><span class="token punctuation">,</span>
            <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
            <span class="token string">"imgurl"</span><span class="token punctuation">:</span> <span class="token string">""</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">3</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"充值18元娃娃币"</span><span class="token punctuation">,</span>
            <span class="token string">"amount"</span><span class="token punctuation">:</span> <span class="token number">18</span><span class="token punctuation">,</span>
            <span class="token string">"coins"</span><span class="token punctuation">:</span> <span class="token number">189</span><span class="token punctuation">,</span>
            <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
            <span class="token string">"imgurl"</span><span class="token punctuation">:</span> <span class="token string">""</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">4</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"首次充值18元娃娃币"</span><span class="token punctuation">,</span>
            <span class="token string">"amount"</span><span class="token punctuation">:</span> <span class="token number">18</span><span class="token punctuation">,</span>
            <span class="token string">"coins"</span><span class="token punctuation">:</span> <span class="token number">198</span><span class="token punctuation">,</span>
            <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
            <span class="token string">"imgurl"</span><span class="token punctuation">:</span> <span class="token string">""</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">5</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"充值60元娃娃币"</span><span class="token punctuation">,</span>
            <span class="token string">"amount"</span><span class="token punctuation">:</span> <span class="token number">60</span><span class="token punctuation">,</span>
            <span class="token string">"coins"</span><span class="token punctuation">:</span> <span class="token number">666</span><span class="token punctuation">,</span>
            <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
            <span class="token string">"imgurl"</span><span class="token punctuation">:</span> <span class="token string">""</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">6</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"首次充值60元娃娃币"</span><span class="token punctuation">,</span>
            <span class="token string">"amount"</span><span class="token punctuation">:</span> <span class="token number">60</span><span class="token punctuation">,</span>
            <span class="token string">"coins"</span><span class="token punctuation">:</span> <span class="token number">690</span><span class="token punctuation">,</span>
            <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
            <span class="token string">"imgurl"</span><span class="token punctuation">:</span> <span class="token string">""</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">7</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"充值118元娃娃币"</span><span class="token punctuation">,</span>
            <span class="token string">"amount"</span><span class="token punctuation">:</span> <span class="token number">118</span><span class="token punctuation">,</span>
            <span class="token string">"coins"</span><span class="token punctuation">:</span> <span class="token number">1357</span><span class="token punctuation">,</span>
            <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
            <span class="token string">"imgurl"</span><span class="token punctuation">:</span> <span class="token string">""</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">8</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"首次充值118元娃娃币"</span><span class="token punctuation">,</span>
            <span class="token string">"amount"</span><span class="token punctuation">:</span> <span class="token number">118</span><span class="token punctuation">,</span>
            <span class="token string">"coins"</span><span class="token punctuation">:</span> <span class="token number">1416</span><span class="token punctuation">,</span>
            <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
            <span class="token string">"imgurl"</span><span class="token punctuation">:</span> <span class="token string">""</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">9</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"充值328元娃娃币"</span><span class="token punctuation">,</span>
            <span class="token string">"amount"</span><span class="token punctuation">:</span> <span class="token number">328</span><span class="token punctuation">,</span>
            <span class="token string">"coins"</span><span class="token punctuation">:</span> <span class="token number">3872</span><span class="token punctuation">,</span>
            <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
            <span class="token string">"imgurl"</span><span class="token punctuation">:</span> <span class="token string">""</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">10</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"首次充值328元娃娃币"</span><span class="token punctuation">,</span>
            <span class="token string">"amount"</span><span class="token punctuation">:</span> <span class="token number">328</span><span class="token punctuation">,</span>
            <span class="token string">"coins"</span><span class="token punctuation">:</span> <span class="token number">4100</span><span class="token punctuation">,</span>
            <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
            <span class="token string">"imgurl"</span><span class="token punctuation">:</span> <span class="token string">""</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">11</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"充值648元娃娃币"</span><span class="token punctuation">,</span>
            <span class="token string">"amount"</span><span class="token punctuation">:</span> <span class="token number">648</span><span class="token punctuation">,</span>
            <span class="token string">"coins"</span><span class="token punctuation">:</span> <span class="token number">7846</span><span class="token punctuation">,</span>
            <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
            <span class="token string">"imgurl"</span><span class="token punctuation">:</span> <span class="token string">""</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">12</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"首次充值648元娃娃币"</span><span class="token punctuation">,</span>
            <span class="token string">"amount"</span><span class="token punctuation">:</span> <span class="token number">648</span><span class="token punctuation">,</span>
            <span class="token string">"coins"</span><span class="token punctuation">:</span> <span class="token number">8424</span><span class="token punctuation">,</span>
            <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
            <span class="token string">"imgurl"</span><span class="token punctuation">:</span> <span class="token string">""</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">13</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"周卡"</span><span class="token punctuation">,</span>
            <span class="token string">"amount"</span><span class="token punctuation">:</span> <span class="token number">28</span><span class="token punctuation">,</span>
            <span class="token string">"coins"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
            <span class="token string">"card"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">"连续7天点击领取，充值当天算第一天"</span><span class="token punctuation">,</span>
            <span class="token string">"imgurl"</span><span class="token punctuation">:</span> <span class="token string">""</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">14</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"月卡"</span><span class="token punctuation">,</span>
            <span class="token string">"amount"</span><span class="token punctuation">:</span> <span class="token number">148</span><span class="token punctuation">,</span>
            <span class="token string">"coins"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
            <span class="token string">"card"</span><span class="token punctuation">:</span> <span class="token number">2</span><span class="token punctuation">,</span>
            <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">"连续30天点击领取，充值当天算第一天"</span><span class="token punctuation">,</span>
            <span class="token string">"imgurl"</span><span class="token punctuation">:</span> <span class="token string">""</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">1</span><span class="token punctuation">,</span>
            <span class="token string">"name"</span><span class="token punctuation">:</span> <span class="token string">"充值0.01元娃娃币"</span><span class="token punctuation">,</span>
            <span class="token string">"amount"</span><span class="token punctuation">:</span> <span class="token number">0.01</span><span class="token punctuation">,</span>
            <span class="token string">"coins"</span><span class="token punctuation">:</span> <span class="token number">100</span><span class="token punctuation">,</span>
            <span class="token string">"description"</span><span class="token punctuation">:</span> <span class="token string">""</span><span class="token punctuation">,</span>
            <span class="token string">"imgurl"</span><span class="token punctuation">:</span> <span class="token string">""</span>
        <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
<span class="token punctuation">}</span>
</code></pre>
<hr>
<h2 id="奖品相关">4.奖品相关</h2>
<h3 id="获取奖品信息">4.1.获取奖品信息</h3>
<p>URL  : prizes/getPrizes</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token string">"pageindex"</span><span class="token punctuation">:</span><span class="token number">1</span><span class="token punctuation">,</span><span class="token string">"pagecount"</span><span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"prizes"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">414</span><span class="token punctuation">,</span>
            <span class="token string">"userId"</span><span class="token punctuation">:</span> <span class="token number">32</span><span class="token punctuation">,</span>
            <span class="token string">"dollTypeId"</span><span class="token punctuation">:</span> <span class="token number">6</span><span class="token punctuation">,</span>
            <span class="token string">"clawRecordId"</span><span class="token punctuation">:</span> <span class="token number">729</span><span class="token punctuation">,</span>
            <span class="token string">"status"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
            <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-12-25T16:33:10.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-12-25T16:33:10.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"statusText"</span><span class="token punctuation">:</span> <span class="token string">"未处理"</span><span class="token punctuation">,</span>
            <span class="token string">"remainDays"</span><span class="token punctuation">:</span> <span class="token number">5</span>
        <span class="token punctuation">}</span>
    <span class="token punctuation">]</span><span class="token punctuation">,</span>
    <span class="token string">"count"</span><span class="token punctuation">:</span> <span class="token number">1</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="将奖品转换为代币">4.2.将奖品转换为代币</h3>
<p>URL  : prizes/convertConis</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token string">"prize_ids"</span><span class="token punctuation">:</span><span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">]</span><span class="token punctuation">}</span> 
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json">		 <span class="token punctuation">{</span>
		    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
		    <span class="token string">"user_coin"</span><span class="token punctuation">:</span> <span class="token number">1014</span><span class="token punctuation">,</span>
		    <span class="token string">"add_coin"</span><span class="token punctuation">:</span> <span class="token number">10</span>
		<span class="token punctuation">}</span>
</code></pre>
<h3 id="通过奖品id获取发货单信息">4.3. 通过奖品Id获取发货单信息</h3>
<p>URL  : prizes/getInvoiceByPrizeId</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token string">"prize_id"</span><span class="token punctuation">:</span><span class="token number">1</span><span class="token punctuation">}</span> 
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"invoice"</span><span class="token punctuation">:</span> <span class="token punctuation">{</span>
        <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
        <span class="token string">"code"</span><span class="token punctuation">:</span> <span class="token string">"123415"</span><span class="token punctuation">,</span>
        <span class="token string">"status"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
        <span class="token string">"contact"</span><span class="token punctuation">:</span> <span class="token string">"张三"</span><span class="token punctuation">,</span>
        <span class="token string">"phone_number"</span><span class="token punctuation">:</span> <span class="token string">"123456"</span><span class="token punctuation">,</span>
        <span class="token string">"address"</span><span class="token punctuation">:</span> <span class="token string">"北京市朝阳区大悦城1133号"</span><span class="token punctuation">,</span>
        <span class="token string">"comment"</span><span class="token punctuation">:</span> <span class="token string">"快点发货"</span>
    <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="奖品申请发货">4.4. 奖品申请发货</h3>
<p>URL  : prizes/sendPrizes</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token punctuation">{</span><span class="token string">"prize_ids"</span><span class="token punctuation">:</span><span class="token punctuation">[</span><span class="token number">98</span><span class="token punctuation">,</span><span class="token number">99</span><span class="token punctuation">]</span><span class="token punctuation">,</span><span class="token string">"address_id"</span><span class="token punctuation">:</span><span class="token number">3</span><span class="token punctuation">,</span> <span class="token string">"comment"</span><span class="token punctuation">:</span> <span class="token string">"快点发货"</span><span class="token punctuation">}</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"invoice_id"</span><span class="token punctuation">:</span> <span class="token number">3</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="通过奖品状态获取奖品列表">4.5. 通过奖品状态获取奖品列表</h3>
<p>奖品状态：<br>
“0”: “未处理”,<br>
“1”: “已兑换娃娃币”,<br>
“2”: “等待发货”,<br>
“3”: “发货中”,<br>
“4”: “已送达”</p>
<p>URL  : prizes/getPrizesByStatus</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token string">"pageindex"</span><span class="token punctuation">:</span><span class="token number">0</span><span class="token punctuation">,</span><span class="token string">"pagecount"</span><span class="token punctuation">:</span><span class="token number">6</span><span class="token punctuation">,</span><span class="token string">"status"</span><span class="token punctuation">:</span><span class="token number">0</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"prizes"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">414</span><span class="token punctuation">,</span>
            <span class="token string">"userId"</span><span class="token punctuation">:</span> <span class="token number">32</span><span class="token punctuation">,</span>
            <span class="token string">"dollTypeId"</span><span class="token punctuation">:</span> <span class="token number">6</span><span class="token punctuation">,</span>
            <span class="token string">"clawRecordId"</span><span class="token punctuation">:</span> <span class="token number">729</span><span class="token punctuation">,</span>
            <span class="token string">"status"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
            <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-12-25T16:33:10.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-12-25T16:33:10.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"statusText"</span><span class="token punctuation">:</span> <span class="token string">"未处理"</span><span class="token punctuation">,</span>
            <span class="token string">"remainDays"</span><span class="token punctuation">:</span> <span class="token number">5</span>
        <span class="token punctuation">}</span>
    <span class="token punctuation">]</span><span class="token punctuation">,</span>
    <span class="token string">"count"</span><span class="token punctuation">:</span> <span class="token number">1</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="通过id获取奖品信息">4.6. 通过id获取奖品信息</h3>
<p>URL  : prizes/getPrizesByIds</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span><span class="token string">"prize_ids"</span><span class="token punctuation">:</span><span class="token punctuation">[</span><span class="token number">98</span><span class="token punctuation">,</span><span class="token number">99</span><span class="token punctuation">]</span><span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"errcode"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
    <span class="token string">"prizes"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
        <span class="token punctuation">{</span>
            <span class="token string">"id"</span><span class="token punctuation">:</span> <span class="token number">414</span><span class="token punctuation">,</span>
            <span class="token string">"userId"</span><span class="token punctuation">:</span> <span class="token number">32</span><span class="token punctuation">,</span>
            <span class="token string">"dollTypeId"</span><span class="token punctuation">:</span> <span class="token number">6</span><span class="token punctuation">,</span>
            <span class="token string">"clawRecordId"</span><span class="token punctuation">:</span> <span class="token number">729</span><span class="token punctuation">,</span>
            <span class="token string">"status"</span><span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
            <span class="token string">"createTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-12-25T16:33:10.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"updateTime"</span><span class="token punctuation">:</span> <span class="token string">"2017-12-25T16:33:10.000Z"</span><span class="token punctuation">,</span>
            <span class="token string">"statusText"</span><span class="token punctuation">:</span> <span class="token string">"未处理"</span><span class="token punctuation">,</span>
            <span class="token string">"remainDays"</span><span class="token punctuation">:</span> <span class="token number">5</span>
        <span class="token punctuation">}</span>
    <span class="token punctuation">]</span><span class="token punctuation">,</span>
    <span class="token string">"count"</span><span class="token punctuation">:</span> <span class="token number">1</span>
<span class="token punctuation">}</span>
</code></pre>
<h3 id="通过发货单id获取快递信息">4.7. 通过发货单id获取快递信息</h3>
<p>URL  : prizes/getExpressInfoByInvoiceId</p>
<p>输入</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
	<span class="token string">"invoice_id"</span><span class="token punctuation">:</span><span class="token number">1</span>
<span class="token punctuation">}</span>
</code></pre>
<p>输出</p>
<pre class=" language-json"><code class="prism  language-json"><span class="token punctuation">{</span>
    <span class="token string">"expressCompany"</span><span class="token punctuation">:</span> <span class="token string">"顺丰"</span><span class="token punctuation">,</span>
    <span class="token string">"expressNumber"</span><span class="token punctuation">:</span> <span class="token string">"1234215"</span><span class="token punctuation">,</span>
    <span class="token string">"traces"</span><span class="token punctuation">:</span> <span class="token punctuation">[</span>
        <span class="token punctuation">{</span>
            <span class="token string">"AcceptTime"</span><span class="token punctuation">:</span> <span class="token string">"2014/06/25 08:05:37"</span><span class="token punctuation">,</span>
            <span class="token string">"AcceptStation"</span><span class="token punctuation">:</span> <span class="token string">"正在派件..(派件人:邓裕富,电话:18718866310)[深圳 市]"</span><span class="token punctuation">,</span>
            <span class="token string">"Remark"</span><span class="token punctuation">:</span> <span class="token keyword">null</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"AcceptTime"</span><span class="token punctuation">:</span> <span class="token string">"2014/06/25 04:01:28"</span><span class="token punctuation">,</span>
            <span class="token string">"AcceptStation"</span><span class="token punctuation">:</span> <span class="token string">"快件在 深圳集散中心 ,准备送往下一站 深圳 [深圳市]"</span><span class="token punctuation">,</span>
            <span class="token string">"Remark"</span><span class="token punctuation">:</span> <span class="token keyword">null</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"AcceptTime"</span><span class="token punctuation">:</span> <span class="token string">"2014/06/25 01:41:06"</span><span class="token punctuation">,</span>
            <span class="token string">"AcceptStation"</span><span class="token punctuation">:</span> <span class="token string">"快件在 深圳集散中心 [深圳市]"</span><span class="token punctuation">,</span>
            <span class="token string">"Remark"</span><span class="token punctuation">:</span> <span class="token keyword">null</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        <span class="token punctuation">{</span>
            <span class="token string">"AcceptTime"</span><span class="token punctuation">:</span> <span class="token string">"2014/06/24 20:18:58"</span><span class="token punctuation">,</span>
            <span class="token string">"AcceptStation"</span><span class="token punctuation">:</span> <span class="token string">"已收件[深圳市]"</span><span class="token punctuation">,</span>
            <span class="token string">"Remark"</span><span class="token punctuation">:</span> <span class="token keyword">null</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
 
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTM1MDk3NTg5N119
-->