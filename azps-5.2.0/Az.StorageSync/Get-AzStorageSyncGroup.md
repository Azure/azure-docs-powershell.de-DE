---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
ms.openlocfilehash: b59d5dd1ca094d4b4d5eed276957f07b7d34f1f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293602"
---
# <span data-ttu-id="d0ea2-101">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d0ea2-101">Get-AzStorageSyncGroup</span></span>

## <span data-ttu-id="d0ea2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0ea2-102">SYNOPSIS</span></span>
<span data-ttu-id="d0ea2-103">Dieser Befehl listet alle Synchronisierungsgruppen innerhalb eines bestimmten Speichersynchronisierungsdiensts auf.</span><span class="sxs-lookup"><span data-stu-id="d0ea2-103">This command lists all sync groups within a given storage sync service.</span></span>

## <span data-ttu-id="d0ea2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0ea2-104">SYNTAX</span></span>

### <span data-ttu-id="d0ea2-105">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d0ea2-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0ea2-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0ea2-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0ea2-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0ea2-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0ea2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d0ea2-108">DESCRIPTION</span></span>
<span data-ttu-id="d0ea2-109">Dieser Befehl listet alle Synchronisierungsgruppen innerhalb eines bestimmten Speichersynchronisierungsdiensts auf.</span><span class="sxs-lookup"><span data-stu-id="d0ea2-109">This command lists all sync groups within a given storage sync service.</span></span> <span data-ttu-id="d0ea2-110">Sie kann auch verwendet werden, um die Attribute jeder Synchronisierungsgruppe auflisten.</span><span class="sxs-lookup"><span data-stu-id="d0ea2-110">It can be used to also list the attributes of each sync group.</span></span>

## <span data-ttu-id="d0ea2-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d0ea2-111">EXAMPLES</span></span>

### <span data-ttu-id="d0ea2-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d0ea2-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncGroup New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="d0ea2-113">Dieser Befehl ruft alle Synchronisierungsgruppen ab, die im angegebenen Speichersynchronisierungsdienst enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d0ea2-113">This command gets all sync groups contained within the specified storage sync service.</span></span> <span data-ttu-id="d0ea2-114">Geben Sie "-Name" an, um einen bestimmten Namen zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="d0ea2-114">Specify -Name to return a specific one.</span></span>

## <span data-ttu-id="d0ea2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0ea2-115">PARAMETERS</span></span>

### <span data-ttu-id="d0ea2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0ea2-116">-DefaultProfile</span></span>
<span data-ttu-id="d0ea2-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0ea2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0ea2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d0ea2-118">-Name</span></span>
<span data-ttu-id="d0ea2-119">Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="d0ea2-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="d0ea2-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d0ea2-120">-ParentObject</span></span>
<span data-ttu-id="d0ea2-121">StorageSyncService-Objekt, das normalerweise über den Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d0ea2-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="d0ea2-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d0ea2-122">-ParentResourceId</span></span>
<span data-ttu-id="d0ea2-123">StorageSyncService-Objekt, das normalerweise über den Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d0ea2-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="d0ea2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0ea2-124">-ResourceGroupName</span></span>
<span data-ttu-id="d0ea2-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="d0ea2-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="d0ea2-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="d0ea2-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="d0ea2-127">Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="d0ea2-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="d0ea2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0ea2-128">CommonParameters</span></span>
<span data-ttu-id="d0ea2-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0ea2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0ea2-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0ea2-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0ea2-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d0ea2-131">INPUTS</span></span>

### <span data-ttu-id="d0ea2-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d0ea2-132">System.String</span></span>

### <span data-ttu-id="d0ea2-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="d0ea2-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="d0ea2-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d0ea2-134">OUTPUTS</span></span>

### <span data-ttu-id="d0ea2-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d0ea2-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="d0ea2-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d0ea2-136">NOTES</span></span>

## <span data-ttu-id="d0ea2-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d0ea2-137">RELATED LINKS</span></span>
