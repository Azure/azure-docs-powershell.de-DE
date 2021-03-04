---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/enable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: 9a4afaa1a67d9f1f9bffa0fdf6c7b40c7cf72b13
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929304"
---
# <span data-ttu-id="21733-101">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="21733-101">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="21733-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21733-102">SYNOPSIS</span></span>
<span data-ttu-id="21733-103">Aktivieren Sie die Aufbewahrungsrichtlinie zum Löschen für den Azure Storage Blob-Dienst.</span><span class="sxs-lookup"><span data-stu-id="21733-103">Enable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="21733-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21733-104">SYNTAX</span></span>

### <span data-ttu-id="21733-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="21733-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RetentionDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21733-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="21733-106">AccountObject</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21733-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="21733-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21733-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21733-108">DESCRIPTION</span></span>
<span data-ttu-id="21733-109">Das **Cmdlet Enable-AzStorageBlobDeleteRetentionPolicy** aktiviert die Löschaufbewahrungsrichtlinie für den Azure Storage Blob-Dienst.</span><span class="sxs-lookup"><span data-stu-id="21733-109">The **Enable-AzStorageBlobDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="21733-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="21733-110">EXAMPLES</span></span>

### <span data-ttu-id="21733-111">Beispiel 1: Aktivieren der Löschaufbewahrungsrichtlinie für den Blobdienst</span><span class="sxs-lookup"><span data-stu-id="21733-111">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru -RetentionDays 4

Enabled Days
------- ----
   True    4
```

<span data-ttu-id="21733-112">Dieser Befehl aktiviert die Löschaufbewahrungsrichtlinie für den Blobdienst und setzt gelöschte Blobaufbewahrungstage auf 4.</span><span class="sxs-lookup"><span data-stu-id="21733-112">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 4.</span></span>

## <span data-ttu-id="21733-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="21733-113">PARAMETERS</span></span>

### <span data-ttu-id="21733-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21733-114">-DefaultProfile</span></span>
<span data-ttu-id="21733-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="21733-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21733-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21733-116">-PassThru</span></span>
<span data-ttu-id="21733-117">Anzeigen von ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="21733-117">Display ServiceProperties</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21733-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21733-118">-ResourceGroupName</span></span>
<span data-ttu-id="21733-119">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="21733-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="21733-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21733-120">-ResourceId</span></span>
<span data-ttu-id="21733-121">Geben Sie eine Ressourcen-ID des Speicherkontos oder eine Blob-Diensteigenschaften-Ressourcen-ID ein.</span><span class="sxs-lookup"><span data-stu-id="21733-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="21733-122">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="21733-122">-RetentionDays</span></span>
<span data-ttu-id="21733-123">Legt die Anzahl der Aufbewahrungstage für deleteRetentionPolicy fest.</span><span class="sxs-lookup"><span data-stu-id="21733-123">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21733-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="21733-124">-StorageAccount</span></span>
<span data-ttu-id="21733-125">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="21733-125">Storage account object</span></span>

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

### <span data-ttu-id="21733-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="21733-126">-StorageAccountName</span></span>
<span data-ttu-id="21733-127">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="21733-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="21733-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="21733-128">-Confirm</span></span>
<span data-ttu-id="21733-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="21733-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21733-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21733-130">-WhatIf</span></span>
<span data-ttu-id="21733-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21733-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21733-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21733-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21733-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21733-133">CommonParameters</span></span>
<span data-ttu-id="21733-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21733-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21733-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21733-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21733-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="21733-136">INPUTS</span></span>

### <span data-ttu-id="21733-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="21733-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="21733-138">System.String</span><span class="sxs-lookup"><span data-stu-id="21733-138">System.String</span></span>

## <span data-ttu-id="21733-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="21733-139">OUTPUTS</span></span>

### <span data-ttu-id="21733-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="21733-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="21733-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="21733-141">NOTES</span></span>

## <span data-ttu-id="21733-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="21733-142">RELATED LINKS</span></span>
