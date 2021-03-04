---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/new-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
ms.openlocfilehash: c24bf60171e152985fb13204f23082f94f8c7ff0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948296"
---
# <span data-ttu-id="fcbef-101">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="fcbef-101">New-AzStorageSyncService</span></span>

## <span data-ttu-id="fcbef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcbef-102">SYNOPSIS</span></span>
<span data-ttu-id="fcbef-103">Mit diesem Befehl wird ein neuer Speichersynchronisierungsdienst in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="fcbef-103">This command creates a new storage sync service in a resource group.</span></span>

## <span data-ttu-id="fcbef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fcbef-104">SYNTAX</span></span>

```
New-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-IncomingTrafficPolicy] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcbef-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fcbef-105">DESCRIPTION</span></span>
<span data-ttu-id="fcbef-106">Ein Speichersynchronisierungsdienst ist die Ressource auf oberster Ebene für Azure File Sync. Mit diesem Befehl wird ein neuer Speichersynchronisierungsdienst in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="fcbef-106">A storage sync service is the top level resource for Azure File Sync. This command creates a new storage sync service in a resource group.</span></span> <span data-ttu-id="fcbef-107">Es wird empfohlen, so wenige Speichersynchronisierungsdienste wie unbedingt erforderlich zu erstellen, um verschiedene Servergruppen in Ihrer Organisation voneinander zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="fcbef-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="fcbef-108">Ein Speichersynchronisierungsdienst enthält Synchronisierungsgruppen und arbeitet auch als Ziel, um Ihre Server zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="fcbef-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="fcbef-109">Ein Server kann nur bei einem einzelnen Speichersynchronisierungsdienst registriert werden.</span><span class="sxs-lookup"><span data-stu-id="fcbef-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="fcbef-110">Wenn Server jemals an der Synchronisierung derselben Gruppe von Dateien teilnehmen müssen, registrieren Sie sie beim gleichen Speichersynchronisierungsdienst.</span><span class="sxs-lookup"><span data-stu-id="fcbef-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="fcbef-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fcbef-111">EXAMPLES</span></span>

### <span data-ttu-id="fcbef-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fcbef-112">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncService -ResourceGroupName "myResourceGroup" -Location "myLocation" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="fcbef-113">Mit diesem Befehl wird ein Speichersynchronisierungsdienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="fcbef-113">This command will create a storage sync service.</span></span>

## <span data-ttu-id="fcbef-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fcbef-114">PARAMETERS</span></span>

### <span data-ttu-id="fcbef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcbef-115">-DefaultProfile</span></span>
<span data-ttu-id="fcbef-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fcbef-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcbef-117">-Location</span><span class="sxs-lookup"><span data-stu-id="fcbef-117">-Location</span></span>
<span data-ttu-id="fcbef-118">Speicherort des Speichersynchronisierungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="fcbef-118">Storage Sync Service location.</span></span>

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

### <span data-ttu-id="fcbef-119">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="fcbef-119">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="fcbef-120">Storage Sync Service IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="fcbef-120">Storage Sync Service IncomingTrafficPolicy</span></span>

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

### <span data-ttu-id="fcbef-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fcbef-121">-Name</span></span>
<span data-ttu-id="fcbef-122">Name des Speichersynchronisierungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="fcbef-122">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="fcbef-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcbef-123">-ResourceGroupName</span></span>
<span data-ttu-id="fcbef-124">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="fcbef-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="fcbef-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="fcbef-125">-Tag</span></span>
<span data-ttu-id="fcbef-126">Speichersynchronisierungsdiensttags.</span><span class="sxs-lookup"><span data-stu-id="fcbef-126">Storage Sync Service Tags.</span></span>

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

### <span data-ttu-id="fcbef-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fcbef-127">-Confirm</span></span>
<span data-ttu-id="fcbef-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fcbef-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcbef-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcbef-129">-WhatIf</span></span>
<span data-ttu-id="fcbef-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fcbef-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fcbef-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fcbef-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcbef-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcbef-132">CommonParameters</span></span>
<span data-ttu-id="fcbef-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcbef-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcbef-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcbef-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcbef-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fcbef-135">INPUTS</span></span>

### <span data-ttu-id="fcbef-136">System.String</span><span class="sxs-lookup"><span data-stu-id="fcbef-136">System.String</span></span>

## <span data-ttu-id="fcbef-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fcbef-137">OUTPUTS</span></span>

### <span data-ttu-id="fcbef-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="fcbef-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="fcbef-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fcbef-139">NOTES</span></span>

## <span data-ttu-id="fcbef-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fcbef-140">RELATED LINKS</span></span>
