---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/new-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
ms.openlocfilehash: 62beafd5546a52bd8e9cc61fae8ff90f7cd2ed1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920355"
---
# <span data-ttu-id="f6879-101">New-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="f6879-101">New-AzSignalR</span></span>

## <span data-ttu-id="f6879-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6879-102">SYNOPSIS</span></span>
<span data-ttu-id="f6879-103">Erstellen Sie einen SignalR-Dienst.</span><span class="sxs-lookup"><span data-stu-id="f6879-103">Create a SignalR service.</span></span>

## <span data-ttu-id="f6879-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6879-104">SYNTAX</span></span>

```
New-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-ServiceMode <String>] [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6879-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6879-105">DESCRIPTION</span></span>
<span data-ttu-id="f6879-106">Erstellen Sie einen SignalR-Dienst.</span><span class="sxs-lookup"><span data-stu-id="f6879-106">Create a SignalR service.</span></span>
<span data-ttu-id="f6879-107">Wenn nicht angegeben, werden die folgenden Werte für die Parameter verwendet:</span><span class="sxs-lookup"><span data-stu-id="f6879-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="f6879-108">`ResourceGroupName`: die von festgelegte `Set-AzDefault -ResourceGroupName` Standardressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f6879-108">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="f6879-109">`Location`: Der Speicherort der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f6879-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="f6879-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="f6879-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="f6879-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f6879-111">EXAMPLES</span></span>

### <span data-ttu-id="f6879-112">Erstellen eines SignalR-Diensts</span><span class="sxs-lookup"><span data-stu-id="f6879-112">Create a SignalR service</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="f6879-113">Angeben von ServiceMode und AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="f6879-113">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -Location eastus -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="f6879-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f6879-114">PARAMETERS</span></span>

### <span data-ttu-id="f6879-115">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="f6879-115">-AllowedOrigin</span></span>
<span data-ttu-id="f6879-116">Die zulässigen Ursprünge für den SignalR-Dienst.</span><span class="sxs-lookup"><span data-stu-id="f6879-116">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="f6879-117">Wenn Sie alle zulassen möchten, verwenden Sie "\*", und entfernen Sie alle anderen Ursprünge aus der Liste.</span><span class="sxs-lookup"><span data-stu-id="f6879-117">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="f6879-118">Schrägstriche sind nicht als Teil der Domäne oder nach TLD zulässig.</span><span class="sxs-lookup"><span data-stu-id="f6879-118">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="f6879-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6879-119">-AsJob</span></span>
<span data-ttu-id="f6879-120">Führen Sie das Cmdlet im Hintergrundauftrag aus.</span><span class="sxs-lookup"><span data-stu-id="f6879-120">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="f6879-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6879-121">-DefaultProfile</span></span>
<span data-ttu-id="f6879-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6879-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6879-123">-Location</span><span class="sxs-lookup"><span data-stu-id="f6879-123">-Location</span></span>
<span data-ttu-id="f6879-124">Der Standort des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="f6879-124">The SignalR service location.</span></span> <span data-ttu-id="f6879-125">Wenn nicht angegeben, wird der Ressourcengruppenspeicherort verwendet.</span><span class="sxs-lookup"><span data-stu-id="f6879-125">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="f6879-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f6879-126">-Name</span></span>
<span data-ttu-id="f6879-127">Der Name des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="f6879-127">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6879-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6879-128">-ResourceGroupName</span></span>
<span data-ttu-id="f6879-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f6879-129">The resource group name.</span></span> <span data-ttu-id="f6879-130">Die Standardeinstellung wird verwendet, wenn sie nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="f6879-130">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="f6879-131">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="f6879-131">-ServiceMode</span></span>
<span data-ttu-id="f6879-132">Der Dienstmodus für den SignalR-Dienst.</span><span class="sxs-lookup"><span data-stu-id="f6879-132">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="f6879-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="f6879-133">-Sku</span></span>
<span data-ttu-id="f6879-134">Die SKU des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="f6879-134">The SignalR service SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Standard_S1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6879-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="f6879-135">-Tag</span></span>
<span data-ttu-id="f6879-136">Die Tags für den SignalR-Dienst.</span><span class="sxs-lookup"><span data-stu-id="f6879-136">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="f6879-137">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="f6879-137">-UnitCount</span></span>
<span data-ttu-id="f6879-138">Die Anzahl der SignalR-Diensteinheiten von 1 bis 10.</span><span class="sxs-lookup"><span data-stu-id="f6879-138">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="f6879-139">Standardmäßig auf 1.</span><span class="sxs-lookup"><span data-stu-id="f6879-139">Default to 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6879-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f6879-140">-Confirm</span></span>
<span data-ttu-id="f6879-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f6879-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6879-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6879-142">-WhatIf</span></span>
<span data-ttu-id="f6879-143">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6879-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6879-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f6879-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6879-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6879-145">CommonParameters</span></span>
<span data-ttu-id="f6879-146">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6879-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6879-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6879-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6879-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f6879-148">INPUTS</span></span>

### <span data-ttu-id="f6879-149">System.String</span><span class="sxs-lookup"><span data-stu-id="f6879-149">System.String</span></span>

## <span data-ttu-id="f6879-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f6879-150">OUTPUTS</span></span>

### <span data-ttu-id="f6879-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="f6879-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="f6879-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f6879-152">NOTES</span></span>

## <span data-ttu-id="f6879-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f6879-153">RELATED LINKS</span></span>
