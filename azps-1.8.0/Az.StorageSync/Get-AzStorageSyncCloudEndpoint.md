---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: decf935cd61c052e2e77dd8fd2eadacd7a548974
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658711"
---
# <span data-ttu-id="768a9-101">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="768a9-101">Get-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="768a9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="768a9-102">SYNOPSIS</span></span>
<span data-ttu-id="768a9-103">Dieser Befehl listet alle Cloud-Endpunkte innerhalb einer bestimmten Synchronisierungsgruppe auf.</span><span class="sxs-lookup"><span data-stu-id="768a9-103">This command lists all cloud endpoints within a given sync group.</span></span>

## <span data-ttu-id="768a9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="768a9-104">SYNTAX</span></span>

### <span data-ttu-id="768a9-105">Objectparameterset (Standard)</span><span class="sxs-lookup"><span data-stu-id="768a9-105">ObjectParameterSet (Default)</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="768a9-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="768a9-106">StringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="768a9-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="768a9-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="768a9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="768a9-108">DESCRIPTION</span></span>
<span data-ttu-id="768a9-109">Dieser Befehl listet alle Cloud-Endpunkte innerhalb einer bestimmten Synchronisierungsgruppe auf.</span><span class="sxs-lookup"><span data-stu-id="768a9-109">This command lists all cloud endpoints within a given sync group.</span></span> <span data-ttu-id="768a9-110">Sie kann auch verwendet werden, um die Attribute der einzelnen Cloud-Endpunkte aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="768a9-110">It can be used to also list the attributes of each cloud endpoint.</span></span>

## <span data-ttu-id="768a9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="768a9-111">EXAMPLES</span></span>

### <span data-ttu-id="768a9-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="768a9-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="768a9-113">Dieser Befehl ruft alle Cloud-Endpunkte ab, die in der angegebenen Synchronisierungsgruppe enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="768a9-113">This command gets all cloud endpoints contained within the specified sync group.</span></span> <span data-ttu-id="768a9-114">Geben Sie-CloudEndpointName ein, um eine bestimmte zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="768a9-114">Specify -CloudEndpointName to return a specific one.</span></span>

## <span data-ttu-id="768a9-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="768a9-115">PARAMETERS</span></span>

### <span data-ttu-id="768a9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="768a9-116">-DefaultProfile</span></span>
<span data-ttu-id="768a9-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="768a9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="768a9-118">-Name</span><span class="sxs-lookup"><span data-stu-id="768a9-118">-Name</span></span>
<span data-ttu-id="768a9-119">Der Name des CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="768a9-119">Name of the CloudEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudEndpointName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="768a9-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="768a9-120">-ParentObject</span></span>
<span data-ttu-id="768a9-121">StorageSyncService-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="768a9-121">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="768a9-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="768a9-122">-ParentResourceId</span></span>
<span data-ttu-id="768a9-123">StorageSyncService-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="768a9-123">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="768a9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="768a9-124">-ResourceGroupName</span></span>
<span data-ttu-id="768a9-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="768a9-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="768a9-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="768a9-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="768a9-127">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="768a9-127">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="768a9-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="768a9-128">-SyncGroupName</span></span>
<span data-ttu-id="768a9-129">Der Name des SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="768a9-129">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="768a9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="768a9-130">CommonParameters</span></span>
<span data-ttu-id="768a9-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="768a9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="768a9-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="768a9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="768a9-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="768a9-133">INPUTS</span></span>

### <span data-ttu-id="768a9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="768a9-134">System.String</span></span>

### <span data-ttu-id="768a9-135">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="768a9-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="768a9-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="768a9-136">OUTPUTS</span></span>

### <span data-ttu-id="768a9-137">Microsoft. Azure. Commands. StorageSync. Models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="768a9-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="768a9-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="768a9-138">NOTES</span></span>

## <span data-ttu-id="768a9-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="768a9-139">RELATED LINKS</span></span>
