---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
ms.openlocfilehash: 8a3949397b12b54062c5cc68f367187f691fb02d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934579"
---
# <span data-ttu-id="06afd-101">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="06afd-101">Add-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="06afd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06afd-102">SYNOPSIS</span></span>
<span data-ttu-id="06afd-103">Fügen Sie dem Slot eine Routingregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="06afd-103">Add a routing Rule to the Slot.</span></span>

## <span data-ttu-id="06afd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06afd-104">SYNTAX</span></span>

```
Add-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06afd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06afd-105">DESCRIPTION</span></span>
<span data-ttu-id="06afd-106">Das **Add-AzWebAppTrafficRouting-Cmdlet** fügt einem Azure Web App-Slot eine Routingregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="06afd-106">The **Add-AzWebAppTrafficRouting** cmdlet adds a Routing rule to an Azure Web App Slot.</span></span>

## <span data-ttu-id="06afd-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="06afd-107">EXAMPLES</span></span>

### <span data-ttu-id="06afd-108">Beispiel 1 Hinzufügen einer Routingregel zum Übertragen von 15 % des Produktionsdatenverkehrs an den Steckplatz "Stg"</span><span class="sxs-lookup"><span data-stu-id="06afd-108">Example 1 Add a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="06afd-109">Mit diesem Befehl wird eine Routingregel zum Übertragen von 15 % des Produktionsdatenverkehrs an den Steckplatz "Stg" addiert.</span><span class="sxs-lookup"><span data-stu-id="06afd-109">This command adds a routing rule to transfer 15% of production traffice to  Stg slot</span></span>

### <span data-ttu-id="06afd-110">Beispiel 2 Fügen Sie eine Routingregel hinzu, um den Produktionsdatenverkehr in inkrementelle Weise zwischen 50 % und 90 % zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="06afd-110">Example 2 Add a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="06afd-111">Dieser Befehl fügt eine Routingregel hinzu, um den Produktionsdatenverkehr in inkrementelle Weise von 50 % bis 90 % an die Stg-Slotbereiche zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="06afd-111">This command adds a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="06afd-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="06afd-112">PARAMETERS</span></span>

### <span data-ttu-id="06afd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06afd-113">-DefaultProfile</span></span>
<span data-ttu-id="06afd-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="06afd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06afd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06afd-115">-ResourceGroupName</span></span>
<span data-ttu-id="06afd-116">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="06afd-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06afd-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="06afd-117">-RoutingRule</span></span>
<span data-ttu-id="06afd-118">Web App RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="06afd-118">Web App RoutingRule.</span></span>
<span data-ttu-id="06afd-119">Beispiel: -RoutingRule @{ActionHostName=$slot. DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span><span class="sxs-lookup"><span data-stu-id="06afd-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06afd-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="06afd-120">-WebAppName</span></span>
<span data-ttu-id="06afd-121">WebApp-Name</span><span class="sxs-lookup"><span data-stu-id="06afd-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06afd-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="06afd-122">-Confirm</span></span>
<span data-ttu-id="06afd-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="06afd-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06afd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06afd-124">-WhatIf</span></span>
<span data-ttu-id="06afd-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="06afd-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06afd-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="06afd-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06afd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06afd-127">CommonParameters</span></span>
<span data-ttu-id="06afd-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06afd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06afd-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06afd-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06afd-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="06afd-130">INPUTS</span></span>

### <span data-ttu-id="06afd-131">Keine</span><span class="sxs-lookup"><span data-stu-id="06afd-131">None</span></span>

## <span data-ttu-id="06afd-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="06afd-132">OUTPUTS</span></span>

### <span data-ttu-id="06afd-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="06afd-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="06afd-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="06afd-134">NOTES</span></span>

## <span data-ttu-id="06afd-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="06afd-135">RELATED LINKS</span></span>
[<span data-ttu-id="06afd-136">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="06afd-136">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="06afd-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="06afd-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="06afd-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="06afd-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
