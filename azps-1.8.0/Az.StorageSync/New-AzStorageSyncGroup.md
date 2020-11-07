---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: 34f4dc1933e755167333d12d4566838ea47c26b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658694"
---
# <span data-ttu-id="61e90-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="61e90-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="61e90-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="61e90-102">SYNOPSIS</span></span>
<span data-ttu-id="61e90-103">Dieser Befehl erstellt eine neue Synchronisierungsgruppe innerhalb eines angegebenen Speicher Synchronisierungs Diensts.</span><span class="sxs-lookup"><span data-stu-id="61e90-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="61e90-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="61e90-104">SYNTAX</span></span>

### <span data-ttu-id="61e90-105">Objectparameterset (Standard)</span><span class="sxs-lookup"><span data-stu-id="61e90-105">ObjectParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61e90-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="61e90-106">StringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61e90-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="61e90-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61e90-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61e90-108">DESCRIPTION</span></span>
<span data-ttu-id="61e90-109">Dieser Befehl erstellt eine neue Synchronisierungsgruppe innerhalb eines angegebenen Speicher Synchronisierungs Diensts.</span><span class="sxs-lookup"><span data-stu-id="61e90-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="61e90-110">Eine Synchronisierungsgruppe wird verwendet, um eine Topologie von Speicherorten zu beschreiben, die als Endpunkte bezeichnet werden, mit denen alle Dateien synchronisiert werden, die in einem der Endpunkte gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="61e90-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="61e90-111">Eine Synchronisierungsgruppe enthält Cloud-Endpunkte, die auf Azure-Dateifreigaben verweisen, und Sie enthält auch Server Endpunkte, die auf einen bestimmten lokalen Pfad auf einem registrierten Server verweisen.</span><span class="sxs-lookup"><span data-stu-id="61e90-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="61e90-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="61e90-112">EXAMPLES</span></span>

### <span data-ttu-id="61e90-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="61e90-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="61e90-114">Dieser Befehl erstellt eine neue Synchronisierungsgruppe innerhalb eines angegebenen Speicher Synchronisierungs Diensts.</span><span class="sxs-lookup"><span data-stu-id="61e90-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="61e90-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="61e90-115">PARAMETERS</span></span>

### <span data-ttu-id="61e90-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61e90-116">-DefaultProfile</span></span>
<span data-ttu-id="61e90-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="61e90-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61e90-118">-Name</span><span class="sxs-lookup"><span data-stu-id="61e90-118">-Name</span></span>
<span data-ttu-id="61e90-119">Der Name des SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="61e90-119">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e90-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="61e90-120">-ParentObject</span></span>
<span data-ttu-id="61e90-121">StorageSyncService-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="61e90-121">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61e90-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="61e90-122">-ParentResourceId</span></span>
<span data-ttu-id="61e90-123">StorageSyncService übergeordnete Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="61e90-123">StorageSyncService Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e90-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61e90-124">-ResourceGroupName</span></span>
<span data-ttu-id="61e90-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="61e90-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="61e90-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="61e90-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="61e90-127">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="61e90-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="61e90-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61e90-128">CommonParameters</span></span>
<span data-ttu-id="61e90-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61e90-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61e90-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61e90-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61e90-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="61e90-131">INPUTS</span></span>

### <span data-ttu-id="61e90-132">System. String</span><span class="sxs-lookup"><span data-stu-id="61e90-132">System.String</span></span>

### <span data-ttu-id="61e90-133">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="61e90-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="61e90-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="61e90-134">OUTPUTS</span></span>

### <span data-ttu-id="61e90-135">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="61e90-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="61e90-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="61e90-136">NOTES</span></span>

## <span data-ttu-id="61e90-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="61e90-137">RELATED LINKS</span></span>
