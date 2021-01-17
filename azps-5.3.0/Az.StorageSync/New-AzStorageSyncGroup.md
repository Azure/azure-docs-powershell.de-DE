---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: fb199887edcc3a9895095101870856d15f86ac08
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460120"
---
# <span data-ttu-id="69ead-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="69ead-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="69ead-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69ead-102">SYNOPSIS</span></span>
<span data-ttu-id="69ead-103">Mit diesem Befehl wird eine neue Synchronisierungsgruppe innerhalb eines angegebenen Speichersynchronisierungsdiensts erstellt.</span><span class="sxs-lookup"><span data-stu-id="69ead-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="69ead-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69ead-104">SYNTAX</span></span>

### <span data-ttu-id="69ead-105">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="69ead-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69ead-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69ead-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69ead-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="69ead-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69ead-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69ead-108">DESCRIPTION</span></span>
<span data-ttu-id="69ead-109">Mit diesem Befehl wird eine neue Synchronisierungsgruppe innerhalb eines angegebenen Speichersynchronisierungsdiensts erstellt.</span><span class="sxs-lookup"><span data-stu-id="69ead-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="69ead-110">Eine Synchronisierungsgruppe wird verwendet, um eine Topologie von Speicherorten zu beschreiben, die als Endpunkte bezeichnet werden und alle Dateien synchronisieren, die in einem der Endpunkte gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="69ead-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="69ead-111">Eine Synchronisierungsgruppe enthält Cloudendpunkte, die auf Azure-Dateifreigaben verweisen, sowie Serverendpunkte, die auf einen bestimmten lokalen Pfad auf einem registrierten Server verweisen.</span><span class="sxs-lookup"><span data-stu-id="69ead-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="69ead-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="69ead-112">EXAMPLES</span></span>

### <span data-ttu-id="69ead-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="69ead-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="69ead-114">Mit diesem Befehl wird eine neue Synchronisierungsgruppe innerhalb eines angegebenen Speichersynchronisierungsdiensts erstellt.</span><span class="sxs-lookup"><span data-stu-id="69ead-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="69ead-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69ead-115">PARAMETERS</span></span>

### <span data-ttu-id="69ead-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69ead-116">-DefaultProfile</span></span>
<span data-ttu-id="69ead-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="69ead-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69ead-118">-Name</span><span class="sxs-lookup"><span data-stu-id="69ead-118">-Name</span></span>
<span data-ttu-id="69ead-119">Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="69ead-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="69ead-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="69ead-120">-ParentObject</span></span>
<span data-ttu-id="69ead-121">StorageSyncService-Objekt, das normalerweise über den Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="69ead-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="69ead-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="69ead-122">-ParentResourceId</span></span>
<span data-ttu-id="69ead-123">StorageSyncService, übergeordnete Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="69ead-123">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="69ead-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69ead-124">-ResourceGroupName</span></span>
<span data-ttu-id="69ead-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="69ead-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="69ead-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="69ead-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="69ead-127">Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="69ead-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="69ead-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69ead-128">-Confirm</span></span>
<span data-ttu-id="69ead-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="69ead-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ead-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="69ead-130">-WhatIf</span></span>
<span data-ttu-id="69ead-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69ead-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69ead-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="69ead-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ead-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69ead-133">CommonParameters</span></span>
<span data-ttu-id="69ead-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69ead-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69ead-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69ead-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69ead-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="69ead-136">INPUTS</span></span>

### <span data-ttu-id="69ead-137">System.String</span><span class="sxs-lookup"><span data-stu-id="69ead-137">System.String</span></span>

### <span data-ttu-id="69ead-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="69ead-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="69ead-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="69ead-139">OUTPUTS</span></span>

### <span data-ttu-id="69ead-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="69ead-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="69ead-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="69ead-141">NOTES</span></span>

## <span data-ttu-id="69ead-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="69ead-142">RELATED LINKS</span></span>
