window.addEventListener(
  'message',
  function (e) {
    var eventName = e.data[0]
    var data = e.data[1]

    if (eventName === 'lc.setHeight' && data?.id === 'lc_reviews_widget') {
      const reviewIframes = document.querySelectorAll('.lc_reviews_widget, #msgsndr_reviews, #highlevel_reviews')

      if (reviewIframes) {
        for (const reviewIframe of reviewIframes) {
          try {
            if (e.source === reviewIframe.contentWindow) {
              reviewIframe.height = data.height;
              break;
            }
          } catch (e) {
            console.error(e)
          }
        }
      }
    }
  },
  false
)
