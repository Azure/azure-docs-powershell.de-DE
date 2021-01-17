---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
ms.openlocfilehash: 0476a881ec1ee479b97dad4ab8dcf95121dd5302
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460108"
---
# <span data-ttu-id="bea1d-101">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="bea1d-101">New-AzStorageSyncService</span></span>

## <span data-ttu-id="bea1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bea1d-102">SYNOPSIS</span></span>
<span data-ttu-id="bea1d-103">Mit diesem Befehl wird ein neuer Speichersynchronisierungsdienst in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="bea1d-103">This command creates a new storage sync service in a resource group.</span></span>

## <span data-ttu-id="bea1d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bea1d-104">SYNTAX</span></span>

```
New-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-IncomingTrafficPolicy] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bea1d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bea1d-105">DESCRIPTION</span></span>
<span data-ttu-id="bea1d-106">Ein Speichersynchronisierungsdienst ist die Ressource der obersten Ebene für die Azure File Sync. Mit diesem Befehl wird ein neuer Speichersynchronisierungsdienst in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="bea1d-106">A storage sync service is the top level resource for Azure File Sync. This command creates a new storage sync service in a resource group.</span></span> <span data-ttu-id="bea1d-107">Es wird empfohlen, so wenige Speichersynchronisierungsdienste wie unbedingt notwendig zu erstellen, um unterschiedliche Servergruppen in Ihrer Organisation voneinander zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="bea1d-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="bea1d-108">Ein Speichersynchronisierungsdienst enthält Synchronisierungsgruppen und kann auch als Ziel verwendet werden, um Ihre Server zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="bea1d-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="bea1d-109">Ein Server kann nur bei einem einzigen Speichersynchronisierungsdienst registriert werden.</span><span class="sxs-lookup"><span data-stu-id="bea1d-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="bea1d-110">Wenn Server jemals an der Synchronisierung derselben Gruppe von Dateien teilnehmen müssen, registrieren Sie sie beim gleichen Speichersynchronisierungsdienst.</span><span class="sxs-lookup"><span data-stu-id="bea1d-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="bea1d-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bea1d-111">EXAMPLES</span></span>

### <span data-ttu-id="bea1d-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bea1d-112">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncService -ResourceGroupName "myResourceGroup" -Location "myLocation" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="bea1d-113">Mit diesem Befehl wird ein Speichersynchronisierungsdienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="bea1d-113">This command will create a storage sync service.</span></span>

## <span data-ttu-id="bea1d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bea1d-114">PARAMETERS</span></span>

### <span data-ttu-id="bea1d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea1d-115">-DefaultProfile</span></span>
<span data-ttu-id="bea1d-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bea1d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bea1d-117">-Location</span><span class="sxs-lookup"><span data-stu-id="bea1d-117">-Location</span></span>
<span data-ttu-id="bea1d-118">Speicherort des Speichersynchronisierungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="bea1d-118">Storage Sync Service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bea1d-119">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="bea1d-119">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="bea1d-120">Storage Sync Service IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="bea1d-120">Storage Sync Service IncomingTrafficPolicy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bea1d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bea1d-121">-Name</span></span>
<span data-ttu-id="bea1d-122">Name des Speichersynchronisierungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="bea1d-122">Name of the storage sync service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageSyncServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bea1d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bea1d-123">-ResourceGroupName</span></span>
<span data-ttu-id="bea1d-124">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="bea1d-124">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bea1d-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="bea1d-125">-Tag</span></span>
<span data-ttu-id="bea1d-126">Tags für den Speichersynchronisierungsdienst.</span><span class="sxs-lookup"><span data-stu-id="bea1d-126">Storage Sync Service Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bea1d-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bea1d-127">-Confirm</span></span>
<span data-ttu-id="bea1d-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bea1d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bea1d-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="bea1d-129">-WhatIf</span></span>
<span data-ttu-id="bea1d-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bea1d-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bea1d-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bea1d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bea1d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea1d-132">CommonParameters</span></span>
<span data-ttu-id="bea1d-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bea1d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea1d-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bea1d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea1d-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bea1d-135">INPUTS</span></span>

### <span data-ttu-id="bea1d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="bea1d-136">System.String</span></span>

## <span data-ttu-id="bea1d-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bea1d-137">OUTPUTS</span></span>

### <span data-ttu-id="bea1d-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="bea1d-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="bea1d-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bea1d-139">NOTES</span></span>

## <span data-ttu-id="bea1d-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bea1d-140">RELATED LINKS</span></span>
