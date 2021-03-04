---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
ms.openlocfilehash: 7e141cb5c1bde59bec9e981ffd228dba6db33089
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922203"
---
# <span data-ttu-id="87a3a-101">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="87a3a-101">New-AzApiManagementUser</span></span>

## <span data-ttu-id="87a3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87a3a-102">SYNOPSIS</span></span>
<span data-ttu-id="87a3a-103">Registriert einen neuen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="87a3a-103">Registers a new user.</span></span>

## <span data-ttu-id="87a3a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87a3a-104">SYNTAX</span></span>

```
New-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87a3a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="87a3a-105">DESCRIPTION</span></span>
<span data-ttu-id="87a3a-106">Das **Cmdlet New-AzApiManagementUser** registriert einen neuen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="87a3a-106">The **New-AzApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="87a3a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="87a3a-107">EXAMPLES</span></span>

### <span data-ttu-id="87a3a-108">Beispiel 1: Registrieren eines neuen Benutzers</span><span class="sxs-lookup"><span data-stu-id="87a3a-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="87a3a-109">Mit diesem Befehl wird ein neuer Benutzer namens "Patti Fuller" registriert.</span><span class="sxs-lookup"><span data-stu-id="87a3a-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="87a3a-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="87a3a-110">PARAMETERS</span></span>

### <span data-ttu-id="87a3a-111">-Context</span><span class="sxs-lookup"><span data-stu-id="87a3a-111">-Context</span></span>
<span data-ttu-id="87a3a-112">Gibt ein **PsApiManagementContext-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="87a3a-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87a3a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87a3a-113">-DefaultProfile</span></span>
<span data-ttu-id="87a3a-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="87a3a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a3a-115">-E-Mail</span><span class="sxs-lookup"><span data-stu-id="87a3a-115">-Email</span></span>
<span data-ttu-id="87a3a-116">Gibt die E-Mail-Adresse des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="87a3a-116">Specifies the email address of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87a3a-117">-Vorname</span><span class="sxs-lookup"><span data-stu-id="87a3a-117">-FirstName</span></span>
<span data-ttu-id="87a3a-118">Gibt den Vornamen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="87a3a-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="87a3a-119">Dieser Parameter muss 1 bis 100 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="87a3a-119">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87a3a-120">-Nachname</span><span class="sxs-lookup"><span data-stu-id="87a3a-120">-LastName</span></span>
<span data-ttu-id="87a3a-121">Gibt den Nachnamen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="87a3a-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="87a3a-122">Dieser Parameter muss 1 bis 100 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="87a3a-122">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87a3a-123">-Hinweis</span><span class="sxs-lookup"><span data-stu-id="87a3a-123">-Note</span></span>
<span data-ttu-id="87a3a-124">Gibt eine Notiz über den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="87a3a-124">Specifies a note about the user.</span></span>
<span data-ttu-id="87a3a-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="87a3a-125">This parameter is optional.</span></span>
<span data-ttu-id="87a3a-126">Der Standardwert ist $Null.</span><span class="sxs-lookup"><span data-stu-id="87a3a-126">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87a3a-127">-Password</span><span class="sxs-lookup"><span data-stu-id="87a3a-127">-Password</span></span>
<span data-ttu-id="87a3a-128">Gibt das Benutzerkennwort an.</span><span class="sxs-lookup"><span data-stu-id="87a3a-128">Specifies the user password.</span></span>
<span data-ttu-id="87a3a-129">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="87a3a-129">This parameter is required.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87a3a-130">-State</span><span class="sxs-lookup"><span data-stu-id="87a3a-130">-State</span></span>
<span data-ttu-id="87a3a-131">Gibt den Benutzerzustand an.</span><span class="sxs-lookup"><span data-stu-id="87a3a-131">Specifies the user state.</span></span>
<span data-ttu-id="87a3a-132">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="87a3a-132">This parameter is optional.</span></span>
<span data-ttu-id="87a3a-133">Der Standardwert dieses Parameters ist $Null.</span><span class="sxs-lookup"><span data-stu-id="87a3a-133">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: (All)
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87a3a-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="87a3a-134">-UserId</span></span>
<span data-ttu-id="87a3a-135">Gibt die Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="87a3a-135">Specifies the user ID.</span></span>
<span data-ttu-id="87a3a-136">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="87a3a-136">This parameter is optional.</span></span>
<span data-ttu-id="87a3a-137">Wenn dieser Parameter nicht angegeben ist, generiert dieses Cmdlet eine Benutzer-ID.</span><span class="sxs-lookup"><span data-stu-id="87a3a-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87a3a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87a3a-138">CommonParameters</span></span>
<span data-ttu-id="87a3a-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87a3a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87a3a-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87a3a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87a3a-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="87a3a-141">INPUTS</span></span>

### <span data-ttu-id="87a3a-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="87a3a-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="87a3a-143">System.String</span><span class="sxs-lookup"><span data-stu-id="87a3a-143">System.String</span></span>

### <span data-ttu-id="87a3a-144">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="87a3a-144">System.Security.SecureString</span></span>

### <span data-ttu-id="87a3a-145">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="87a3a-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="87a3a-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="87a3a-146">OUTPUTS</span></span>

### <span data-ttu-id="87a3a-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="87a3a-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="87a3a-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="87a3a-148">NOTES</span></span>

## <span data-ttu-id="87a3a-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="87a3a-149">RELATED LINKS</span></span>

[<span data-ttu-id="87a3a-150">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="87a3a-150">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="87a3a-151">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="87a3a-151">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


