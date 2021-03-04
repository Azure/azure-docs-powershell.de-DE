---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/remove-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
ms.openlocfilehash: c878f7559d6e4dcfab79ae9daccaa2f82f548a62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937624"
---
# <span data-ttu-id="ecbee-101">Remove-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="ecbee-101">Remove-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="ecbee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecbee-102">SYNOPSIS</span></span>
<span data-ttu-id="ecbee-103">Löschen oder Entfernen eines registrierten ASNs aus der übergeordneten Peeringressource.</span><span class="sxs-lookup"><span data-stu-id="ecbee-103">Delete or remove a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="ecbee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ecbee-104">SYNTAX</span></span>

### <span data-ttu-id="ecbee-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ecbee-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecbee-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ecbee-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredAsn -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecbee-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ecbee-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecbee-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ecbee-108">DESCRIPTION</span></span>
<span data-ttu-id="ecbee-109">Ermöglicht das Entfernen des registrierten ASN aus der übergeordneten Peeringressource.</span><span class="sxs-lookup"><span data-stu-id="ecbee-109">Allows the removal of registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="ecbee-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ecbee-110">EXAMPLES</span></span>

### <span data-ttu-id="ecbee-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ecbee-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredAsn -ResourceId $resourceId
```

<span data-ttu-id="ecbee-112">Entfernen Sie einen registrierten ASN nach Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ecbee-112">Remove a registerd ASN by resource id.</span></span>

## <span data-ttu-id="ecbee-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ecbee-113">PARAMETERS</span></span>

### <span data-ttu-id="ecbee-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ecbee-114">-AsJob</span></span>
<span data-ttu-id="ecbee-115">Führen Sie im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="ecbee-115">Run in the background.</span></span>

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

### <span data-ttu-id="ecbee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecbee-116">-DefaultProfile</span></span>
<span data-ttu-id="ecbee-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ecbee-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecbee-118">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="ecbee-118">-Force</span></span>
<span data-ttu-id="ecbee-119">Erzwingen des Vorgangs</span><span class="sxs-lookup"><span data-stu-id="ecbee-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="ecbee-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecbee-120">-InputObject</span></span>
<span data-ttu-id="ecbee-121">Verwenden eines Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="ecbee-121">Use a Get-AzPeeringServicePrefix</span></span>

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

### <span data-ttu-id="ecbee-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ecbee-122">-Name</span></span>
<span data-ttu-id="ecbee-123">Der Name des registrierten ASN</span><span class="sxs-lookup"><span data-stu-id="ecbee-123">The name of the registered ASN</span></span>

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

### <span data-ttu-id="ecbee-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecbee-124">-PassThru</span></span>
<span data-ttu-id="ecbee-125">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="ecbee-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="ecbee-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="ecbee-126">-PeeringName</span></span>
<span data-ttu-id="ecbee-127">Der eindeutige Name des PSPeerings.</span><span class="sxs-lookup"><span data-stu-id="ecbee-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="ecbee-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecbee-128">-ResourceGroupName</span></span>
<span data-ttu-id="ecbee-129">Erstellen oder Verwenden eines vorhandenen Ressourcengruppennamens.</span><span class="sxs-lookup"><span data-stu-id="ecbee-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="ecbee-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecbee-130">-ResourceId</span></span>
<span data-ttu-id="ecbee-131">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ecbee-131">The resource id string name.</span></span>

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

### <span data-ttu-id="ecbee-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ecbee-132">-Confirm</span></span>
<span data-ttu-id="ecbee-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ecbee-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecbee-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecbee-134">-WhatIf</span></span>
<span data-ttu-id="ecbee-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ecbee-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecbee-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ecbee-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecbee-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecbee-137">CommonParameters</span></span>
<span data-ttu-id="ecbee-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecbee-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecbee-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecbee-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecbee-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ecbee-140">INPUTS</span></span>

### <span data-ttu-id="ecbee-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="ecbee-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="ecbee-142">System.String</span><span class="sxs-lookup"><span data-stu-id="ecbee-142">System.String</span></span>

## <span data-ttu-id="ecbee-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ecbee-143">OUTPUTS</span></span>

### <span data-ttu-id="ecbee-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ecbee-144">System.Boolean</span></span>

## <span data-ttu-id="ecbee-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ecbee-145">NOTES</span></span>

## <span data-ttu-id="ecbee-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ecbee-146">RELATED LINKS</span></span>
