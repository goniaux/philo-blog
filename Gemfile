source "https://rubygems.org"

# Ce gem installe exactement la même version de Jekyll et les mêmes plugins
# que ceux utilisés par GitHub Pages en production. Cela évite les surprises
# entre ce que tu vois en local et ce qui est publié en ligne.
gem "github-pages", group: :jekyll_plugins

group :jekyll_plugins do
  gem "jekyll-paginate"
  gem "jekyll-seo-tag"
  gem "jekyll-sitemap"
  gem "jekyll-feed"
end

# Nécessaire sur certains systèmes récents (Windows notamment)
gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]

# Corrige un souci de compatibilité Ruby 3.x
gem "webrick"
