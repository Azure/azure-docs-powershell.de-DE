---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d43fe033b58ba6295728bc0c21ddb1d853587b59
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172277"
---
# <span data-ttu-id="27599-101">Remove-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="27599-101">Remove-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="27599-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27599-102">SYNOPSIS</span></span>
<span data-ttu-id="27599-103">Löschen oder entfernen Sie einen registrierten ASN aus der übergeordneten Peeringressource.</span><span class="sxs-lookup"><span data-stu-id="27599-103">Delete or remove a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="27599-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27599-104">SYNTAX</span></span>

### <span data-ttu-id="27599-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="27599-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27599-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="27599-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredAsn -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27599-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="27599-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27599-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27599-108">DESCRIPTION</span></span>
<span data-ttu-id="27599-109">Ermöglicht das Entfernen des registrierten ASNs aus der übergeordneten Peeringressource.</span><span class="sxs-lookup"><span data-stu-id="27599-109">Allows the removal of registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="27599-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="27599-110">EXAMPLES</span></span>

### <span data-ttu-id="27599-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="27599-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredAsn -ResourceId $resourceId
```

<span data-ttu-id="27599-112">Entfernen Sie einen registrierten ASN nach Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="27599-112">Remove a registerd ASN by resource id.</span></span>

## <span data-ttu-id="27599-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27599-113">PARAMETERS</span></span>

### <span data-ttu-id="27599-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27599-114">-AsJob</span></span>
<span data-ttu-id="27599-115">Führen Sie die Ausführung im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="27599-115">Run in the background.</span></span>

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

### <span data-ttu-id="27599-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27599-116">-DefaultProfile</span></span>
<span data-ttu-id="27599-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="27599-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27599-118">-Force</span><span class="sxs-lookup"><span data-stu-id="27599-118">-Force</span></span>
<span data-ttu-id="27599-119">Erzwingen des Vorgangs</span><span class="sxs-lookup"><span data-stu-id="27599-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="27599-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27599-120">-InputObject</span></span>
<span data-ttu-id="27599-121">Verwenden eines Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="27599-121">Use a Get-AzPeeringServicePrefix</span></span>

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

### <span data-ttu-id="27599-122">-Name</span><span class="sxs-lookup"><span data-stu-id="27599-122">-Name</span></span>
<span data-ttu-id="27599-123">Der Name des registrierten ASNs</span><span class="sxs-lookup"><span data-stu-id="27599-123">The name of the registered ASN</span></span>

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

### <span data-ttu-id="27599-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27599-124">-PassThru</span></span>
<span data-ttu-id="27599-125">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="27599-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="27599-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="27599-126">-PeeringName</span></span>
<span data-ttu-id="27599-127">Der eindeutige Name von PSPeering.</span><span class="sxs-lookup"><span data-stu-id="27599-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="27599-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27599-128">-ResourceGroupName</span></span>
<span data-ttu-id="27599-129">Der Name einer vorhandenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="27599-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="27599-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27599-130">-ResourceId</span></span>
<span data-ttu-id="27599-131">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="27599-131">The resource id string name.</span></span>

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

### <span data-ttu-id="27599-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27599-132">-Confirm</span></span>
<span data-ttu-id="27599-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="27599-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27599-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="27599-134">-WhatIf</span></span>
<span data-ttu-id="27599-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="27599-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27599-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27599-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27599-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27599-137">CommonParameters</span></span>
<span data-ttu-id="27599-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27599-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27599-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27599-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27599-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="27599-140">INPUTS</span></span>

### <span data-ttu-id="27599-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="27599-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="27599-142">System.String</span><span class="sxs-lookup"><span data-stu-id="27599-142">System.String</span></span>

## <span data-ttu-id="27599-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="27599-143">OUTPUTS</span></span>

### <span data-ttu-id="27599-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="27599-144">System.Boolean</span></span>

## <span data-ttu-id="27599-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="27599-145">NOTES</span></span>

## <span data-ttu-id="27599-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="27599-146">RELATED LINKS</span></span>
