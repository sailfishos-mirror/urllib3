Fixed HTTP pools created using ``ProxyManager.connection_from_url`` to strip
sensitive headers specified in ``Retry.remove_headers_on_redirect`` when
redirecting to a different host.
