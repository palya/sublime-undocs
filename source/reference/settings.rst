====================
Settings – Reference
====================

.. warning::

   This page may contain outdated or incomplete information.
   You can see a description of most available settings in the
   default settings file (**Preferences → Settings - Default** or
   :file:`Default/Preferences.sublime-settings`).

.. seealso::

   :doc:`Customization - Settings </customization/settings>`
      A detailed overview on settings in Sublime Text and their order of
      precedence.


Global Settings
===============

These settings can only be modified from :file:`Preferences.sublime-settings`
and :file:`Preferences ({platform}).sublime-settings`.

.. XXX obviously, some settings are missing here ... but do we really need to
.. include all the settings with a brief description? That's what the comments
.. in the default settings are for, actually.

.. include:: /_includes/settings_global.g.txt

File Settings
=============

Whitespace and Indentation
**************************


``auto_indent``
   Toggles automatic indentation.
``tab_size``
   Number of spaces a tab is considered equal to.
``translate_tabs_to_spaces``
   Determines whether to replace a tab character with ``tab_size`` number of
   spaces when :kbd:`Tab` is pressed.
``use_tab_stops``
   If ``translate_tabs_to_spaces`` is ``true``, will make :kbd:`Tab` and
   :kbd:`Backspace` insert/delete ``tab_size`` number of spaces per key press.
``trim_automatic_white_space``
   Toggles deletion of white space added by ``auto_indent``.
``detect_indentation``
   Set to ``false`` to disable detection of tabs vs. spaces whenever a buffer
   is loaded. If set to ``true``, it automatically will modify
   ``translate_tabs_to_spaces`` and ``tab_size``.
``draw_white_space``
   Valid values: ``none``, ``selection``, ``all``.
``trim_trailing_white_space_on_save``
   Set to ``true`` to remove white space on save.

Visual Settings
***************
``always_show_minimap_viewport``
  if set to true, then it will always show rectangle on minimap highlighting current document position; defualt false,   which shows position only on mouse over the minimap. 
``color_scheme``
   Sets the colors used for text highlighting. Accepts a path rooted at the
   data directory (e.g.: :file:`Packages/Color Scheme - Default/Monokai Bright.tmTheme`).
``font_face``
   Font face to be used for editable text.
``font_size``
   Size of the font for editable text.
``font_options``
   Valid values: ``bold``, ``italic``, ``no_antialias``, ``gray_antialias``,
   ``subpixel_antialias``, ``directwrite`` (Windows).
``gutter``
   Toggles display of gutter.
``rulers``
   Columns in which to display vertical rules. Accepts a list of numeric values
   (such as ``[79, 89, 99]``) or a single numeric value (for example, ``79``).
``draw_minimap_border``
   Set to ``true`` to draw a border around the minimap's region corresponding
   to the the view's currently visible text. The active color scheme's
   ``minimapBorder`` key controls the border's color.
``highlight_line``
   Set to ``false`` to stop highlighting lines with a cursor.
``line_padding_top``
   Additional spacing at the top of each line, in pixels.
``line_padding_bottom``
   Additional spacing at the bottom of each line, in pixels.
``scroll_past_end``
   Set to ``false`` to disable scrolling past the end of the buffer. If ``true``,
   Sublime Text will leave a wide, empty margin between the last line and the
   bottom of the window.
``line_numbers``
   Toggles display of line numbers in the gutter.
``word_wrap``
   If set to ``false``, long lines will be clipped instead of wrapped. Scroll
   the screen horizontally to see the clipped text.
``wrap_width``
   If greater than ``0``, wraps long lines at the specified column as opposed
   to the window width. Only takes effect if ``word_wrap`` is set to ``true``.
``indent_subsequent_lines``
   If set to ``false``, wrapped lines will not be indented. Only takes effect
   if ``word_wrap`` is set to ``true``.
``draw_centered``
   If set to ``true``, text will be drawn centered rather than left-aligned.
``match_brackets``
   Set to ``false`` to disable underlining the brackets surrounding the cursor.
``match_brackets_content``
   Set this to ``false`` if you'd rather have brackets highlighted only when the
   cursor is next to one.
``match_brackets_square``
   Set to ``false`` to stop highlighting square brackets. Only takes effect if
   ``match_brackets`` is ``true``.
``match_brackets_braces``
   Set to ``false`` to stop highlighting curly brackets. Only takes effect if
   ``match_brackets`` is ``true``.
``match_brackets_angle``
   Set to ``false`` to stop highlighting angle brackets. Only takes effect if
   ``match_brackets`` is ``true``.

Automatic Behavior
******************

``auto_match_enabled``
   Toggles automatic pairing of quotes, brackets, etc.
``save_on_focus_lost``
   Set to true to save files automatically when switching to a different file
   or application.
``find_selected_text``
   If ``true``, the selected text will be copied into the find panel when it's
   shown.
``word_separators``
   Characters considered to divide words for actions like advancing the cursor,
   etc. Not used for every context where a notion of a word separator is
   useful (for example, word wrapping). In some contexts, the text might be
   tokenized based on other criteria (for example, the syntax definition rules).
``ensure_newline_at_eof_on_save``
   Always adds a new line at the end of the file if not present when saving.

System and Miscellaneous Settings
*********************************

``is_widget``
   Returns ``true`` if the buffer is an input field in a dialog, as opposed to
   a regular buffer.
``spell_check``
   Toggles the spell checker.
``dictionary``
   Word list to be used by the spell checker. Accepts a path rooted at the
   data directory (such as :file:`Packages/Language - English/en_US.dic`). You can
   `add more dictionaries <http://extensions.services.openoffice.org/en/dictionaries>`_.
``fallback_encoding``
   The encoding to use when the encoding can't be determined automatically.
   ASCII, UTF-8 and UTF-16 encodings will be detected automatically .
``default_line_ending``
   Determines what characters to use to designate new lines. Valid values:
   ``system`` (OS-dependant), ``windows`` (``CRLF``) and ``unix`` (``LF``).
``tab_completion``
   Determines whether pressing :kbd:`Tab` will insert completions.


Build and Error Navigation Settings
***********************************

``result_file_regex`` and ``result_line_regex``
   Regular expressions used to extract error information from some output dumped
   into a view or output panel. Follows the same rules as :ref:`error capturing
   in build systems <build-capture-error-output>`.
``result_base_dir``
   Folder to start looking for offending files based on information
   extracted with ``result_file_regex`` and ``result_line_regex``.
``build_env``
   List of paths to add to build systems by default.


File and Directory Settings
***************************

``default_dir``
   Sets the default save folder for the view.


Input Settings
**************

``command_mode``
   If set to ``true``, the buffer will ignore key strokes. Useful when emulating
   Vim's modal behavior.
   
``move_to_limit_on_up_down``
   This setting controls what happens when reaching the first or last line by pressing the up or down arrows. 
   If set to ``true`` and the caret is somewhere on the first line, then pressing the up arrow will move
   the caret to the beginning of the line. From somewhere on the last line, the down arrow will
   move the caret to the end of the last line. 
