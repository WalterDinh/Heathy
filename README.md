# Yo-Learner-Mobile

```diff
# hot fix for xcode 11
- 1. Go to node_modules/react-native/React/Base/RCTModuleMethod.mm
- 2. Find RCTParseUnused
- 3. Add `RCTReadString(input, "__attribute__((__unused__))") ||`

static BOOL RCTParseUnused(const char **input)
{	{
  return RCTReadString(input, "__attribute__((unused))") ||	  return RCTReadString(input, "__attribute__((unused))") ||
+         RCTReadString(input, "__attribute__((__unused__))") ||
         RCTReadString(input, "__unused");	         RCTReadString(input, "__unused");
}	}
```#   H e a t h y  
 