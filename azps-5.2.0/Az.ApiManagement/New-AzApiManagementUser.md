---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
ms.openlocfilehash: 6cc922ceb09509e70a4017241dc6beb6e5443d1a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366132"
---
# <span data-ttu-id="c112b-101">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="c112b-101">New-AzApiManagementUser</span></span>

## <span data-ttu-id="c112b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c112b-102">SYNOPSIS</span></span>
<span data-ttu-id="c112b-103">Registriert einen neuen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="c112b-103">Registers a new user.</span></span>

## <span data-ttu-id="c112b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c112b-104">SYNTAX</span></span>

```
New-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c112b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c112b-105">DESCRIPTION</span></span>
<span data-ttu-id="c112b-106">Das **Cmdlet "New-AzApiManagementUser"** registriert einen neuen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="c112b-106">The **New-AzApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="c112b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c112b-107">EXAMPLES</span></span>

### <span data-ttu-id="c112b-108">Beispiel 1: Registrieren eines neuen Benutzers</span><span class="sxs-lookup"><span data-stu-id="c112b-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="c112b-109">Mit diesem Befehl wird ein neuer Benutzer namens "Personeni Fuller" registriert.</span><span class="sxs-lookup"><span data-stu-id="c112b-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="c112b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c112b-110">PARAMETERS</span></span>

### <span data-ttu-id="c112b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c112b-111">-Context</span></span>
<span data-ttu-id="c112b-112">Gibt ein **"PsApiManagementContext"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="c112b-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c112b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c112b-113">-DefaultProfile</span></span>
<span data-ttu-id="c112b-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c112b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c112b-115">-Email</span><span class="sxs-lookup"><span data-stu-id="c112b-115">-Email</span></span>
<span data-ttu-id="c112b-116">Gibt die E-Mail-Adresse des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="c112b-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="c112b-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="c112b-117">-FirstName</span></span>
<span data-ttu-id="c112b-118">Gibt den Vornamen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="c112b-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="c112b-119">Dieser Parameter muss 1 bis 100 Zeichen umfassen.</span><span class="sxs-lookup"><span data-stu-id="c112b-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="c112b-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="c112b-120">-LastName</span></span>
<span data-ttu-id="c112b-121">Gibt den Nachnamen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="c112b-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="c112b-122">Dieser Parameter muss 1 bis 100 Zeichen umfassen.</span><span class="sxs-lookup"><span data-stu-id="c112b-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="c112b-123">-Note</span><span class="sxs-lookup"><span data-stu-id="c112b-123">-Note</span></span>
<span data-ttu-id="c112b-124">Gibt eine Notiz zum Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="c112b-124">Specifies a note about the user.</span></span>
<span data-ttu-id="c112b-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="c112b-125">This parameter is optional.</span></span>
<span data-ttu-id="c112b-126">Der Standardwert ist $Null.</span><span class="sxs-lookup"><span data-stu-id="c112b-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="c112b-127">-Password</span><span class="sxs-lookup"><span data-stu-id="c112b-127">-Password</span></span>
<span data-ttu-id="c112b-128">Gibt das Benutzerkennwort an.</span><span class="sxs-lookup"><span data-stu-id="c112b-128">Specifies the user password.</span></span>
<span data-ttu-id="c112b-129">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c112b-129">This parameter is required.</span></span>

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

### <span data-ttu-id="c112b-130">-State</span><span class="sxs-lookup"><span data-stu-id="c112b-130">-State</span></span>
<span data-ttu-id="c112b-131">Gibt den Benutzerzustand an.</span><span class="sxs-lookup"><span data-stu-id="c112b-131">Specifies the user state.</span></span>
<span data-ttu-id="c112b-132">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="c112b-132">This parameter is optional.</span></span>
<span data-ttu-id="c112b-133">Der Standardwert dieses Parameters ist $Null.</span><span class="sxs-lookup"><span data-stu-id="c112b-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="c112b-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="c112b-134">-UserId</span></span>
<span data-ttu-id="c112b-135">Gibt die Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="c112b-135">Specifies the user ID.</span></span>
<span data-ttu-id="c112b-136">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="c112b-136">This parameter is optional.</span></span>
<span data-ttu-id="c112b-137">Wenn dieser Parameter nicht angegeben wird, generiert dieses Cmdlet eine Benutzer-ID.</span><span class="sxs-lookup"><span data-stu-id="c112b-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="c112b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c112b-138">CommonParameters</span></span>
<span data-ttu-id="c112b-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c112b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c112b-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c112b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c112b-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c112b-141">INPUTS</span></span>

### <span data-ttu-id="c112b-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c112b-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c112b-143">System.String</span><span class="sxs-lookup"><span data-stu-id="c112b-143">System.String</span></span>

### <span data-ttu-id="c112b-144">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="c112b-144">System.Security.SecureString</span></span>

### <span data-ttu-id="c112b-145">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="c112b-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c112b-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c112b-146">OUTPUTS</span></span>

### <span data-ttu-id="c112b-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="c112b-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="c112b-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c112b-148">NOTES</span></span>

## <span data-ttu-id="c112b-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c112b-149">RELATED LINKS</span></span>

[<span data-ttu-id="c112b-150">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="c112b-150">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="c112b-151">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="c112b-151">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


