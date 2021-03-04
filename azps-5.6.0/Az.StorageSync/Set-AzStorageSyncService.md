---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/set-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
ms.openlocfilehash: f7b3f0924b1033f1c3b4ffd773ebbbbed985fa3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929611"
---
# <span data-ttu-id="c4363-101">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="c4363-101">Set-AzStorageSyncService</span></span>

## <span data-ttu-id="c4363-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4363-102">SYNOPSIS</span></span>
<span data-ttu-id="c4363-103">Mit diesem Befehl wird der Speichersynchronisierungsdienst in einer Ressourcengruppe definiert.</span><span class="sxs-lookup"><span data-stu-id="c4363-103">This command sets storage sync service in a resource group.</span></span>

## <span data-ttu-id="c4363-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4363-104">SYNTAX</span></span>

```
Set-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4363-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c4363-105">DESCRIPTION</span></span>
<span data-ttu-id="c4363-106">Ein Speichersynchronisierungsdienst ist die Ressource auf oberster Ebene für Azure File Sync. Mit diesem Befehl wird der Speichersynchronisierungsdienst in einer Ressourcengruppe definiert.</span><span class="sxs-lookup"><span data-stu-id="c4363-106">A storage sync service is the top level resource for Azure File Sync. This command sets storage sync service in a resource group.</span></span> <span data-ttu-id="c4363-107">Es wird empfohlen, so wenige Speichersynchronisierungsdienste wie unbedingt erforderlich zu erstellen, um verschiedene Servergruppen in Ihrer Organisation voneinander zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="c4363-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="c4363-108">Ein Speichersynchronisierungsdienst enthält Synchronisierungsgruppen und arbeitet auch als Ziel, um Ihre Server zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="c4363-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="c4363-109">Ein Server kann nur bei einem einzelnen Speichersynchronisierungsdienst registriert werden.</span><span class="sxs-lookup"><span data-stu-id="c4363-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="c4363-110">Wenn Server jemals an der Synchronisierung derselben Gruppe von Dateien teilnehmen müssen, registrieren Sie sie beim gleichen Speichersynchronisierungsdienst.</span><span class="sxs-lookup"><span data-stu-id="c4363-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="c4363-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c4363-111">EXAMPLES</span></span>

### <span data-ttu-id="c4363-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c4363-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncService -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="c4363-113">Mit diesem Befehl wird ein Speichersynchronisierungsdienst festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c4363-113">This command will set a storage sync service.</span></span>

## <span data-ttu-id="c4363-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c4363-114">PARAMETERS</span></span>

### <span data-ttu-id="c4363-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4363-115">-DefaultProfile</span></span>
<span data-ttu-id="c4363-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4363-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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
### <span data-ttu-id="c4363-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c4363-117">-Name</span></span>
<span data-ttu-id="c4363-118">Name des Speichersynchronisierungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="c4363-118">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="c4363-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4363-119">-ResourceGroupName</span></span>
<span data-ttu-id="c4363-120">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="c4363-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="c4363-121">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="c4363-121">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="c4363-122">Storage Sync Service IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="c4363-122">Storage Sync Service IncomingTrafficPolicy</span></span>

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

### <span data-ttu-id="c4363-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="c4363-123">-Tag</span></span>
<span data-ttu-id="c4363-124">Speichersynchronisierungsdiensttags.</span><span class="sxs-lookup"><span data-stu-id="c4363-124">Storage Sync Service Tags.</span></span>

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

### <span data-ttu-id="c4363-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c4363-125">-Confirm</span></span>
<span data-ttu-id="c4363-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c4363-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4363-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4363-127">-WhatIf</span></span>
<span data-ttu-id="c4363-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4363-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4363-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4363-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4363-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4363-130">CommonParameters</span></span>
<span data-ttu-id="c4363-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4363-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4363-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4363-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4363-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c4363-133">INPUTS</span></span>

### <span data-ttu-id="c4363-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c4363-134">System.String</span></span>

## <span data-ttu-id="c4363-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c4363-135">OUTPUTS</span></span>

### <span data-ttu-id="c4363-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="c4363-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="c4363-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c4363-137">NOTES</span></span>

## <span data-ttu-id="c4363-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c4363-138">RELATED LINKS</span></span>
