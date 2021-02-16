---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
ms.openlocfilehash: ebee7b772fc4da3ef14d2273b79b089d57fa317f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150337"
---
# <span data-ttu-id="0f713-101">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="0f713-101">Get-AzStorageSyncServer</span></span>

## <span data-ttu-id="0f713-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f713-102">SYNOPSIS</span></span>
<span data-ttu-id="0f713-103">Dieser Befehl listet alle Server auf, die für einen bestimmten Speichersynchronisierungsdienst registriert sind.</span><span class="sxs-lookup"><span data-stu-id="0f713-103">This command lists all servers registered to a given storage sync service.</span></span>

## <span data-ttu-id="0f713-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f713-104">SYNTAX</span></span>

### <span data-ttu-id="0f713-105">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0f713-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f713-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f713-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f713-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f713-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentResourceId] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f713-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f713-108">DESCRIPTION</span></span>
<span data-ttu-id="0f713-109">Dieser Befehl listet alle Server auf, die für einen bestimmten Speichersynchronisierungsdienst registriert sind.</span><span class="sxs-lookup"><span data-stu-id="0f713-109">This command lists all servers registered to a given storage sync service.</span></span> <span data-ttu-id="0f713-110">Sie kann auch verwendet werden, um die Attribute der einzelnen registrierten Server auflisten.</span><span class="sxs-lookup"><span data-stu-id="0f713-110">It can be used to also list the attributes of each registered server.</span></span>

## <span data-ttu-id="0f713-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0f713-111">EXAMPLES</span></span>

### <span data-ttu-id="0f713-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0f713-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="0f713-113">Mit diesem Befehl werden alle Server für einen bestimmten Speichersynchronisierungsdienst registriert.</span><span class="sxs-lookup"><span data-stu-id="0f713-113">This command gets all servers registered to a specific storage sync service.</span></span>

## <span data-ttu-id="0f713-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f713-114">PARAMETERS</span></span>

### <span data-ttu-id="0f713-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f713-115">-DefaultProfile</span></span>
<span data-ttu-id="0f713-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0f713-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f713-117">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0f713-117">-ParentObject</span></span>
<span data-ttu-id="0f713-118">StorageSyncService-Objekt, das normalerweise über den Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="0f713-118">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="0f713-119">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0f713-119">-ParentResourceId</span></span>
<span data-ttu-id="0f713-120">StorageSyncService-Objekt, das normalerweise über den Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="0f713-120">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="0f713-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f713-121">-ResourceGroupName</span></span>
<span data-ttu-id="0f713-122">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="0f713-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="0f713-123">-ServerId</span><span class="sxs-lookup"><span data-stu-id="0f713-123">-ServerId</span></span>
<span data-ttu-id="0f713-124">Name des RegisteredServer.</span><span class="sxs-lookup"><span data-stu-id="0f713-124">Name of the RegisteredServer.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: RegisteredServerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f713-125">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="0f713-125">-StorageSyncServiceName</span></span>
<span data-ttu-id="0f713-126">Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="0f713-126">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="0f713-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f713-127">CommonParameters</span></span>
<span data-ttu-id="0f713-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f713-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f713-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f713-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f713-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0f713-130">INPUTS</span></span>

### <span data-ttu-id="0f713-131">System.String</span><span class="sxs-lookup"><span data-stu-id="0f713-131">System.String</span></span>

### <span data-ttu-id="0f713-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="0f713-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="0f713-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="0f713-133">System.Guid</span></span>

## <span data-ttu-id="0f713-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0f713-134">OUTPUTS</span></span>

### <span data-ttu-id="0f713-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="0f713-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="0f713-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0f713-136">NOTES</span></span>

## <span data-ttu-id="0f713-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0f713-137">RELATED LINKS</span></span>
