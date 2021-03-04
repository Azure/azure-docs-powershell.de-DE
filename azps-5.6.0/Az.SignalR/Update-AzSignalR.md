---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/update-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
ms.openlocfilehash: d02db6e59c688a79b0088c3b3b42fde0cbc13bb8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920291"
---
# <span data-ttu-id="78f5f-101">Update-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="78f5f-101">Update-AzSignalR</span></span>

## <span data-ttu-id="78f5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78f5f-102">SYNOPSIS</span></span>
<span data-ttu-id="78f5f-103">Aktualisieren eines SignalR-Diensts</span><span class="sxs-lookup"><span data-stu-id="78f5f-103">Update a SignalR service.</span></span>

## <span data-ttu-id="78f5f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78f5f-104">SYNTAX</span></span>

### <span data-ttu-id="78f5f-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="78f5f-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78f5f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78f5f-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalR -ResourceId <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78f5f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78f5f-107">InputObjectParameterSet</span></span>
```
Update-AzSignalR -InputObject <PSSignalRResource> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78f5f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="78f5f-108">DESCRIPTION</span></span>
<span data-ttu-id="78f5f-109">Aktualisieren eines SignalR-Diensts</span><span class="sxs-lookup"><span data-stu-id="78f5f-109">Update a SignalR service.</span></span>
<span data-ttu-id="78f5f-110">Wenn nicht angegeben, werden die folgenden Werte für die Parameter verwendet:</span><span class="sxs-lookup"><span data-stu-id="78f5f-110">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="78f5f-111">`ResourceGroupName`: die von festgelegte `Set-AzDefault -ResourceGroupName` Standardressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="78f5f-111">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="78f5f-112">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="78f5f-112">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="78f5f-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="78f5f-113">EXAMPLES</span></span>

### <span data-ttu-id="78f5f-114">Aktualisieren Sie einen bestimmten SignalR-Dienst.</span><span class="sxs-lookup"><span data-stu-id="78f5f-114">Update a specific SignalR service.</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="78f5f-115">Angeben von ServiceMode und AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="78f5f-115">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="78f5f-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="78f5f-116">PARAMETERS</span></span>

### <span data-ttu-id="78f5f-117">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="78f5f-117">-AllowedOrigin</span></span>
<span data-ttu-id="78f5f-118">Die zulässigen Ursprünge für den SignalR-Dienst.</span><span class="sxs-lookup"><span data-stu-id="78f5f-118">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="78f5f-119">Wenn Sie alle zulassen möchten, verwenden Sie "\*", und entfernen Sie alle anderen Ursprünge aus der Liste.</span><span class="sxs-lookup"><span data-stu-id="78f5f-119">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="78f5f-120">Schrägstriche sind nicht als Teil der Domäne oder nach TLD zulässig.</span><span class="sxs-lookup"><span data-stu-id="78f5f-120">Slashes are not allowed as part of domain or after TLD</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f5f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78f5f-121">-AsJob</span></span>
<span data-ttu-id="78f5f-122">Führen Sie das Cmdlet im Hintergrundauftrag aus.</span><span class="sxs-lookup"><span data-stu-id="78f5f-122">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="78f5f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78f5f-123">-DefaultProfile</span></span>
<span data-ttu-id="78f5f-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78f5f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78f5f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78f5f-125">-InputObject</span></span>
<span data-ttu-id="78f5f-126">Das SignalR-Ressourcenobjekt.</span><span class="sxs-lookup"><span data-stu-id="78f5f-126">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78f5f-127">-Name</span><span class="sxs-lookup"><span data-stu-id="78f5f-127">-Name</span></span>
<span data-ttu-id="78f5f-128">Der Name des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="78f5f-128">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f5f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78f5f-129">-ResourceGroupName</span></span>
<span data-ttu-id="78f5f-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="78f5f-130">The resource group name.</span></span>
<span data-ttu-id="78f5f-131">Die Standardeinstellung wird verwendet, wenn sie nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="78f5f-131">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f5f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78f5f-132">-ResourceId</span></span>
<span data-ttu-id="78f5f-133">Die Ressourcen-ID des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="78f5f-133">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78f5f-134">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="78f5f-134">-ServiceMode</span></span>
<span data-ttu-id="78f5f-135">Der Dienstmodus für den SignalR-Dienst.</span><span class="sxs-lookup"><span data-stu-id="78f5f-135">The service mode for the SignalR service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f5f-136">-Sku</span><span class="sxs-lookup"><span data-stu-id="78f5f-136">-Sku</span></span>
<span data-ttu-id="78f5f-137">Die SKU des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="78f5f-137">The SignalR service SKU.</span></span>
<span data-ttu-id="78f5f-138">Standardmäßig auf "Standard_S1".</span><span class="sxs-lookup"><span data-stu-id="78f5f-138">Default to "Standard_S1".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f5f-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="78f5f-139">-Tag</span></span>
<span data-ttu-id="78f5f-140">Die Tags für den SignalR-Dienst.</span><span class="sxs-lookup"><span data-stu-id="78f5f-140">The tags for the SignalR service.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f5f-141">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="78f5f-141">-UnitCount</span></span>
<span data-ttu-id="78f5f-142">Die Anzahl der SignalR-Diensteinheiten, wert nur von {1, 2, 5, 10, 20, 50, 100}.</span><span class="sxs-lookup"><span data-stu-id="78f5f-142">The SignalR service unit count, value only from {1, 2, 5, 10, 20, 50, 100}.</span></span>
<span data-ttu-id="78f5f-143">Standardmäßig auf 1.</span><span class="sxs-lookup"><span data-stu-id="78f5f-143">Default to 1.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f5f-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="78f5f-144">-Confirm</span></span>
<span data-ttu-id="78f5f-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="78f5f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78f5f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78f5f-146">-WhatIf</span></span>
<span data-ttu-id="78f5f-147">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="78f5f-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78f5f-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="78f5f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78f5f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78f5f-149">CommonParameters</span></span>
<span data-ttu-id="78f5f-150">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78f5f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78f5f-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78f5f-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78f5f-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="78f5f-152">INPUTS</span></span>

### <span data-ttu-id="78f5f-153">System.String</span><span class="sxs-lookup"><span data-stu-id="78f5f-153">System.String</span></span>

### <span data-ttu-id="78f5f-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="78f5f-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="78f5f-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="78f5f-155">OUTPUTS</span></span>

### <span data-ttu-id="78f5f-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="78f5f-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="78f5f-157">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="78f5f-157">NOTES</span></span>

## <span data-ttu-id="78f5f-158">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="78f5f-158">RELATED LINKS</span></span>
