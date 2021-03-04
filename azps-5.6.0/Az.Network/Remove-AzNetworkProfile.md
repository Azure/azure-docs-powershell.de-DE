---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
ms.openlocfilehash: 02a8fef51ca0689fb92d3990bf5bcc182f902549
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941584"
---
# <span data-ttu-id="a2294-101">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a2294-101">Remove-AzNetworkProfile</span></span>

## <span data-ttu-id="a2294-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2294-102">SYNOPSIS</span></span>
<span data-ttu-id="a2294-103">Entfernt ein Netzwerkprofil.</span><span class="sxs-lookup"><span data-stu-id="a2294-103">Removes a network profile.</span></span>

## <span data-ttu-id="a2294-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2294-104">SYNTAX</span></span>

### <span data-ttu-id="a2294-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a2294-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2294-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2294-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2294-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2294-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2294-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a2294-108">DESCRIPTION</span></span>
<span data-ttu-id="a2294-109">Das **Cmdlet Remove-AzNetworkProfile** entfernt ein Netzwerkprofil, wenn keine Containernetzwerkschnittstellen (im Gegensatz zu einer Containernetzwerkschnittstellenkonfiguration) erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="a2294-109">The **Remove-AzNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration**) have been created.</span></span>

## <span data-ttu-id="a2294-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a2294-110">EXAMPLES</span></span>

### <span data-ttu-id="a2294-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a2294-111">Example 1</span></span>
```powershell
Remove-AzNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="a2294-112">Dadurch wird das Netzwerkprofil mit dem Namen np1 aus der Ressourcengruppe rg1 entfernt.</span><span class="sxs-lookup"><span data-stu-id="a2294-112">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="a2294-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a2294-113">PARAMETERS</span></span>

### <span data-ttu-id="a2294-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2294-114">-AsJob</span></span>
<span data-ttu-id="a2294-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a2294-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2294-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2294-116">-DefaultProfile</span></span>
<span data-ttu-id="a2294-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2294-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2294-118">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="a2294-118">-Force</span></span>
<span data-ttu-id="a2294-119">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="a2294-119">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="a2294-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2294-120">-InputObject</span></span>
<span data-ttu-id="a2294-121">Netzwerkprofilobjekt.</span><span class="sxs-lookup"><span data-stu-id="a2294-121">Network profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2294-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a2294-122">-Name</span></span>
<span data-ttu-id="a2294-123">Der Name des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="a2294-123">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2294-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2294-124">-PassThru</span></span>
<span data-ttu-id="a2294-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="a2294-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="a2294-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2294-126">-ResourceGroupName</span></span>
<span data-ttu-id="a2294-127">Der Ressourcengruppenname des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="a2294-127">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2294-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2294-128">-ResourceId</span></span>
<span data-ttu-id="a2294-129">Die Azure Resource Manager-Ressourcen-ID des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="a2294-129">The Azure resource manager resource ID of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2294-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a2294-130">-Confirm</span></span>
<span data-ttu-id="a2294-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a2294-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2294-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2294-132">-WhatIf</span></span>
<span data-ttu-id="a2294-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2294-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2294-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2294-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2294-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2294-135">CommonParameters</span></span>
<span data-ttu-id="a2294-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2294-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2294-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2294-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2294-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a2294-138">INPUTS</span></span>

### <span data-ttu-id="a2294-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a2294-139">System.String</span></span>

### <span data-ttu-id="a2294-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a2294-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="a2294-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a2294-141">OUTPUTS</span></span>

### <span data-ttu-id="a2294-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a2294-142">System.Boolean</span></span>

## <span data-ttu-id="a2294-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a2294-143">NOTES</span></span>

## <span data-ttu-id="a2294-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a2294-144">RELATED LINKS</span></span>

[<span data-ttu-id="a2294-145">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a2294-145">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="a2294-146">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a2294-146">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="a2294-147">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a2294-147">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
