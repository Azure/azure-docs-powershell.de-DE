---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: cd32f29a0202fa8c38abed43075a8623efe068a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476374"
---
# <span data-ttu-id="a7f44-101">Remove-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="a7f44-101">Remove-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="a7f44-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a7f44-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f44-103">Eine bestimmte API-Revision entfernt</span><span class="sxs-lookup"><span data-stu-id="a7f44-103">Removed a particular API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7f44-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7f44-104">SYNTAX</span></span>

### <span data-ttu-id="a7f44-105">ByApiId (Standard)</span><span class="sxs-lookup"><span data-stu-id="a7f44-105">ByApiId (Default)</span></span>
```
Remove-AzureRmApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7f44-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a7f44-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiRevision -InputObject <PsApiManagementApi> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7f44-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7f44-107">DESCRIPTION</span></span>
<span data-ttu-id="a7f44-108">Das Cmdlet **Remove-AzureRmApiManagementApiRevision** entfernt eine bestimmte API-Revision.</span><span class="sxs-lookup"><span data-stu-id="a7f44-108">The cmdlet **Remove-AzureRmApiManagementApiRevision** removes a particular API revision.</span></span>

## <span data-ttu-id="a7f44-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7f44-109">EXAMPLES</span></span>

### <span data-ttu-id="a7f44-110">Beispiel 1: Entfernen einer API-Revision</span><span class="sxs-lookup"><span data-stu-id="a7f44-110">Example 1: Remove an API Revision</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiRevision -Context $apimContext -ApiId "echo-api" -ApiRevision "2"
```

<span data-ttu-id="a7f44-111">Mit diesem Befehl wird die `2` Überarbeitung der API `echo-api` vom API-Verwaltungsdienst entfernt.</span><span class="sxs-lookup"><span data-stu-id="a7f44-111">This command removes the `2` revision of the API `echo-api` from API Management service.</span></span>

## <span data-ttu-id="a7f44-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7f44-112">PARAMETERS</span></span>

### <span data-ttu-id="a7f44-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a7f44-113">-ApiId</span></span>
<span data-ttu-id="a7f44-114">Bezeichner der API.</span><span class="sxs-lookup"><span data-stu-id="a7f44-114">Identifier of the API.</span></span>
<span data-ttu-id="a7f44-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a7f44-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7f44-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="a7f44-116">-ApiRevision</span></span>
<span data-ttu-id="a7f44-117">Bezeichner der API-Revision.</span><span class="sxs-lookup"><span data-stu-id="a7f44-117">Identifier of the API Revision.</span></span> <span data-ttu-id="a7f44-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a7f44-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7f44-119">-Context</span><span class="sxs-lookup"><span data-stu-id="a7f44-119">-Context</span></span>
<span data-ttu-id="a7f44-120">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a7f44-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a7f44-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a7f44-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7f44-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f44-122">-DefaultProfile</span></span>
<span data-ttu-id="a7f44-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a7f44-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7f44-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a7f44-124">-InputObject</span></span>
<span data-ttu-id="a7f44-125">Instanz von PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="a7f44-125">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="a7f44-126">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a7f44-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7f44-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7f44-127">-PassThru</span></span>
<span data-ttu-id="a7f44-128">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="a7f44-128">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="a7f44-129">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a7f44-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="a7f44-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a7f44-130">-Confirm</span></span>
<span data-ttu-id="a7f44-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a7f44-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7f44-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7f44-132">-WhatIf</span></span>
<span data-ttu-id="a7f44-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a7f44-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7f44-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7f44-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7f44-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f44-135">CommonParameters</span></span>
<span data-ttu-id="a7f44-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7f44-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f44-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7f44-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f44-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a7f44-138">INPUTS</span></span>

### <span data-ttu-id="a7f44-139">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a7f44-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a7f44-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a7f44-140">System.String</span></span>

### <span data-ttu-id="a7f44-141">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a7f44-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="a7f44-142">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a7f44-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="a7f44-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a7f44-143">OUTPUTS</span></span>

### <span data-ttu-id="a7f44-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a7f44-144">System.Boolean</span></span>

## <span data-ttu-id="a7f44-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="a7f44-145">NOTES</span></span>

## <span data-ttu-id="a7f44-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a7f44-146">RELATED LINKS</span></span>

[<span data-ttu-id="a7f44-147">Get-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="a7f44-147">Get-AzureRmApiManagementApiRevision</span></span>](./Get-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="a7f44-148">Neu – AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="a7f44-148">New-AzureRmApiManagementApiRevision</span></span>](./New-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="a7f44-149">Satz-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="a7f44-149">Set-AzureRmApiManagementApiRevision</span></span>](./Set-AzureRmApiManagementApiRevision.md)
