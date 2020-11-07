---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
ms.openlocfilehash: 8c8240ed1df30dface1bdb2ce0b649bacf17d08a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659299"
---
# <span data-ttu-id="15fe4-101">New-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="15fe4-101">New-AzSignalR</span></span>

## <span data-ttu-id="15fe4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="15fe4-102">SYNOPSIS</span></span>
<span data-ttu-id="15fe4-103">Erstellen Sie einen Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="15fe4-103">Create a SignalR service.</span></span>

## <span data-ttu-id="15fe4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="15fe4-104">SYNTAX</span></span>

```
New-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15fe4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15fe4-105">DESCRIPTION</span></span>
<span data-ttu-id="15fe4-106">Erstellen Sie einen Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="15fe4-106">Create a SignalR service.</span></span>
<span data-ttu-id="15fe4-107">Die folgenden Werte werden für die Parameter verwendet, wenn Sie nicht angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="15fe4-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="15fe4-108">`ResourceGroupName`: die standardmäßige Ressourcengruppe, die von eingerichtet wird `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="15fe4-108">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="15fe4-109">`Location`: der Speicherort der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="15fe4-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="15fe4-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="15fe4-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="15fe4-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15fe4-111">EXAMPLES</span></span>

### <span data-ttu-id="15fe4-112">Erstellen eines Signalisierungs-Serivce</span><span class="sxs-lookup"><span data-stu-id="15fe4-112">Create a SignalR serivce</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0-preview
```

## <span data-ttu-id="15fe4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="15fe4-113">PARAMETERS</span></span>

### <span data-ttu-id="15fe4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15fe4-114">-AsJob</span></span>
<span data-ttu-id="15fe4-115">Führen Sie das Cmdlet im Hintergrund Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="15fe4-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="15fe4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15fe4-116">-DefaultProfile</span></span>
<span data-ttu-id="15fe4-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="15fe4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15fe4-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="15fe4-118">-Location</span></span>
<span data-ttu-id="15fe4-119">Der Signalisierungs Dienststandort.</span><span class="sxs-lookup"><span data-stu-id="15fe4-119">The SignalR service location.</span></span> <span data-ttu-id="15fe4-120">Wenn nicht angegeben, wird der Speicherort der Ressourcengruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="15fe4-120">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="15fe4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="15fe4-121">-Name</span></span>
<span data-ttu-id="15fe4-122">Der Name des Signal Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="15fe4-122">The SignalR service name.</span></span>

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

### <span data-ttu-id="15fe4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15fe4-123">-ResourceGroupName</span></span>
<span data-ttu-id="15fe4-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="15fe4-124">The resource group name.</span></span> <span data-ttu-id="15fe4-125">Wenn nicht angegeben, wird der Standardwert verwendet.</span><span class="sxs-lookup"><span data-stu-id="15fe4-125">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="15fe4-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="15fe4-126">-Sku</span></span>
<span data-ttu-id="15fe4-127">Die signaldienst-SKU.</span><span class="sxs-lookup"><span data-stu-id="15fe4-127">The SignalR service SKU.</span></span>

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

### <span data-ttu-id="15fe4-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="15fe4-128">-Tag</span></span>
<span data-ttu-id="15fe4-129">Die Tags für den Signalisierungs Dienst.</span><span class="sxs-lookup"><span data-stu-id="15fe4-129">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="15fe4-130">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="15fe4-130">-UnitCount</span></span>
<span data-ttu-id="15fe4-131">Die Anzahl der Signalisierungs Dienste von 1 bis 10.</span><span class="sxs-lookup"><span data-stu-id="15fe4-131">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="15fe4-132">Standardwert 1.</span><span class="sxs-lookup"><span data-stu-id="15fe4-132">Default to 1.</span></span>

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

### <span data-ttu-id="15fe4-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="15fe4-133">-Confirm</span></span>
<span data-ttu-id="15fe4-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="15fe4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15fe4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15fe4-135">-WhatIf</span></span>
<span data-ttu-id="15fe4-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15fe4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15fe4-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15fe4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15fe4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15fe4-138">CommonParameters</span></span>
<span data-ttu-id="15fe4-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15fe4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15fe4-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15fe4-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15fe4-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="15fe4-141">INPUTS</span></span>

### <span data-ttu-id="15fe4-142">Keine</span><span class="sxs-lookup"><span data-stu-id="15fe4-142">None</span></span>

## <span data-ttu-id="15fe4-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="15fe4-143">OUTPUTS</span></span>

### <span data-ttu-id="15fe4-144">Microsoft. Azure. Commands. signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="15fe4-144">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="15fe4-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="15fe4-145">NOTES</span></span>

## <span data-ttu-id="15fe4-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="15fe4-146">RELATED LINKS</span></span>
