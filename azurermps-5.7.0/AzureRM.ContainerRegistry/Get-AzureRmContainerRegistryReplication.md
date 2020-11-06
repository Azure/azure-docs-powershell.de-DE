---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: db03414e9cebe4c1593013a928b8a66d9b70bd91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481302"
---
# <span data-ttu-id="aa295-101">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="aa295-101">Get-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="aa295-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aa295-102">SYNOPSIS</span></span>
<span data-ttu-id="aa295-103">Ruft eine Replikation einer Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="aa295-103">Gets a replication of a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa295-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa295-104">SYNTAX</span></span>

### <span data-ttu-id="aa295-105">ListReplicationByNameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="aa295-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa295-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa295-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa295-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa295-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa295-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa295-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa295-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa295-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa295-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa295-110">DESCRIPTION</span></span>
<span data-ttu-id="aa295-111">Das Get-AzureRmContainerRegistryReplication-Cmdlet ruft eine angegebene Replikation einer Container Registrierung oder aller Replikate einer Container Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="aa295-111">The Get-AzureRmContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="aa295-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa295-112">EXAMPLES</span></span>

### <span data-ttu-id="aa295-113">Beispiel 1: Ruft eine angegebene Replikation einer Container Registrierung ab</span><span class="sxs-lookup"><span data-stu-id="aa295-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="aa295-114">Ruft eine angegebene Replikation einer Container Registrierung ab</span><span class="sxs-lookup"><span data-stu-id="aa295-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="aa295-115">Beispiel 2: Ruft alle Replikate einer Container Registrierung ab</span><span class="sxs-lookup"><span data-stu-id="aa295-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="aa295-116">Ruft alle Replikate einer Container Registrierung ab</span><span class="sxs-lookup"><span data-stu-id="aa295-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="aa295-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa295-117">PARAMETERS</span></span>

### <span data-ttu-id="aa295-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa295-118">-DefaultProfile</span></span>
<span data-ttu-id="aa295-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aa295-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa295-120">-Name</span><span class="sxs-lookup"><span data-stu-id="aa295-120">-Name</span></span>
<span data-ttu-id="aa295-121">Name der Container Registrierungsreplikation</span><span class="sxs-lookup"><span data-stu-id="aa295-121">Container Registry Replication Name.</span></span>

```yaml
Type: String
Parameter Sets: ShowReplicationByNameResourceGroupParameterSet, ShowReplicationByRegistryObjectParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa295-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="aa295-122">-Registry</span></span>
<span data-ttu-id="aa295-123">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="aa295-123">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: ShowReplicationByRegistryObjectParameterSet, ListReplicationByRegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa295-124">-Registryname</span><span class="sxs-lookup"><span data-stu-id="aa295-124">-RegistryName</span></span>
<span data-ttu-id="aa295-125">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="aa295-125">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa295-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa295-126">-ResourceGroupName</span></span>
<span data-ttu-id="aa295-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="aa295-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa295-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="aa295-128">-ResourceId</span></span>
<span data-ttu-id="aa295-129">Die Ressourcen-ID der Container Registrierungsreplikation</span><span class="sxs-lookup"><span data-stu-id="aa295-129">The container registry replication resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa295-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa295-130">CommonParameters</span></span>
<span data-ttu-id="aa295-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa295-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa295-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa295-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa295-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aa295-133">INPUTS</span></span>

### <span data-ttu-id="aa295-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="aa295-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="aa295-135">System. String</span><span class="sxs-lookup"><span data-stu-id="aa295-135">System.String</span></span>

## <span data-ttu-id="aa295-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aa295-136">OUTPUTS</span></span>

### <span data-ttu-id="aa295-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="aa295-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>
<span data-ttu-id="aa295-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication []</span><span class="sxs-lookup"><span data-stu-id="aa295-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication[]</span></span>

## <span data-ttu-id="aa295-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="aa295-139">NOTES</span></span>

## <span data-ttu-id="aa295-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aa295-140">RELATED LINKS</span></span>

[<span data-ttu-id="aa295-141">Neu – AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="aa295-141">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="aa295-142">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="aa295-142">Remove-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)
