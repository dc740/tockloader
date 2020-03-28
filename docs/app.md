# Package tockloader.app Documentation

## Class App
Representation of a Tock app stored on a board.
### \_\_init\_\_
```py

def __init__(self, tbfh, address, name, app_binary=None)

```



Initialize self.  See help(type(self)) for accurate signature.


### get\_app\_binary
```py

def get_app_binary(self)

```



Return just the compiled application code binary. Does not include
the TBF header.


### get\_binary
```py

def get_binary(self)

```



Return the binary array comprising the entire application.


### get\_header\_binary
```py

def get_header_binary(self)

```



Get the TBF header as a bytes array.


### get\_header\_size
```py

def get_header_size(self)

```



Return the size of the TBF header in bytes.


### get\_size
```py

def get_size(self)

```



Return the total size (including TBF header) of this app in bytes.


### has\_app\_binary
```py

def has_app_binary(self)

```



Whether we have the actual application binary for this app.


### info
```py

def info(self, verbose=False)

```



Get a string describing various properties of the app.


### is\_modified
```py

def is_modified(self)

```



Returns whether this app has been modified by tockloader since it was
initially created by `__init__`.


### is\_sticky
```py

def is_sticky(self)

```



Returns true if the app is set as sticky and will not be removed with
a normal app erase command. Sticky apps must be force removed.


### set\_address
```py

def set_address(self, address)

```



Set the address of flash where this app is or should go.


### set\_app\_binary
```py

def set_app_binary(self, app_binary)

```



Update the application binary. Likely this binary would come from the
existing contents of flash on a board.


### set\_size
```py

def set_size(self, size)

```



Force the entire app to be a certain size. If `size` is smaller than the
actual app an error will be thrown.


### set\_sticky
```py

def set_sticky(self)

```



Mark this app as "sticky" in the app's header. This makes it harder to
accidentally remove this app if it is a core service or debug app.


### \_\_str\_\_
```py

def __str__(self)

```



Return str(self).



