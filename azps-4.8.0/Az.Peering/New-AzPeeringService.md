---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
ms.openlocfilehash: 60772963530d14eeb93f2f28fbf5e067ac5833ab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009002"
---
# <span data-ttu-id="24b9d-101">New-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="24b9d-101">New-AzPeeringService</span></span>

## <span data-ttu-id="24b9d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="24b9d-102">SYNOPSIS</span></span>
<span data-ttu-id="24b9d-103">Erstellt einen neuen peeringdienst.</span><span class="sxs-lookup"><span data-stu-id="24b9d-103">Creates a new peering service.</span></span>

## <span data-ttu-id="24b9d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="24b9d-104">SYNTAX</span></span>

```
New-AzPeeringService [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeeringServiceProvider] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24b9d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24b9d-105">DESCRIPTION</span></span>
<span data-ttu-id="24b9d-106">Erstellt peeringdienst.</span><span class="sxs-lookup"><span data-stu-id="24b9d-106">Creates peering service.</span></span>

## <span data-ttu-id="24b9d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="24b9d-107">EXAMPLES</span></span>

### <span data-ttu-id="24b9d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="24b9d-108">Example 1</span></span>
```powershell
PS C:\> New-AzPeeringService -ResourceGroupName $resourceGroup -Name $name -Location $loc -PeeringServiceProvider $provider

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="24b9d-109">Erstellt ein Peering-Dienstobjekt mit dem Anbieter und dem Peering-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="24b9d-109">Creates a peering service object with provider and peering location.</span></span> <span data-ttu-id="24b9d-110">Verwendung in Verbindung mit `Get-AzPeeringServiceProvider` und `Get-AzPeeringServiceLocation`</span><span class="sxs-lookup"><span data-stu-id="24b9d-110">Use in conjuction with `Get-AzPeeringServiceProvider` and `Get-AzPeeringServiceLocation`</span></span>

## <span data-ttu-id="24b9d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="24b9d-111">PARAMETERS</span></span>

### <span data-ttu-id="24b9d-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24b9d-112">-AsJob</span></span>
<span data-ttu-id="24b9d-113">Im Hintergrund ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="24b9d-113">Run in the background.</span></span>

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

### <span data-ttu-id="24b9d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24b9d-114">-DefaultProfile</span></span>
<span data-ttu-id="24b9d-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="24b9d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24b9d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="24b9d-116">-Name</span></span>
<span data-ttu-id="24b9d-117">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="24b9d-117">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24b9d-118">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="24b9d-118">-PeeringLocation</span></span>
<span data-ttu-id="24b9d-119">Der physikalische Standort, der sich vom Azure-Bereich unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="24b9d-119">The Physical Location Different from Azure Region.</span></span> <span data-ttu-id="24b9d-120">Verwenden von Get-AzPeeringServiceLocation [-Country <country> ]</span><span class="sxs-lookup"><span data-stu-id="24b9d-120">Use Get-AzPeeringServiceLocation [-Country <country>]</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24b9d-121">-PeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="24b9d-121">-PeeringServiceProvider</span></span>
<span data-ttu-id="24b9d-122">Der Name des Peering-Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="24b9d-122">The peering service provider name.</span></span>
<span data-ttu-id="24b9d-123">Verwenden des Get-AzPeeringServiceProvider-Cmdlets für eine Liste</span><span class="sxs-lookup"><span data-stu-id="24b9d-123">Use Get-AzPeeringServiceProvider cmdlet for a list</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24b9d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24b9d-124">-ResourceGroupName</span></span>
<span data-ttu-id="24b9d-125">Der Name der vorhandenen Ressourcengruppe erstellen oder verwenden</span><span class="sxs-lookup"><span data-stu-id="24b9d-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="24b9d-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="24b9d-126">-Tag</span></span>
<span data-ttu-id="24b9d-127">Die Tags, die dem Microsoft Inputobject-Dienst zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="24b9d-127">The tags to associate with the Microsoft InputObject Service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24b9d-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="24b9d-128">-Confirm</span></span>
<span data-ttu-id="24b9d-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="24b9d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24b9d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24b9d-130">-WhatIf</span></span>
<span data-ttu-id="24b9d-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="24b9d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24b9d-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="24b9d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24b9d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24b9d-133">CommonParameters</span></span>
<span data-ttu-id="24b9d-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24b9d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24b9d-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24b9d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24b9d-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="24b9d-136">INPUTS</span></span>

### <span data-ttu-id="24b9d-137">Keine</span><span class="sxs-lookup"><span data-stu-id="24b9d-137">None</span></span>

## <span data-ttu-id="24b9d-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="24b9d-138">OUTPUTS</span></span>

### <span data-ttu-id="24b9d-139">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="24b9d-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="24b9d-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="24b9d-140">NOTES</span></span>

## <span data-ttu-id="24b9d-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="24b9d-141">RELATED LINKS</span></span>
