---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 076a1393365e93a8008f15137d078a49491d81f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165448"
---
# <span data-ttu-id="c63b4-101">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="c63b4-101">Get-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="c63b4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c63b4-102">SYNOPSIS</span></span>
<span data-ttu-id="c63b4-103">Dieser Befehl listet alle Cloud-Endpunkte innerhalb einer bestimmten Synchronisierungsgruppe auf.</span><span class="sxs-lookup"><span data-stu-id="c63b4-103">This command lists all cloud endpoints within a given sync group.</span></span>

## <span data-ttu-id="c63b4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c63b4-104">SYNTAX</span></span>

### <span data-ttu-id="c63b4-105">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c63b4-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c63b4-106">Objectparameterset</span><span class="sxs-lookup"><span data-stu-id="c63b4-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c63b4-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c63b4-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c63b4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c63b4-108">DESCRIPTION</span></span>
<span data-ttu-id="c63b4-109">Dieser Befehl listet alle Cloud-Endpunkte innerhalb einer bestimmten Synchronisierungsgruppe auf.</span><span class="sxs-lookup"><span data-stu-id="c63b4-109">This command lists all cloud endpoints within a given sync group.</span></span> <span data-ttu-id="c63b4-110">Sie kann auch verwendet werden, um die Attribute der einzelnen Cloud-Endpunkte aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="c63b4-110">It can be used to also list the attributes of each cloud endpoint.</span></span>

## <span data-ttu-id="c63b4-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c63b4-111">EXAMPLES</span></span>

### <span data-ttu-id="c63b4-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c63b4-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="c63b4-113">Dieser Befehl ruft alle Cloud-Endpunkte ab, die in der angegebenen Synchronisierungsgruppe enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c63b4-113">This command gets all cloud endpoints contained within the specified sync group.</span></span> <span data-ttu-id="c63b4-114">Geben Sie-CloudEndpointName ein, um eine bestimmte zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="c63b4-114">Specify -CloudEndpointName to return a specific one.</span></span>

## <span data-ttu-id="c63b4-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c63b4-115">PARAMETERS</span></span>

### <span data-ttu-id="c63b4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c63b4-116">-DefaultProfile</span></span>
<span data-ttu-id="c63b4-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c63b4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c63b4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c63b4-118">-Name</span></span>
<span data-ttu-id="c63b4-119">Der Name des CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="c63b4-119">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="c63b4-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c63b4-120">-ParentObject</span></span>
<span data-ttu-id="c63b4-121">StorageSyncService-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="c63b4-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="c63b4-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c63b4-122">-ParentResourceId</span></span>
<span data-ttu-id="c63b4-123">StorageSyncService-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="c63b4-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="c63b4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c63b4-124">-ResourceGroupName</span></span>
<span data-ttu-id="c63b4-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c63b4-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c63b4-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="c63b4-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="c63b4-127">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="c63b4-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="c63b4-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="c63b4-128">-SyncGroupName</span></span>
<span data-ttu-id="c63b4-129">Der Name des SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="c63b4-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="c63b4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c63b4-130">CommonParameters</span></span>
<span data-ttu-id="c63b4-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c63b4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c63b4-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c63b4-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c63b4-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c63b4-133">INPUTS</span></span>

### <span data-ttu-id="c63b4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c63b4-134">System.String</span></span>

### <span data-ttu-id="c63b4-135">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c63b4-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="c63b4-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c63b4-136">OUTPUTS</span></span>

### <span data-ttu-id="c63b4-137">Microsoft. Azure. Commands. StorageSync. Models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="c63b4-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="c63b4-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="c63b4-138">NOTES</span></span>

## <span data-ttu-id="c63b4-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c63b4-139">RELATED LINKS</span></span>
