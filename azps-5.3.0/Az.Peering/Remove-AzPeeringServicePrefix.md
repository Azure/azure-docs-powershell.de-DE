---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
ms.openlocfilehash: 0fbf44e9a68a5cfaaea4138ec17caa2960a41e67
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384640"
---
# <span data-ttu-id="ae844-101">Remove-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="ae844-101">Remove-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="ae844-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae844-102">SYNOPSIS</span></span>
<span data-ttu-id="ae844-103">Entfernt ein neues Peeringdienstpräfix</span><span class="sxs-lookup"><span data-stu-id="ae844-103">Removes a new peering service prefix</span></span>

## <span data-ttu-id="ae844-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae844-104">SYNTAX</span></span>

### <span data-ttu-id="ae844-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ae844-105">ByName (Default)</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceGroupName] <String> [-Name] <String> [-PrefixName] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae844-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ae844-106">InputObject</span></span>
```
Remove-AzPeeringServicePrefix [-InputObject] <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae844-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ae844-107">ByResourceId</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae844-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae844-108">DESCRIPTION</span></span>
<span data-ttu-id="ae844-109">Entfernt ein Peeringdienstpräfix aus einem Peeringdienst.</span><span class="sxs-lookup"><span data-stu-id="ae844-109">Removes a peering service prefix from a peering service.</span></span>

## <span data-ttu-id="ae844-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ae844-110">EXAMPLES</span></span>

### <span data-ttu-id="ae844-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ae844-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | Remove-AzPeeringServicePrefix -Name $prefixName
```

<span data-ttu-id="ae844-112">Entfernen eines Präfixes von einem Peeringdienstobjekt</span><span class="sxs-lookup"><span data-stu-id="ae844-112">Remove a prefix from a peering service object</span></span>

### <span data-ttu-id="ae844-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ae844-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceId $peeringServiceResourceId -Name $prefixName -PassThru

True
```

<span data-ttu-id="ae844-114">Entfernen Sie ein Präfix von einer Peeringdienstressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ae844-114">Remove a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="ae844-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ae844-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -PassThru

True
```

<span data-ttu-id="ae844-116">Entfernen eines Präfixes aus dem Namen und Namen einer Peeringdienstressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ae844-116">Remove a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="ae844-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae844-117">PARAMETERS</span></span>

### <span data-ttu-id="ae844-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae844-118">-AsJob</span></span>
<span data-ttu-id="ae844-119">Führen Sie die Ausführung im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="ae844-119">Run in the background.</span></span>

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

### <span data-ttu-id="ae844-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae844-120">-DefaultProfile</span></span>
<span data-ttu-id="ae844-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae844-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae844-122">-Force</span><span class="sxs-lookup"><span data-stu-id="ae844-122">-Force</span></span>
<span data-ttu-id="ae844-123">Erzwingen des Vorgangs</span><span class="sxs-lookup"><span data-stu-id="ae844-123">Force the operation to complete</span></span>

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

### <span data-ttu-id="ae844-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae844-124">-InputObject</span></span>
<span data-ttu-id="ae844-125">Verwenden eines Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="ae844-125">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae844-126">-Name</span><span class="sxs-lookup"><span data-stu-id="ae844-126">-Name</span></span>
<span data-ttu-id="ae844-127">Der eindeutige Name von PSPeering.</span><span class="sxs-lookup"><span data-stu-id="ae844-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="ae844-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae844-128">-PassThru</span></span>
<span data-ttu-id="ae844-129">Gibt "true" für "success" oder "false" für "failed" zurück.</span><span class="sxs-lookup"><span data-stu-id="ae844-129">Returns true for success or false for failed.</span></span>

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

### <span data-ttu-id="ae844-130">-PrefixName</span><span class="sxs-lookup"><span data-stu-id="ae844-130">-PrefixName</span></span>
<span data-ttu-id="ae844-131">Der Name des Präfixes.</span><span class="sxs-lookup"><span data-stu-id="ae844-131">The name of prefix.</span></span>

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

### <span data-ttu-id="ae844-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae844-132">-ResourceGroupName</span></span>
<span data-ttu-id="ae844-133">Der Name einer vorhandenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ae844-133">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="ae844-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae844-134">-ResourceId</span></span>
<span data-ttu-id="ae844-135">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ae844-135">The resource id string name.</span></span>

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

### <span data-ttu-id="ae844-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae844-136">-Confirm</span></span>
<span data-ttu-id="ae844-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ae844-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae844-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ae844-138">-WhatIf</span></span>
<span data-ttu-id="ae844-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ae844-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae844-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae844-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae844-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae844-141">CommonParameters</span></span>
<span data-ttu-id="ae844-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae844-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae844-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae844-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae844-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ae844-144">INPUTS</span></span>

### <span data-ttu-id="ae844-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="ae844-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="ae844-146">System.String</span><span class="sxs-lookup"><span data-stu-id="ae844-146">System.String</span></span>

## <span data-ttu-id="ae844-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ae844-147">OUTPUTS</span></span>

### <span data-ttu-id="ae844-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ae844-148">System.Boolean</span></span>

## <span data-ttu-id="ae844-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ae844-149">NOTES</span></span>

## <span data-ttu-id="ae844-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ae844-150">RELATED LINKS</span></span>
