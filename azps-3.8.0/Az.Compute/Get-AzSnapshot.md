---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzSnapshot.md
ms.openlocfilehash: 135d9fab47f06dbd2fca1273094548e27273b32e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004846"
---
# <span data-ttu-id="0827a-101">Get-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="0827a-101">Get-AzSnapshot</span></span>

## <span data-ttu-id="0827a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0827a-102">SYNOPSIS</span></span>
<span data-ttu-id="0827a-103">Ruft die Eigenschaften eines Snapshots ab.</span><span class="sxs-lookup"><span data-stu-id="0827a-103">Gets the properties of a snapshot</span></span>

## <span data-ttu-id="0827a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0827a-104">SYNTAX</span></span>

```
Get-AzSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0827a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0827a-105">DESCRIPTION</span></span>
<span data-ttu-id="0827a-106">Das Cmdlet " **Get-AzSnapshot** " Ruft die Eigenschaften eines Snapshots ab.</span><span class="sxs-lookup"><span data-stu-id="0827a-106">The **Get-AzSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="0827a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0827a-107">EXAMPLES</span></span>

### <span data-ttu-id="0827a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0827a-108">Example 1</span></span>
```
PS C:\> Get-AzSnapshot

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName1
Name               : SnapshotName1
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName2
Name               : SnapshotName2
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroupName2
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName2/providers/Microsoft.Compu
                     te/snapshots/SnapshotName3
Name               : SnapshotName3
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}
```

<span data-ttu-id="0827a-109">Dieser Befehl ruft die Eigenschaften aller Snapshots des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="0827a-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="0827a-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0827a-110">Example 2</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1"

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName1
Name               : SnapshotName1
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName2
Name               : SnapshotName2
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}
```

<span data-ttu-id="0827a-111">Dieser Befehl ruft die Eigenschaften aller Schnappschüsse in der Ressourcengruppe mit dem Namen "ResourceGroupName1" ab.</span><span class="sxs-lookup"><span data-stu-id="0827a-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="0827a-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="0827a-112">Example 3</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName1
Name               : SnapshotName1
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}
```

<span data-ttu-id="0827a-113">Mit diesem Befehl werden die Eigenschaften des Snapshots mit dem Namen "SnapshotName1" in der Ressourcengruppe "ResourceGroupName1" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0827a-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="0827a-114">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="0827a-114">Example 4</span></span>
```
PS C:\> Get-AzSnapshot -SnapshotName "SnapshotName*"

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName1
Name               : SnapshotName1
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName2
Name               : SnapshotName2
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroupName2
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName2/providers/Microsoft.Compu
                     te/snapshots/SnapshotName3
Name               : SnapshotName3
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}
```

<span data-ttu-id="0827a-115">Dieser Befehl ruft alle Snapshots ab, die mit "Snapshotname" beginnen.</span><span class="sxs-lookup"><span data-stu-id="0827a-115">This command gets all snapshots that start with "SnapshotName"</span></span>

## <span data-ttu-id="0827a-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="0827a-116">PARAMETERS</span></span>

### <span data-ttu-id="0827a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0827a-117">-DefaultProfile</span></span>
<span data-ttu-id="0827a-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0827a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0827a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0827a-119">-ResourceGroupName</span></span>
<span data-ttu-id="0827a-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0827a-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0827a-121">-Snapshotname</span><span class="sxs-lookup"><span data-stu-id="0827a-121">-SnapshotName</span></span>
<span data-ttu-id="0827a-122">Gibt den Namen eines Schnappschusses an.</span><span class="sxs-lookup"><span data-stu-id="0827a-122">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0827a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0827a-123">CommonParameters</span></span>
<span data-ttu-id="0827a-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0827a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0827a-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0827a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0827a-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0827a-126">INPUTS</span></span>

### <span data-ttu-id="0827a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="0827a-127">System.String</span></span>

## <span data-ttu-id="0827a-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0827a-128">OUTPUTS</span></span>

### <span data-ttu-id="0827a-129">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="0827a-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="0827a-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="0827a-130">NOTES</span></span>

## <span data-ttu-id="0827a-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0827a-131">RELATED LINKS</span></span>
