---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
ms.openlocfilehash: 41bdf9bbc33239590f9d3a6db4ffaa88ddf752a1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296350"
---
# <span data-ttu-id="3bc00-101">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="3bc00-101">Remove-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="3bc00-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3bc00-102">SYNOPSIS</span></span>
<span data-ttu-id="3bc00-103">Entfernt eine Container Registrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="3bc00-103">Removes a container registry replication.</span></span>

## <span data-ttu-id="3bc00-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3bc00-104">SYNTAX</span></span>

### <span data-ttu-id="3bc00-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3bc00-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bc00-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bc00-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -Replication <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bc00-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bc00-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bc00-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3bc00-108">DESCRIPTION</span></span>
<span data-ttu-id="3bc00-109">Das Remove-AzContainerRegistryReplication-Cmdlet entfernt eine Container Registrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="3bc00-109">The Remove-AzContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="3bc00-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3bc00-110">EXAMPLES</span></span>

### <span data-ttu-id="3bc00-111">Beispiel 1: entfernt eine Container Registrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="3bc00-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="3bc00-112">Entfernt eine Container Registrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="3bc00-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="3bc00-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3bc00-113">PARAMETERS</span></span>

### <span data-ttu-id="3bc00-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bc00-114">-DefaultProfile</span></span>
<span data-ttu-id="3bc00-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3bc00-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bc00-116">-Name</span><span class="sxs-lookup"><span data-stu-id="3bc00-116">-Name</span></span>
<span data-ttu-id="3bc00-117">Name der Container Registrierungsreplikation</span><span class="sxs-lookup"><span data-stu-id="3bc00-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="3bc00-118">Standardmäßig auf den Namen des Standorts.</span><span class="sxs-lookup"><span data-stu-id="3bc00-118">Default to the location name.</span></span>

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

### <span data-ttu-id="3bc00-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3bc00-119">-PassThru</span></span>
<span data-ttu-id="3bc00-120">Gibt an, dass dieses Cmdlet "true" zurückgibt, wenn die Entfernung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="3bc00-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="3bc00-121">-Registryname</span><span class="sxs-lookup"><span data-stu-id="3bc00-121">-RegistryName</span></span>
<span data-ttu-id="3bc00-122">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="3bc00-122">Container Registry Name.</span></span>

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

### <span data-ttu-id="3bc00-123">-Replikation</span><span class="sxs-lookup"><span data-stu-id="3bc00-123">-Replication</span></span>
<span data-ttu-id="3bc00-124">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="3bc00-124">Container Registry Object.</span></span>

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

### <span data-ttu-id="3bc00-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bc00-125">-ResourceGroupName</span></span>
<span data-ttu-id="3bc00-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3bc00-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="3bc00-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3bc00-127">-ResourceId</span></span>
<span data-ttu-id="3bc00-128">Die Ressourcen-ID der Container Registrierungsreplikation</span><span class="sxs-lookup"><span data-stu-id="3bc00-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="3bc00-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3bc00-129">-Confirm</span></span>
<span data-ttu-id="3bc00-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3bc00-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bc00-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bc00-131">-WhatIf</span></span>
<span data-ttu-id="3bc00-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3bc00-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bc00-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3bc00-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bc00-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc00-134">CommonParameters</span></span>
<span data-ttu-id="3bc00-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bc00-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc00-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3bc00-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc00-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3bc00-137">INPUTS</span></span>

### <span data-ttu-id="3bc00-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="3bc00-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

### <span data-ttu-id="3bc00-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3bc00-139">System.String</span></span>

## <span data-ttu-id="3bc00-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3bc00-140">OUTPUTS</span></span>

### <span data-ttu-id="3bc00-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3bc00-141">System.Boolean</span></span>

## <span data-ttu-id="3bc00-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="3bc00-142">NOTES</span></span>

## <span data-ttu-id="3bc00-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3bc00-143">RELATED LINKS</span></span>

[<span data-ttu-id="3bc00-144">Neu – AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="3bc00-144">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="3bc00-145">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="3bc00-145">Get-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)

