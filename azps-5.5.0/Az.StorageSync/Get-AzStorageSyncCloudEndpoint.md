---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 076a1393365e93a8008f15137d078a49491d81f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150353"
---
# <span data-ttu-id="2c535-101">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c535-101">Get-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="2c535-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c535-102">SYNOPSIS</span></span>
<span data-ttu-id="2c535-103">Mit diesem Befehl werden alle Cloudendpunkte innerhalb einer bestimmten Synchronisierungsgruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2c535-103">This command lists all cloud endpoints within a given sync group.</span></span>

## <span data-ttu-id="2c535-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c535-104">SYNTAX</span></span>

### <span data-ttu-id="2c535-105">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2c535-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c535-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c535-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c535-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c535-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c535-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2c535-108">DESCRIPTION</span></span>
<span data-ttu-id="2c535-109">Mit diesem Befehl werden alle Cloudendpunkte innerhalb einer bestimmten Synchronisierungsgruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2c535-109">This command lists all cloud endpoints within a given sync group.</span></span> <span data-ttu-id="2c535-110">Sie kann auch verwendet werden, um die Attribute der einzelnen Cloudendpunkte auflisten.</span><span class="sxs-lookup"><span data-stu-id="2c535-110">It can be used to also list the attributes of each cloud endpoint.</span></span>

## <span data-ttu-id="2c535-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2c535-111">EXAMPLES</span></span>

### <span data-ttu-id="2c535-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2c535-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="2c535-113">Dieser Befehl ruft alle Cloudendpunkte ab, die in der angegebenen Synchronisierungsgruppe enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="2c535-113">This command gets all cloud endpoints contained within the specified sync group.</span></span> <span data-ttu-id="2c535-114">Geben Sie "-CloudEndpointName" an, um einen bestimmten Namen zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="2c535-114">Specify -CloudEndpointName to return a specific one.</span></span>

## <span data-ttu-id="2c535-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c535-115">PARAMETERS</span></span>

### <span data-ttu-id="2c535-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c535-116">-DefaultProfile</span></span>
<span data-ttu-id="2c535-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2c535-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c535-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2c535-118">-Name</span></span>
<span data-ttu-id="2c535-119">Der Name von CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="2c535-119">Name of the CloudEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudEndpointName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c535-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2c535-120">-ParentObject</span></span>
<span data-ttu-id="2c535-121">StorageSyncService-Objekt, das normalerweise über den Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2c535-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="2c535-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2c535-122">-ParentResourceId</span></span>
<span data-ttu-id="2c535-123">StorageSyncService-Objekt, das normalerweise über den Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2c535-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="2c535-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c535-124">-ResourceGroupName</span></span>
<span data-ttu-id="2c535-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="2c535-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="2c535-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="2c535-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="2c535-127">Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="2c535-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="2c535-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="2c535-128">-SyncGroupName</span></span>
<span data-ttu-id="2c535-129">Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2c535-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="2c535-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c535-130">CommonParameters</span></span>
<span data-ttu-id="2c535-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c535-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c535-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c535-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c535-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2c535-133">INPUTS</span></span>

### <span data-ttu-id="2c535-134">System.String</span><span class="sxs-lookup"><span data-stu-id="2c535-134">System.String</span></span>

### <span data-ttu-id="2c535-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2c535-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="2c535-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2c535-136">OUTPUTS</span></span>

### <span data-ttu-id="2c535-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c535-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="2c535-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2c535-138">NOTES</span></span>

## <span data-ttu-id="2c535-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2c535-139">RELATED LINKS</span></span>
