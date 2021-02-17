---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
ms.openlocfilehash: 222a40c101d0491a6d9409a7404e6731d739a2ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156260"
---
# <span data-ttu-id="91f99-101">New-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="91f99-101">New-AzSignalR</span></span>

## <span data-ttu-id="91f99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91f99-102">SYNOPSIS</span></span>
<span data-ttu-id="91f99-103">Erstellen Sie einen SignalR-Dienst.</span><span class="sxs-lookup"><span data-stu-id="91f99-103">Create a SignalR service.</span></span>

## <span data-ttu-id="91f99-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91f99-104">SYNTAX</span></span>

```
New-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-ServiceMode <String>] [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91f99-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91f99-105">DESCRIPTION</span></span>
<span data-ttu-id="91f99-106">Erstellen Sie einen SignalR-Dienst.</span><span class="sxs-lookup"><span data-stu-id="91f99-106">Create a SignalR service.</span></span>
<span data-ttu-id="91f99-107">Die folgenden Werte werden für die Parameter verwendet, wenn diese nicht angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="91f99-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="91f99-108">`ResourceGroupName`: die standardmäßige Ressourcengruppe, die von `Set-AzDefault -ResourceGroupName` festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="91f99-108">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="91f99-109">`Location`: Der Speicherort der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="91f99-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="91f99-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="91f99-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="91f99-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="91f99-111">EXAMPLES</span></span>

### <span data-ttu-id="91f99-112">Erstellen eines SignalR-Diensts</span><span class="sxs-lookup"><span data-stu-id="91f99-112">Create a SignalR service</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="91f99-113">Angeben von "ServiceMode" und "AllowedOrigin"</span><span class="sxs-lookup"><span data-stu-id="91f99-113">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -Location eastus -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="91f99-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91f99-114">PARAMETERS</span></span>

### <span data-ttu-id="91f99-115">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="91f99-115">-AllowedOrigin</span></span>
<span data-ttu-id="91f99-116">Die zulässigen Ursprünge für den SignalR-Dienst.</span><span class="sxs-lookup"><span data-stu-id="91f99-116">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="91f99-117">Wenn Sie alle zulassen möchten, verwenden Sie "\*", und entfernen Sie alle anderen Ursprünge aus der Liste.</span><span class="sxs-lookup"><span data-stu-id="91f99-117">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="91f99-118">Schrägstriche sind als Teil der Domäne oder nach TLD nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="91f99-118">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="91f99-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91f99-119">-AsJob</span></span>
<span data-ttu-id="91f99-120">Führen Sie das Cmdlet im Hintergrundauftrag aus.</span><span class="sxs-lookup"><span data-stu-id="91f99-120">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="91f99-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91f99-121">-DefaultProfile</span></span>
<span data-ttu-id="91f99-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="91f99-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91f99-123">-Location</span><span class="sxs-lookup"><span data-stu-id="91f99-123">-Location</span></span>
<span data-ttu-id="91f99-124">Der Standort des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="91f99-124">The SignalR service location.</span></span> <span data-ttu-id="91f99-125">Der Speicherort der Ressourcengruppe wird verwendet, wenn dieser nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="91f99-125">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="91f99-126">-Name</span><span class="sxs-lookup"><span data-stu-id="91f99-126">-Name</span></span>
<span data-ttu-id="91f99-127">Der Name des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="91f99-127">The SignalR service name.</span></span>

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

### <span data-ttu-id="91f99-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91f99-128">-ResourceGroupName</span></span>
<span data-ttu-id="91f99-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="91f99-129">The resource group name.</span></span> <span data-ttu-id="91f99-130">Die Standardeinstellung wird verwendet, wenn sie nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="91f99-130">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="91f99-131">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="91f99-131">-ServiceMode</span></span>
<span data-ttu-id="91f99-132">Der Dienstmodus für den SignalR-Dienst.</span><span class="sxs-lookup"><span data-stu-id="91f99-132">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="91f99-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="91f99-133">-Sku</span></span>
<span data-ttu-id="91f99-134">Die SKU des SignalR-Diensts.</span><span class="sxs-lookup"><span data-stu-id="91f99-134">The SignalR service SKU.</span></span>

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

### <span data-ttu-id="91f99-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="91f99-135">-Tag</span></span>
<span data-ttu-id="91f99-136">Die Tags für den SignalR-Dienst.</span><span class="sxs-lookup"><span data-stu-id="91f99-136">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="91f99-137">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="91f99-137">-UnitCount</span></span>
<span data-ttu-id="91f99-138">Die Anzahl der SignalR-Serviceeinheiten, von 1 bis 10.</span><span class="sxs-lookup"><span data-stu-id="91f99-138">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="91f99-139">Der Standardwert ist "1".</span><span class="sxs-lookup"><span data-stu-id="91f99-139">Default to 1.</span></span>

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

### <span data-ttu-id="91f99-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91f99-140">-Confirm</span></span>
<span data-ttu-id="91f99-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="91f99-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91f99-142">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="91f99-142">-WhatIf</span></span>
<span data-ttu-id="91f99-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="91f99-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91f99-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="91f99-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91f99-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91f99-145">CommonParameters</span></span>
<span data-ttu-id="91f99-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91f99-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91f99-147">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91f99-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91f99-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="91f99-148">INPUTS</span></span>

### <span data-ttu-id="91f99-149">System.String</span><span class="sxs-lookup"><span data-stu-id="91f99-149">System.String</span></span>

## <span data-ttu-id="91f99-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="91f99-150">OUTPUTS</span></span>

### <span data-ttu-id="91f99-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="91f99-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="91f99-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="91f99-152">NOTES</span></span>

## <span data-ttu-id="91f99-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="91f99-153">RELATED LINKS</span></span>
