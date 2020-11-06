---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 71256ab72d8c5c6042aa6c17b184066f96b3a813
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476378"
---
# <span data-ttu-id="78b49-101">Remove-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="78b49-101">Remove-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="78b49-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="78b49-102">SYNOPSIS</span></span>
<span data-ttu-id="78b49-103">Entfernt eine bestimmte API-Version</span><span class="sxs-lookup"><span data-stu-id="78b49-103">Removes a particular API Release</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78b49-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="78b49-104">SYNTAX</span></span>

### <span data-ttu-id="78b49-105">ByApiReleaseId (Standard)</span><span class="sxs-lookup"><span data-stu-id="78b49-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78b49-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="78b49-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78b49-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78b49-107">DESCRIPTION</span></span>

<span data-ttu-id="78b49-108">Das Cmdlet **Remove-AzureRmApiManagementApiRelease** entfernt eine vorhandene API-Version.</span><span class="sxs-lookup"><span data-stu-id="78b49-108">The **Remove-AzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="78b49-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78b49-109">EXAMPLES</span></span>

### <span data-ttu-id="78b49-110">Beispiel 1: Entfernen einer API-Version</span><span class="sxs-lookup"><span data-stu-id="78b49-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="78b49-111">Mit diesem Befehl wird die API-Version mit dem angegebenen ApiId und der angegebenen Veröffentlichungs-Nr entfernt.</span><span class="sxs-lookup"><span data-stu-id="78b49-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="78b49-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="78b49-112">PARAMETERS</span></span>

### <span data-ttu-id="78b49-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="78b49-113">-ApiId</span></span>
<span data-ttu-id="78b49-114">Bezeichner der API.</span><span class="sxs-lookup"><span data-stu-id="78b49-114">Identifier of the API.</span></span>
<span data-ttu-id="78b49-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="78b49-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78b49-116">-Context</span><span class="sxs-lookup"><span data-stu-id="78b49-116">-Context</span></span>
<span data-ttu-id="78b49-117">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="78b49-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="78b49-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="78b49-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78b49-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78b49-119">-DefaultProfile</span></span>
<span data-ttu-id="78b49-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="78b49-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78b49-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="78b49-121">-InputObject</span></span>
<span data-ttu-id="78b49-122">Instanz von PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="78b49-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="78b49-123">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="78b49-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78b49-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78b49-124">-PassThru</span></span>
<span data-ttu-id="78b49-125">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="78b49-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="78b49-126">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="78b49-126">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b49-127">-Veröffentlichungs-Nr</span><span class="sxs-lookup"><span data-stu-id="78b49-127">-ReleaseId</span></span>
<span data-ttu-id="78b49-128">Bezeichner der API-Version.</span><span class="sxs-lookup"><span data-stu-id="78b49-128">Identifier of the API Release.</span></span>
<span data-ttu-id="78b49-129">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="78b49-129">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78b49-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="78b49-130">-Confirm</span></span>
<span data-ttu-id="78b49-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="78b49-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78b49-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78b49-132">-WhatIf</span></span>
<span data-ttu-id="78b49-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="78b49-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78b49-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="78b49-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78b49-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78b49-135">CommonParameters</span></span>
<span data-ttu-id="78b49-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78b49-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78b49-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78b49-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78b49-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="78b49-138">INPUTS</span></span>

### <span data-ttu-id="78b49-139">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="78b49-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="78b49-140">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="78b49-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>
<span data-ttu-id="78b49-141">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="78b49-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="78b49-142">System. String</span><span class="sxs-lookup"><span data-stu-id="78b49-142">System.String</span></span>

## <span data-ttu-id="78b49-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="78b49-143">OUTPUTS</span></span>

### <span data-ttu-id="78b49-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="78b49-144">System.Boolean</span></span>

## <span data-ttu-id="78b49-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="78b49-145">NOTES</span></span>

## <span data-ttu-id="78b49-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="78b49-146">RELATED LINKS</span></span>

[<span data-ttu-id="78b49-147">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="78b49-147">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="78b49-148">Neu – AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="78b49-148">New-AzureRmApiManagementApiRelease</span></span>](./New-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="78b49-149">Satz-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="78b49-149">Set-AzureRmApiManagementApiRelease</span></span>](./Set-AzureRmApiManagementApiRelease.md)
