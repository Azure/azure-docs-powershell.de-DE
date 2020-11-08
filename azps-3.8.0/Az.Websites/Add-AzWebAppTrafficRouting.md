---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
ms.openlocfilehash: 822a26d37bc083a059cfb4b89a0f526a104fbb84
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995563"
---
# <span data-ttu-id="ae4df-101">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="ae4df-101">Add-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="ae4df-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ae4df-102">SYNOPSIS</span></span>
<span data-ttu-id="ae4df-103">Fügen Sie dem Steckplatz eine Routingregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="ae4df-103">Add a routing Rule to the Slot.</span></span>

## <span data-ttu-id="ae4df-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae4df-104">SYNTAX</span></span>

```
Add-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae4df-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae4df-105">DESCRIPTION</span></span>
<span data-ttu-id="ae4df-106">Das Cmdlet **Add-AzWebAppTrafficRouting** fügt eine Routing Regel zu einem Azure Web App-Steckplatz hinzu.</span><span class="sxs-lookup"><span data-stu-id="ae4df-106">The **Add-AzWebAppTrafficRouting** cmdlet adds a Routing rule to an Azure Web App Slot.</span></span>

## <span data-ttu-id="ae4df-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ae4df-107">EXAMPLES</span></span>

### <span data-ttu-id="ae4df-108">Beispiel 1: Hinzufügen einer Routingregel zur Übertragung von 15% des Produktions Datenverkehrs an den STG-Steckplatz</span><span class="sxs-lookup"><span data-stu-id="ae4df-108">Example 1 Add a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
- RoutingRule @{AtionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="ae4df-109">Dieser Befehl fügt eine Routingregel hinzu, um 15% des Produktions Verkehrs an den STG-Steckplatz zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="ae4df-109">This command adds a routing rule to transfer 15% of production traffice to  Stg slot</span></span>

### <span data-ttu-id="ae4df-110">Beispiel 2 Fügen Sie eine Routingregel hinzu, um den Produktionsverkehr in den STG-Steckplatz zu übertragen, der sich in inkrementeller Weise von 50% auf 90% erstreckt.</span><span class="sxs-lookup"><span data-stu-id="ae4df-110">Example 2 Add a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="ae4df-111">Mit diesem Befehl wird eine Routingregel hinzugefügt, um den Produktionsverkehr in die STG-Steckplatz Bereiche von 50% auf 90% in inkrementeller Weise zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="ae4df-111">This command adds a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="ae4df-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae4df-112">PARAMETERS</span></span>

### <span data-ttu-id="ae4df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae4df-113">-DefaultProfile</span></span>
<span data-ttu-id="ae4df-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ae4df-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae4df-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae4df-115">-ResourceGroupName</span></span>
<span data-ttu-id="ae4df-116">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="ae4df-116">Resource Group Name</span></span>

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

### <span data-ttu-id="ae4df-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="ae4df-117">-RoutingRule</span></span>
<span data-ttu-id="ae4df-118">Web App-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="ae4df-118">Web App RoutingRule.</span></span>
<span data-ttu-id="ae4df-119">Beispiel:-RoutingRule @ {ActionHostName = $Slot. DefaultHostName ReroutePercentage = $ReroutePercentage; Name = $slotName}</span><span class="sxs-lookup"><span data-stu-id="ae4df-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

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

### <span data-ttu-id="ae4df-120">-Webbasierter</span><span class="sxs-lookup"><span data-stu-id="ae4df-120">-WebAppName</span></span>
<span data-ttu-id="ae4df-121">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="ae4df-121">WebApp Name</span></span>

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

### <span data-ttu-id="ae4df-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ae4df-122">-Confirm</span></span>
<span data-ttu-id="ae4df-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ae4df-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae4df-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae4df-124">-WhatIf</span></span>
<span data-ttu-id="ae4df-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ae4df-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae4df-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae4df-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae4df-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae4df-127">CommonParameters</span></span>
<span data-ttu-id="ae4df-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae4df-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae4df-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae4df-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae4df-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ae4df-130">INPUTS</span></span>

### <span data-ttu-id="ae4df-131">Keine</span><span class="sxs-lookup"><span data-stu-id="ae4df-131">None</span></span>

## <span data-ttu-id="ae4df-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ae4df-132">OUTPUTS</span></span>

### <span data-ttu-id="ae4df-133">Microsoft. Azure. Management. Websites. Models. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="ae4df-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="ae4df-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="ae4df-134">NOTES</span></span>

## <span data-ttu-id="ae4df-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ae4df-135">RELATED LINKS</span></span>
[<span data-ttu-id="ae4df-136">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="ae4df-136">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="ae4df-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="ae4df-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="ae4df-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="ae4df-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)