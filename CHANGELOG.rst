Change Log
----------

**0.30** (2021-08-18)
- Add support for Swedish smart meters (`pull request #86 <https://github.com/ndokter/dsmr_parser/pull/86>`_).

**0.29** (2021-04-18)
- Add value and unit properties to ProfileGenericObject to make sure that code like iterators that rely on that do not break (`pull request #71 <https://github.com/ndokter/dsmr_parser/pull/71>`_).
Remove deprecated asyncio coroutine decorator (`pull request #76 <https://github.com/ndokter/dsmr_parser/pull/76>`_).

**0.28** (2021-02-21)
- Optional keep alive monitoring for TCP/IP connections (`pull request #73 <https://github.com/ndokter/dsmr_parser/pull/73>`_).
- Catch parse errors in TelegramParser, ignore lines that can not be parsed (`pull request #74 <https://github.com/ndokter/dsmr_parser/pull/74>`_).

**0.27** (2020-12-24)
- fix for empty parentheses in ProfileGenericParser (redone) (`pull request #69 <https://github.com/ndokter/dsmr_parser/pull/69>`_).

**0.26** (2020-12-15)
- reverted fix for empty parentheses in ProfileGenericParser (`pull request #68 <https://github.com/ndokter/dsmr_parser/pull/68>`_).

**0.25** (2020-12-14)
- fix for empty parentheses in ProfileGenericParser (`pull request #57 <https://github.com/ndokter/dsmr_parser/pull/57>`_).

**0.24** (2020-11-27)
- Add Luxembourg equipment identifier (`pull request #62 <https://github.com/ndokter/dsmr_parser/pull/62>`_).

**0.23** (2020-11-07)
- Resolved issue with x-x:24.3.0 where it contains non-integer character (`pull request #61 <https://github.com/ndokter/dsmr_parser/pull/61>`_).
- Tests are not installed anymore (`pull request #59 <https://github.com/ndokter/dsmr_parser/pull/59>`_).
- Example telegram improvement (`pull request #58 <https://github.com/ndokter/dsmr_parser/pull/58>`_).

**0.22** (2020-08-23)

- CRC check speed is improved
- Exception info improvement

**0.21** (2020-05-25)

- All objects can produce a json serialization of their state.

**0.20** (2020-05-12)

- All objects can now print their values
- Add parser + object for generic profile

**0.19** (2020-05-03)

- Add following missing elements to telegram specification v4:
    - SHORT_POWER_FAILURE_COUNT,
    - INSTANTANEOUS_CURRENT_L1,
    - INSTANTANEOUS_CURRENT_L2,
    - INSTANTANEOUS_CURRENT_L3
- Add missing tests + fix small test bugs
- Complete telegram object v4 parse test

**0.18** (2020-01-28)

- PyCRC replacement (`pull request #48 <https://github.com/ndokter/dsmr_parser/pull/48>`_).

**0.17** (2019-12-21)

- Add a true telegram object (`pull request #40 <https://github.com/ndokter/dsmr_parser/pull/40>`_).

**0.16** (2019-12-21)

- Add support for Belgian and Smarty meters (`pull request #44 <https://github.com/ndokter/dsmr_parser/pull/44>`_).

**0.15** (2019-12-12)

- Fixed asyncio loop issue (`pull request #43 <https://github.com/ndokter/dsmr_parser/pull/43>`_).

**0.14** (2019-10-08)

- Changed serial reading to reduce CPU usage (`pull request #37 <https://github.com/ndokter/dsmr_parser/pull/37>`_).

**0.13** (2019-03-04)

- Fix DSMR v5.0 serial settings which were not used (`pull request #33 <https://github.com/ndokter/dsmr_parser/pull/33>`_).

**0.12** (2018-09-23)

- Add serial settings for DSMR v5.0 (`pull request #31 <https://github.com/ndokter/dsmr_parser/pull/31>`_).
- Lux-creos-obis-1.8.0 (`pull request #32 <https://github.com/ndokter/dsmr_parser/pull/32>`_). 

**0.11** (2017-09-18)

- NULL value fix in checksum (`pull request #26 <https://github.com/ndokter/dsmr_parser/pull/26>`_)

**0.10** (2017-06-05)

- bugfix: don't force full telegram signatures (`pull request #25 <https://github.com/ndokter/dsmr_parser/pull/25>`_)
- removed unused code for automatic telegram detection as this needs reworking after the fix mentioned above
- InvalidChecksumError's are logged as warning instead of error

**0.9** (2017-05-12)

- added DSMR v5 serial settings

**0.8** (2017-01-26)

- added support for DSMR v3
- added support for DSMR v5

**IMPORTANT: this release has the following backwards incompatible changes:**

- Removed TelegramParserV2_2 in favor of TelegramParser
- Removed TelegramParserV4 in favor of TelegramParser

**0.7** (2017-01-14)

- Internal refactoring related to the way clients feed their data into the parse module. Clients can now supply the telegram data in single characters, lines (which was common) or complete telegram strings. (`pull request #17 <https://github.com/ndokter/dsmr_parser/pull/17>`_)

**IMPORTANT: this release has the following backwards incompatible changes:**

- Client related imports from dsmr_parser.serial and dsmr_parser.protocol have been moved to dsmr_parser.clients (import these from the clients/__init__.py module)
- The .parse() method of TelegramParser, TelegramParserV2_2, TelegramParserV4 now accepts a string containing the entire telegram (including \r\n characters) and not a list


**0.6** (2017-01-04)

- Fixed bug in CRC checksum verification for the asyncio client (`pull request #15 <https://github.com/ndokter/dsmr_parser/pull/15>`_)
- Support added for TCP connections using the asyncio client (`pull request #12 <https://github.com/ndokter/dsmr_parser/pull/12/>`_)

**0.5** (2016-12-29)

- CRC checksum verification for DSMR v4 telegrams (`issue #10 <https://github.com/ndokter/dsmr_parser/issues/10>`_)

**0.4** (2016-11-21)

- DSMR v2.2 serial settings now uses parity serial.EVEN by default (`pull request #5 <https://github.com/ndokter/dsmr_parser/pull/5>`_)
- improved asyncio reader and improve it's error handling (`pull request #8 <https://github.com/ndokter/dsmr_parser/pull/8>`_)

**0.3** (2016-11-12)

- asyncio reader for non-blocking reads (`pull request #3 <https://github.com/ndokter/dsmr_parser/pull/3>`_)

**0.2** (2016-11-08)

- support for DMSR version 2.2 (`pull request #2 <https://github.com/ndokter/dsmr_parser/pull/2>`_)

**0.1** (2016-08-22)

- initial version with a serial reader and support for DSMR version 4.x
