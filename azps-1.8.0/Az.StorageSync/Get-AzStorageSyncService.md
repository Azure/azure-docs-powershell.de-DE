---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: c724527b380e0004d30e0790024634bcc6ce550d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658707"
---
# <span data-ttu-id="ec33f-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="ec33f-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="ec33f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ec33f-102">SYNOPSIS</span></span>
<span data-ttu-id="ec33f-103">Dieser Befehl listet alle Speicher Synchronisierungsdienste in einem bestimmten Bereich des Abonnements/der Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="ec33f-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="ec33f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec33f-104">SYNTAX</span></span>

### <span data-ttu-id="ec33f-105">ParentStringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ec33f-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec33f-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec33f-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec33f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec33f-107">DESCRIPTION</span></span>
<span data-ttu-id="ec33f-108">Dieser Befehl listet alle Speicher Synchronisierungsdienste in einem bestimmten Bereich des Abonnements/der Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="ec33f-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="ec33f-109">Sie kann auch verwendet werden, um die Attribute der einzelnen Speicher Synchronisierungsdienste aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="ec33f-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="ec33f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ec33f-110">EXAMPLES</span></span>

### <span data-ttu-id="ec33f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ec33f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="ec33f-112">Dieser Befehl listet alle Speicher Synchronisierungsdienst Ressourcen innerhalb einer bestimmten Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="ec33f-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="ec33f-113">Sie kann auch verwendet werden, um die Attribute der einzelnen Speicher Synchronisierungsdienste aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="ec33f-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="ec33f-114">Geben Sie-StorageSyncServiceName ein, um eine bestimmte zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="ec33f-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="ec33f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec33f-115">PARAMETERS</span></span>

### <span data-ttu-id="ec33f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec33f-116">-DefaultProfile</span></span>
<span data-ttu-id="ec33f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ec33f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec33f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ec33f-118">-Name</span></span>
<span data-ttu-id="ec33f-119">Der Name des Speicher Synchronisierungs Diensts.</span><span class="sxs-lookup"><span data-stu-id="ec33f-119">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="ec33f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec33f-120">-ResourceGroupName</span></span>
<span data-ttu-id="ec33f-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ec33f-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="ec33f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec33f-122">CommonParameters</span></span>
<span data-ttu-id="ec33f-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec33f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec33f-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec33f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec33f-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ec33f-125">INPUTS</span></span>

### <span data-ttu-id="ec33f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ec33f-126">System.String</span></span>

## <span data-ttu-id="ec33f-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ec33f-127">OUTPUTS</span></span>

### <span data-ttu-id="ec33f-128">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="ec33f-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="ec33f-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="ec33f-129">NOTES</span></span>

## <span data-ttu-id="ec33f-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ec33f-130">RELATED LINKS</span></span>
