---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 1f6692067c48cc093e7d74d75c678374aba30f24
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826391"
---
# <span data-ttu-id="4567a-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4567a-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="4567a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4567a-102">SYNOPSIS</span></span>
<span data-ttu-id="4567a-103">Dieser Befehl listet alle Server Endpunkte innerhalb einer bestimmten Synchronisierungsgruppe auf.</span><span class="sxs-lookup"><span data-stu-id="4567a-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="4567a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4567a-104">SYNTAX</span></span>

### <span data-ttu-id="4567a-105">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4567a-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4567a-106">Objectparameterset</span><span class="sxs-lookup"><span data-stu-id="4567a-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4567a-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="4567a-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4567a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4567a-108">DESCRIPTION</span></span>
<span data-ttu-id="4567a-109">Dieser Befehl listet alle Server Endpunkte innerhalb einer bestimmten Synchronisierungsgruppe auf.</span><span class="sxs-lookup"><span data-stu-id="4567a-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="4567a-110">Sie kann auch verwendet werden, um die Attribute der einzelnen Server Endpunkte aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="4567a-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="4567a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4567a-111">EXAMPLES</span></span>

### <span data-ttu-id="4567a-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4567a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="4567a-113">Dieser Befehl ruft alle Server Endpunkte ab, die in der angegebenen Synchronisierungsgruppe enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="4567a-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="4567a-114">Geben Sie-ServerEndpointName ein, um eine bestimmte zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="4567a-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="4567a-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="4567a-115">PARAMETERS</span></span>

### <span data-ttu-id="4567a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4567a-116">-DefaultProfile</span></span>
<span data-ttu-id="4567a-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4567a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4567a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4567a-118">-Name</span></span>
<span data-ttu-id="4567a-119">Der Name des Server Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="4567a-119">Name of the server endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerEndpointName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4567a-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4567a-120">-ParentObject</span></span>
<span data-ttu-id="4567a-121">StorageSyncService-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="4567a-121">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4567a-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4567a-122">-ParentResourceId</span></span>
<span data-ttu-id="4567a-123">StorageSyncService-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="4567a-123">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4567a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4567a-124">-ResourceGroupName</span></span>
<span data-ttu-id="4567a-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4567a-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="4567a-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="4567a-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="4567a-127">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="4567a-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="4567a-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="4567a-128">-SyncGroupName</span></span>
<span data-ttu-id="4567a-129">Der Name des SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="4567a-129">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4567a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4567a-130">CommonParameters</span></span>
<span data-ttu-id="4567a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4567a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4567a-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4567a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4567a-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4567a-133">INPUTS</span></span>

### <span data-ttu-id="4567a-134">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4567a-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="4567a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4567a-135">System.String</span></span>

## <span data-ttu-id="4567a-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4567a-136">OUTPUTS</span></span>

### <span data-ttu-id="4567a-137">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4567a-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="4567a-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="4567a-138">NOTES</span></span>

## <span data-ttu-id="4567a-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4567a-139">RELATED LINKS</span></span>
