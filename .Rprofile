if (interactive()) {
  source("~/.Rprofile", local = TRUE)
  message("Loading .Rprofile")
  library("blogdown")
  options(blogdown.author = "Lluís Revilla Sancho",
        blogdown.ext = ".Rmd",
        blogdown.knit.on_save = TRUE,
        blogdown.hugo.version = "0.91.2",
        bitmapType = "cairo",
        xfun.bg_process.verbose = TRUE,
        blogdown.use.processx = FALSE)
  }
# Attempt 1
# https://tinyheero.github.io/2015/09/15/semi-transparency-r.html
setHook(packageEvent("grDevices", "onLoad"),
				function(...) grDevices::X11.options(type='cairo'))
options(device='x11')
