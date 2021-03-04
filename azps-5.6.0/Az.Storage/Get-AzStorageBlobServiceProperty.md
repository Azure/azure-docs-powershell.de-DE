---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 72e26a8fbb059db78fcdfa56721bed94e388ef55
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944585"
---
# <span data-ttu-id="742be-101">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="742be-101">Get-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="742be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="742be-102">SYNOPSIS</span></span>
<span data-ttu-id="742be-103">Ruft Diensteigenschaften für Azure Storage Blob Services ab.</span><span class="sxs-lookup"><span data-stu-id="742be-103">Gets service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="742be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="742be-104">SYNTAX</span></span>

### <span data-ttu-id="742be-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="742be-105">AccountName (Default)</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="742be-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="742be-106">AccountObject</span></span>
```
Get-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="742be-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="742be-107">BlobServicePropertiesResourceId</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="742be-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="742be-108">DESCRIPTION</span></span>
<span data-ttu-id="742be-109">Das **Get-AzStorageBlobServiceProperty-Cmdlet** ruft die Diensteigenschaften für Azure Storage Blob-Dienste ab.</span><span class="sxs-lookup"><span data-stu-id="742be-109">The **Get-AzStorageBlobServiceProperty** cmdlet gets the service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="742be-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="742be-110">EXAMPLES</span></span>

### <span data-ttu-id="742be-111">Beispiel 1: Azure Storage Blob Services-Eigenschaft eines angegebenen Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="742be-111">Example 1: Get  Azure Storage Blob services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : True
IsVersioningEnabled           : True
```

<span data-ttu-id="742be-112">Dieser Befehl ruft die Blob services-Eigenschaft eines angegebenen Speicherkontos ab.</span><span class="sxs-lookup"><span data-stu-id="742be-112">This command gets the Blob services property of a specified Storage Account.</span></span>

## <span data-ttu-id="742be-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="742be-113">PARAMETERS</span></span>

### <span data-ttu-id="742be-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="742be-114">-DefaultProfile</span></span>
<span data-ttu-id="742be-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="742be-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="742be-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="742be-116">-ResourceGroupName</span></span>
<span data-ttu-id="742be-117">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="742be-117">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="742be-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="742be-118">-ResourceId</span></span>
<span data-ttu-id="742be-119">Blob Service Properties Resource Id.</span><span class="sxs-lookup"><span data-stu-id="742be-119">Blob Service Properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="742be-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="742be-120">-StorageAccount</span></span>
<span data-ttu-id="742be-121">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="742be-121">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="742be-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="742be-122">-StorageAccountName</span></span>
<span data-ttu-id="742be-123">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="742be-123">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="742be-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="742be-124">CommonParameters</span></span>
<span data-ttu-id="742be-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="742be-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="742be-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="742be-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="742be-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="742be-127">INPUTS</span></span>

### <span data-ttu-id="742be-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="742be-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="742be-129">System.String</span><span class="sxs-lookup"><span data-stu-id="742be-129">System.String</span></span>

## <span data-ttu-id="742be-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="742be-130">OUTPUTS</span></span>

### <span data-ttu-id="742be-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="742be-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="742be-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="742be-132">NOTES</span></span>

## <span data-ttu-id="742be-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="742be-133">RELATED LINKS</span></span>
