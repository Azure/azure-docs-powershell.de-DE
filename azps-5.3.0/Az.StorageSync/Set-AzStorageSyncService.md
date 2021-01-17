---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
ms.openlocfilehash: 2e22912df9a567ac836f22c8ac82d0a70610f2f3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460087"
---
# <span data-ttu-id="ef94c-101">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="ef94c-101">Set-AzStorageSyncService</span></span>

## <span data-ttu-id="ef94c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef94c-102">SYNOPSIS</span></span>
<span data-ttu-id="ef94c-103">Dieser Befehl legt den Speichersynchronisierungsdienst in einer Ressourcengruppe fest.</span><span class="sxs-lookup"><span data-stu-id="ef94c-103">This command sets storage sync service in a resource group.</span></span>

## <span data-ttu-id="ef94c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef94c-104">SYNTAX</span></span>

```
Set-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef94c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef94c-105">DESCRIPTION</span></span>
<span data-ttu-id="ef94c-106">Ein Speichersynchronisierungsdienst ist die Ressource der obersten Ebene für die Azure File Sync. Dieser Befehl legt den Speichersynchronisierungsdienst in einer Ressourcengruppe fest.</span><span class="sxs-lookup"><span data-stu-id="ef94c-106">A storage sync service is the top level resource for Azure File Sync. This command sets storage sync service in a resource group.</span></span> <span data-ttu-id="ef94c-107">Es wird empfohlen, so wenige Speichersynchronisierungsdienste wie unbedingt notwendig zu erstellen, um unterschiedliche Servergruppen in Ihrer Organisation voneinander zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="ef94c-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="ef94c-108">Ein Speichersynchronisierungsdienst enthält Synchronisierungsgruppen und kann auch als Ziel verwendet werden, um Ihre Server zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="ef94c-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="ef94c-109">Ein Server kann nur bei einem einzigen Speichersynchronisierungsdienst registriert werden.</span><span class="sxs-lookup"><span data-stu-id="ef94c-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="ef94c-110">Wenn Server jemals an der Synchronisierung derselben Gruppe von Dateien teilnehmen müssen, registrieren Sie sie beim gleichen Speichersynchronisierungsdienst.</span><span class="sxs-lookup"><span data-stu-id="ef94c-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="ef94c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ef94c-111">EXAMPLES</span></span>

### <span data-ttu-id="ef94c-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ef94c-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncService -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="ef94c-113">Mit diesem Befehl wird ein Speichersynchronisierungsdienst festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ef94c-113">This command will set a storage sync service.</span></span>

## <span data-ttu-id="ef94c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef94c-114">PARAMETERS</span></span>

### <span data-ttu-id="ef94c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef94c-115">-DefaultProfile</span></span>
<span data-ttu-id="ef94c-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef94c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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
### <span data-ttu-id="ef94c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ef94c-117">-Name</span></span>
<span data-ttu-id="ef94c-118">Name des Speichersynchronisierungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="ef94c-118">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="ef94c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef94c-119">-ResourceGroupName</span></span>
<span data-ttu-id="ef94c-120">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="ef94c-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="ef94c-121">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="ef94c-121">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="ef94c-122">Storage Sync Service IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="ef94c-122">Storage Sync Service IncomingTrafficPolicy</span></span>

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

### <span data-ttu-id="ef94c-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="ef94c-123">-Tag</span></span>
<span data-ttu-id="ef94c-124">Tags für den Speichersynchronisierungsdienst.</span><span class="sxs-lookup"><span data-stu-id="ef94c-124">Storage Sync Service Tags.</span></span>

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

### <span data-ttu-id="ef94c-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef94c-125">-Confirm</span></span>
<span data-ttu-id="ef94c-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ef94c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef94c-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ef94c-127">-WhatIf</span></span>
<span data-ttu-id="ef94c-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef94c-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef94c-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ef94c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef94c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef94c-130">CommonParameters</span></span>
<span data-ttu-id="ef94c-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef94c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef94c-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef94c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef94c-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ef94c-133">INPUTS</span></span>

### <span data-ttu-id="ef94c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="ef94c-134">System.String</span></span>

## <span data-ttu-id="ef94c-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ef94c-135">OUTPUTS</span></span>

### <span data-ttu-id="ef94c-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="ef94c-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="ef94c-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ef94c-137">NOTES</span></span>

## <span data-ttu-id="ef94c-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ef94c-138">RELATED LINKS</span></span>
