---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 35a3e8c3eecfe8e710addde0eb2080aa20333f0b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845783"
---
# <span data-ttu-id="43fdf-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="43fdf-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="43fdf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43fdf-102">SYNOPSIS</span></span>
<span data-ttu-id="43fdf-103">Dieser Befehl listet alle Server Endpunkte innerhalb einer bestimmten Synchronisierungsgruppe auf.</span><span class="sxs-lookup"><span data-stu-id="43fdf-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="43fdf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43fdf-104">SYNTAX</span></span>

### <span data-ttu-id="43fdf-105">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="43fdf-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43fdf-106">Objectparameterset</span><span class="sxs-lookup"><span data-stu-id="43fdf-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43fdf-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="43fdf-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43fdf-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43fdf-108">DESCRIPTION</span></span>
<span data-ttu-id="43fdf-109">Dieser Befehl listet alle Server Endpunkte innerhalb einer bestimmten Synchronisierungsgruppe auf.</span><span class="sxs-lookup"><span data-stu-id="43fdf-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="43fdf-110">Sie kann auch verwendet werden, um die Attribute der einzelnen Server Endpunkte aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="43fdf-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="43fdf-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43fdf-111">EXAMPLES</span></span>

### <span data-ttu-id="43fdf-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="43fdf-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="43fdf-113">Dieser Befehl ruft alle Server Endpunkte ab, die in der angegebenen Synchronisierungsgruppe enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="43fdf-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="43fdf-114">Geben Sie-ServerEndpointName ein, um eine bestimmte zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="43fdf-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="43fdf-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="43fdf-115">PARAMETERS</span></span>

### <span data-ttu-id="43fdf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43fdf-116">-DefaultProfile</span></span>
<span data-ttu-id="43fdf-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="43fdf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43fdf-118">-Name</span><span class="sxs-lookup"><span data-stu-id="43fdf-118">-Name</span></span>
<span data-ttu-id="43fdf-119">Der Name des Server Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="43fdf-119">Name of the server endpoint.</span></span>

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

### <span data-ttu-id="43fdf-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="43fdf-120">-ParentObject</span></span>
<span data-ttu-id="43fdf-121">StorageSyncService-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="43fdf-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="43fdf-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="43fdf-122">-ParentResourceId</span></span>
<span data-ttu-id="43fdf-123">StorageSyncService-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="43fdf-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="43fdf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43fdf-124">-ResourceGroupName</span></span>
<span data-ttu-id="43fdf-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="43fdf-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="43fdf-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="43fdf-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="43fdf-127">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="43fdf-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="43fdf-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="43fdf-128">-SyncGroupName</span></span>
<span data-ttu-id="43fdf-129">Der Name des SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="43fdf-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="43fdf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43fdf-130">CommonParameters</span></span>
<span data-ttu-id="43fdf-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43fdf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43fdf-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43fdf-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43fdf-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43fdf-133">INPUTS</span></span>

### <span data-ttu-id="43fdf-134">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="43fdf-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="43fdf-135">System. String</span><span class="sxs-lookup"><span data-stu-id="43fdf-135">System.String</span></span>

## <span data-ttu-id="43fdf-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43fdf-136">OUTPUTS</span></span>

### <span data-ttu-id="43fdf-137">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="43fdf-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="43fdf-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="43fdf-138">NOTES</span></span>

## <span data-ttu-id="43fdf-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43fdf-139">RELATED LINKS</span></span>
