---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: d2cac696382f807a1fc4afe94f9d2d61ea65cece
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662183"
---
# <span data-ttu-id="a716b-101">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="a716b-101">Get-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="a716b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a716b-102">SYNOPSIS</span></span>
<span data-ttu-id="a716b-103">Ruft eine Replikation einer Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="a716b-103">Gets a replication of a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a716b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a716b-104">SYNTAX</span></span>

### <span data-ttu-id="a716b-105">ListReplicationByNameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a716b-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a716b-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="a716b-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a716b-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a716b-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a716b-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a716b-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a716b-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a716b-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a716b-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a716b-110">DESCRIPTION</span></span>
<span data-ttu-id="a716b-111">Das Get-AzureRmContainerRegistryReplication-Cmdlet ruft eine angegebene Replikation einer Container Registrierung oder aller Replikate einer Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="a716b-111">The Get-AzureRmContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="a716b-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a716b-112">EXAMPLES</span></span>

### <span data-ttu-id="a716b-113">Beispiel 1: Ruft eine angegebene Replikation einer Container Registrierung ab</span><span class="sxs-lookup"><span data-stu-id="a716b-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="a716b-114">Ruft eine angegebene Replikation einer Container Registrierung ab</span><span class="sxs-lookup"><span data-stu-id="a716b-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="a716b-115">Beispiel 2: Ruft alle Replikate einer Container Registrierung ab</span><span class="sxs-lookup"><span data-stu-id="a716b-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="a716b-116">Ruft alle Replikate einer Container Registrierung ab</span><span class="sxs-lookup"><span data-stu-id="a716b-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="a716b-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="a716b-117">PARAMETERS</span></span>

### <span data-ttu-id="a716b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a716b-118">-DefaultProfile</span></span>
<span data-ttu-id="a716b-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a716b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a716b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a716b-120">-Name</span></span>
<span data-ttu-id="a716b-121">Name der Container Registrierungsreplikation</span><span class="sxs-lookup"><span data-stu-id="a716b-121">Container Registry Replication Name.</span></span>

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

### <span data-ttu-id="a716b-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="a716b-122">-Registry</span></span>
<span data-ttu-id="a716b-123">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="a716b-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="a716b-124">-Registryname</span><span class="sxs-lookup"><span data-stu-id="a716b-124">-RegistryName</span></span>
<span data-ttu-id="a716b-125">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="a716b-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="a716b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a716b-126">-ResourceGroupName</span></span>
<span data-ttu-id="a716b-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a716b-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="a716b-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a716b-128">-ResourceId</span></span>
<span data-ttu-id="a716b-129">Die Ressourcen-ID der Container Registrierungsreplikation</span><span class="sxs-lookup"><span data-stu-id="a716b-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="a716b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a716b-130">CommonParameters</span></span>
<span data-ttu-id="a716b-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a716b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a716b-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a716b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a716b-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a716b-133">INPUTS</span></span>

### <span data-ttu-id="a716b-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a716b-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="a716b-135">Parameter: Registrierung (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a716b-135">Parameters: Registry (ByValue)</span></span>

### <span data-ttu-id="a716b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a716b-136">System.String</span></span>

## <span data-ttu-id="a716b-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a716b-137">OUTPUTS</span></span>

### <span data-ttu-id="a716b-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="a716b-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="a716b-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="a716b-139">NOTES</span></span>

## <span data-ttu-id="a716b-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a716b-140">RELATED LINKS</span></span>

[<span data-ttu-id="a716b-141">Neu – AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="a716b-141">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="a716b-142">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="a716b-142">Remove-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)
