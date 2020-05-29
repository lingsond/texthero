---
id: texthero.visualization.wordcloud
title: visualization.wordcloud
hide_title: true
---

<div>
<div class="section" id="texthero-visualization-wordcloud">
<h1>texthero.visualization.wordcloud<a class="headerlink" href="#texthero-visualization-wordcloud" title="Permalink to this headline">¶</a></h1>
<dl class="py function">
<dt id="texthero.visualization.wordcloud">
<code class="sig-name descname">wordcloud</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">s</span><span class="p">:</span> <span class="n">pandas.core.series.Series</span></em>, <em class="sig-param"><span class="n">font_path</span><span class="p">:</span> <span class="n">str</span> <span class="o">=</span> <span class="default_value">None</span></em>, <em class="sig-param"><span class="n">width</span><span class="p">:</span> <span class="n">int</span> <span class="o">=</span> <span class="default_value">400</span></em>, <em class="sig-param"><span class="n">height</span><span class="p">:</span> <span class="n">int</span> <span class="o">=</span> <span class="default_value">200</span></em>, <em class="sig-param"><span class="n">margin</span><span class="o">=</span><span class="default_value">2</span></em>, <em class="sig-param"><span class="n">ranks_only</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">prefer_horizontal</span><span class="o">=</span><span class="default_value">0.9</span></em>, <em class="sig-param"><span class="n">mask</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">scale</span><span class="o">=</span><span class="default_value">1</span></em>, <em class="sig-param"><span class="n">color_func</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">max_words</span><span class="o">=</span><span class="default_value">200</span></em>, <em class="sig-param"><span class="n">min_font_size</span><span class="o">=</span><span class="default_value">4</span></em>, <em class="sig-param"><span class="n">stopwords</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">random_state</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">background_color</span><span class="o">=</span><span class="default_value">'black'</span></em>, <em class="sig-param"><span class="n">max_font_size</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">font_step</span><span class="o">=</span><span class="default_value">1</span></em>, <em class="sig-param"><span class="n">mode</span><span class="o">=</span><span class="default_value">'RGB'</span></em>, <em class="sig-param"><span class="n">relative_scaling</span><span class="o">=</span><span class="default_value">'auto'</span></em>, <em class="sig-param"><span class="n">regexp</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">collocations</span><span class="o">=</span><span class="default_value">True</span></em>, <em class="sig-param"><span class="n">colormap</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">normalize_plurals</span><span class="o">=</span><span class="default_value">True</span></em>, <em class="sig-param"><span class="n">contour_width</span><span class="o">=</span><span class="default_value">0</span></em>, <em class="sig-param"><span class="n">contour_color</span><span class="o">=</span><span class="default_value">'black'</span></em>, <em class="sig-param"><span class="n">repeat</span><span class="o">=</span><span class="default_value">False</span></em>, <em class="sig-param"><span class="n">include_numbers</span><span class="o">=</span><span class="default_value">False</span></em>, <em class="sig-param"><span class="n">min_word_length</span><span class="o">=</span><span class="default_value">0</span></em>, <em class="sig-param"><span class="n">collocation_threshold</span><span class="o">=</span><span class="default_value">30</span></em>, <em class="sig-param"><span class="n">return_figure</span><span class="o">=</span><span class="default_value">False</span></em><span class="sig-paren">)</span><a class="headerlink" href="#texthero.visualization.wordcloud" title="Permalink to this definition">¶</a></dt>
<dd><p>Plot wordcloud image using WordCloud from word_cloud package.</p>
<p>Most of the arguments are very similar if not equal to the mother function. In constrast, all words are taken into account when computing the wordcloud, inclusive stopwords. They can be easily removed with preprocessing.remove_stopwords.</p>
<p>Word are compute using generate_from_frequencies.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><dl class="simple">
<dt><strong>s</strong><span class="classifier">pd.Series</span></dt><dd></dd>
<dt><strong>font_path</strong><span class="classifier">str</span></dt><dd><p>Font path to the font that will be used (OTF or TTF). Defaults to DroidSansMono path on a Linux machine. If you are on another OS or don’t have this font, you need to adjust this path.</p>
</dd>
<dt><strong>width</strong><span class="classifier">int</span></dt><dd><p>Width of the canvas.</p>
</dd>
<dt><strong>height</strong><span class="classifier">int</span></dt><dd><p>Height of the canvas.</p>
</dd>
<dt><strong>max_words</strong><span class="classifier">number (default=200)</span></dt><dd><p>The maximum number of words.</p>
</dd>
<dt><strong>mask</strong><span class="classifier">nd-array or None (default=None)</span></dt><dd><p>When set, gives a binary mask on where to draw words. When set, width and height will be ignored and the shape of mask will be used instead. All white (#FF or #FFFFFF) entries will be considerd “masked out” while other entries will be free to draw on.</p>
</dd>
<dt><strong>contour_width: float (default=0)</strong></dt><dd><p>If mask is not None and contour_width &gt; 0, draw the mask contour.</p>
</dd>
<dt><strong>contour_color: color value (default=”black”)</strong></dt><dd><p>Mask contour color.</p>
</dd>
<dt><strong>min_font_size</strong><span class="classifier">int (default=4)</span></dt><dd><p>Smallest font size to use. Will stop when there is no more room in this size.</p>
</dd>
<dt><strong>background_color</strong><span class="classifier">color value (default=”black”)</span></dt><dd><p>Background color for the word cloud image.</p>
</dd>
<dt><strong>max_font_size</strong><span class="classifier">int or None (default=None)</span></dt><dd><p>Maximum font size for the largest word. If None, height of the image is used.</p>
</dd>
<dt><strong>relative_scaling</strong><span class="classifier">float (default=’auto’)</span></dt><dd><p>Importance of relative word frequencies for font-size.  With
relative_scaling=0, only word-ranks are considered.  With
relative_scaling=1, a word that is twice as frequent will have twice
the size.  If you want to consider the word frequencies and not only
their rank, relative_scaling around .5 often looks good.
If ‘auto’ it will be set to 0.5 unless repeat is true, in which
case it will be set to 0.</p>
</dd>
<dt><strong>colormap</strong><span class="classifier">string or matplotlib colormap, default=”viridis”</span></dt><dd><p>Matplotlib colormap to randomly draw colors from for each word.</p>
</dd>
</dl>
</dd>
</dl>
</dd></dl>
</div>
</div>