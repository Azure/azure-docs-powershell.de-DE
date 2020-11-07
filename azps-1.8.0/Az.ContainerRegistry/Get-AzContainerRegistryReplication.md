---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 21e821a4575fb918599ad2315c569a7f270e0a84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661389"
---
# <span data-ttu-id="8259c-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="8259c-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="8259c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8259c-102">SYNOPSIS</span></span>
<span data-ttu-id="8259c-103">Ruft eine Replikation einer Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="8259c-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="8259c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8259c-104">SYNTAX</span></span>

### <span data-ttu-id="8259c-105">ListReplicationByNameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8259c-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8259c-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="8259c-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8259c-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8259c-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8259c-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8259c-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8259c-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8259c-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8259c-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8259c-110">DESCRIPTION</span></span>
<span data-ttu-id="8259c-111">Das Get-AzContainerRegistryReplication-Cmdlet ruft eine angegebene Replikation einer Container Registrierung oder aller Replikate einer Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="8259c-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="8259c-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8259c-112">EXAMPLES</span></span>

### <span data-ttu-id="8259c-113">Beispiel 1: Ruft eine angegebene Replikation einer Container Registrierung ab</span><span class="sxs-lookup"><span data-stu-id="8259c-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="8259c-114">Ruft eine angegebene Replikation einer Container Registrierung ab</span><span class="sxs-lookup"><span data-stu-id="8259c-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="8259c-115">Beispiel 2: Ruft alle Replikate einer Container Registrierung ab</span><span class="sxs-lookup"><span data-stu-id="8259c-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="8259c-116">Ruft alle Replikate einer Container Registrierung ab</span><span class="sxs-lookup"><span data-stu-id="8259c-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="8259c-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="8259c-117">PARAMETERS</span></span>

### <span data-ttu-id="8259c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8259c-118">-DefaultProfile</span></span>
<span data-ttu-id="8259c-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8259c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8259c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8259c-120">-Name</span></span>
<span data-ttu-id="8259c-121">Name der Container Registrierungsreplikation</span><span class="sxs-lookup"><span data-stu-id="8259c-121">Container Registry Replication Name.</span></span>

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

### <span data-ttu-id="8259c-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="8259c-122">-Registry</span></span>
<span data-ttu-id="8259c-123">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="8259c-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="8259c-124">-Registryname</span><span class="sxs-lookup"><span data-stu-id="8259c-124">-RegistryName</span></span>
<span data-ttu-id="8259c-125">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="8259c-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="8259c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8259c-126">-ResourceGroupName</span></span>
<span data-ttu-id="8259c-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8259c-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="8259c-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8259c-128">-ResourceId</span></span>
<span data-ttu-id="8259c-129">Die Ressourcen-ID der Container Registrierungsreplikation</span><span class="sxs-lookup"><span data-stu-id="8259c-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="8259c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8259c-130">CommonParameters</span></span>
<span data-ttu-id="8259c-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8259c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8259c-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8259c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8259c-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8259c-133">INPUTS</span></span>

### <span data-ttu-id="8259c-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8259c-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="8259c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="8259c-135">System.String</span></span>

## <span data-ttu-id="8259c-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8259c-136">OUTPUTS</span></span>

### <span data-ttu-id="8259c-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="8259c-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="8259c-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="8259c-138">NOTES</span></span>

## <span data-ttu-id="8259c-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8259c-139">RELATED LINKS</span></span>

[<span data-ttu-id="8259c-140">Neu – AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="8259c-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="8259c-141">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="8259c-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)