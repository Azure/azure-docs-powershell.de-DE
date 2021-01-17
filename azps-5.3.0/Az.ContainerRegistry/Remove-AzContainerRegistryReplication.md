---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
ms.openlocfilehash: 41bdf9bbc33239590f9d3a6db4ffaa88ddf752a1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470781"
---
# <span data-ttu-id="3a549-101">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="3a549-101">Remove-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="3a549-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a549-102">SYNOPSIS</span></span>
<span data-ttu-id="3a549-103">Entfernt eine Containerregistrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="3a549-103">Removes a container registry replication.</span></span>

## <span data-ttu-id="3a549-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a549-104">SYNTAX</span></span>

### <span data-ttu-id="3a549-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3a549-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a549-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a549-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -Replication <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a549-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a549-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a549-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a549-108">DESCRIPTION</span></span>
<span data-ttu-id="3a549-109">Das Remove-AzContainerRegistryReplication cmdlet entfernt eine Containerregistrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="3a549-109">The Remove-AzContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="3a549-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3a549-110">EXAMPLES</span></span>

### <span data-ttu-id="3a549-111">Beispiel 1: Entfernt eine Containerregistrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="3a549-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="3a549-112">Entfernt eine Containerregistrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="3a549-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="3a549-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a549-113">PARAMETERS</span></span>

### <span data-ttu-id="3a549-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a549-114">-DefaultProfile</span></span>
<span data-ttu-id="3a549-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a549-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a549-116">-Name</span><span class="sxs-lookup"><span data-stu-id="3a549-116">-Name</span></span>
<span data-ttu-id="3a549-117">Container-Registrierungsreplikationsname.</span><span class="sxs-lookup"><span data-stu-id="3a549-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="3a549-118">Standardmäßig wird der Standortname verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a549-118">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a549-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a549-119">-PassThru</span></span>
<span data-ttu-id="3a549-120">Gibt an, dass dieses Cmdlet "true" zurückgibt, wenn das Entfernen erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="3a549-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="3a549-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="3a549-121">-RegistryName</span></span>
<span data-ttu-id="3a549-122">Containerregistrierungsname.</span><span class="sxs-lookup"><span data-stu-id="3a549-122">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a549-123">-Replikation</span><span class="sxs-lookup"><span data-stu-id="3a549-123">-Replication</span></span>
<span data-ttu-id="3a549-124">Containerregistrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="3a549-124">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases: Replicatoin

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a549-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a549-125">-ResourceGroupName</span></span>
<span data-ttu-id="3a549-126">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="3a549-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a549-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a549-127">-ResourceId</span></span>
<span data-ttu-id="3a549-128">Die Ressourcen-ID der Containerregistrierungsreplikation</span><span class="sxs-lookup"><span data-stu-id="3a549-128">The container registry replication resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a549-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a549-129">-Confirm</span></span>
<span data-ttu-id="3a549-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3a549-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a549-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3a549-131">-WhatIf</span></span>
<span data-ttu-id="3a549-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a549-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a549-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a549-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a549-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a549-134">CommonParameters</span></span>
<span data-ttu-id="3a549-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a549-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a549-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a549-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a549-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3a549-137">INPUTS</span></span>

### <span data-ttu-id="3a549-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="3a549-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

### <span data-ttu-id="3a549-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3a549-139">System.String</span></span>

## <span data-ttu-id="3a549-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3a549-140">OUTPUTS</span></span>

### <span data-ttu-id="3a549-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3a549-141">System.Boolean</span></span>

## <span data-ttu-id="3a549-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3a549-142">NOTES</span></span>

## <span data-ttu-id="3a549-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3a549-143">RELATED LINKS</span></span>

[<span data-ttu-id="3a549-144">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="3a549-144">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="3a549-145">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="3a549-145">Get-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)

