# Custom EXT Items verlinkbar machen

## TCEMAIN.typoscript

````typoscript
TCEMAIN {
    linkHandler {
        tx_news {
            handler = TYPO3\CMS\Recordlist\LinkHandler\RecordLinkHandler
            label = News
            configuration {
                table = tx_news_domain_model_news
                storagePid = 22
                hidePageTree = 1
            }
            scanAfter = page
        }

        EXTNAME {
            handler = TYPO3\CMS\Recordlist\LinkHandler\RecordLinkHandler
            label = Projects
            configuration {
                table = tx_EXTNAME_domain_model_projects
                storagePid = 25
                hidePageTree = 0
            }
            scanAfter = page
            displayAfter = tx_news
        }
    }
}
````

## Setup.typoscript
```typoscript
config {
	...
		recordLinks {
			tx_news {
				typolink {
					parameter = 24
					additionalParams.data = field:uid
					additionalParams.wrap = &tx_news_pi1[controller]=News&tx_news_pi1[action]=detail&tx_news_pi1[news]=|
					useCacheHash = 1

					ATagParams.data = parameters:allParams
					target.data = parameters:target
					title.data = parameters:title

					extTarget = _blank
					extTarget.override.data = parameters:target
				}
				forceLink = 1
			}

			lap_projects {
				typolink {
					parameter = 26
					additionalParams.data = field:uid
					additionalParams.wrap = &tx_EXTNAME[action]=show&tx_EXTNAME_projects[controller]=Projects&tx_EXTNAME_projects[project]=|
					useCacheHash = 1

					ATagParams.data = parameters:allParams
					target.data = parameters:target
					title.data = parameters:title

					extTarget = _blank
					extTarget.override.data = parameters:target
				}
				forceLink = 1
			}
	}
}
```
