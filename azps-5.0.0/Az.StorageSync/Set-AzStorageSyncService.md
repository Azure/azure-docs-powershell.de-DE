---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
ms.openlocfilehash: 2e22912df9a567ac836f22c8ac82d0a70610f2f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178190"
---
# <span data-ttu-id="f2a00-101">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f2a00-101">Set-AzStorageSyncService</span></span>

## <span data-ttu-id="f2a00-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f2a00-102">SYNOPSIS</span></span>
<span data-ttu-id="f2a00-103">Dieser Befehl legt den Speicher Synchronisierungsdienst in einer Ressourcengruppe fest.</span><span class="sxs-lookup"><span data-stu-id="f2a00-103">This command sets storage sync service in a resource group.</span></span>

## <span data-ttu-id="f2a00-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2a00-104">SYNTAX</span></span>

```
Set-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2a00-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2a00-105">DESCRIPTION</span></span>
<span data-ttu-id="f2a00-106">Ein Speicher Synchronisierungsdienst ist die Ressource der obersten Ebene für Azure-Dateisynchronisierung. Dieser Befehl legt den Speicher Synchronisierungsdienst in einer Ressourcengruppe fest.</span><span class="sxs-lookup"><span data-stu-id="f2a00-106">A storage sync service is the top level resource for Azure File Sync. This command sets storage sync service in a resource group.</span></span> <span data-ttu-id="f2a00-107">Wir empfehlen, so wenige Speicher Synchronisierungsdienste wie unbedingt erforderlich zu erstellen, um unterschiedliche Servergruppen in Ihrer Organisation zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="f2a00-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="f2a00-108">Ein Speicher Synchronisierungsdienst enthält Synchronisierungsgruppen und funktioniert auch als Ziel für die Registrierung Ihrer Server.</span><span class="sxs-lookup"><span data-stu-id="f2a00-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="f2a00-109">Ein Server kann nur für einen einzelnen Speicher Synchronisierungsdienst registriert werden.</span><span class="sxs-lookup"><span data-stu-id="f2a00-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="f2a00-110">Wenn Server jemals an der Synchronisierung desselben Satzes von Dateien teilnehmen müssen, registrieren Sie diese beim gleichen Speicher Synchronisierungsdienst.</span><span class="sxs-lookup"><span data-stu-id="f2a00-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="f2a00-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f2a00-111">EXAMPLES</span></span>

### <span data-ttu-id="f2a00-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f2a00-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncService -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="f2a00-113">Mit diesem Befehl wird ein Speicher Synchronisierungsdienst eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="f2a00-113">This command will set a storage sync service.</span></span>

## <span data-ttu-id="f2a00-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2a00-114">PARAMETERS</span></span>

### <span data-ttu-id="f2a00-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2a00-115">-DefaultProfile</span></span>
<span data-ttu-id="f2a00-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f2a00-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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
### <span data-ttu-id="f2a00-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f2a00-117">-Name</span></span>
<span data-ttu-id="f2a00-118">Der Name des Speicher Synchronisierungs Diensts.</span><span class="sxs-lookup"><span data-stu-id="f2a00-118">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="f2a00-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2a00-119">-ResourceGroupName</span></span>
<span data-ttu-id="f2a00-120">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f2a00-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="f2a00-121">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="f2a00-121">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="f2a00-122">Speicher Synchronisierungsdienst IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="f2a00-122">Storage Sync Service IncomingTrafficPolicy</span></span>

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

### <span data-ttu-id="f2a00-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="f2a00-123">-Tag</span></span>
<span data-ttu-id="f2a00-124">Synchronisierungsdienst-Tags für den Speicher.</span><span class="sxs-lookup"><span data-stu-id="f2a00-124">Storage Sync Service Tags.</span></span>

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

### <span data-ttu-id="f2a00-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f2a00-125">-Confirm</span></span>
<span data-ttu-id="f2a00-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f2a00-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2a00-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2a00-127">-WhatIf</span></span>
<span data-ttu-id="f2a00-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2a00-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2a00-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2a00-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2a00-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2a00-130">CommonParameters</span></span>
<span data-ttu-id="f2a00-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2a00-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2a00-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2a00-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2a00-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f2a00-133">INPUTS</span></span>

### <span data-ttu-id="f2a00-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f2a00-134">System.String</span></span>

## <span data-ttu-id="f2a00-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f2a00-135">OUTPUTS</span></span>

### <span data-ttu-id="f2a00-136">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f2a00-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="f2a00-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="f2a00-137">NOTES</span></span>

## <span data-ttu-id="f2a00-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f2a00-138">RELATED LINKS</span></span>
