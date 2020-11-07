---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
ms.openlocfilehash: d8d88c2071cafad33fd4a80cb4c2de63ccf89647
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658225"
---
# <span data-ttu-id="533f1-101">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="533f1-101">New-AzApiManagementUser</span></span>

## <span data-ttu-id="533f1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="533f1-102">SYNOPSIS</span></span>
<span data-ttu-id="533f1-103">Registriert einen neuen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="533f1-103">Registers a new user.</span></span>

## <span data-ttu-id="533f1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="533f1-104">SYNTAX</span></span>

```
New-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="533f1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="533f1-105">DESCRIPTION</span></span>
<span data-ttu-id="533f1-106">Das Cmdlet **New-AzApiManagementUser** registriert einen neuen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="533f1-106">The **New-AzApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="533f1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="533f1-107">EXAMPLES</span></span>

### <span data-ttu-id="533f1-108">Beispiel 1: Registrieren eines neuen Benutzers</span><span class="sxs-lookup"><span data-stu-id="533f1-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="533f1-109">Mit diesem Befehl wird ein neuer Benutzernamens Patti Fuller registriert.</span><span class="sxs-lookup"><span data-stu-id="533f1-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="533f1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="533f1-110">PARAMETERS</span></span>

### <span data-ttu-id="533f1-111">-Context</span><span class="sxs-lookup"><span data-stu-id="533f1-111">-Context</span></span>
<span data-ttu-id="533f1-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="533f1-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="533f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="533f1-113">-DefaultProfile</span></span>
<span data-ttu-id="533f1-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="533f1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="533f1-115">– E-Mail</span><span class="sxs-lookup"><span data-stu-id="533f1-115">-Email</span></span>
<span data-ttu-id="533f1-116">Gibt die e-Mail-Adresse des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="533f1-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="533f1-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="533f1-117">-FirstName</span></span>
<span data-ttu-id="533f1-118">Gibt den Vornamen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="533f1-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="533f1-119">Dieser Parameter muss 1 bis 100 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="533f1-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="533f1-120">-Nachname</span><span class="sxs-lookup"><span data-stu-id="533f1-120">-LastName</span></span>
<span data-ttu-id="533f1-121">Gibt den letzten Namen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="533f1-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="533f1-122">Dieser Parameter muss 1 bis 100 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="533f1-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="533f1-123">-Hinweis</span><span class="sxs-lookup"><span data-stu-id="533f1-123">-Note</span></span>
<span data-ttu-id="533f1-124">Gibt eine Notiz über den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="533f1-124">Specifies a note about the user.</span></span>
<span data-ttu-id="533f1-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="533f1-125">This parameter is optional.</span></span>
<span data-ttu-id="533f1-126">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="533f1-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="533f1-127">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="533f1-127">-Password</span></span>
<span data-ttu-id="533f1-128">Gibt das Benutzerkennwort an.</span><span class="sxs-lookup"><span data-stu-id="533f1-128">Specifies the user password.</span></span>
<span data-ttu-id="533f1-129">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="533f1-129">This parameter is required.</span></span>

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

### <span data-ttu-id="533f1-130">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="533f1-130">-State</span></span>
<span data-ttu-id="533f1-131">Gibt den Benutzerstatus an.</span><span class="sxs-lookup"><span data-stu-id="533f1-131">Specifies the user state.</span></span>
<span data-ttu-id="533f1-132">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="533f1-132">This parameter is optional.</span></span>
<span data-ttu-id="533f1-133">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="533f1-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="533f1-134">-UserID</span><span class="sxs-lookup"><span data-stu-id="533f1-134">-UserId</span></span>
<span data-ttu-id="533f1-135">Gibt die Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="533f1-135">Specifies the user ID.</span></span>
<span data-ttu-id="533f1-136">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="533f1-136">This parameter is optional.</span></span>
<span data-ttu-id="533f1-137">Wenn dieser Parameter nicht angegeben wird, generiert dieses Cmdlet eine Benutzer-ID.</span><span class="sxs-lookup"><span data-stu-id="533f1-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="533f1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="533f1-138">CommonParameters</span></span>
<span data-ttu-id="533f1-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="533f1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="533f1-140">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="533f1-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="533f1-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="533f1-141">INPUTS</span></span>

### <span data-ttu-id="533f1-142">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="533f1-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="533f1-143">System. String</span><span class="sxs-lookup"><span data-stu-id="533f1-143">System.String</span></span>

### <span data-ttu-id="533f1-144">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="533f1-144">System.Security.SecureString</span></span>

### <span data-ttu-id="533f1-145">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementUserState, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. Servicemanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="533f1-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="533f1-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="533f1-146">OUTPUTS</span></span>

### <span data-ttu-id="533f1-147">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="533f1-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="533f1-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="533f1-148">NOTES</span></span>

## <span data-ttu-id="533f1-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="533f1-149">RELATED LINKS</span></span>

[<span data-ttu-id="533f1-150">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="533f1-150">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="533f1-151">Satz-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="533f1-151">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


