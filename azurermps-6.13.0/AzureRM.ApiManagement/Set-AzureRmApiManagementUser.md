---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
ms.openlocfilehash: 705deeb8e9b248b480bd2a28662cc7e968f8c228
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478017"
---
# <span data-ttu-id="029f7-101">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="029f7-101">Set-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="029f7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="029f7-102">SYNOPSIS</span></span>
<span data-ttu-id="029f7-103">Legt Benutzer Details fest.</span><span class="sxs-lookup"><span data-stu-id="029f7-103">Sets user details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="029f7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="029f7-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="029f7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="029f7-105">DESCRIPTION</span></span>
<span data-ttu-id="029f7-106">Das Cmdlet " **Set-AzureRmApiManagementUser** " legt Benutzer Details fest.</span><span class="sxs-lookup"><span data-stu-id="029f7-106">The **Set-AzureRmApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="029f7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="029f7-107">EXAMPLES</span></span>

### <span data-ttu-id="029f7-108">Beispiel 1: Ändern des Kennworts, der e-Mail-Adresse und des Status eines Benutzers</span><span class="sxs-lookup"><span data-stu-id="029f7-108">Example 1: Change a user's password, email address and state</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="029f7-109">Mit diesem Befehl wird ein neues Benutzerkennwort und eine e-Mail-Adresse festgelegt und der Benutzer blockiert.</span><span class="sxs-lookup"><span data-stu-id="029f7-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="029f7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="029f7-110">PARAMETERS</span></span>

### <span data-ttu-id="029f7-111">-Context</span><span class="sxs-lookup"><span data-stu-id="029f7-111">-Context</span></span>
<span data-ttu-id="029f7-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="029f7-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="029f7-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="029f7-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="029f7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="029f7-114">-DefaultProfile</span></span>
<span data-ttu-id="029f7-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="029f7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="029f7-116">– E-Mail</span><span class="sxs-lookup"><span data-stu-id="029f7-116">-Email</span></span>
<span data-ttu-id="029f7-117">Gibt die e-Mail-Adresse des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="029f7-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="029f7-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="029f7-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="029f7-119">-FirstName</span><span class="sxs-lookup"><span data-stu-id="029f7-119">-FirstName</span></span>
<span data-ttu-id="029f7-120">Gibt den Vornamen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="029f7-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="029f7-121">Dieser Parameter muss 1 bis 100 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="029f7-121">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="029f7-122">-Nachname</span><span class="sxs-lookup"><span data-stu-id="029f7-122">-LastName</span></span>
<span data-ttu-id="029f7-123">Gibt den letzten Namen des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="029f7-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="029f7-124">Dieser Parameter muss 1 bis 100 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="029f7-124">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="029f7-125">-Hinweis</span><span class="sxs-lookup"><span data-stu-id="029f7-125">-Note</span></span>
<span data-ttu-id="029f7-126">Gibt eine Notiz über den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="029f7-126">Specifies a note about the user.</span></span>
<span data-ttu-id="029f7-127">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="029f7-127">This parameter is optional.</span></span>
<span data-ttu-id="029f7-128">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="029f7-128">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="029f7-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="029f7-129">-PassThru</span></span>
<span data-ttu-id="029f7-130">passthru</span><span class="sxs-lookup"><span data-stu-id="029f7-130">passthru</span></span>

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

### <span data-ttu-id="029f7-131">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="029f7-131">-Password</span></span>
<span data-ttu-id="029f7-132">Gibt das Benutzerkennwort an.</span><span class="sxs-lookup"><span data-stu-id="029f7-132">Specifies the user password.</span></span>
<span data-ttu-id="029f7-133">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="029f7-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="029f7-134">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="029f7-134">-State</span></span>
<span data-ttu-id="029f7-135">Gibt den Benutzerstatus an.</span><span class="sxs-lookup"><span data-stu-id="029f7-135">Specifies the user state.</span></span>
<span data-ttu-id="029f7-136">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="029f7-136">This parameter is optional.</span></span>
<span data-ttu-id="029f7-137">Der Standardwert ist aktiv.</span><span class="sxs-lookup"><span data-stu-id="029f7-137">The default value is Active.</span></span>

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

### <span data-ttu-id="029f7-138">-UserID</span><span class="sxs-lookup"><span data-stu-id="029f7-138">-UserId</span></span>
<span data-ttu-id="029f7-139">Gibt die Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="029f7-139">Specifies the user ID.</span></span>
<span data-ttu-id="029f7-140">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="029f7-140">This parameter is required.</span></span>

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

### <span data-ttu-id="029f7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="029f7-141">CommonParameters</span></span>
<span data-ttu-id="029f7-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="029f7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="029f7-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="029f7-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="029f7-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="029f7-144">INPUTS</span></span>

### <span data-ttu-id="029f7-145">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="029f7-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="029f7-146">System. String</span><span class="sxs-lookup"><span data-stu-id="029f7-146">System.String</span></span>

### <span data-ttu-id="029f7-147">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="029f7-147">System.Security.SecureString</span></span>

### <span data-ttu-id="029f7-148">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementUserState</span><span class="sxs-lookup"><span data-stu-id="029f7-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState</span></span>

### <span data-ttu-id="029f7-149">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="029f7-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="029f7-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="029f7-150">OUTPUTS</span></span>

### <span data-ttu-id="029f7-151">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="029f7-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="029f7-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="029f7-152">NOTES</span></span>

## <span data-ttu-id="029f7-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="029f7-153">RELATED LINKS</span></span>

[<span data-ttu-id="029f7-154">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="029f7-154">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="029f7-155">Neu – AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="029f7-155">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="029f7-156">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="029f7-156">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)


