# doc_loader/

## `UncommonDocLoader` 
doc loader for uncommon document formats: .epub, .csv, .json, .xml, .rst, .tex

- `__init__`(self, path: Union[str, Path], encoding: str = "utf-8")

- load(self) -> List[str]

- _load_epub(self, path: Path) -> str

- _load_csv(self, path: Path) -> str

- _load_json(self, path: Path) -> str

- _load_xml(self, path: Path) -> str

- _load_plaintext(self, path: Path) -> str

## `UniversalDocLoader` 
universal document loader supporting .txt, .md, .pdf, .docx, .html

* `__init__`(self, path: Union[str, Path], encoding: str = "utf-8")

* load(self) -> List[str]

* _load_txt(self, path: Path) -> str

* _load_pdf(self, path: Path) -> str

* _load_docx(self, path: Path) -> str

* _load_html(self, path: Path) -> str
