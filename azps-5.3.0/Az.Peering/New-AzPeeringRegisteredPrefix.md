---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ec3e37cafca19aefce7634bf84be41cd00e4e04d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384752"
---
# <span data-ttu-id="50dff-101">New-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="50dff-101">New-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="50dff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50dff-102">SYNOPSIS</span></span>
<span data-ttu-id="50dff-103">Erstellen Sie registrierte Präfixe für Peeringobjekte.</span><span class="sxs-lookup"><span data-stu-id="50dff-103">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="50dff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50dff-104">SYNTAX</span></span>

### <span data-ttu-id="50dff-105">ByResourceGroupAndName (Standard)</span><span class="sxs-lookup"><span data-stu-id="50dff-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50dff-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="50dff-106">InputObject</span></span>
```
New-AzPeeringRegisteredPrefix -InputObject <PSPeering> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50dff-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="50dff-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50dff-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50dff-108">DESCRIPTION</span></span>
<span data-ttu-id="50dff-109">Erstellen Sie registrierte Präfixe für Peeringobjekte.</span><span class="sxs-lookup"><span data-stu-id="50dff-109">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="50dff-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="50dff-110">EXAMPLES</span></span>

### <span data-ttu-id="50dff-111">Peering erhalten und ein registriertes Präfix erstellen</span><span class="sxs-lookup"><span data-stu-id="50dff-111">Get peering and create a registered prefix</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredPrefix -Name $asnName -Asn $asn
```

<span data-ttu-id="50dff-112">Holen Sie sich das Peering, dem Sie ein registriertes Präfix hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="50dff-112">Get the peering you want to add a registered prefix.</span></span> <span data-ttu-id="50dff-113">Übergeben Sie dies dann an das Commandlet.</span><span class="sxs-lookup"><span data-stu-id="50dff-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="50dff-114">Verwenden der PeeringressourceId zum Erstellen eines registrierten Asns</span><span class="sxs-lookup"><span data-stu-id="50dff-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredPrefix -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="50dff-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50dff-115">PARAMETERS</span></span>

### <span data-ttu-id="50dff-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50dff-116">-AsJob</span></span>
<span data-ttu-id="50dff-117">Führen Sie die Ausführung im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="50dff-117">Run in the background.</span></span>

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

### <span data-ttu-id="50dff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50dff-118">-DefaultProfile</span></span>
<span data-ttu-id="50dff-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="50dff-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50dff-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50dff-120">-InputObject</span></span>
<span data-ttu-id="50dff-121">Verwenden eines Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="50dff-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50dff-122">-Name</span><span class="sxs-lookup"><span data-stu-id="50dff-122">-Name</span></span>
<span data-ttu-id="50dff-123">Der Name des Präfixes.</span><span class="sxs-lookup"><span data-stu-id="50dff-123">The name of prefix.</span></span>

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

### <span data-ttu-id="50dff-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="50dff-124">-PeeringName</span></span>
<span data-ttu-id="50dff-125">Der eindeutige Name von PSPeering.</span><span class="sxs-lookup"><span data-stu-id="50dff-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50dff-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="50dff-126">-Prefix</span></span>
<span data-ttu-id="50dff-127">Das Sitzungs-IPv4-Präfix</span><span class="sxs-lookup"><span data-stu-id="50dff-127">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="50dff-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50dff-128">-ResourceGroupName</span></span>
<span data-ttu-id="50dff-129">Der Name einer vorhandenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="50dff-129">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50dff-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50dff-130">-ResourceId</span></span>
<span data-ttu-id="50dff-131">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="50dff-131">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50dff-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50dff-132">-Confirm</span></span>
<span data-ttu-id="50dff-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="50dff-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50dff-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="50dff-134">-WhatIf</span></span>
<span data-ttu-id="50dff-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="50dff-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50dff-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="50dff-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50dff-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50dff-137">CommonParameters</span></span>
<span data-ttu-id="50dff-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50dff-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50dff-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50dff-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50dff-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="50dff-140">INPUTS</span></span>

### <span data-ttu-id="50dff-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="50dff-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="50dff-142">System.String</span><span class="sxs-lookup"><span data-stu-id="50dff-142">System.String</span></span>

## <span data-ttu-id="50dff-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="50dff-143">OUTPUTS</span></span>

### <span data-ttu-id="50dff-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="50dff-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="50dff-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="50dff-145">NOTES</span></span>

## <span data-ttu-id="50dff-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="50dff-146">RELATED LINKS</span></span>
