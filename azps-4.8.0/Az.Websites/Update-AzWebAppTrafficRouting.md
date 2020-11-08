---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
ms.openlocfilehash: 7fba74a3778df0c8c26ed4b581e5d2777ff75029
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173327"
---
# <span data-ttu-id="7adf5-101">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7adf5-101">Update-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="7adf5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7adf5-102">SYNOPSIS</span></span>
<span data-ttu-id="7adf5-103">Aktualisieren Sie eine Routingregel auf den Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="7adf5-103">Update a routing Rule to the Slot.</span></span>

## <span data-ttu-id="7adf5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7adf5-104">SYNTAX</span></span>

```
Update-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7adf5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7adf5-105">DESCRIPTION</span></span>
<span data-ttu-id="7adf5-106">Das Cmdlet **Update-AzWebAppTrafficRouting** aktualisiert die Routingregelkonfiguration für einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="7adf5-106">The **Update-AzWebAppTrafficRouting** cmdlet updates the routing rule configuration for an Azure Web App Slot.</span></span>

## <span data-ttu-id="7adf5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7adf5-107">EXAMPLES</span></span>

### <span data-ttu-id="7adf5-108">Beispiel 1 Aktualisieren einer Routingregel, um 15% des Produktions Verkehrs an den STG-Steckplatz zu übertragen</span><span class="sxs-lookup"><span data-stu-id="7adf5-108">Example 1 Update a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
- RoutingRule @{AtionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="7adf5-109">Mit diesem Befehl wird eine Routingregel aktualisiert, um 15% des Produktions Datenverkehrs an den STG-Steckplatz zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="7adf5-109">This command updates a routing rule to transfer 15% of production traffic to Stg slot.</span></span>

### <span data-ttu-id="7adf5-110">Beispiel 2 Aktualisieren einer Routingregel zur Übertragung des Produktions Datenverkehrs auf den STG-Steckplatz Bereich von 50% auf 90% in inkrementeller Weise.</span><span class="sxs-lookup"><span data-stu-id="7adf5-110">Example 2 Update a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="7adf5-111">Mit diesem Befehl wird eine Routingregel aktualisiert, um den Produktionsverkehr in die STG-Steckplatz Bereiche von 50% auf 90% in inkrementeller Weise zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="7adf5-111">This command Updates a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="7adf5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7adf5-112">PARAMETERS</span></span>

### <span data-ttu-id="7adf5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7adf5-113">-DefaultProfile</span></span>
<span data-ttu-id="7adf5-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7adf5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7adf5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7adf5-115">-ResourceGroupName</span></span>
<span data-ttu-id="7adf5-116">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7adf5-116">ResourceGroupName</span></span>
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

### <span data-ttu-id="7adf5-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="7adf5-117">-RoutingRule</span></span>
<span data-ttu-id="7adf5-118">Web App-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="7adf5-118">Web App RoutingRule.</span></span>
<span data-ttu-id="7adf5-119">Beispiel:-RoutingRule @ {ActionHostName = $Slot. DefaultHostName ReroutePercentage = $ReroutePercentage; Name = $slotName}</span><span class="sxs-lookup"><span data-stu-id="7adf5-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

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

### <span data-ttu-id="7adf5-120">-Webbasierter</span><span class="sxs-lookup"><span data-stu-id="7adf5-120">-WebAppName</span></span>
<span data-ttu-id="7adf5-121">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="7adf5-121">WebApp Name</span></span>

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

### <span data-ttu-id="7adf5-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7adf5-122">-Confirm</span></span>
<span data-ttu-id="7adf5-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7adf5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7adf5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7adf5-124">-WhatIf</span></span>
<span data-ttu-id="7adf5-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7adf5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7adf5-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7adf5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7adf5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7adf5-127">CommonParameters</span></span>
<span data-ttu-id="7adf5-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7adf5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7adf5-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7adf5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7adf5-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7adf5-130">INPUTS</span></span>

### <span data-ttu-id="7adf5-131">Keine</span><span class="sxs-lookup"><span data-stu-id="7adf5-131">None</span></span>

## <span data-ttu-id="7adf5-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7adf5-132">OUTPUTS</span></span>

### <span data-ttu-id="7adf5-133">Microsoft. Azure. Management. Websites. Models. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="7adf5-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="7adf5-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="7adf5-134">NOTES</span></span>

## <span data-ttu-id="7adf5-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7adf5-135">RELATED LINKS</span></span>

[<span data-ttu-id="7adf5-136">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7adf5-136">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="7adf5-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7adf5-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="7adf5-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="7adf5-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)