---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
ms.openlocfilehash: a9d5b5582a630a3131761d44c329a47c49546f11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658709"
---
# <span data-ttu-id="b72fd-101">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="b72fd-101">Get-AzStorageSyncServer</span></span>

## <span data-ttu-id="b72fd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b72fd-102">SYNOPSIS</span></span>
<span data-ttu-id="b72fd-103">Dieser Befehl listet alle Server auf, die für einen bestimmten Speicher Synchronisierungsdienst registriert sind.</span><span class="sxs-lookup"><span data-stu-id="b72fd-103">This command lists all servers registered to a given storage sync service.</span></span>

## <span data-ttu-id="b72fd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b72fd-104">SYNTAX</span></span>

### <span data-ttu-id="b72fd-105">Objectparameterset (Standard)</span><span class="sxs-lookup"><span data-stu-id="b72fd-105">ObjectParameterSet (Default)</span></span>
```
Get-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b72fd-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b72fd-106">StringParameterSet</span></span>
```
Get-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b72fd-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b72fd-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentResourceId] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b72fd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b72fd-108">DESCRIPTION</span></span>
<span data-ttu-id="b72fd-109">Dieser Befehl listet alle Server auf, die für einen bestimmten Speicher Synchronisierungsdienst registriert sind.</span><span class="sxs-lookup"><span data-stu-id="b72fd-109">This command lists all servers registered to a given storage sync service.</span></span> <span data-ttu-id="b72fd-110">Sie kann auch verwendet werden, um die Attribute der einzelnen registrierten Server aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="b72fd-110">It can be used to also list the attributes of each registered server.</span></span>

## <span data-ttu-id="b72fd-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b72fd-111">EXAMPLES</span></span>

### <span data-ttu-id="b72fd-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b72fd-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="b72fd-113">Dieser Befehl ruft alle Server ab, die für einen bestimmten Speicher Synchronisierungsdienst registriert sind.</span><span class="sxs-lookup"><span data-stu-id="b72fd-113">This command gets all servers registered to a specific storage sync service.</span></span>

## <span data-ttu-id="b72fd-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b72fd-114">PARAMETERS</span></span>

### <span data-ttu-id="b72fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b72fd-115">-DefaultProfile</span></span>
<span data-ttu-id="b72fd-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b72fd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b72fd-117">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b72fd-117">-ParentObject</span></span>
<span data-ttu-id="b72fd-118">StorageSyncService-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="b72fd-118">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="b72fd-119">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b72fd-119">-ParentResourceId</span></span>
<span data-ttu-id="b72fd-120">StorageSyncService-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="b72fd-120">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="b72fd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b72fd-121">-ResourceGroupName</span></span>
<span data-ttu-id="b72fd-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b72fd-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="b72fd-123">-Server-Nr</span><span class="sxs-lookup"><span data-stu-id="b72fd-123">-ServerId</span></span>
<span data-ttu-id="b72fd-124">Der Name des registeredserver.</span><span class="sxs-lookup"><span data-stu-id="b72fd-124">Name of the RegisteredServer.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: RegisteredServerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b72fd-125">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="b72fd-125">-StorageSyncServiceName</span></span>
<span data-ttu-id="b72fd-126">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="b72fd-126">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="b72fd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b72fd-127">CommonParameters</span></span>
<span data-ttu-id="b72fd-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b72fd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b72fd-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b72fd-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b72fd-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b72fd-130">INPUTS</span></span>

### <span data-ttu-id="b72fd-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b72fd-131">System.String</span></span>

### <span data-ttu-id="b72fd-132">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="b72fd-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="b72fd-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b72fd-133">System.Guid</span></span>

## <span data-ttu-id="b72fd-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b72fd-134">OUTPUTS</span></span>

### <span data-ttu-id="b72fd-135">Microsoft. Azure. Commands. StorageSync. Models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="b72fd-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="b72fd-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="b72fd-136">NOTES</span></span>

## <span data-ttu-id="b72fd-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b72fd-137">RELATED LINKS</span></span>
