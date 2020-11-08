---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
ms.openlocfilehash: 52e422f6c86f17c6620c58c1034b45250d4edf08
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995984"
---
# <span data-ttu-id="b9d27-101">Update-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="b9d27-101">Update-AzSignalR</span></span>

## <span data-ttu-id="b9d27-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b9d27-102">SYNOPSIS</span></span>
<span data-ttu-id="b9d27-103">Aktualisieren Sie einen Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="b9d27-103">Update a SignalR service.</span></span>

## <span data-ttu-id="b9d27-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9d27-104">SYNTAX</span></span>

### <span data-ttu-id="b9d27-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b9d27-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9d27-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9d27-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalR -ResourceId <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9d27-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9d27-107">InputObjectParameterSet</span></span>
```
Update-AzSignalR -InputObject <PSSignalRResource> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9d27-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9d27-108">DESCRIPTION</span></span>
<span data-ttu-id="b9d27-109">Aktualisieren Sie einen Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="b9d27-109">Update a SignalR service.</span></span>
<span data-ttu-id="b9d27-110">Die folgenden Werte werden für die Parameter verwendet, wenn Sie nicht angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="b9d27-110">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="b9d27-111">`ResourceGroupName`: die standardmäßige Ressourcengruppe, die von eingerichtet wird `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="b9d27-111">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="b9d27-112">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="b9d27-112">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="b9d27-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9d27-113">EXAMPLES</span></span>

### <span data-ttu-id="b9d27-114">Aktualisieren Sie einen bestimmten Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="b9d27-114">Update a specific SignalR service.</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="b9d27-115">Angeben von ServiceMode und AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="b9d27-115">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="b9d27-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9d27-116">PARAMETERS</span></span>

### <span data-ttu-id="b9d27-117">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="b9d27-117">-AllowedOrigin</span></span>
<span data-ttu-id="b9d27-118">Die zulässigen Ursprünge für den Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="b9d27-118">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="b9d27-119">Wenn Sie alle zulassen möchten, verwenden Sie "\*", und entfernen Sie alle anderen Ursprünge aus der Liste.</span><span class="sxs-lookup"><span data-stu-id="b9d27-119">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="b9d27-120">Schrägstriche sind als Teil der Domäne oder nach TLD nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="b9d27-120">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="b9d27-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9d27-121">-AsJob</span></span>
<span data-ttu-id="b9d27-122">Führen Sie das Cmdlet im Hintergrund Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="b9d27-122">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="b9d27-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9d27-123">-DefaultProfile</span></span>
<span data-ttu-id="b9d27-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b9d27-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9d27-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b9d27-125">-InputObject</span></span>
<span data-ttu-id="b9d27-126">Das Resource-Objekt des Signals.</span><span class="sxs-lookup"><span data-stu-id="b9d27-126">The SignalR resource object.</span></span>

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

### <span data-ttu-id="b9d27-127">-Name</span><span class="sxs-lookup"><span data-stu-id="b9d27-127">-Name</span></span>
<span data-ttu-id="b9d27-128">Der Name des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="b9d27-128">The SignalR service name.</span></span>

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

### <span data-ttu-id="b9d27-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9d27-129">-ResourceGroupName</span></span>
<span data-ttu-id="b9d27-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b9d27-130">The resource group name.</span></span>
<span data-ttu-id="b9d27-131">Wenn nicht angegeben, wird der Standardwert verwendet.</span><span class="sxs-lookup"><span data-stu-id="b9d27-131">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="b9d27-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b9d27-132">-ResourceId</span></span>
<span data-ttu-id="b9d27-133">Die Ressourcen-ID des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="b9d27-133">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9d27-134">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="b9d27-134">-ServiceMode</span></span>
<span data-ttu-id="b9d27-135">Der Dienstmodus für den Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="b9d27-135">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="b9d27-136">-SKU</span><span class="sxs-lookup"><span data-stu-id="b9d27-136">-Sku</span></span>
<span data-ttu-id="b9d27-137">Die signaldienst-SKU.</span><span class="sxs-lookup"><span data-stu-id="b9d27-137">The SignalR service SKU.</span></span>
<span data-ttu-id="b9d27-138">Standardmäßig auf "Standard_S1".</span><span class="sxs-lookup"><span data-stu-id="b9d27-138">Default to "Standard_S1".</span></span>

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

### <span data-ttu-id="b9d27-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="b9d27-139">-Tag</span></span>
<span data-ttu-id="b9d27-140">Die Tags für den Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="b9d27-140">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="b9d27-141">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="b9d27-141">-UnitCount</span></span>
<span data-ttu-id="b9d27-142">Die Anzahl der Signalisierungs Dienst Einheiten, nur Wert von {1, 2, 5, 10, 20, 50, 100}.</span><span class="sxs-lookup"><span data-stu-id="b9d27-142">The SignalR service unit count, value only from {1, 2, 5, 10, 20, 50, 100}.</span></span>
<span data-ttu-id="b9d27-143">Standardwert 1.</span><span class="sxs-lookup"><span data-stu-id="b9d27-143">Default to 1.</span></span>

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

### <span data-ttu-id="b9d27-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b9d27-144">-Confirm</span></span>
<span data-ttu-id="b9d27-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b9d27-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9d27-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9d27-146">-WhatIf</span></span>
<span data-ttu-id="b9d27-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b9d27-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9d27-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9d27-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9d27-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9d27-149">CommonParameters</span></span>
<span data-ttu-id="b9d27-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9d27-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9d27-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9d27-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9d27-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b9d27-152">INPUTS</span></span>

### <span data-ttu-id="b9d27-153">System. String</span><span class="sxs-lookup"><span data-stu-id="b9d27-153">System.String</span></span>

### <span data-ttu-id="b9d27-154">Microsoft. Azure. Commands. signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="b9d27-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="b9d27-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b9d27-155">OUTPUTS</span></span>

### <span data-ttu-id="b9d27-156">Microsoft. Azure. Commands. signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="b9d27-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="b9d27-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="b9d27-157">NOTES</span></span>

## <span data-ttu-id="b9d27-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b9d27-158">RELATED LINKS</span></span>
