# Ego - Authentication & Authorization 

<br />

<a href="https://www.overture.bio/"><img src="data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz4KPHN2ZyB3aWR0aD0iMTY4cHgiIGhlaWdodD0iMzJweCIgdmlld0JveD0iMCAwIDE2OCAzMiIgdmVyc2lvbj0iMS4xIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIj4KICAgIDwhLS0gR2VuZXJhdG9yOiBTa2V0Y2ggNDkuMyAoNTExNjcpIC0gaHR0cDovL3d3dy5ib2hlbWlhbmNvZGluZy5jb20vc2tldGNoIC0tPgogICAgPHRpdGxlPlBhZ2UgMTwvdGl0bGU+CiAgICA8ZGVzYz5DcmVhdGVkIHdpdGggU2tldGNoLjwvZGVzYz4KICAgIDxkZWZzPjwvZGVmcz4KICAgIDxnIGlkPSJTeW1ib2xzIiBzdHJva2U9Im5vbmUiIHN0cm9rZS13aWR0aD0iMSIgZmlsbD0ibm9uZSIgZmlsbC1ydWxlPSJldmVub2RkIj4KICAgICAgICA8ZyBpZD0ibmF2aS1iYXItLS1wcm9kdWN0cyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoLTE4LjAwMDAwMCwgLTE5LjAwMDAwMCkiPgogICAgICAgICAgICA8ZyBpZD0iUGFnZS0xIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxOS4wMDAwMDAsIDIwLjAwMDAwMCkiPgogICAgICAgICAgICAgICAgPHBhdGggZD0iTTI3LjQxMTMzNzMsMTMuMzcyMzAzIEMyNS41NDg5Mjk2LDE4LjU2OTk2NzMgMTkuODI1NDI2LDIxLjI3Mzc2NzkgMTQuNjI3NzMzMywxOS40MTEzNzA0IEM5LjQzMDA0MDUxLDE3LjU0ODk3MjkgNi43MjYyMjUwOCwxMS44MjU1MDA2IDguNTg4NjMyNzksNi42Mjc4MzYzNiBDMTAuNDUxMDQwNSwxLjQyOTg5NjIgMTYuMTc0NTQ0MSwtMS4yNzM5MDQ0NCAyMS4zNzIyMzY5LDAuNTg4NzY4OTUyIEMyNi41NzAyMDU1LDIuNDUxMTY2NDcgMjkuMjczNzQ1LDguMTc0NjM4NzQgMjcuNDExMzM3MywxMy4zNzIzMDMiIGlkPSJGaWxsLTEiIGZpbGw9IiNEOUUwMjEiPjwvcGF0aD4KICAgICAgICAgICAgICAgIDxwYXRoIGQ9Ik0xOS40MTEzNjcyLDIwLjM3MjA3NDIgQzE3LjU0ODk1OTUsMjUuNTY5OTc5NiAxMS44MjU0NTU5LDI4LjI3Mzc2MjEgNi42Mjc3NjMxNCwyNi40MTEzNzcxIEMxLjQyOTc5NDUyLDI0LjU0ODcxNjIgLTEuMjczNzQ1MDQsMTguODI1NTU4IDAuNTg4NjYyNjcxLDEzLjYyNzY1MjYgQzIuNDUxMDcwMzgsOC40MzAwMjMxMiA4LjE3NDU3Mzk5LDUuNzI2MjQwNTcgMTMuMzcyMjY2Nyw3LjU4ODYyNTYzIEMxOC41Njk5NTk1LDkuNDUxMDEwNjkgMjEuMjczNzc0OSwxNS4xNzQ0NDQ3IDE5LjQxMTM2NzIsMjAuMzcyMDc0MiIgaWQ9IkZpbGwtMyIgZmlsbD0iIzlFMDA1RCI+PC9wYXRoPgogICAgICAgICAgICAgICAgPHBhdGggZD0iTTI4LjQxMTMzNzMsMjMuMzcyMDc0MiBDMjYuNTQ4OTI5NiwyOC41Njk5Nzk2IDIwLjgyNTQyNiwzMS4yNzM3NjIxIDE1LjYyNzczMzMsMjkuNDExMzc3MSBDMTAuNDMwMDQwNSwyNy41NDg3MTYyIDcuNzI2MjI1MDgsMjEuODI1NTU4IDkuNTg4NjMyNzksMTYuNjI3NjUyNiBDMTEuNDUxMDQwNSwxMS40MzAwMjMxIDE3LjE3NDU0NDEsOC43MjYyNDA1NyAyMi4zNzIyMzY5LDEwLjU4ODYyNTYgQzI3LjU3MDIwNTUsMTIuNDUxMDEwNyAzMC4yNzM3NDUsMTguMTc0NDQ0NyAyOC40MTEzMzczLDIzLjM3MjA3NDIiIGlkPSJGaWxsLTUiIGZpbGw9IiMyOUFCRTIiPjwvcGF0aD4KICAgICAgICAgICAgICAgIDxwYXRoIGQ9Ik0yNy42NTI2ODE4LDEyLjYwMzIyNzggQzI2LjIxNTA4MzYsMTcuOTMzOTkwNiAyMC43Mjc4Nzc4LDIxLjA5MDI5NDQgMTUuMzk2ODE4OCwxOS42NTI3MDE2IEMxMC4wNjU3NTk5LDE4LjIxNDgzMyA2LjkwOTcxOTk2LDEyLjcyNzY0ODIgOC4zNDczMTgyLDcuMzk2ODg1MzYgQzkuNzg0OTE2NDUsMi4wNjU4NDY2OCAxNS4yNzIzOTgsLTEuMDkwNDU3MDYgMjAuNjAzMTgxMiwwLjM0NzQxMTU3NiBDMjUuOTM0MjQwMSwxLjc4NTAwNDM0IDI5LjA5MDI4LDcuMjcyMTg5MTYgMjcuNjUyNjgxOCwxMi42MDMyMjc4IFoiIGlkPSJTdHJva2UtNyIgc3Ryb2tlPSIjRkZGRkZGIiBzdHJva2UtbGluZWNhcD0icm91bmQiPjwvcGF0aD4KICAgICAgICAgICAgICAgIDxwYXRoIGQ9Ik0zNy42NzY5OTMxLDE1LjAzNzIwNjUgQzM3LjY3Njk5MzEsMTguOTU4MzA4NSA0MC43NzAxMTM3LDIyLjQzMTI4NDYgNDQuODMyMTYzNywyMi40MzEyODQ2IEM0OS4wNDMyNzk3LDIyLjQzMTI4NDYgNTIuMzIzMDA2OSwxOS4yMTk3MTUzIDUyLjMyMzAwNjksMTUuMDM3MjA2NSBDNTIuMzIzMDA2OSwxMC43ODAwMTAxIDQ5LjA4MDU0NjIsNy41Njg0NDA4IDQ0LjgzMjE2MzcsNy41Njg0NDA4IEM0MC43MzI4NDcyLDcuNTY4NDQwOCAzNy42NzY5OTMxLDExLjA0MTE0MjMgMzcuNjc2OTkzMSwxNS4wMzcyMDY1IE01NCwxNC45OTk1ODgxIEM1NCwyMC4xMTU5NjcyIDUwLjAxMjQ4MzEsMjQgNDQuOTQzOTYzMiwyNCBDMzkuOTg3NTE2OSwyNCAzNiwxOS45MjkyNDgxIDM2LDE1LjAzNzIwNjUgQzM2LDEwLjA3MDQ3NzMgMzkuOTUwMjUwNCw2IDQ0Ljk0Mzk2MzIsNiBDNTAuMDEyNDgzMSw2IDU0LDkuODgzNDgzNTkgNTQsMTQuOTk5NTg4MSIgaWQ9IkZpbGwtOSIgZmlsbD0iIzI5QUJFMiI+PC9wYXRoPgogICAgICAgICAgICAgICAgPHBvbHlnb24gaWQ9IkZpbGwtMTEiIGZpbGw9IiMyOUFCRTIiIHBvaW50cz0iNjMuMDU2NzM1NiAyMC4wODIxMzU1IDY5LjI1OTgyOTcgNiA3MSA2IDYzLjAxODkxMTkgMjQgNTUgNiA1Ni43NDAxNzAzIDYiPjwvcG9seWdvbj4KICAgICAgICAgICAgICAgIDxwYXRoIGQ9Ik04OC4yODQ0NzU1LDEzLjU4MDYzODMgQzg3Ljg2NTIwODMsMTAuNDA2MzY0NCA4NS4xOTcxNDQzLDcuNTY4MTkwMTQgODEuNTc1OTIsNy41NjgxOTAxNCBDNzcuOTkzMDkxMiw3LjU2ODE5MDE0IDc1LjAyMDM4NTksMTAuMzMxNjc1NiA3NC43MTUxODQsMTMuNTgwNjM4MyBMODguMjg0NDc1NSwxMy41ODA2MzgzIFogTTc0LjcxNTE4NCwxNS4xNDkzNzc2IEM3NC42MDExMTg3LDE5LjUxODY3MjIgNzcuNjg4MTY5NiwyMi40MzEyNjA3IDgxLjc2Njc3NjMsMjIuNDMxMjYwNyBDODQuNTExMDcwNywyMi40MzEyNjA3IDg2LjcyMTc1MjMsMjAuODI1NzI2MSA4Ny45Nzk1NTM5LDE4LjUxMDM3MzQgTDg5LjQyNzkzMTUsMTkuMzMxOTUwMiBDODcuODI3MDkzMSwyMi4zMTkyMjc1IDg1LjAwNjU2ODMsMjQgODEuNTM4MDg1MSwyNCBDNzYuMzE2MzAyNywyNCA3MywxOS44NTQ3NzE4IDczLDE0Ljk2MjY1NTYgQzczLDEwLjE0NDk1MzYgNzYuMzkyMjUyOCw2IDgxLjUzODA4NTEsNiBDODYuODc0MjEzMSw2IDkwLjAzNzc3NDcsMTAuMTgyNTcyNiA4OS45OTk2NTk1LDE1LjE0OTM3NzYgTDc0LjcxNTE4NCwxNS4xNDkzNzc2IFoiIGlkPSJGaWxsLTEzIiBmaWxsPSIjMjlBQkUyIj48L3BhdGg+CiAgICAgICAgICAgICAgICA8cGF0aCBkPSJNOTUuODM2NjY1OCw4LjY2OTQ0OTk0IEw5NS45MTgyOTU0LDguNjY5NDQ5OTQgQzk2LjY1MzI2MTgsNy4wNjc3Nzk5OCA5Ny45OTk4NDk5LDYgOTkuOTk5Nzc0OSw2IEMxMDAuNzM0NDQxLDYgMTAxLjM0NjY2Myw2LjE1MjI1OTU5IDEwMiw2LjQxOTc2NTM5IEwxMDEuMDIwMTQ1LDcuOTQ0ODg0OTYgQzEwMC41NzExODIsNy43MTYwNzQ5NiAxMDAuMjA0MTQ5LDcuNjAxNjY5OTYgOTkuNzE0MzcxNSw3LjYwMTY2OTk2IEM5NS41OTIwNzcxLDcuNjAxNjY5OTYgOTUuODM2NjY1OCwxMi40MDY2Nzk5IDk1LjgzNjY2NTgsMTQuOTk5ODU5OCBMOTUuODM2NjY1OCwyNCBMOTQsMjQgTDk0LDYuMzgxMzQ5OTkgTDk1LjgzNjY2NTgsNi4zODEzNDk5OSBMOTUuODM2NjY1OCw4LjY2OTQ0OTk0IFoiIGlkPSJGaWxsLTE1IiBmaWxsPSIjMjlBQkUyIj48L3BhdGg+CiAgICAgICAgICAgICAgICA8cG9seWdvbiBpZD0iRmlsbC0xNyIgZmlsbD0iIzI5QUJFMiIgcG9pbnRzPSIxMDguNzk2NzQzIDIzIDEwNy4wMTcxNTYgMjMgMTA3LjAxNzE1NiA3LjU5MzMwMTQ0IDEwNSA3LjU5MzMwMTQ0IDEwNSA2LjA1MjM2MTg1IDEwNy4wMTcxNTYgNi4wNTIzNjE4NSAxMDcuMDE3MTU2IDAgMTA4Ljc5Njc0MyAwIDEwOC43OTY3NDMgNi4wNTIzNjE4NSAxMTIgNi4wNTIzNjE4NSAxMTIgNy41OTMzMDE0NCAxMDguNzk2NzQzIDcuNTkzMzAxNDQiPjwvcG9seWdvbj4KICAgICAgICAgICAgICAgIDxwYXRoIGQ9Ik0xMzEuOTk5ODM3LDYgTDEzMS45OTk4MzcsMTYuNTYzNjc1MiBDMTMxLjk5OTgzNywxOC4zNTU3Mzk3IDEzMi4wMzg5OTMsMjAuMTQ4MzY1MSAxMzAuOTAzMTkxLDIxLjYzNTYzMDEgQzEyOS42NTA0OTksMjMuMjM3MyAxMjcuNTM2MDk1LDI0IDEyNS41MDAwMDIsMjQgQzEyMy40NjM5MDksMjQgMTIxLjM0OTUwNSwyMy4yMzczIDEyMC4wOTYyMzYsMjEuNjM1NjMwMSBDMTE4Ljk2MDcyMywyMC4xNDgzNjUxIDExOS4wMDAxNjYsMTguMzU1NzM5NyAxMTkuMDAwMTY2LDE2LjU2MzY3NTIgTDExOS4wMDAxNjYsNiBMMTIwLjc2MjE3LDYgTDEyMC43NjIxNywxNS45NTMyMzQ4IEMxMjAuNzYyMTcsMTkuMzQ3NTMwMSAxMjEuMTUzNDM4LDIyLjM5ODA0OTYgMTI1LjUwMDAwMiwyMi4zOTgwNDk2IEMxMjkuODQ2Mjc3LDIyLjM5ODA0OTYgMTMwLjIzNzgzNCwxOS4zNDc1MzAxIDEzMC4yMzc4MzQsMTUuOTUzMjM0OCBMMTMwLjIzNzgzNCw2IEwxMzEuOTk5ODM3LDYgWiIgaWQ9IkZpbGwtMTkiIGZpbGw9IiMyOUFCRTIiPjwvcGF0aD4KICAgICAgICAgICAgICAgIDxwYXRoIGQ9Ik0xNDAuODM2NjY2LDguNjY5NDQ5OTQgTDE0MC45MTgyOTUsOC42Njk0NDk5NCBDMTQxLjY1MzI2Miw3LjA2Nzc3OTk4IDE0Mi45OTk4NSw2IDE0NC45OTk3NzUsNiBDMTQ1LjczNDQ0MSw2IDE0Ni4zNDY2NjMsNi4xNTIyNTk1OSAxNDcsNi40MTk3NjUzOSBMMTQ2LjAyMDE0NSw3Ljk0NDg4NDk2IEMxNDUuNTcxMTgyLDcuNzE2MDc0OTYgMTQ1LjIwNDE0OSw3LjYwMTY2OTk2IDE0NC43MTQzNzEsNy42MDE2Njk5NiBDMTQwLjU5MjA3Nyw3LjYwMTY2OTk2IDE0MC44MzY2NjYsMTIuNDA2Njc5OSAxNDAuODM2NjY2LDE0Ljk5OTg1OTggTDE0MC44MzY2NjYsMjQgTDEzOSwyNCBMMTM5LDYuMzgxMzQ5OTkgTDE0MC44MzY2NjYsNi4zODEzNDk5OSBMMTQwLjgzNjY2Niw4LjY2OTQ0OTk0IFoiIGlkPSJGaWxsLTIxIiBmaWxsPSIjMjlBQkUyIj48L3BhdGg+CiAgICAgICAgICAgICAgICA8cGF0aCBkPSJNMTY1LjI4NDQ3NSwxMy41ODA2MzgzIEMxNjQuODY1MjA4LDEwLjQwNjM2NDQgMTYyLjE5NzE0NCw3LjU2ODE5MDE0IDE1OC41NzU5Miw3LjU2ODE5MDE0IEMxNTQuOTkzMDkxLDcuNTY4MTkwMTQgMTUyLjAyMDM4NiwxMC4zMzE2NzU2IDE1MS43MTUxODQsMTMuNTgwNjM4MyBMMTY1LjI4NDQ3NSwxMy41ODA2MzgzIFogTTE1MS43MTUxODQsMTUuMTQ5Mzc3NiBDMTUxLjYwMTExOSwxOS41MTg2NzIyIDE1NC42ODgxNywyMi40MzEyNjA3IDE1OC43NjY3NzYsMjIuNDMxMjYwNyBDMTYxLjUxMTA3MSwyMi40MzEyNjA3IDE2My43MjE3NTIsMjAuODI1NzI2MSAxNjQuOTc5NTU0LDE4LjUxMDM3MzQgTDE2Ni40Mjc5MzEsMTkuMzMxOTUwMiBDMTY0LjgyNzA5MywyMi4zMTkyMjc1IDE2Mi4wMDY1NjgsMjQgMTU4LjUzODA4NSwyNCBDMTUzLjMxNjMwMywyNCAxNTAsMTkuODU0NzcxOCAxNTAsMTQuOTYyNjU1NiBDMTUwLDEwLjE0NDk1MzYgMTUzLjM5MjI1Myw2IDE1OC41MzgwODUsNiBDMTYzLjg3NDIxMyw2IDE2Ny4wMzc3NzUsMTAuMTgyNTcyNiAxNjYuOTk5NjU5LDE1LjE0OTM3NzYgTDE1MS43MTUxODQsMTUuMTQ5Mzc3NiBaIiBpZD0iRmlsbC0yMyIgZmlsbD0iIzI5QUJFMiI+PC9wYXRoPgogICAgICAgICAgICAgICAgPHBhdGggZD0iTTEzLDI5IEMxMi4zNzIxNzY5LDI4LjI4MTQwODQgMTEuNzkyNDgyLDI3LjQ3ODkxMTIgMTEuMzM0NDI0OSwyNi41NTgwNDcyIEMxMC44NzM5NzM0LDI1LjYzOTg4MDEgMTAuNTQ2MTc0MSwyNC42MTExMzc1IDEwLjMzNDc0NDcsMjMuNTU0ODI1OCBDMTAuMTE4Mjg3LDIyLjUwMTIxMTEgOS45OTk1MjI1NSwyMS40MDIzNDc0IDEwLjAwMDAwMTQsMjAuMjk4MDg5NiBDOS45OTk3NjIsMTkuMTkzMjMyNiAxMC4xMTMyNTg2LDE4LjA4MTc4MyAxMC4zNDAyNTE5LDE3IEwxMS4yNTQyMTExLDE3LjM1NzE5ODIgQzEwLjk3NjIxNjIsMTguMzEwMTI2MSAxMC43OTQ5NTY4LDE5LjMxNDI5NjQgMTAuNzE4MzM0NiwyMC4zMzc2NDUxIEMxMC42NDEyMzM1LDIxLjM2MTg5MjkgMTAuNjc0Mjc2OCwyMi40MDE0MjM0IDEwLjgwNTAxMzQsMjMuNDMyODYzIEMxMC45MzA5NjEyLDI0LjQ2MjgwNDMgMTEuMTY2NTc0NCwyNS40NzIzNjg2IDExLjU0MzY5OTMsMjYuNDEwNjEzMSBDMTEuOTE4MTkwMywyNy4zNTEyNTQ4IDEyLjQyODIwNjgsMjguMjEwMzg4MyAxMywyOSIgaWQ9IkZpbGwtMjUiIGZpbGw9IiNGRkZGRkYiPjwvcGF0aD4KICAgICAgICAgICAgICAgIDxwYXRoIGQ9Ik04LDcuMTg4MDM5OTYgQzkuNzU3MTAxNTUsNi44NTI2Mzk5NiAxMS42MzU1Mzg5LDYuOTY3ODUxNyAxMy4zNzg0NjU3LDcuNTE4MTkxMTMgQzE1LjEyMjgxLDguMDYwOTE5NzYgMTYuNzM4NzMxMSw5LjAzMzI2NDgyIDE4LDEwLjM0MDQ4NSBMMTcuMTE3NzYzOCwxMSBDMTYuMTI4MzY2NSw5LjcyNTg0NzQzIDE0Ljc1NjgxODEsOC42Nzk3NTYzNyAxMy4xNjg5NjMsOC4wMDU4MDcwOCBDMTEuNTg2MjEwOCw3LjMyNjM0NjUzIDkuNzg2NTg1MDIsNy4wMjYxMTM2NyA4LDcuMTg4MDM5OTYiIGlkPSJGaWxsLTI3IiBmaWxsPSIjRkZGRkZGIj48L3BhdGg+CiAgICAgICAgICAgICAgICA8cGF0aCBkPSJNMjcsMTIgQzI2Ljc4MjcxOCwxMi45NjEyNDY4IDI2LjQyNTcxNzQsMTMuODkzMDA3NiAyNS45NDMxMDA2LDE0Ljc1MTQ3NDMgQzI1LjQ2MDQ4MzgsMTUuNjA5NjYwMiAyNC44NTg3Nzk3LDE2LjM5NzM2MDMgMjQuMTcwMzcxOCwxNy4wODcwNTQyIEMyMi44MDI0MzUzLDE4LjQ3NzExMzIgMjEuMDc5ODQ4NSwxOS41MDM3OTExIDE5LjIwMzk2MywyMCBMMTksMTguODk4MDYyMyBDMjAuNzMwOTQzOCwxOC42MjM3MDEyIDIyLjQxMjc5MDEsMTcuODQ4NjM4IDIzLjgzMDYwNzUsMTYuNjU5NjQ2MiBDMjQuNTQzMDQxOCwxNi4wNzEwNDc1IDI1LjE4NDk2MzksMTUuMzc3OTgzNyAyNS43MjU4MTg2LDE0LjU5NTA1NzYgQzI2LjI2NjE1MDksMTMuODEyMTMxNCAyNi42OTkxNDgsMTIuOTM1MTMwNiAyNywxMiIgaWQ9IkZpbGwtMjkiIGZpbGw9IiNGRkZGRkYiPjwvcGF0aD4KICAgICAgICAgICAgICAgIDxwYXRoIGQ9Ik0xNy42MTk5NDIzLDEwIEMxNC4yNDk3NTA0LDEwLjU5MDA3NTggMTEuMjgzMjEsMTIuOTE1NDY0OSAxMC4wNDY0NDk4LDE2LjM1Nzg0MDIgQzEwLjAyOTYwODQsMTYuNDA0MjE0OCAxMC4wMTYwMjY1LDE2LjQ1MTEyMjMgMTAsMTYuNDk3NzYzNCBDMTEuMDgzODI5LDE3Ljc4NjEyMjIgMTIuNTEyMzY0NCwxOC44MTU0MjMzIDE0LjIxNDQzNzcsMTkuNDIzMzU2IEMxNS45MzExNzkzLDIwLjAzNjg4NTYgMTcuNzA1MjM2MSwyMC4xNDM3NjAyIDE5LjM3NTI1NjMsMTkuODI1MDAyIEMxOS4zOTAxOTYzLDE5Ljc4NTgyMzUgMTkuNDA2NzY2MSwxOS43NDc0NDQ2IDE5LjQyMDg5MTIsMTkuNzA3NzMzMSBDMjAuNjU3NjUxNCwxNi4yNjU2MjQyIDE5Ljg0NzM2MDIsMTIuNTkwMzEwMiAxNy42MTk5NDIzLDEwIiBpZD0iRmlsbC0zMSIgZmlsbD0iI0ZGRkZGRiI+PC9wYXRoPgogICAgICAgICAgICAgICAgPHBhdGggZD0iTTI4LjY1MjY4MTgsMjIuNjAzMTU2NSBDMjcuMjE1MDgzNiwyNy45MzQxNjUgMjEuNzI3ODc3OCwzMS4wOTA0NTA5IDE2LjM5NjgxODgsMjkuNjUyNTkwNCBDMTEuMDY1NzU5OSwyOC4yMTUwMDU4IDcuOTA5NzE5OTYsMjIuNzI3ODUyIDkuMzQ3MzE4MiwxNy4zOTY4NDM1IEMxMC43ODQ5MTY0LDEyLjA2NTgzNSAxNi4yNzIxMjIyLDguOTA5NTQ5MTEgMjEuNjAzMTgxMiwxMC4zNDc0MDk2IEMyNi45MzQyNDAxLDExLjc4NDk5NDIgMzAuMDkwMjgsMTcuMjcyMTQ4IDI4LjY1MjY4MTgsMjIuNjAzMTU2NSBaIiBpZD0iU3Ryb2tlLTMzIiBzdHJva2U9IiNGRkZGRkYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCI+PC9wYXRoPgogICAgICAgICAgICAgICAgPHBhdGggZD0iTTE5LjY1MjY4MTgsMTkuNjAzMjg3NiBDMTguMjE1MDgzNiwyNC45MzQwMDczIDEyLjcyNzg3NzgsMjguMDkwMjg1NiA3LjM5NjgxODg1LDI2LjY1MjcwNDQgQzQuNTA0OTgzNDcsMjUuODcyNzM4MiAyLjI1MzE1Mjg5LDIzLjkwMTI2MDMgMS4wMjczODA4LDIxLjQwOTU3NDEgQy0wLjAwNjU0MTIwODcyLDE5LjMwNzg3MDggLTAuMzEwNDU0MjE1LDE2LjgzNjA1NTUgMC4zNDczMTgyMDUsMTQuMzk2OTg3MSBDMS43ODQ5MTY0NSw5LjA2NTk5MTQ3IDcuMjcyMzk4MDQsNS45MDk3MTMyIDEyLjYwMzE4MTIsNy4zNDcyOTQzNiBDMTcuOTM0MjQwMSw4Ljc4NTE1MTQgMjEuMDkwMjgsMTQuMjcyMjkxOSAxOS42NTI2ODE4LDE5LjYwMzI4NzYgWiIgaWQ9IlN0cm9rZS0zNSIgc3Ryb2tlPSIjRkZGRkZGIiBzdHJva2UtbGluZWNhcD0icm91bmQiPjwvcGF0aD4KICAgICAgICAgICAgPC9nPgogICAgICAgIDwvZz4KICAgIDwvZz4KPC9zdmc+"></a>

