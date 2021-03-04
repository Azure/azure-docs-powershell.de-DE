---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: 3aa6c569eb7f67b6021f7f40059cc9e528355a51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929176"
---
# <span data-ttu-id="dd8a1-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="dd8a1-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="dd8a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd8a1-102">SYNOPSIS</span></span>
<span data-ttu-id="dd8a1-103">Mit diesem Befehl werden alle Speichersynchronisierungsdienste in einem bestimmten Bereich der Abonnement-/Ressourcengruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd8a1-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="dd8a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd8a1-104">SYNTAX</span></span>

### <span data-ttu-id="dd8a1-105">ParentStringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="dd8a1-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd8a1-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd8a1-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd8a1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd8a1-107">DESCRIPTION</span></span>
<span data-ttu-id="dd8a1-108">Mit diesem Befehl werden alle Speichersynchronisierungsdienste in einem bestimmten Bereich der Abonnement-/Ressourcengruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd8a1-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="dd8a1-109">Es kann auch verwendet werden, um die Attribute der einzelnen Speichersynchronisierungsdienst auflisten.</span><span class="sxs-lookup"><span data-stu-id="dd8a1-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="dd8a1-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dd8a1-110">EXAMPLES</span></span>

### <span data-ttu-id="dd8a1-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dd8a1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="dd8a1-112">Mit diesem Befehl werden alle Speichersynchronisierungsdienstressourcen innerhalb einer bestimmten Ressourcengruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd8a1-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="dd8a1-113">Es kann auch verwendet werden, um die Attribute der einzelnen Speichersynchronisierungsdienst auflisten.</span><span class="sxs-lookup"><span data-stu-id="dd8a1-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="dd8a1-114">Geben Sie -StorageSyncServiceName an, um einen bestimmten Namen zurücksennen.</span><span class="sxs-lookup"><span data-stu-id="dd8a1-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="dd8a1-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dd8a1-115">PARAMETERS</span></span>

### <span data-ttu-id="dd8a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd8a1-116">-DefaultProfile</span></span>
<span data-ttu-id="dd8a1-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd8a1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd8a1-118">-Name</span><span class="sxs-lookup"><span data-stu-id="dd8a1-118">-Name</span></span>
<span data-ttu-id="dd8a1-119">Name des Speichersynchronisierungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="dd8a1-119">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="dd8a1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd8a1-120">-ResourceGroupName</span></span>
<span data-ttu-id="dd8a1-121">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="dd8a1-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="dd8a1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd8a1-122">CommonParameters</span></span>
<span data-ttu-id="dd8a1-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd8a1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd8a1-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd8a1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd8a1-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dd8a1-125">INPUTS</span></span>

### <span data-ttu-id="dd8a1-126">System.String</span><span class="sxs-lookup"><span data-stu-id="dd8a1-126">System.String</span></span>

## <span data-ttu-id="dd8a1-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dd8a1-127">OUTPUTS</span></span>

### <span data-ttu-id="dd8a1-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="dd8a1-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="dd8a1-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="dd8a1-129">NOTES</span></span>

## <span data-ttu-id="dd8a1-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="dd8a1-130">RELATED LINKS</span></span>
