---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
ms.openlocfilehash: ccd19f0390957466f9fb799d3655aa8bb1d02d68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658125"
---
# <span data-ttu-id="178c2-101">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="178c2-101">Set-AzApiManagementUser</span></span>

## <span data-ttu-id="178c2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="178c2-102">SYNOPSIS</span></span>
<span data-ttu-id="178c2-103">Legt Benutzer Details fest.</span><span class="sxs-lookup"><span data-stu-id="178c2-103">Sets user details.</span></span>

## <span data-ttu-id="178c2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="178c2-104">SYNTAX</span></span>

```
Set-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="178c2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="178c2-105">DESCRIPTION</span></span>
<span data-ttu-id="178c2-106">Das Cmdlet " **Set-AzApiManagementUser** " legt Benutzer Details fest.</span><span class="sxs-lookup"><span data-stu-id="178c2-106">The **Set-AzApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="178c2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="178c2-107">EXAMPLES</span></span>

### <span data-ttu-id="178c2-108">Beispiel 1: Ändern des Kennworts, der e-Mail-Adresse und des Status eines Benutzers</span><span class="sxs-lookup"><span data-stu-id="178c2-108">Example 1: Change a user's password, email address and state</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="178c2-109">Mit diesem Befehl wird ein neues Benutzerkennwort und eine e-Mail-Adresse festgelegt und der Benutzer blockiert.</span><span class="sxs-lookup"><span data-stu-id="178c2-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="178c2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="178c2-110">PARAMETERS</span></span>

### <span data-ttu-id="178c2-111">-Context</span><span class="sxs-lookup"><span data-stu-id="178c2-111">-Context</span></span>
<span data-ttu-id="178c2-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="178c2-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="178c2-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="178c2-113">This parameter is required.</span></span>

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

### <span data-ttu-id="178c2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="178c2-114">-DefaultProfile</span></span>
<span data-ttu-id="178c2-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="178c2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="178c2-116">– E-Mail</span><span class="sxs-lookup"><span data-stu-id="178c2-116">-Email</span></span>
<span data-ttu-id="178c2-117">Gibt die e-Mail-Adresse des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="178c2-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="178c2-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="178c2-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="178c2-119">-FirstName</span><span class="sxs-lookup"><span data-stu-id="178c2-119">-FirstName</span></span>
<span data-ttu-id="178c2-120">Gibt den Vornamen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="178c2-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="178c2-121">Dieser Parameter muss 1 bis 100 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="178c2-121">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="178c2-122">-Nachname</span><span class="sxs-lookup"><span data-stu-id="178c2-122">-LastName</span></span>
<span data-ttu-id="178c2-123">Gibt den letzten Namen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="178c2-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="178c2-124">Dieser Parameter muss 1 bis 100 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="178c2-124">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="178c2-125">-Hinweis</span><span class="sxs-lookup"><span data-stu-id="178c2-125">-Note</span></span>
<span data-ttu-id="178c2-126">Gibt eine Notiz über den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="178c2-126">Specifies a note about the user.</span></span>
<span data-ttu-id="178c2-127">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="178c2-127">This parameter is optional.</span></span>
<span data-ttu-id="178c2-128">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="178c2-128">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="178c2-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="178c2-129">-PassThru</span></span>
<span data-ttu-id="178c2-130">passthru</span><span class="sxs-lookup"><span data-stu-id="178c2-130">passthru</span></span>

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

### <span data-ttu-id="178c2-131">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="178c2-131">-Password</span></span>
<span data-ttu-id="178c2-132">Gibt das Benutzerkennwort an.</span><span class="sxs-lookup"><span data-stu-id="178c2-132">Specifies the user password.</span></span>
<span data-ttu-id="178c2-133">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="178c2-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="178c2-134">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="178c2-134">-State</span></span>
<span data-ttu-id="178c2-135">Gibt den Benutzerstatus an.</span><span class="sxs-lookup"><span data-stu-id="178c2-135">Specifies the user state.</span></span>
<span data-ttu-id="178c2-136">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="178c2-136">This parameter is optional.</span></span>
<span data-ttu-id="178c2-137">Der Standardwert ist aktiv.</span><span class="sxs-lookup"><span data-stu-id="178c2-137">The default value is Active.</span></span>

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

### <span data-ttu-id="178c2-138">-UserID</span><span class="sxs-lookup"><span data-stu-id="178c2-138">-UserId</span></span>
<span data-ttu-id="178c2-139">Gibt die Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="178c2-139">Specifies the user ID.</span></span>
<span data-ttu-id="178c2-140">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="178c2-140">This parameter is required.</span></span>

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

### <span data-ttu-id="178c2-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="178c2-141">-Confirm</span></span>
<span data-ttu-id="178c2-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="178c2-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="178c2-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="178c2-143">-WhatIf</span></span>
<span data-ttu-id="178c2-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="178c2-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="178c2-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="178c2-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="178c2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="178c2-146">CommonParameters</span></span>
<span data-ttu-id="178c2-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="178c2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="178c2-148">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="178c2-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="178c2-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="178c2-149">INPUTS</span></span>

### <span data-ttu-id="178c2-150">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="178c2-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="178c2-151">System. String</span><span class="sxs-lookup"><span data-stu-id="178c2-151">System.String</span></span>

### <span data-ttu-id="178c2-152">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="178c2-152">System.Security.SecureString</span></span>

### <span data-ttu-id="178c2-153">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementUserState</span><span class="sxs-lookup"><span data-stu-id="178c2-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState</span></span>

### <span data-ttu-id="178c2-154">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="178c2-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="178c2-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="178c2-155">OUTPUTS</span></span>

### <span data-ttu-id="178c2-156">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="178c2-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="178c2-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="178c2-157">NOTES</span></span>

## <span data-ttu-id="178c2-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="178c2-158">RELATED LINKS</span></span>

[<span data-ttu-id="178c2-159">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="178c2-159">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="178c2-160">Neu – AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="178c2-160">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="178c2-161">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="178c2-161">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)


