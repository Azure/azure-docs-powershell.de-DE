---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
ms.openlocfilehash: d2d18a908b53c9a8ab077671b7e2026516d40b17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658692"
---
# <span data-ttu-id="ff562-101">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="ff562-101">New-AzStorageSyncService</span></span>

## <span data-ttu-id="ff562-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ff562-102">SYNOPSIS</span></span>
<span data-ttu-id="ff562-103">Mit diesem Befehl wird ein neuer Speicher Synchronisierungsdienst in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="ff562-103">This command creates a new storage sync service in a resource group.</span></span>

## <span data-ttu-id="ff562-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff562-104">SYNTAX</span></span>

```
New-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff562-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ff562-105">DESCRIPTION</span></span>
<span data-ttu-id="ff562-106">Ein Speicher Synchronisierungsdienst ist die Ressource der obersten Ebene für Azure-Dateisynchronisierung. Mit diesem Befehl wird ein neuer Speicher Synchronisierungsdienst in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="ff562-106">A storage sync service is the top level resource for Azure File Sync. This command creates a new storage sync service in a resource group.</span></span> <span data-ttu-id="ff562-107">Wir empfehlen, so wenige Speicher Synchronisierungsdienste wie unbedingt erforderlich zu erstellen, um unterschiedliche Servergruppen in Ihrer Organisation zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="ff562-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="ff562-108">Ein Speicher Synchronisierungsdienst enthält Synchronisierungsgruppen und funktioniert auch als Ziel für die Registrierung Ihrer Server.</span><span class="sxs-lookup"><span data-stu-id="ff562-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="ff562-109">Ein Server kann nur für einen einzelnen Speicher Synchronisierungsdienst registriert werden.</span><span class="sxs-lookup"><span data-stu-id="ff562-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="ff562-110">Wenn Server jemals an der Synchronisierung desselben Satzes von Dateien teilnehmen müssen, registrieren Sie diese beim gleichen Speicher Synchronisierungsdienst.</span><span class="sxs-lookup"><span data-stu-id="ff562-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="ff562-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ff562-111">EXAMPLES</span></span>

### <span data-ttu-id="ff562-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ff562-112">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncService -ResourceGroupName "myResourceGroup" -Location "myLocation" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="ff562-113">Mit diesem Befehl wird ein Speicher Synchronisierungsdienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="ff562-113">This command will create a storage sync service.</span></span>

## <span data-ttu-id="ff562-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff562-114">PARAMETERS</span></span>

### <span data-ttu-id="ff562-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff562-115">-DefaultProfile</span></span>
<span data-ttu-id="ff562-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ff562-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff562-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="ff562-117">-Location</span></span>
<span data-ttu-id="ff562-118">Speicherort für den Speicher Synchronisierungsdienst</span><span class="sxs-lookup"><span data-stu-id="ff562-118">Storage Sync Service location.</span></span>

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

### <span data-ttu-id="ff562-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ff562-119">-Name</span></span>
<span data-ttu-id="ff562-120">Der Name des Speicher Synchronisierungs Diensts.</span><span class="sxs-lookup"><span data-stu-id="ff562-120">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="ff562-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff562-121">-ResourceGroupName</span></span>
<span data-ttu-id="ff562-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ff562-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="ff562-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="ff562-123">-Tag</span></span>
<span data-ttu-id="ff562-124">Synchronisierungsdienst-Tags für den Speicher.</span><span class="sxs-lookup"><span data-stu-id="ff562-124">Storage Sync Service Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff562-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff562-125">CommonParameters</span></span>
<span data-ttu-id="ff562-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff562-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff562-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff562-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff562-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ff562-128">INPUTS</span></span>

### <span data-ttu-id="ff562-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ff562-129">System.String</span></span>

## <span data-ttu-id="ff562-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ff562-130">OUTPUTS</span></span>

### <span data-ttu-id="ff562-131">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="ff562-131">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="ff562-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="ff562-132">NOTES</span></span>

## <span data-ttu-id="ff562-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ff562-133">RELATED LINKS</span></span>
