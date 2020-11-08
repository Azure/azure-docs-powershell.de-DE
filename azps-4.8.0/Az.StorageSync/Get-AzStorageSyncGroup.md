---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
ms.openlocfilehash: b59d5dd1ca094d4b4d5eed276957f07b7d34f1f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165447"
---
# <span data-ttu-id="ef806-101">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ef806-101">Get-AzStorageSyncGroup</span></span>

## <span data-ttu-id="ef806-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ef806-102">SYNOPSIS</span></span>
<span data-ttu-id="ef806-103">Dieser Befehl listet alle Synchronisierungsgruppen in einem bestimmten Speicher Synchronisierungsdienst auf.</span><span class="sxs-lookup"><span data-stu-id="ef806-103">This command lists all sync groups within a given storage sync service.</span></span>

## <span data-ttu-id="ef806-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef806-104">SYNTAX</span></span>

### <span data-ttu-id="ef806-105">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ef806-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef806-106">Objectparameterset</span><span class="sxs-lookup"><span data-stu-id="ef806-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef806-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef806-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef806-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef806-108">DESCRIPTION</span></span>
<span data-ttu-id="ef806-109">Dieser Befehl listet alle Synchronisierungsgruppen in einem bestimmten Speicher Synchronisierungsdienst auf.</span><span class="sxs-lookup"><span data-stu-id="ef806-109">This command lists all sync groups within a given storage sync service.</span></span> <span data-ttu-id="ef806-110">Sie kann auch verwendet werden, um die Attribute jeder Synchronisierungsgruppe aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="ef806-110">It can be used to also list the attributes of each sync group.</span></span>

## <span data-ttu-id="ef806-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef806-111">EXAMPLES</span></span>

### <span data-ttu-id="ef806-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ef806-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncGroup New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="ef806-113">Dieser Befehl ruft alle Synchronisierungsgruppen ab, die im angegebenen Speicher Synchronisierungsdienst enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ef806-113">This command gets all sync groups contained within the specified storage sync service.</span></span> <span data-ttu-id="ef806-114">Geben Sie den Namen an, um einen bestimmten Wert zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="ef806-114">Specify -Name to return a specific one.</span></span>

## <span data-ttu-id="ef806-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef806-115">PARAMETERS</span></span>

### <span data-ttu-id="ef806-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef806-116">-DefaultProfile</span></span>
<span data-ttu-id="ef806-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ef806-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef806-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ef806-118">-Name</span></span>
<span data-ttu-id="ef806-119">Der Name des SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="ef806-119">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef806-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ef806-120">-ParentObject</span></span>
<span data-ttu-id="ef806-121">StorageSyncService-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="ef806-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="ef806-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ef806-122">-ParentResourceId</span></span>
<span data-ttu-id="ef806-123">StorageSyncService-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="ef806-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="ef806-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef806-124">-ResourceGroupName</span></span>
<span data-ttu-id="ef806-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ef806-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="ef806-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="ef806-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="ef806-127">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="ef806-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="ef806-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef806-128">CommonParameters</span></span>
<span data-ttu-id="ef806-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef806-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef806-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef806-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef806-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ef806-131">INPUTS</span></span>

### <span data-ttu-id="ef806-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ef806-132">System.String</span></span>

### <span data-ttu-id="ef806-133">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="ef806-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="ef806-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ef806-134">OUTPUTS</span></span>

### <span data-ttu-id="ef806-135">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ef806-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="ef806-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="ef806-136">NOTES</span></span>

## <span data-ttu-id="ef806-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ef806-137">RELATED LINKS</span></span>
