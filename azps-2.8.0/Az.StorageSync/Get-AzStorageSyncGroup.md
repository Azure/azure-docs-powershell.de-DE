---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
ms.openlocfilehash: 9d378139fb4783922973b5982039271461447c9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826395"
---
# <span data-ttu-id="02768-101">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="02768-101">Get-AzStorageSyncGroup</span></span>

## <span data-ttu-id="02768-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="02768-102">SYNOPSIS</span></span>
<span data-ttu-id="02768-103">Dieser Befehl listet alle Synchronisierungsgruppen in einem bestimmten Speicher Synchronisierungsdienst auf.</span><span class="sxs-lookup"><span data-stu-id="02768-103">This command lists all sync groups within a given storage sync service.</span></span>

## <span data-ttu-id="02768-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="02768-104">SYNTAX</span></span>

### <span data-ttu-id="02768-105">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="02768-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02768-106">Objectparameterset</span><span class="sxs-lookup"><span data-stu-id="02768-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02768-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="02768-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02768-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02768-108">DESCRIPTION</span></span>
<span data-ttu-id="02768-109">Dieser Befehl listet alle Synchronisierungsgruppen in einem bestimmten Speicher Synchronisierungsdienst auf.</span><span class="sxs-lookup"><span data-stu-id="02768-109">This command lists all sync groups within a given storage sync service.</span></span> <span data-ttu-id="02768-110">Sie kann auch verwendet werden, um die Attribute jeder Synchronisierungsgruppe aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="02768-110">It can be used to also list the attributes of each sync group.</span></span>

## <span data-ttu-id="02768-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02768-111">EXAMPLES</span></span>

### <span data-ttu-id="02768-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="02768-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncGroup New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="02768-113">Dieser Befehl ruft alle Synchronisierungsgruppen ab, die im angegebenen Speicher Synchronisierungsdienst enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="02768-113">This command gets all sync groups contained within the specified storage sync service.</span></span> <span data-ttu-id="02768-114">Geben Sie den Namen an, um einen bestimmten Wert zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="02768-114">Specify -Name to return a specific one.</span></span>

## <span data-ttu-id="02768-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="02768-115">PARAMETERS</span></span>

### <span data-ttu-id="02768-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02768-116">-DefaultProfile</span></span>
<span data-ttu-id="02768-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="02768-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02768-118">-Name</span><span class="sxs-lookup"><span data-stu-id="02768-118">-Name</span></span>
<span data-ttu-id="02768-119">Der Name des SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="02768-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="02768-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="02768-120">-ParentObject</span></span>
<span data-ttu-id="02768-121">StorageSyncService-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="02768-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="02768-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="02768-122">-ParentResourceId</span></span>
<span data-ttu-id="02768-123">StorageSyncService-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="02768-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="02768-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02768-124">-ResourceGroupName</span></span>
<span data-ttu-id="02768-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="02768-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="02768-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="02768-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="02768-127">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="02768-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="02768-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02768-128">CommonParameters</span></span>
<span data-ttu-id="02768-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02768-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02768-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02768-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02768-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="02768-131">INPUTS</span></span>

### <span data-ttu-id="02768-132">System. String</span><span class="sxs-lookup"><span data-stu-id="02768-132">System.String</span></span>

### <span data-ttu-id="02768-133">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="02768-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="02768-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="02768-134">OUTPUTS</span></span>

### <span data-ttu-id="02768-135">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="02768-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="02768-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="02768-136">NOTES</span></span>

## <span data-ttu-id="02768-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="02768-137">RELATED LINKS</span></span>
