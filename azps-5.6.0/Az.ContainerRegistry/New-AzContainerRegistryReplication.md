---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/new-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
ms.openlocfilehash: a446fe34ba29789e93e8907d3155af654a93ff21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941283"
---
# <span data-ttu-id="4dec1-101">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4dec1-101">New-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="4dec1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dec1-102">SYNOPSIS</span></span>
<span data-ttu-id="4dec1-103">Erstellt eine Containerregistrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="4dec1-103">Creates a container registry replication.</span></span>

## <span data-ttu-id="4dec1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4dec1-104">SYNTAX</span></span>

### <span data-ttu-id="4dec1-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4dec1-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String> -Location <String>
 [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4dec1-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dec1-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dec1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dec1-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dec1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4dec1-108">DESCRIPTION</span></span>
<span data-ttu-id="4dec1-109">Das New-AzContainerRegistryReplication-Cmdlet erstellt eine neue Containerregistrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="4dec1-109">The New-AzContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="4dec1-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4dec1-110">EXAMPLES</span></span>

### <span data-ttu-id="4dec1-111">Beispiel 1: Erstellen einer neuen Containerregistrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="4dec1-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="4dec1-112">Erstellen Sie eine neue Containerregistrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="4dec1-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="4dec1-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4dec1-113">PARAMETERS</span></span>

### <span data-ttu-id="4dec1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dec1-114">-DefaultProfile</span></span>
<span data-ttu-id="4dec1-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4dec1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4dec1-116">-Location</span><span class="sxs-lookup"><span data-stu-id="4dec1-116">-Location</span></span>
<span data-ttu-id="4dec1-117">Containerregistrierungsort.</span><span class="sxs-lookup"><span data-stu-id="4dec1-117">Container Registry Location.</span></span>
<span data-ttu-id="4dec1-118">Standard für den Speicherort der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4dec1-118">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationLocation

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dec1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4dec1-119">-Name</span></span>
<span data-ttu-id="4dec1-120">Name der Containerregistrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="4dec1-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="4dec1-121">Standardmäßig wird der Ortsname verwendet.</span><span class="sxs-lookup"><span data-stu-id="4dec1-121">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dec1-122">-Registrierung</span><span class="sxs-lookup"><span data-stu-id="4dec1-122">-Registry</span></span>
<span data-ttu-id="4dec1-123">Containerregistrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="4dec1-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dec1-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="4dec1-124">-RegistryName</span></span>
<span data-ttu-id="4dec1-125">Containerregistrierungsname.</span><span class="sxs-lookup"><span data-stu-id="4dec1-125">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dec1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dec1-126">-ResourceGroupName</span></span>
<span data-ttu-id="4dec1-127">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="4dec1-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dec1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4dec1-128">-ResourceId</span></span>
<span data-ttu-id="4dec1-129">Die Containerregistrierungsressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4dec1-129">The container registry resource id</span></span>

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

### <span data-ttu-id="4dec1-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="4dec1-130">-Tag</span></span>
<span data-ttu-id="4dec1-131">Containerregistrierungstags.</span><span class="sxs-lookup"><span data-stu-id="4dec1-131">Container Registry Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dec1-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4dec1-132">-Confirm</span></span>
<span data-ttu-id="4dec1-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4dec1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dec1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dec1-134">-WhatIf</span></span>
<span data-ttu-id="4dec1-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4dec1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dec1-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4dec1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dec1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dec1-137">CommonParameters</span></span>
<span data-ttu-id="4dec1-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dec1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dec1-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4dec1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dec1-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4dec1-140">INPUTS</span></span>

### <span data-ttu-id="4dec1-141">System.String</span><span class="sxs-lookup"><span data-stu-id="4dec1-141">System.String</span></span>

## <span data-ttu-id="4dec1-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4dec1-142">OUTPUTS</span></span>

### <span data-ttu-id="4dec1-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4dec1-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="4dec1-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4dec1-144">NOTES</span></span>

## <span data-ttu-id="4dec1-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4dec1-145">RELATED LINKS</span></span>

[<span data-ttu-id="4dec1-146">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4dec1-146">Get-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="4dec1-147">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4dec1-147">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)