  patterns:
    - "/**/*.md"
  files:
    - path: README.md
      render_and_split:
        - to: getting_started.htmf
          start_at: "a[name='installation']"
          stop_before: "a[name='troubleshooting_guide']"
          heading: Getting Started
    - path: Advanced.md
      render_and_split: true #Use automatic convention, a[name='split-installation'] a[name-'split-installation-stop']

    - path: Plugins/AdvancedFilters/Readme.md
      to: plugins/advancedfilters.md

    - path: Contrib/PdfRenderer/License.md
      to: /licenses/pdfrenderer.md

    - to: /licenses/pdfrenderer.md
      title: PDF renderer licensing
