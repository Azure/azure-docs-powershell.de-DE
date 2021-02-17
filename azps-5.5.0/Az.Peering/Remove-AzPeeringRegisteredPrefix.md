---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: b3d505d7c9412b15c2933ec03bb66af6f43a6b26
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172272"
---
# <span data-ttu-id="b0b4a-101">Remove-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="b0b4a-101">Remove-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="b0b4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0b4a-102">SYNOPSIS</span></span>
<span data-ttu-id="b0b4a-103">Löschen oder entfernen Sie ein registriertes Präfix aus der übergeordneten Peeringressource.</span><span class="sxs-lookup"><span data-stu-id="b0b4a-103">Delete or remove a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="b0b4a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0b4a-104">SYNTAX</span></span>

### <span data-ttu-id="b0b4a-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b0b4a-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 [-Force] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0b4a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b0b4a-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredPrefix -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0b4a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b0b4a-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0b4a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b0b4a-108">DESCRIPTION</span></span>
<span data-ttu-id="b0b4a-109">Ermöglicht das Entfernen des registrierten Präfixes aus der übergeordneten Peeringressource.</span><span class="sxs-lookup"><span data-stu-id="b0b4a-109">Allows the removal of registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="b0b4a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b0b4a-110">EXAMPLES</span></span>

### <span data-ttu-id="b0b4a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b0b4a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredPrefix -ResourceId $resourceId
```

<span data-ttu-id="b0b4a-112">Entfernen Sie ein registriertes Präfix nach Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b0b4a-112">Remove a registerd prefix by resource id.</span></span>

## <span data-ttu-id="b0b4a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0b4a-113">PARAMETERS</span></span>

### <span data-ttu-id="b0b4a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0b4a-114">-AsJob</span></span>
<span data-ttu-id="b0b4a-115">Führen Sie die Ausführung im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="b0b4a-115">Run in the background.</span></span>

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

### <span data-ttu-id="b0b4a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0b4a-116">-DefaultProfile</span></span>
<span data-ttu-id="b0b4a-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b0b4a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0b4a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b0b4a-118">-Force</span></span>
<span data-ttu-id="b0b4a-119">Erzwingen des Vorgangs</span><span class="sxs-lookup"><span data-stu-id="b0b4a-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="b0b4a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0b4a-120">-InputObject</span></span>
<span data-ttu-id="b0b4a-121">Verwenden eines Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="b0b4a-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="b0b4a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b0b4a-122">-Name</span></span>
<span data-ttu-id="b0b4a-123">Der Name des Präfixes.</span><span class="sxs-lookup"><span data-stu-id="b0b4a-123">The name of prefix.</span></span>

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

### <span data-ttu-id="b0b4a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0b4a-124">-PassThru</span></span>
<span data-ttu-id="b0b4a-125">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="b0b4a-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="b0b4a-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="b0b4a-126">-PeeringName</span></span>
<span data-ttu-id="b0b4a-127">Der eindeutige Name von PSPeering.</span><span class="sxs-lookup"><span data-stu-id="b0b4a-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="b0b4a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0b4a-128">-ResourceGroupName</span></span>
<span data-ttu-id="b0b4a-129">Der Name einer vorhandenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b0b4a-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="b0b4a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0b4a-130">-ResourceId</span></span>
<span data-ttu-id="b0b4a-131">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b0b4a-131">The resource id string name.</span></span>

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

### <span data-ttu-id="b0b4a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0b4a-132">-Confirm</span></span>
<span data-ttu-id="b0b4a-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b0b4a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0b4a-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b0b4a-134">-WhatIf</span></span>
<span data-ttu-id="b0b4a-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b0b4a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0b4a-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b0b4a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0b4a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0b4a-137">CommonParameters</span></span>
<span data-ttu-id="b0b4a-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0b4a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0b4a-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0b4a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0b4a-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b0b4a-140">INPUTS</span></span>

### <span data-ttu-id="b0b4a-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="b0b4a-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="b0b4a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b0b4a-142">System.String</span></span>

## <span data-ttu-id="b0b4a-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b0b4a-143">OUTPUTS</span></span>

### <span data-ttu-id="b0b4a-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b0b4a-144">System.Boolean</span></span>

## <span data-ttu-id="b0b4a-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b0b4a-145">NOTES</span></span>

## <span data-ttu-id="b0b4a-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b0b4a-146">RELATED LINKS</span></span>
