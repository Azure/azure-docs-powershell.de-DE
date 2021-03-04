---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 3054c6ed8083d1108c853ab188903cc3b2ebd380
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945239"
---
# <span data-ttu-id="2b498-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="2b498-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="2b498-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b498-102">SYNOPSIS</span></span>
<span data-ttu-id="2b498-103">Ruft eine Replikation einer Containerregistrierung ab.</span><span class="sxs-lookup"><span data-stu-id="2b498-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="2b498-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b498-104">SYNTAX</span></span>

### <span data-ttu-id="2b498-105">ListReplicationByNameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2b498-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b498-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b498-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b498-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b498-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b498-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b498-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b498-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b498-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b498-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b498-110">DESCRIPTION</span></span>
<span data-ttu-id="2b498-111">Das Get-AzContainerRegistryReplication-Cmdlet ruft eine angegebene Replikation einer Containerregistrierung oder aller Replikationen einer Containerregistrierung ab.</span><span class="sxs-lookup"><span data-stu-id="2b498-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="2b498-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2b498-112">EXAMPLES</span></span>

### <span data-ttu-id="2b498-113">Beispiel 1: Ruft eine angegebene Replikation einer Containerregistrierung ab.</span><span class="sxs-lookup"><span data-stu-id="2b498-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="2b498-114">Ruft eine angegebene Replikation einer Containerregistrierung ab.</span><span class="sxs-lookup"><span data-stu-id="2b498-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="2b498-115">Beispiel 2: Ruft alle Replikationen einer Containerregistrierung ab.</span><span class="sxs-lookup"><span data-stu-id="2b498-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="2b498-116">Ruft alle Replikationen einer Containerregistrierung ab.</span><span class="sxs-lookup"><span data-stu-id="2b498-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="2b498-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2b498-117">PARAMETERS</span></span>

### <span data-ttu-id="2b498-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b498-118">-DefaultProfile</span></span>
<span data-ttu-id="2b498-119">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2b498-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b498-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2b498-120">-Name</span></span>
<span data-ttu-id="2b498-121">Name der Containerregistrierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="2b498-121">Container Registry Replication Name.</span></span>

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

### <span data-ttu-id="2b498-122">-Registrierung</span><span class="sxs-lookup"><span data-stu-id="2b498-122">-Registry</span></span>
<span data-ttu-id="2b498-123">Containerregistrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="2b498-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="2b498-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="2b498-124">-RegistryName</span></span>
<span data-ttu-id="2b498-125">Containerregistrierungsname.</span><span class="sxs-lookup"><span data-stu-id="2b498-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="2b498-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b498-126">-ResourceGroupName</span></span>
<span data-ttu-id="2b498-127">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="2b498-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="2b498-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b498-128">-ResourceId</span></span>
<span data-ttu-id="2b498-129">Ressourcen-ID der Containerregistrierungsreplikation</span><span class="sxs-lookup"><span data-stu-id="2b498-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="2b498-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b498-130">CommonParameters</span></span>
<span data-ttu-id="2b498-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b498-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b498-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b498-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b498-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2b498-133">INPUTS</span></span>

### <span data-ttu-id="2b498-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2b498-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="2b498-135">System.String</span><span class="sxs-lookup"><span data-stu-id="2b498-135">System.String</span></span>

## <span data-ttu-id="2b498-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2b498-136">OUTPUTS</span></span>

### <span data-ttu-id="2b498-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="2b498-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="2b498-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2b498-138">NOTES</span></span>

## <span data-ttu-id="2b498-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2b498-139">RELATED LINKS</span></span>

[<span data-ttu-id="2b498-140">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="2b498-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="2b498-141">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="2b498-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)