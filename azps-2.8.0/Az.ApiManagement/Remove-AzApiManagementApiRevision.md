---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRevision.md
ms.openlocfilehash: 2b8db6f5d550c91f806595c80be4beb300a95273
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658208"
---
# <span data-ttu-id="29600-101">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="29600-101">Remove-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="29600-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29600-102">SYNOPSIS</span></span>
<span data-ttu-id="29600-103">Eine bestimmte API-Revision entfernt</span><span class="sxs-lookup"><span data-stu-id="29600-103">Removed a particular API Revision</span></span>

## <span data-ttu-id="29600-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29600-104">SYNTAX</span></span>

### <span data-ttu-id="29600-105">ByApiId (Standard)</span><span class="sxs-lookup"><span data-stu-id="29600-105">ByApiId (Default)</span></span>
```
Remove-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29600-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="29600-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29600-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29600-107">DESCRIPTION</span></span>
<span data-ttu-id="29600-108">Das Cmdlet **Remove-AzApiManagementApiRevision** entfernt eine bestimmte API-Revision.</span><span class="sxs-lookup"><span data-stu-id="29600-108">The cmdlet **Remove-AzApiManagementApiRevision** removes a particular API revision.</span></span>

## <span data-ttu-id="29600-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29600-109">EXAMPLES</span></span>

### <span data-ttu-id="29600-110">Beispiel 1: Entfernen einer API-Revision</span><span class="sxs-lookup"><span data-stu-id="29600-110">Example 1: Remove an API Revision</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRevision -Context $apimContext -ApiId "echo-api" -ApiRevision "2"
```

<span data-ttu-id="29600-111">Mit diesem Befehl wird die `2` Überarbeitung der API `echo-api` vom API-Verwaltungsdienst entfernt.</span><span class="sxs-lookup"><span data-stu-id="29600-111">This command removes the `2` revision of the API `echo-api` from API Management service.</span></span>

## <span data-ttu-id="29600-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="29600-112">PARAMETERS</span></span>

### <span data-ttu-id="29600-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="29600-113">-ApiId</span></span>
<span data-ttu-id="29600-114">Bezeichner der API.</span><span class="sxs-lookup"><span data-stu-id="29600-114">Identifier of the API.</span></span>
<span data-ttu-id="29600-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="29600-115">This parameter is required.</span></span>

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

### <span data-ttu-id="29600-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="29600-116">-ApiRevision</span></span>
<span data-ttu-id="29600-117">Bezeichner der API-Revision.</span><span class="sxs-lookup"><span data-stu-id="29600-117">Identifier of the API Revision.</span></span> <span data-ttu-id="29600-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="29600-118">This parameter is required.</span></span>

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

### <span data-ttu-id="29600-119">-Context</span><span class="sxs-lookup"><span data-stu-id="29600-119">-Context</span></span>
<span data-ttu-id="29600-120">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="29600-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="29600-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="29600-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29600-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29600-122">-DefaultProfile</span></span>
<span data-ttu-id="29600-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="29600-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29600-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="29600-124">-InputObject</span></span>
<span data-ttu-id="29600-125">Instanz von PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="29600-125">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="29600-126">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="29600-126">This parameter is required.</span></span>

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

### <span data-ttu-id="29600-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29600-127">-PassThru</span></span>
<span data-ttu-id="29600-128">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="29600-128">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="29600-129">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="29600-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="29600-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="29600-130">-Confirm</span></span>
<span data-ttu-id="29600-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="29600-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29600-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29600-132">-WhatIf</span></span>
<span data-ttu-id="29600-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29600-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29600-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29600-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29600-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29600-135">CommonParameters</span></span>
<span data-ttu-id="29600-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29600-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29600-137">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29600-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29600-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29600-138">INPUTS</span></span>

### <span data-ttu-id="29600-139">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="29600-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="29600-140">System. String</span><span class="sxs-lookup"><span data-stu-id="29600-140">System.String</span></span>

### <span data-ttu-id="29600-141">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="29600-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="29600-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29600-142">OUTPUTS</span></span>

### <span data-ttu-id="29600-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="29600-143">System.Boolean</span></span>

## <span data-ttu-id="29600-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="29600-144">NOTES</span></span>

## <span data-ttu-id="29600-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29600-145">RELATED LINKS</span></span>

[<span data-ttu-id="29600-146">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="29600-146">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="29600-147">Neu – AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="29600-147">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="29600-148">Satz-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="29600-148">Set-AzApiManagementApiRevision</span></span>](./Set-AzApiManagementApiRevision.md)