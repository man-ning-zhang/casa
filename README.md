# casa

Personal academic website for **Manning Zhang** — medical and cultural sociologist, PhD candidate in Sociology and
Social Policy at Brandeis University.

Built with Jekyll, originally based on the [academicpages](https://github.com/stuartgeiger/academicpages) template.
Live at <https://man-ning-zhang.github.io/casa/>.

## Structure

| Directory | Contents |
| --- | --- |
| `_pages/` | Static pages: about (home), research, publications, writing, CV |
| `_publications/` | One Markdown file per publication (`category:` controls grouping) |
| `_talks/` | One Markdown file per conference presentation |
| `_teaching/` | Teaching and mentorship entries |
| `files/` | CV PDF |
| `images/` | Portrait and favicons |

## Editing

- Add a publication: copy an existing file in `_publications/`, set `category` to `published`, `under-review`, or
  `working`.
- Add a talk: copy an existing file in `_talks/` and fill in `title`, `type`, `venue`, `date`, `location`.
- Site-wide settings (name, email, links, navigation) live in `_config.yml` and `_data/navigation.yml`.

## Running locally

```bash
bundle install
bundle exec jekyll serve
```

Then open <http://localhost:4000/casa/>.
