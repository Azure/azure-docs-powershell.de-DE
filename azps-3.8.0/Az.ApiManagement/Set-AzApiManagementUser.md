---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
ms.openlocfilehash: a70cc953da853fd07dcee835f5a97a0efd2f6406
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004374"
---
# <span data-ttu-id="852f0-101">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="852f0-101">Set-AzApiManagementUser</span></span>

## <span data-ttu-id="852f0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="852f0-102">SYNOPSIS</span></span>
<span data-ttu-id="852f0-103">Legt Benutzer Details fest.</span><span class="sxs-lookup"><span data-stu-id="852f0-103">Sets user details.</span></span>

## <span data-ttu-id="852f0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="852f0-104">SYNTAX</span></span>

```
Set-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="852f0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="852f0-105">DESCRIPTION</span></span>
<span data-ttu-id="852f0-106">Das Cmdlet " **Set-AzApiManagementUser** " legt Benutzer Details fest.</span><span class="sxs-lookup"><span data-stu-id="852f0-106">The **Set-AzApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="852f0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="852f0-107">EXAMPLES</span></span>

### <span data-ttu-id="852f0-108">Beispiel 1: Ändern des Kennworts, der e-Mail-Adresse und des Status eines Benutzers</span><span class="sxs-lookup"><span data-stu-id="852f0-108">Example 1: Change a user's password, email address and state</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="852f0-109">Mit diesem Befehl wird ein neues Benutzerkennwort und eine e-Mail-Adresse festgelegt und der Benutzer blockiert.</span><span class="sxs-lookup"><span data-stu-id="852f0-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="852f0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="852f0-110">PARAMETERS</span></span>

### <span data-ttu-id="852f0-111">-Context</span><span class="sxs-lookup"><span data-stu-id="852f0-111">-Context</span></span>
<span data-ttu-id="852f0-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="852f0-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="852f0-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="852f0-113">This parameter is required.</span></span>

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

### <span data-ttu-id="852f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="852f0-114">-DefaultProfile</span></span>
<span data-ttu-id="852f0-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="852f0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="852f0-116">– E-Mail</span><span class="sxs-lookup"><span data-stu-id="852f0-116">-Email</span></span>
<span data-ttu-id="852f0-117">Gibt die e-Mail-Adresse des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="852f0-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="852f0-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="852f0-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="852f0-119">-FirstName</span><span class="sxs-lookup"><span data-stu-id="852f0-119">-FirstName</span></span>
<span data-ttu-id="852f0-120">Gibt den Vornamen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="852f0-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="852f0-121">Dieser Parameter muss 1 bis 100 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="852f0-121">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="852f0-122">-Nachname</span><span class="sxs-lookup"><span data-stu-id="852f0-122">-LastName</span></span>
<span data-ttu-id="852f0-123">Gibt den letzten Namen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="852f0-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="852f0-124">Dieser Parameter muss 1 bis 100 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="852f0-124">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="852f0-125">-Hinweis</span><span class="sxs-lookup"><span data-stu-id="852f0-125">-Note</span></span>
<span data-ttu-id="852f0-126">Gibt eine Notiz über den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="852f0-126">Specifies a note about the user.</span></span>
<span data-ttu-id="852f0-127">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="852f0-127">This parameter is optional.</span></span>
<span data-ttu-id="852f0-128">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="852f0-128">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="852f0-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="852f0-129">-PassThru</span></span>
<span data-ttu-id="852f0-130">passthru</span><span class="sxs-lookup"><span data-stu-id="852f0-130">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="852f0-131">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="852f0-131">-Password</span></span>
<span data-ttu-id="852f0-132">Gibt das Benutzerkennwort an.</span><span class="sxs-lookup"><span data-stu-id="852f0-132">Specifies the user password.</span></span>
<span data-ttu-id="852f0-133">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="852f0-133">This parameter is optional.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="852f0-134">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="852f0-134">-State</span></span>
<span data-ttu-id="852f0-135">Gibt den Benutzerstatus an.</span><span class="sxs-lookup"><span data-stu-id="852f0-135">Specifies the user state.</span></span>
<span data-ttu-id="852f0-136">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="852f0-136">This parameter is optional.</span></span>
<span data-ttu-id="852f0-137">Der Standardwert ist aktiv.</span><span class="sxs-lookup"><span data-stu-id="852f0-137">The default value is Active.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="852f0-138">-UserID</span><span class="sxs-lookup"><span data-stu-id="852f0-138">-UserId</span></span>
<span data-ttu-id="852f0-139">Gibt die Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="852f0-139">Specifies the user ID.</span></span>
<span data-ttu-id="852f0-140">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="852f0-140">This parameter is required.</span></span>

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

### <span data-ttu-id="852f0-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="852f0-141">-Confirm</span></span>
<span data-ttu-id="852f0-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="852f0-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="852f0-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="852f0-143">-WhatIf</span></span>
<span data-ttu-id="852f0-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="852f0-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="852f0-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="852f0-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="852f0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="852f0-146">CommonParameters</span></span>
<span data-ttu-id="852f0-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="852f0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="852f0-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="852f0-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="852f0-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="852f0-149">INPUTS</span></span>

### <span data-ttu-id="852f0-150">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="852f0-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="852f0-151">System. String</span><span class="sxs-lookup"><span data-stu-id="852f0-151">System.String</span></span>

### <span data-ttu-id="852f0-152">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="852f0-152">System.Security.SecureString</span></span>

### <span data-ttu-id="852f0-153">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementUserState</span><span class="sxs-lookup"><span data-stu-id="852f0-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState</span></span>

### <span data-ttu-id="852f0-154">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="852f0-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="852f0-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="852f0-155">OUTPUTS</span></span>

### <span data-ttu-id="852f0-156">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="852f0-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="852f0-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="852f0-157">NOTES</span></span>

## <span data-ttu-id="852f0-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="852f0-158">RELATED LINKS</span></span>

[<span data-ttu-id="852f0-159">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="852f0-159">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="852f0-160">Neu – AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="852f0-160">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="852f0-161">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="852f0-161">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)


