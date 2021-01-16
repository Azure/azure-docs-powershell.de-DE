---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
ms.openlocfilehash: 65d47c57720e66ecad8267ae45f9e08eb3e4c4ca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369087"
---
# <span data-ttu-id="fad44-101">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fad44-101">Update-AzCustomIpPrefix</span></span>

## <span data-ttu-id="fad44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fad44-102">SYNOPSIS</span></span>
<span data-ttu-id="fad44-103">Aktualisiert ein CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fad44-103">Updates a CustomIpPrefix</span></span>

## <span data-ttu-id="fad44-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fad44-104">SYNTAX</span></span>

### <span data-ttu-id="fad44-105">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fad44-105">UpdateByNameParameterSet</span></span>
```
Update-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Commission] [-Decomission]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fad44-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fad44-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Commission] [-Decomission] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fad44-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fad44-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzCustomIpPrefix -ResourceId <String> [-Commission] [-Decomission] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fad44-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fad44-108">DESCRIPTION</span></span>
<span data-ttu-id="fad44-109">Mit **dem Cmdlet "Update-AzCustomIpPrefix"** kann der Benutzer sein CustomIpPrefix entweder in die Provision oder außer Betrieb genommen oder die Tags der Ressource bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="fad44-109">The **Update-AzCustomIpPrefix** cmdlet allows the user to either commission or decommission their CustomIpPrefix, or edit the tags of the resource.</span></span>

## <span data-ttu-id="fad44-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fad44-110">EXAMPLES</span></span>

### <span data-ttu-id="fad44-111">Beispiel 1: Provision des CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fad44-111">Example 1 : Commission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Commission
```

<span data-ttu-id="fad44-112">Der oben aufgeführte Befehl startet den Provisionierungsprozess von CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="fad44-112">The above command will start the commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="fad44-113">Beispiel 2: Außerbetriebnahme von CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fad44-113">Example 2 : Decommission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Decommission
```

<span data-ttu-id="fad44-114">Mit dem oben angegebenen Befehl wird der De provisioning process von CustomIpPrefix gestartet.</span><span class="sxs-lookup"><span data-stu-id="fad44-114">The above command will start the de-commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="fad44-115">Beispiel 3: Aktualisieren von Tags für CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fad44-115">Example 3 : Update tags for the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Tag $tags
```

<span data-ttu-id="fad44-116">Mit dem oben angegebenen Befehl werden die Tags für CustomIpPrefix aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fad44-116">The above command will update the tags for the CustomIpPrefix.</span></span>

## <span data-ttu-id="fad44-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fad44-117">PARAMETERS</span></span>

### <span data-ttu-id="fad44-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fad44-118">-AsJob</span></span>
<span data-ttu-id="fad44-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fad44-119">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fad44-120">-Commission</span><span class="sxs-lookup"><span data-stu-id="fad44-120">-Commission</span></span>
<span data-ttu-id="fad44-121">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fad44-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fad44-122">-Decomission</span><span class="sxs-lookup"><span data-stu-id="fad44-122">-Decomission</span></span>
<span data-ttu-id="fad44-123">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fad44-123">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fad44-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fad44-124">-DefaultProfile</span></span>
<span data-ttu-id="fad44-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fad44-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fad44-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fad44-126">-InputObject</span></span>
<span data-ttu-id="fad44-127">Das festgelegte CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="fad44-127">The CustomIpPrefix to set.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fad44-128">-Name</span><span class="sxs-lookup"><span data-stu-id="fad44-128">-Name</span></span>
<span data-ttu-id="fad44-129">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="fad44-129">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fad44-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fad44-130">-ResourceGroupName</span></span>
<span data-ttu-id="fad44-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fad44-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fad44-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fad44-132">-ResourceId</span></span>
<span data-ttu-id="fad44-133">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="fad44-133">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fad44-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="fad44-134">-Tag</span></span>
<span data-ttu-id="fad44-135">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="fad44-135">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Hashtable
Parameter Sets: SetByInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fad44-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fad44-136">-Confirm</span></span>
<span data-ttu-id="fad44-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fad44-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fad44-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fad44-138">-WhatIf</span></span>
<span data-ttu-id="fad44-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fad44-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fad44-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fad44-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fad44-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fad44-141">CommonParameters</span></span>
<span data-ttu-id="fad44-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fad44-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fad44-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fad44-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fad44-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fad44-144">INPUTS</span></span>

### <span data-ttu-id="fad44-145">System.String</span><span class="sxs-lookup"><span data-stu-id="fad44-145">System.String</span></span>

### <span data-ttu-id="fad44-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fad44-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

### <span data-ttu-id="fad44-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="fad44-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fad44-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fad44-148">OUTPUTS</span></span>

### <span data-ttu-id="fad44-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fad44-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="fad44-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fad44-150">NOTES</span></span>

## <span data-ttu-id="fad44-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fad44-151">RELATED LINKS</span></span>

[<span data-ttu-id="fad44-152">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fad44-152">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="fad44-153">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fad44-153">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="fad44-154">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fad44-154">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)