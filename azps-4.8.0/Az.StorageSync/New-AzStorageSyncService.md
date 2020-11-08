---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
ms.openlocfilehash: 0476a881ec1ee479b97dad4ab8dcf95121dd5302
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165959"
---
# <span data-ttu-id="f0340-101">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f0340-101">New-AzStorageSyncService</span></span>

## <span data-ttu-id="f0340-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f0340-102">SYNOPSIS</span></span>
<span data-ttu-id="f0340-103">Mit diesem Befehl wird ein neuer Speicher Synchronisierungsdienst in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="f0340-103">This command creates a new storage sync service in a resource group.</span></span>

## <span data-ttu-id="f0340-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0340-104">SYNTAX</span></span>

```
New-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-IncomingTrafficPolicy] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0340-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0340-105">DESCRIPTION</span></span>
<span data-ttu-id="f0340-106">Ein Speicher Synchronisierungsdienst ist die Ressource der obersten Ebene für Azure-Dateisynchronisierung. Mit diesem Befehl wird ein neuer Speicher Synchronisierungsdienst in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="f0340-106">A storage sync service is the top level resource for Azure File Sync. This command creates a new storage sync service in a resource group.</span></span> <span data-ttu-id="f0340-107">Wir empfehlen, so wenige Speicher Synchronisierungsdienste wie unbedingt erforderlich zu erstellen, um unterschiedliche Servergruppen in Ihrer Organisation zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="f0340-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="f0340-108">Ein Speicher Synchronisierungsdienst enthält Synchronisierungsgruppen und funktioniert auch als Ziel für die Registrierung Ihrer Server.</span><span class="sxs-lookup"><span data-stu-id="f0340-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="f0340-109">Ein Server kann nur für einen einzelnen Speicher Synchronisierungsdienst registriert werden.</span><span class="sxs-lookup"><span data-stu-id="f0340-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="f0340-110">Wenn Server jemals an der Synchronisierung desselben Satzes von Dateien teilnehmen müssen, registrieren Sie diese beim gleichen Speicher Synchronisierungsdienst.</span><span class="sxs-lookup"><span data-stu-id="f0340-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="f0340-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f0340-111">EXAMPLES</span></span>

### <span data-ttu-id="f0340-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f0340-112">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncService -ResourceGroupName "myResourceGroup" -Location "myLocation" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="f0340-113">Mit diesem Befehl wird ein Speicher Synchronisierungsdienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="f0340-113">This command will create a storage sync service.</span></span>

## <span data-ttu-id="f0340-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0340-114">PARAMETERS</span></span>

### <span data-ttu-id="f0340-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0340-115">-DefaultProfile</span></span>
<span data-ttu-id="f0340-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f0340-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0340-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="f0340-117">-Location</span></span>
<span data-ttu-id="f0340-118">Speicherort für den Speicher Synchronisierungsdienst</span><span class="sxs-lookup"><span data-stu-id="f0340-118">Storage Sync Service location.</span></span>

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

### <span data-ttu-id="f0340-119">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="f0340-119">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="f0340-120">Speicher Synchronisierungsdienst IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="f0340-120">Storage Sync Service IncomingTrafficPolicy</span></span>

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

### <span data-ttu-id="f0340-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f0340-121">-Name</span></span>
<span data-ttu-id="f0340-122">Der Name des Speicher Synchronisierungs Diensts.</span><span class="sxs-lookup"><span data-stu-id="f0340-122">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="f0340-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0340-123">-ResourceGroupName</span></span>
<span data-ttu-id="f0340-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f0340-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="f0340-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="f0340-125">-Tag</span></span>
<span data-ttu-id="f0340-126">Synchronisierungsdienst-Tags für den Speicher.</span><span class="sxs-lookup"><span data-stu-id="f0340-126">Storage Sync Service Tags.</span></span>

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

### <span data-ttu-id="f0340-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f0340-127">-Confirm</span></span>
<span data-ttu-id="f0340-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f0340-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0340-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0340-129">-WhatIf</span></span>
<span data-ttu-id="f0340-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0340-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0340-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0340-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0340-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0340-132">CommonParameters</span></span>
<span data-ttu-id="f0340-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0340-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0340-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0340-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0340-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f0340-135">INPUTS</span></span>

### <span data-ttu-id="f0340-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f0340-136">System.String</span></span>

## <span data-ttu-id="f0340-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f0340-137">OUTPUTS</span></span>

### <span data-ttu-id="f0340-138">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f0340-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="f0340-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="f0340-139">NOTES</span></span>

## <span data-ttu-id="f0340-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f0340-140">RELATED LINKS</span></span>