<br />

[<img src="https://img.shields.io/badge/chat-on--slack-blue">](http://slack.overture.bio) 
[<img src="https://img.shields.io/badge/License-gpl--v3.0-blue">](https://github.com/overture-stack/ego/blob/develop/LICENSE)

## Worry Less Science More

This Overture repository is where we ([the OICR Genome Informatics Team](https://softeng.oicr.on.ca/team/)) develop the [Ego](https://www.overture.bio/products/ego/) authentication and authorization microservice. [Overture]((https://www.overture.bio/)) is a collection of open-source, extendable solutions, made for big-data genomic science. Our core products enable researchers and clinicians to securely contribute, access, analyze, visiualize and share both molecular and clinical data. For more information on what Overture can offer visit our [webpage](https://www.overture.bio/) and check out our other projects here on [github](https://github.com/overture-stack/).

## Description

![](https://www.overture.bio/static/screenshot-21fc2cfc0ac1c3fd9bd7e62196477554.png)

Ego simplifies user management by providing a secure system to authenticate and authorize users of your application. Ego does not manage usernames and passwords but instead relies on popular single-sign-on identity providers including Google, GitHub, LinkedIn and ORCiD. Ego is [OAuth 2.0](https://oauth.net/2/) and [OpenID Connect](https://auth0.com/docs/authenticate/protocols/openid-connect-protocol) compliant. It is written in JAVA and uses [Sprint Boot](https://spring.io/projects/spring-boot) and [Spring Security Frameworks](https://spring.io/projects/spring-security). It provides stateless authorization using [JSON Web Tokens (JWT)](https://jwt.io/) allowing it to scale to a large number of users. For more information see our [documentation & web guides](https://www.overture.bio/documentation/ego/). 

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Contribution](#how-to-contribute)
- [Feedback](#feedback)
- [Code of Conduct](#code-of-conduct)
- [License](#license)

## Installation

For detailed information see our documentation linked below:

- [Setup Prerequisites](https://www.overture.bio/documentation/ego/installation/prereq/)
- [Installation](https://www.overture.bio/documentation/ego/installation/installation/)
- [Configuration](https://www.overture.bio/documentation/ego/installation/configuration/)
- [Authentication](https://www.overture.bio/documentation/ego/installation/authentication/)



<!--

## Quick Start

 Here you will find a simplified quickstart guide to getting Ego setup. 

<br />

### 1. Set up a google oauth client app; 
- [summary steps linked here](https://www.overture.bio/documentation/ego/installation/prereq/#google). 
- Use the following redirect URI: ```http://localhost:8081/oauth/code/google```

<br />

### 2. Update  ```docker-compose-all.yml``` with the provided client id and secret 

```
spring.security.oauth2.client.registration.google.clientId : "<insert-provided-client-Id>"
spring.security.oauth2.client.registration.google.clientSecret: "<insert-provided-clientSecret>"
```

<br />

### 3. Run docker compose

```
docker-compose -f docker-compose-all.yml up 
```

You will need to wait for all the services to boot up, to watch the progress you can type the following into a seperate terminal

```
watch -n 2 docker service
```

<br />

### 4. Ego requires seed data to authorize the Ego UI as a client. 

```
docker exec ego_postgres_1  psql -h localhost -p 5432 -U postgres -d ego --command "INSERT INTO EGOAPPLICATION (name, clientId, clientSecret, redirectUri, description, status, errorredirecturi) VALUES ('ego ui', 'ego-ui', 'secret', 'http://localhost:8080/', '...', 'APPROVED', 'http://localhost:8080/error') on conflict do nothing"
```

Alternatively if you have ```Make``` installed you can run  ```make init-db```

### 5. Access the Ego UI through ```http://localhost:8080/ego-ui```
- This will require your google sign in 
- Once signed in you will have access to the admin dashboard (image above).
- The Ego swagger ui can be located at ```http://localhost:8080/swagger-ui.html```

<br />

-->

<!--
#### 1. Set up a database.
- Install [Postgres](https://www.postgresql.org/about/)
- Create a database

```
sudo -u postgress psql
create database ego;
q exit out of psql
```

<br />

### 2. Define the tables in your database.
- Copy the [psql.schema.spl](https://github.com/overture-stack/ego/blob/develop/src/main/resources/schemas/01-psql-schema.sql) file locally
- Execute the SQL script to setup the tables

```
psql -U postgres -d ego -a -f psql-schema.sql
```
<br />

### 3. Run one of the three supported Ego profiles
- ```Default``` is the most simple profile. It allows you to test API endpoints with a valid JWT
- ```Auth``` allows all the above as well as including JWT validations 
- ```Secure``` allows all the above as well as integration with https protocol



```
psql -U postgres -d ego -a -f psql-schema.sql
```

<br />

-->

## Usage

For detailed information see our documentation linked below:

- [Using the Admin UI](https://www.overture.bio/documentation/ego/user-guide/admin-ui/)
- [Using the API](https://www.overture.bio/documentation/ego/user-guide/api/)


## Contribute

* [Making a Contribition ](CONTRIBUTING.md)
* [Filing an issue](https://github.com/overture-stack/ego/issues)

## Feedback

* Connect with us on [Slack](http://slack.overture.bio)
* [Upvote](https://github.com/overture-stack/ego/issues?q=is%3Aopen+is%3Aissue+label%3Anew-feature+sort%3Areactions-%2B1-desc) feature requests

## Code of Conduct

&emsp; [![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](code_of_conduct.md)

## License

Licensed under the [GNU Lesser General Public License v3.0](LICENSE.txt) license.
