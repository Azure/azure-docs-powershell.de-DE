---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 57b482368834d91e36a3f557c9657c82cea24f4e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165858"
---
# <span data-ttu-id="905c3-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="905c3-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="905c3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="905c3-102">SYNOPSIS</span></span>
<span data-ttu-id="905c3-103">Ruft eine Replikation einer Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="905c3-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="905c3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="905c3-104">SYNTAX</span></span>

### <span data-ttu-id="905c3-105">ListReplicationByNameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="905c3-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="905c3-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="905c3-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="905c3-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="905c3-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="905c3-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="905c3-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="905c3-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="905c3-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="905c3-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="905c3-110">DESCRIPTION</span></span>
<span data-ttu-id="905c3-111">Das Get-AzContainerRegistryReplication-Cmdlet ruft eine angegebene Replikation einer Container Registrierung oder aller Replikate einer Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="905c3-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="905c3-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="905c3-112">EXAMPLES</span></span>

### <span data-ttu-id="905c3-113">Beispiel 1: Ruft eine angegebene Replikation einer Container Registrierung ab</span><span class="sxs-lookup"><span data-stu-id="905c3-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="905c3-114">Ruft eine angegebene Replikation einer Container Registrierung ab</span><span class="sxs-lookup"><span data-stu-id="905c3-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="905c3-115">Beispiel 2: Ruft alle Replikate einer Container Registrierung ab</span><span class="sxs-lookup"><span data-stu-id="905c3-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="905c3-116">Ruft alle Replikate einer Container Registrierung ab</span><span class="sxs-lookup"><span data-stu-id="905c3-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="905c3-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="905c3-117">PARAMETERS</span></span>

### <span data-ttu-id="905c3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="905c3-118">-DefaultProfile</span></span>
<span data-ttu-id="905c3-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="905c3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="905c3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="905c3-120">-Name</span></span>
<span data-ttu-id="905c3-121">Name der Container Registrierungsreplikation</span><span class="sxs-lookup"><span data-stu-id="905c3-121">Container Registry Replication Name.</span></span>

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

### <span data-ttu-id="905c3-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="905c3-122">-Registry</span></span>
<span data-ttu-id="905c3-123">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="905c3-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="905c3-124">-Registryname</span><span class="sxs-lookup"><span data-stu-id="905c3-124">-RegistryName</span></span>
<span data-ttu-id="905c3-125">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="905c3-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="905c3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="905c3-126">-ResourceGroupName</span></span>
<span data-ttu-id="905c3-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="905c3-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="905c3-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="905c3-128">-ResourceId</span></span>
<span data-ttu-id="905c3-129">Die Ressourcen-ID der Container Registrierungsreplikation</span><span class="sxs-lookup"><span data-stu-id="905c3-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="905c3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="905c3-130">CommonParameters</span></span>
<span data-ttu-id="905c3-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="905c3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="905c3-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="905c3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="905c3-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="905c3-133">INPUTS</span></span>

### <span data-ttu-id="905c3-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="905c3-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="905c3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="905c3-135">System.String</span></span>

## <span data-ttu-id="905c3-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="905c3-136">OUTPUTS</span></span>

### <span data-ttu-id="905c3-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="905c3-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="905c3-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="905c3-138">NOTES</span></span>

## <span data-ttu-id="905c3-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="905c3-139">RELATED LINKS</span></span>

[<span data-ttu-id="905c3-140">Neu – AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="905c3-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="905c3-141">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="905c3-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)