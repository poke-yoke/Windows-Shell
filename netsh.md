# NETSH

netsh winhttp show proxy

netsh winhttp set proxy proxy-server="http=www-proxy:80;https=www-proxy:80" bypass-list="*.local.domain.com;localhost"

Note on WSUS
If the system proxy has been set by netsh , WSUS will default to using these settings.  Unfortunately the system isn't clever enough to expand a WSUS hostname to FQDN so may inadvertently route via the proxy.  Simple to correct, simply use the FQDN for the WSUS server hostname.

With no system proxy WSUS appears to use WPAD as per https://support.microsoft.com/en-gb/help/900935/how-the-windows-update-client-determines-which-proxy-server-to-use-to
