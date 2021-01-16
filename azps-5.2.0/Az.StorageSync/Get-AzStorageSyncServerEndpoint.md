---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 35a3e8c3eecfe8e710addde0eb2080aa20333f0b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366735"
---
# <span data-ttu-id="03aab-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="03aab-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="03aab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03aab-102">SYNOPSIS</span></span>
<span data-ttu-id="03aab-103">Dieser Befehl listet alle Serverendpunkte innerhalb einer bestimmten Synchronisierungsgruppe auf.</span><span class="sxs-lookup"><span data-stu-id="03aab-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="03aab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03aab-104">SYNTAX</span></span>

### <span data-ttu-id="03aab-105">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="03aab-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03aab-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03aab-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03aab-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="03aab-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03aab-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03aab-108">DESCRIPTION</span></span>
<span data-ttu-id="03aab-109">Dieser Befehl listet alle Serverendpunkte innerhalb einer bestimmten Synchronisierungsgruppe auf.</span><span class="sxs-lookup"><span data-stu-id="03aab-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="03aab-110">Sie kann auch verwendet werden, um die Attribute der einzelnen Serverendpunkte auflisten.</span><span class="sxs-lookup"><span data-stu-id="03aab-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="03aab-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="03aab-111">EXAMPLES</span></span>

### <span data-ttu-id="03aab-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="03aab-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="03aab-113">Dieser Befehl ruft alle Serverendpunkte ab, die in der angegebenen Synchronisierungsgruppe enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="03aab-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="03aab-114">Geben Sie "-ServerEndpointName" an, um einen bestimmten Wert zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="03aab-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="03aab-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03aab-115">PARAMETERS</span></span>

### <span data-ttu-id="03aab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03aab-116">-DefaultProfile</span></span>
<span data-ttu-id="03aab-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="03aab-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03aab-118">-Name</span><span class="sxs-lookup"><span data-stu-id="03aab-118">-Name</span></span>
<span data-ttu-id="03aab-119">Name des Serverendpunkts.</span><span class="sxs-lookup"><span data-stu-id="03aab-119">Name of the server endpoint.</span></span>

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

### <span data-ttu-id="03aab-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="03aab-120">-ParentObject</span></span>
<span data-ttu-id="03aab-121">StorageSyncService-Objekt, das normalerweise über den Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="03aab-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="03aab-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="03aab-122">-ParentResourceId</span></span>
<span data-ttu-id="03aab-123">StorageSyncService-Objekt, das normalerweise über den Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="03aab-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="03aab-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03aab-124">-ResourceGroupName</span></span>
<span data-ttu-id="03aab-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="03aab-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="03aab-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="03aab-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="03aab-127">Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="03aab-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="03aab-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="03aab-128">-SyncGroupName</span></span>
<span data-ttu-id="03aab-129">Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="03aab-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="03aab-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03aab-130">CommonParameters</span></span>
<span data-ttu-id="03aab-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03aab-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03aab-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03aab-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03aab-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="03aab-133">INPUTS</span></span>

### <span data-ttu-id="03aab-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="03aab-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="03aab-135">System.String</span><span class="sxs-lookup"><span data-stu-id="03aab-135">System.String</span></span>

## <span data-ttu-id="03aab-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="03aab-136">OUTPUTS</span></span>

### <span data-ttu-id="03aab-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="03aab-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="03aab-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="03aab-138">NOTES</span></span>

## <span data-ttu-id="03aab-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="03aab-139">RELATED LINKS</span></span>
