---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 57b482368834d91e36a3f557c9657c82cea24f4e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470792"
---
# <span data-ttu-id="0ea0f-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="0ea0f-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="0ea0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ea0f-102">SYNOPSIS</span></span>
<span data-ttu-id="0ea0f-103">Ruft eine Replikation einer Containerregistrierung ab.</span><span class="sxs-lookup"><span data-stu-id="0ea0f-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="0ea0f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0ea0f-104">SYNTAX</span></span>

### <span data-ttu-id="0ea0f-105">ListReplicationByNameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0ea0f-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ea0f-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ea0f-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ea0f-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ea0f-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ea0f-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ea0f-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ea0f-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ea0f-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ea0f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ea0f-110">DESCRIPTION</span></span>
<span data-ttu-id="0ea0f-111">Das Get-AzContainerRegistryReplication-Cmdlet ruft eine angegebene Replikation einer Containerregistrierung oder aller Replikationen einer Containerregistrierung ab.</span><span class="sxs-lookup"><span data-stu-id="0ea0f-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="0ea0f-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0ea0f-112">EXAMPLES</span></span>

### <span data-ttu-id="0ea0f-113">Beispiel 1: Ruft eine angegebene Replikation einer Containerregistrierung ab.</span><span class="sxs-lookup"><span data-stu-id="0ea0f-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="0ea0f-114">Ruft eine angegebene Replikation einer Containerregistrierung ab.</span><span class="sxs-lookup"><span data-stu-id="0ea0f-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="0ea0f-115">Beispiel 2: Ruft alle Replikationen einer Containerregistrierung ab.</span><span class="sxs-lookup"><span data-stu-id="0ea0f-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="0ea0f-116">Ruft alle Replikationen einer Containerregistrierung ab.</span><span class="sxs-lookup"><span data-stu-id="0ea0f-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="0ea0f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ea0f-117">PARAMETERS</span></span>

### <span data-ttu-id="0ea0f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ea0f-118">-DefaultProfile</span></span>
<span data-ttu-id="0ea0f-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0ea0f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ea0f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0ea0f-120">-Name</span></span>
<span data-ttu-id="0ea0f-121">Container-Registrierungsreplikationsname.</span><span class="sxs-lookup"><span data-stu-id="0ea0f-121">Container Registry Replication Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShowReplicationByNameResourceGroupParameterSet, ShowReplicationByRegistryObjectParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ea0f-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="0ea0f-122">-Registry</span></span>
<span data-ttu-id="0ea0f-123">Containerregistrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="0ea0f-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: ShowReplicationByRegistryObjectParameterSet, ListReplicationByRegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ea0f-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="0ea0f-124">-RegistryName</span></span>
<span data-ttu-id="0ea0f-125">Containerregistrierungsname.</span><span class="sxs-lookup"><span data-stu-id="0ea0f-125">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ea0f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ea0f-126">-ResourceGroupName</span></span>
<span data-ttu-id="0ea0f-127">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="0ea0f-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ea0f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ea0f-128">-ResourceId</span></span>
<span data-ttu-id="0ea0f-129">Die Ressourcen-ID der Containerregistrierungsreplikation</span><span class="sxs-lookup"><span data-stu-id="0ea0f-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="0ea0f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ea0f-130">CommonParameters</span></span>
<span data-ttu-id="0ea0f-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ea0f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ea0f-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ea0f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ea0f-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0ea0f-133">INPUTS</span></span>

### <span data-ttu-id="0ea0f-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0ea0f-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="0ea0f-135">System.String</span><span class="sxs-lookup"><span data-stu-id="0ea0f-135">System.String</span></span>

## <span data-ttu-id="0ea0f-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0ea0f-136">OUTPUTS</span></span>

### <span data-ttu-id="0ea0f-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="0ea0f-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="0ea0f-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0ea0f-138">NOTES</span></span>

## <span data-ttu-id="0ea0f-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0ea0f-139">RELATED LINKS</span></span>

[<span data-ttu-id="0ea0f-140">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="0ea0f-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="0ea0f-141">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="0ea0f-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)