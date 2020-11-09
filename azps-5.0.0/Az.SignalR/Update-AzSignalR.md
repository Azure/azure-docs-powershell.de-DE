---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
ms.openlocfilehash: 632f271a085df8384a100392e8ed74ad7b5d0762
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300507"
---
# <span data-ttu-id="224d3-101">Update-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="224d3-101">Update-AzSignalR</span></span>

## <span data-ttu-id="224d3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="224d3-102">SYNOPSIS</span></span>
<span data-ttu-id="224d3-103">Aktualisieren Sie einen Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="224d3-103">Update a SignalR service.</span></span>

## <span data-ttu-id="224d3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="224d3-104">SYNTAX</span></span>

### <span data-ttu-id="224d3-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="224d3-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="224d3-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="224d3-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalR -ResourceId <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="224d3-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="224d3-107">InputObjectParameterSet</span></span>
```
Update-AzSignalR -InputObject <PSSignalRResource> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="224d3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="224d3-108">DESCRIPTION</span></span>
<span data-ttu-id="224d3-109">Aktualisieren Sie einen Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="224d3-109">Update a SignalR service.</span></span>
<span data-ttu-id="224d3-110">Die folgenden Werte werden für die Parameter verwendet, wenn Sie nicht angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="224d3-110">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="224d3-111">`ResourceGroupName`: die standardmäßige Ressourcengruppe, die von eingerichtet wird `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="224d3-111">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="224d3-112">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="224d3-112">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="224d3-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="224d3-113">EXAMPLES</span></span>

### <span data-ttu-id="224d3-114">Aktualisieren Sie einen bestimmten Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="224d3-114">Update a specific SignalR service.</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="224d3-115">Angeben von ServiceMode und AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="224d3-115">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="224d3-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="224d3-116">PARAMETERS</span></span>

### <span data-ttu-id="224d3-117">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="224d3-117">-AllowedOrigin</span></span>
<span data-ttu-id="224d3-118">Die zulässigen Ursprünge für den Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="224d3-118">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="224d3-119">Wenn Sie alle zulassen möchten, verwenden Sie "\*", und entfernen Sie alle anderen Ursprünge aus der Liste.</span><span class="sxs-lookup"><span data-stu-id="224d3-119">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="224d3-120">Schrägstriche sind als Teil der Domäne oder nach TLD nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="224d3-120">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="224d3-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="224d3-121">-AsJob</span></span>
<span data-ttu-id="224d3-122">Führen Sie das Cmdlet im Hintergrund Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="224d3-122">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="224d3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="224d3-123">-DefaultProfile</span></span>
<span data-ttu-id="224d3-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="224d3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="224d3-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="224d3-125">-InputObject</span></span>
<span data-ttu-id="224d3-126">Das Resource-Objekt des Signals.</span><span class="sxs-lookup"><span data-stu-id="224d3-126">The SignalR resource object.</span></span>

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

### <span data-ttu-id="224d3-127">-Name</span><span class="sxs-lookup"><span data-stu-id="224d3-127">-Name</span></span>
<span data-ttu-id="224d3-128">Der Name des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="224d3-128">The SignalR service name.</span></span>

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

### <span data-ttu-id="224d3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="224d3-129">-ResourceGroupName</span></span>
<span data-ttu-id="224d3-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="224d3-130">The resource group name.</span></span>
<span data-ttu-id="224d3-131">Wenn nicht angegeben, wird der Standardwert verwendet.</span><span class="sxs-lookup"><span data-stu-id="224d3-131">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="224d3-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="224d3-132">-ResourceId</span></span>
<span data-ttu-id="224d3-133">Die Ressourcen-ID des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="224d3-133">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="224d3-134">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="224d3-134">-ServiceMode</span></span>
<span data-ttu-id="224d3-135">Der Dienstmodus für den Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="224d3-135">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="224d3-136">-SKU</span><span class="sxs-lookup"><span data-stu-id="224d3-136">-Sku</span></span>
<span data-ttu-id="224d3-137">Die signaldienst-SKU.</span><span class="sxs-lookup"><span data-stu-id="224d3-137">The SignalR service SKU.</span></span>
<span data-ttu-id="224d3-138">Standardmäßig auf "Standard_S1".</span><span class="sxs-lookup"><span data-stu-id="224d3-138">Default to "Standard_S1".</span></span>

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

### <span data-ttu-id="224d3-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="224d3-139">-Tag</span></span>
<span data-ttu-id="224d3-140">Die Tags für den Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="224d3-140">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="224d3-141">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="224d3-141">-UnitCount</span></span>
<span data-ttu-id="224d3-142">Die Anzahl der Signalisierungs Dienst Einheiten, nur Wert von {1, 2, 5, 10, 20, 50, 100}.</span><span class="sxs-lookup"><span data-stu-id="224d3-142">The SignalR service unit count, value only from {1, 2, 5, 10, 20, 50, 100}.</span></span>
<span data-ttu-id="224d3-143">Standardwert 1.</span><span class="sxs-lookup"><span data-stu-id="224d3-143">Default to 1.</span></span>

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

### <span data-ttu-id="224d3-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="224d3-144">-Confirm</span></span>
<span data-ttu-id="224d3-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="224d3-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="224d3-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="224d3-146">-WhatIf</span></span>
<span data-ttu-id="224d3-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="224d3-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="224d3-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="224d3-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="224d3-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="224d3-149">CommonParameters</span></span>
<span data-ttu-id="224d3-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="224d3-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="224d3-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="224d3-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="224d3-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="224d3-152">INPUTS</span></span>

### <span data-ttu-id="224d3-153">System. String</span><span class="sxs-lookup"><span data-stu-id="224d3-153">System.String</span></span>

### <span data-ttu-id="224d3-154">Microsoft. Azure. Commands. signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="224d3-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="224d3-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="224d3-155">OUTPUTS</span></span>

### <span data-ttu-id="224d3-156">Microsoft. Azure. Commands. signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="224d3-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="224d3-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="224d3-157">NOTES</span></span>

## <span data-ttu-id="224d3-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="224d3-158">RELATED LINKS</span></span>
