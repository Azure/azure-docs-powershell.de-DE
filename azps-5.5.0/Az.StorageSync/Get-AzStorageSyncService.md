---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: ec446a92c96bd92d7a4af5610f00ff76dcd50b50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157908"
---
# <span data-ttu-id="1438d-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="1438d-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="1438d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1438d-102">SYNOPSIS</span></span>
<span data-ttu-id="1438d-103">Mit diesem Befehl werden alle Speichersynchronisierungsdienste innerhalb eines bestimmten Bereichs der Abonnement-/Ressourcengruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="1438d-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="1438d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1438d-104">SYNTAX</span></span>

### <span data-ttu-id="1438d-105">ParentStringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1438d-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1438d-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="1438d-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1438d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1438d-107">DESCRIPTION</span></span>
<span data-ttu-id="1438d-108">Mit diesem Befehl werden alle Speichersynchronisierungsdienste innerhalb eines bestimmten Bereichs der Abonnement-/Ressourcengruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="1438d-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="1438d-109">Sie kann auch verwendet werden, um die Attribute der einzelnen Speichersynchronisierungsdienst auflisten.</span><span class="sxs-lookup"><span data-stu-id="1438d-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="1438d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1438d-110">EXAMPLES</span></span>

### <span data-ttu-id="1438d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1438d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="1438d-112">Dieser Befehl listet alle Speichersynchronisierungsdienstressourcen innerhalb einer bestimmten Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="1438d-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="1438d-113">Sie kann auch verwendet werden, um die Attribute der einzelnen Speichersynchronisierungsdienst auflisten.</span><span class="sxs-lookup"><span data-stu-id="1438d-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="1438d-114">Geben Sie "-StorageSyncServiceName" an, um einen bestimmten Wert zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="1438d-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="1438d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1438d-115">PARAMETERS</span></span>

### <span data-ttu-id="1438d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1438d-116">-DefaultProfile</span></span>
<span data-ttu-id="1438d-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1438d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1438d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1438d-118">-Name</span></span>
<span data-ttu-id="1438d-119">Name des Speichersynchronisierungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="1438d-119">Name of the storage sync service.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: StorageSyncServiceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1438d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1438d-120">-ResourceGroupName</span></span>
<span data-ttu-id="1438d-121">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="1438d-121">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="1438d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1438d-122">CommonParameters</span></span>
<span data-ttu-id="1438d-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1438d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1438d-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1438d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1438d-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1438d-125">INPUTS</span></span>

### <span data-ttu-id="1438d-126">System.String</span><span class="sxs-lookup"><span data-stu-id="1438d-126">System.String</span></span>

## <span data-ttu-id="1438d-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1438d-127">OUTPUTS</span></span>

### <span data-ttu-id="1438d-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="1438d-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="1438d-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1438d-129">NOTES</span></span>

## <span data-ttu-id="1438d-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1438d-130">RELATED LINKS</span></span>
