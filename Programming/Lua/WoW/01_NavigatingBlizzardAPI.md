### Gethe's Repository

This article focuses on the **GitHub** version of obtaining the Blizzard API.  
All further information is correct at time of writing: [`11:23:24 AM EST`, June 22<sup>nd</sup>, 2026]

The [**`Interface`**](https://github.com/Gethe/wow-ui-source/tree/live/Interface) folder contains: 
|File|Lines|
|-:|:-|
|[**AddOns** folder](https://github.com/Gethe/wow-ui-source/tree/live/Interface/AddOns)|`317` *folders*|
|[ui-code-list.txt](https://github.com/Gethe/wow-ui-source/blob/live/Interface/ui-code-list.txt)|`3679`|
|[ui-gen-addon-list.txt](https://github.com/Gethe/wow-ui-source/blob/live/Interface/ui-gen-addon-list.txt)|`0`|
|[ui-toc-list.txt](https://github.com/Gethe/wow-ui-source/blob/live/Interface/ui-toc-list.txt)|`346`|

### `Blizzard_APIDocumentationGenerated`

To make things simpler, head specifically to the **Blizzard_APIDocumentationGenerated** folder within the **AddOns** folder.

A file that is easier to understand is `AccountInfoDocumentation.lua`, as seen below.

```
local AccountInfo =
{
	Name = "AccountInfo",
	Type = "System",
	Namespace = "C_AccountInfo",
	Environment = "All",

	Functions =
	{
		{
			Name = "GetIDFromBattleNetAccountGUID",
			Type = "Function",
			SecretArguments = "AllowedWhenUntainted",

			Arguments =
			{
				{ Name = "battleNetAccountGUID", Type = "WOWGUID", Nilable = false },
			},

			Returns =
			{
				{ Name = "battleNetAccountID", Type = "number", Nilable = false },
			},
		},
		{
			Name = "IsGUIDBattleNetAccountType",
			Type = "Function",
			SecretArguments = "AllowedWhenUntainted",

			Arguments =
			{
				{ Name = "guid", Type = "WOWGUID", Nilable = false },
			},

			Returns =
			{
				{ Name = "isBNet", Type = "bool", Nilable = false },
			},
		},
		{
			Name = "IsGUIDRelatedToLocalAccount",
			Type = "Function",
			SecretArguments = "AllowedWhenUntainted",

			Arguments =
			{
				{ Name = "guid", Type = "WOWGUID", Nilable = false },
			},

			Returns =
			{
				{ Name = "isLocalUser", Type = "bool", Nilable = false },
			},
		},
	},

	Events =
	{
	},

	Tables =
	{
	},
	Predicates =
	{
	},
};

APIDocumentation:AddDocumentationTable(AccountInfo);
```

### Simplifying the Code

This can look incredibly overwhelming, especially as someone not well-versed in programming.
Extract what the file is *actually* saying and it will look much less challenging.

```
local AccountInfo =
{
	Name = "AccountInfo",
	Type = "System",
	Namespace = "C_AccountInfo",
	Environment = "All",
```

While not everyone's favorite subject, programming is akin to math in a plethora of ways.
Just how a variable in math is a value that represents something else (typically `x`), a variable in programming is a value that represents something else.

This variable is declared as `local`, essentially meaning what it does inside will *only* exist until the entirety of its insides are closed.

The variable defined here is `AccountInfo`, very legible, simple, and easy to understand. 

The opening brace (`{`) serves to enclose whatever comes after until its partner closing brace (`}`) appears.

So far, we have the first two lines down: a local variable named `AccountInfo` is going to equal whatever appears after the opening brace (`{`).

Then it defines some global variables, ones that appear across the entire body. As these are declared within a `local` variable that cannot spread its contents elsewhere, there is no reason to specifically mark these as local variables as well.

The variables here are: `Name`, `Type`, `Namespace`, and `Environment`.

The variable called `Name` represents `AccountInfo` (meaning the variable that was marked `local` in the beginning).
The variable called `Type` represents something and the type given is `System`. One could safely assume that this means it is a macro-level effect (on a large scale).
The variable called `Namespace` represents `C_AccountInfo`, which sounds just like `AccountInfo`! As this is a `Namespace`, it can be thought of as a holder, where other information could be held. In this case, think `C` for `C`ontainer. It's going to `C`ontain_`AccountInfo`.
The variable called `Environment` represents the areas in which it could extend out to. Since this equates to `All`, the effect is ever-reaching.

Then two more opening braces (`{`) appear, marking more enclosures. This parent is called `Functions`.

```
	Functions =
	{
		{
```

Within the 2nd enclosure above (`3 enclosures deep`), there are more similar variables.

```
      Name = "GetIDFromBattleNetAccountGUID",
			Type = "Function",
			SecretArguments = "AllowedWhenUntainted",
```

Another `Name`, this time referencing `GetIDFromBattleNetAccountGUID`. As this is in the `Functions` enclosure, it's safe to assume that `GetIDFromBattleNetAccountGUID` is a function. Functions are typically followed by a pair of parentheses `()`, with any number (or none at all) of `arguments`, individual variables that would go into the function.

So the `Name` of this is `GetIDFromBattleNetAccountGUID()`, and the `Type` is `Function` so that's right on the nose. The last variable, `SecretArguments`, going off of the name, is restricted to only some arguments allowed. It equates to `AllowedWhenUntainted`, meaning that if all is well and nothing butts head against another than this function is allowed.

The next block is called `Arguments`, allowing us to see what they're using! There is only one here.

```
			Arguments =
			{
				{ Name = "battleNetAccountGUID", Type = "WOWGUID", Nilable = false },
			},
```
`Name` for this argument is `battleNetAccountGUID` and its `Type` is `WOWGUID`. It's safe to assume that ensures that `WoW` renders this information specifically based on the `Battle.net` variables.

The last argument is `Nilable`, referencing the value of `nil`, common in programming languages.

`nil` is the same as `null`, `none`, `never`, etc. It's a negation! Since this is set to `false`, this argument MUST have a value associated with it. That makes sense in this context as it requires an account to be valid and every account but have a GUID! (Generic Unique ID) (?).

The next block is quite simple as well.

```
			Returns =
			{
				{ Name = "battleNetAccountID", Type = "number", Nilable = false },
			},
```

Returns, meaning that it outputs something.This one is a `Name`, giving `battleNetAccountID`, different from `battleNetAccountGUID` as noticed by the change in type! The `Type` is a `number` and cannot be empty. That also makes sense as this points to an active account.


The next block is structured in the same exact fashion as above, meaning looking through it should be easier!

```
		{
			Name = "IsGUIDBattleNetAccountType",
			Type = "Function",
			SecretArguments = "AllowedWhenUntainted",

			Arguments =
			{
				{ Name = "guid", Type = "WOWGUID", Nilable = false },
			},

			Returns =
			{
				{ Name = "isBNet", Type = "bool", Nilable = false },
			},
		},
```

This is a `Function`, with a`Name` of `IsGUIDBattleNetAccountType()` and it is `AllowedWhenUntainted`.
It takes a `Name` called `guid` and a type of `WOWGUID`, and cannot be false.
It returns a `Name` called `isBNet`, with a type `bool`, meaning `boolean`, named after an individual (Last Name of Bool (Francis?)). It simply means `True`/`False`, `Yes`/`No`, `1`/`0`, and so on. It's a binary statement of one or the other. It cannot be assigned `nil`. `nil` is a tricky value, automatically assigned as `false` under a `boolean` condition. A reasonable question would be "why would an element with only one option be considered that type?" and that would be easy to answer! The output MUST be true and `isBNet` only cares about one thing, if the article it references it from `BNet`. While it may not be nilable here, it *could* somewhere else!

One more block of these!

```
{
			Name = "IsGUIDRelatedToLocalAccount",
			Type = "Function",
			SecretArguments = "AllowedWhenUntainted",

			Arguments =
			{
				{ Name = "guid", Type = "WOWGUID", Nilable = false },
			},

			Returns =
			{
				{ Name = "isLocalUser", Type = "bool", Nilable = false },
			},
```

A `Function`, called `IsGuideRelatedToLocalAccount()` that is `AllowedWhenUntainted` takes a `WOWGUID` called `guid` that cannot be false and returns a `bool` of `isLocalUser` that cannot be false.

The idea of this function is that it directly coorelates the Battle.Net AccountID, WoW-associated AccountID, and their relation to each other.

The next block is entirely empty, likely due to programming convention to save them down the road.

```
	Events =
	{
	},

	Tables =
	{
	},
	Predicates =
	{
	},
};
```

`Events`, `Tables`, and `Predicates` aren't define here but it's fairly safe to assume that `Events` refers to something that is triggered, `Tables` mean it holds certain values, and `Predicates` means it may require some other information from a separate file to equal something to run.

The very last block is a simple function!

```
APIDocumentation:AddDocumentationTable(AccountInfo);
```

`APIDocumentation` is *outside* of the `local` variable defined as `AccountInfo` (as seen by the final closing brace after `},` from Predicates, `};`. Semicolons (`;`) are a programming convention to signify the end of a related line (in this case, the properties of `local AccountInfo`. Lua does not interpret semicolons in this fashion. In convention, many programmers still utilise them.

The colon (`:`) after `APIDocumentation` is a "shortcut" for lack of a better word to reference a specific function within its own table (called `APIDocumentation`). In the `APIDocumentation` Table, it's safe to assume that this holds all of the required functions needed to be in a document of variables.

The inner function (as it is suffixed with `()` and an argument inside of `AccountInfo`) is `AddDocumentationTable`, likely meaning that the entire collection of blocks just witnessed will now be in documentation to define what `AccountInfo` really means. 

An example of where `AccountInfo` is used, (appearing as `accountInfo` in the files), is in `Blizzard_SharedXML/AccountUtil.lua` on line `45`: `function BNet_GetBNetAccountName(accountInfo)`.

The internal function is quite simple here as well!

```
function BNet_GetBNetAccountName(accountInfo)
	if not accountInfo then
		return;
	end

	local name = accountInfo.accountName;
	if name == "" then
		name = BNet_GetTruncatedBattleTag(accountInfo.battleTag);
	end

	return name;
end
```

`BNet_GetBNetAccountName(accountInfo)` is a global function that wants to retrieve what the `BNet` account is of the specific individual.

Looking at the information given in `accountInfo`, `BNet_GetBNetAccountName` is going to return: `GetIDFromBattleNetAccountGUID` [`battleNetAccountID`], `IsGUIDBattleNetAccountType` [`isBNet`], and `IsGuidRelatedToLocalAccount` [`isLocalUser`]. 

That makes sense with what we know. `BNet_GetBNetAccountName` is going to retrieve the AccountID, check it to make sure it is from `BNet`, wrapping it up with checking if the user in question on whatever instance they're at is that same person (against known IDs of theirs, such as other games or characters).

In `BNet_GetBNetAccountName()`, the first thing that happens is:
```
	if not accountInfo then
		return;
	end
```

Here, an `if`/`then` statement appears, checking a specific circumstance of whatever comes after and then stating what to do if that is encountered.

Here, it is asking if there is `accountInfo` at all. If not, then `end` (which will break out of the entire function, disregarding what still has to perform.

This makes sense because each variable within `accountInfo` has `nilable = false`. Those IDs MUST exist.
If a player's BNetAccountName is desired, `BNet_GetBNetAccountName` is going to search for the player's `battleNetAccountID`, `isBNet`, and `isLocalUser`. If those are false, there will not be a BNet Account Name as there won't be a BNet Account as all!

If there *is* valid `accountInfo` however, then `BNet_GetBNetAccountName()` continues.

```
	local name = accountInfo.accountName;
	if name == "" then
		name = BNet_GetTruncatedBattleTag(accountInfo.battleTag);
	end

	return name;
```

A local variable (as its parent function is global) named `name` appears, equating it to `accountInfo.accountName`. That dot (`.`) references another variable *within* the original variable.

Recalling `local AccountName =`, there were braces (`{}`) involved, marking what was inside as together, a table. There was no `accountName` here so it must be added elsewhere! Information can be added to tables in multiple environments. Segregating the environments to add specific things can be helpful to keep files clean and legible.

Here, if the variable of `accountName` was `==` (meaning the two values are equivalent, not a definition of a value to another thing) to `""`, representing an opening quote (`"`) with nothing inside of it, such as text, followed by a closing quote (`"`). Text is referred to as a `string`, meaning this would be `if` `accountInfo.accountName` is equivalent to nothing, then set `accountInfo.accountName` to `accountInfo.battleTag`, found in the function `BNet_GetTruncatedBattleTag()`.

After that, it will end the function.

If neither of those `if` statements are true however, then the function performs a much simpler purpose.
See below for the same function, without the `if` statements.

```
function BNet_GetBNetAccountName(accountInfo)
	local name = accountInfo.accountName;

	return name;
end
```

`BNet_GetBNetAccountName` calls on `accountInfo`'s table for `accountName` and calling it `name`. If it exists, which is the only other option here since the other two `if` statements accounted for non-existent or non-string answers, then it will simply return what it is.

I.E. `BNet_GetBNetAccountName` is going to return `accountName`, from witin the `accountInfo` table.
