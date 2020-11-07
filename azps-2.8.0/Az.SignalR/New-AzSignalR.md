---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
ms.openlocfilehash: 0f393a6442732e1f25edc6d6192bd6cf0a926a55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823132"
---
# <span data-ttu-id="c85f3-101">New-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="c85f3-101">New-AzSignalR</span></span>

## <span data-ttu-id="c85f3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c85f3-102">SYNOPSIS</span></span>
<span data-ttu-id="c85f3-103">Erstellen Sie einen Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="c85f3-103">Create a SignalR service.</span></span>

## <span data-ttu-id="c85f3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c85f3-104">SYNTAX</span></span>

```
New-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-ServiceMode <String>] [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c85f3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c85f3-105">DESCRIPTION</span></span>
<span data-ttu-id="c85f3-106">Erstellen Sie einen Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="c85f3-106">Create a SignalR service.</span></span>
<span data-ttu-id="c85f3-107">Die folgenden Werte werden für die Parameter verwendet, wenn Sie nicht angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="c85f3-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="c85f3-108">`ResourceGroupName`: die standardmäßige Ressourcengruppe, die von eingerichtet wird `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="c85f3-108">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="c85f3-109">`Location`: der Speicherort der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="c85f3-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="c85f3-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="c85f3-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="c85f3-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c85f3-111">EXAMPLES</span></span>

### <span data-ttu-id="c85f3-112">Erstellen eines Signalisierungs Diensts</span><span class="sxs-lookup"><span data-stu-id="c85f3-112">Create a SignalR service</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="c85f3-113">Angeben von ServiceMode und AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="c85f3-113">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -Location eastus -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="c85f3-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c85f3-114">PARAMETERS</span></span>

### <span data-ttu-id="c85f3-115">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="c85f3-115">-AllowedOrigin</span></span>
<span data-ttu-id="c85f3-116">Die zulässigen Ursprünge für den Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="c85f3-116">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="c85f3-117">Wenn Sie alle zulassen möchten, verwenden Sie "\*", und entfernen Sie alle anderen Ursprünge aus der Liste.</span><span class="sxs-lookup"><span data-stu-id="c85f3-117">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="c85f3-118">Schrägstriche sind als Teil der Domäne oder nach TLD nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="c85f3-118">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="c85f3-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c85f3-119">-AsJob</span></span>
<span data-ttu-id="c85f3-120">Führen Sie das Cmdlet im Hintergrund Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="c85f3-120">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="c85f3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c85f3-121">-DefaultProfile</span></span>
<span data-ttu-id="c85f3-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c85f3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c85f3-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="c85f3-123">-Location</span></span>
<span data-ttu-id="c85f3-124">Der Signalisierungs Dienststandort.</span><span class="sxs-lookup"><span data-stu-id="c85f3-124">The SignalR service location.</span></span> <span data-ttu-id="c85f3-125">Wenn nicht angegeben, wird der Speicherort der Ressourcengruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="c85f3-125">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="c85f3-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c85f3-126">-Name</span></span>
<span data-ttu-id="c85f3-127">Der Name des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="c85f3-127">The SignalR service name.</span></span>

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

### <span data-ttu-id="c85f3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c85f3-128">-ResourceGroupName</span></span>
<span data-ttu-id="c85f3-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c85f3-129">The resource group name.</span></span> <span data-ttu-id="c85f3-130">Wenn nicht angegeben, wird der Standardwert verwendet.</span><span class="sxs-lookup"><span data-stu-id="c85f3-130">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="c85f3-131">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="c85f3-131">-ServiceMode</span></span>
<span data-ttu-id="c85f3-132">Der Dienstmodus für den Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="c85f3-132">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="c85f3-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="c85f3-133">-Sku</span></span>
<span data-ttu-id="c85f3-134">Die signaldienst-SKU.</span><span class="sxs-lookup"><span data-stu-id="c85f3-134">The SignalR service SKU.</span></span>

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

### <span data-ttu-id="c85f3-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="c85f3-135">-Tag</span></span>
<span data-ttu-id="c85f3-136">Die Tags für den Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="c85f3-136">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="c85f3-137">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="c85f3-137">-UnitCount</span></span>
<span data-ttu-id="c85f3-138">Die Anzahl der Signalisierungs Dienste von 1 bis 10.</span><span class="sxs-lookup"><span data-stu-id="c85f3-138">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="c85f3-139">Standardwert 1.</span><span class="sxs-lookup"><span data-stu-id="c85f3-139">Default to 1.</span></span>

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

### <span data-ttu-id="c85f3-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c85f3-140">-Confirm</span></span>
<span data-ttu-id="c85f3-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c85f3-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c85f3-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c85f3-142">-WhatIf</span></span>
<span data-ttu-id="c85f3-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c85f3-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c85f3-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c85f3-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c85f3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c85f3-145">CommonParameters</span></span>
<span data-ttu-id="c85f3-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c85f3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c85f3-147">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c85f3-147">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c85f3-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c85f3-148">INPUTS</span></span>

### <span data-ttu-id="c85f3-149">System. String</span><span class="sxs-lookup"><span data-stu-id="c85f3-149">System.String</span></span>

## <span data-ttu-id="c85f3-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c85f3-150">OUTPUTS</span></span>

### <span data-ttu-id="c85f3-151">Microsoft. Azure. Commands. signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="c85f3-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="c85f3-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="c85f3-152">NOTES</span></span>

## <span data-ttu-id="c85f3-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c85f3-153">RELATED LINKS</span></span>
