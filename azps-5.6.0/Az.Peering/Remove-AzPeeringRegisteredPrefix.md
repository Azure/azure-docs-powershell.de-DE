---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/remove-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: db62779ab2ac03e6ef528b09dda99fb5ebb244a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937619"
---
# <span data-ttu-id="184dd-101">Remove-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="184dd-101">Remove-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="184dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="184dd-102">SYNOPSIS</span></span>
<span data-ttu-id="184dd-103">Löschen oder Entfernen eines registrierten Präfixes aus der übergeordneten Peeringressource.</span><span class="sxs-lookup"><span data-stu-id="184dd-103">Delete or remove a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="184dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="184dd-104">SYNTAX</span></span>

### <span data-ttu-id="184dd-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="184dd-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 [-Force] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="184dd-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="184dd-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredPrefix -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="184dd-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="184dd-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="184dd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="184dd-108">DESCRIPTION</span></span>
<span data-ttu-id="184dd-109">Ermöglicht das Entfernen des registrierten Präfixes aus der übergeordneten Peeringressource.</span><span class="sxs-lookup"><span data-stu-id="184dd-109">Allows the removal of registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="184dd-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="184dd-110">EXAMPLES</span></span>

### <span data-ttu-id="184dd-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="184dd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredPrefix -ResourceId $resourceId
```

<span data-ttu-id="184dd-112">Entfernen Sie ein registriertes Präfix nach Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="184dd-112">Remove a registerd prefix by resource id.</span></span>

## <span data-ttu-id="184dd-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="184dd-113">PARAMETERS</span></span>

### <span data-ttu-id="184dd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="184dd-114">-AsJob</span></span>
<span data-ttu-id="184dd-115">Führen Sie im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="184dd-115">Run in the background.</span></span>

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

### <span data-ttu-id="184dd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="184dd-116">-DefaultProfile</span></span>
<span data-ttu-id="184dd-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="184dd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="184dd-118">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="184dd-118">-Force</span></span>
<span data-ttu-id="184dd-119">Erzwingen des Vorgangs</span><span class="sxs-lookup"><span data-stu-id="184dd-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="184dd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="184dd-120">-InputObject</span></span>
<span data-ttu-id="184dd-121">Verwenden eines Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="184dd-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="184dd-122">-Name</span><span class="sxs-lookup"><span data-stu-id="184dd-122">-Name</span></span>
<span data-ttu-id="184dd-123">Der Name des Präfixes.</span><span class="sxs-lookup"><span data-stu-id="184dd-123">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="184dd-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="184dd-124">-PassThru</span></span>
<span data-ttu-id="184dd-125">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="184dd-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="184dd-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="184dd-126">-PeeringName</span></span>
<span data-ttu-id="184dd-127">Der eindeutige Name des PSPeerings.</span><span class="sxs-lookup"><span data-stu-id="184dd-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="184dd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="184dd-128">-ResourceGroupName</span></span>
<span data-ttu-id="184dd-129">Erstellen oder Verwenden eines vorhandenen Ressourcengruppennamens.</span><span class="sxs-lookup"><span data-stu-id="184dd-129">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="184dd-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="184dd-130">-ResourceId</span></span>
<span data-ttu-id="184dd-131">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="184dd-131">The resource id string name.</span></span>

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

### <span data-ttu-id="184dd-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="184dd-132">-Confirm</span></span>
<span data-ttu-id="184dd-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="184dd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="184dd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="184dd-134">-WhatIf</span></span>
<span data-ttu-id="184dd-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="184dd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="184dd-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="184dd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="184dd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="184dd-137">CommonParameters</span></span>
<span data-ttu-id="184dd-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="184dd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="184dd-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="184dd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="184dd-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="184dd-140">INPUTS</span></span>

### <span data-ttu-id="184dd-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="184dd-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="184dd-142">System.String</span><span class="sxs-lookup"><span data-stu-id="184dd-142">System.String</span></span>

## <span data-ttu-id="184dd-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="184dd-143">OUTPUTS</span></span>

### <span data-ttu-id="184dd-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="184dd-144">System.Boolean</span></span>

## <span data-ttu-id="184dd-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="184dd-145">NOTES</span></span>

## <span data-ttu-id="184dd-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="184dd-146">RELATED LINKS</span></span>
