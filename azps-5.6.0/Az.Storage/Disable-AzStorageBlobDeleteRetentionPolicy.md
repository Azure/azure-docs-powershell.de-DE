---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/disable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: f4ffd20a835a8357972c9f8b9209d505fd311c1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929363"
---
# <span data-ttu-id="bcec6-101">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bcec6-101">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="bcec6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcec6-102">SYNOPSIS</span></span>
<span data-ttu-id="bcec6-103">Deaktivieren Sie die Löschaufbewahrungsrichtlinie für den Azure Storage Blob-Dienst.</span><span class="sxs-lookup"><span data-stu-id="bcec6-103">Disable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="bcec6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bcec6-104">SYNTAX</span></span>

### <span data-ttu-id="bcec6-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="bcec6-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcec6-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="bcec6-106">AccountObject</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcec6-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="bcec6-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcec6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bcec6-108">DESCRIPTION</span></span>
<span data-ttu-id="bcec6-109">Das **Cmdlet Disable-AzStorageBlobDeleteRetentionPolicy** deaktiviert die Löschaufbewahrungsrichtlinie für den Azure Storage Blob-Dienst.</span><span class="sxs-lookup"><span data-stu-id="bcec6-109">The **Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="bcec6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bcec6-110">EXAMPLES</span></span>

### <span data-ttu-id="bcec6-111">Beispiel 1: Deaktivieren der Löschaufbewahrungsrichtlinie für den Blobdienst</span><span class="sxs-lookup"><span data-stu-id="bcec6-111">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru

Enabled Days
------- ----
  False
```

<span data-ttu-id="bcec6-112">Mit diesem Befehl wird die Löschaufbewahrungsrichtlinie für den Blobdienst deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="bcec6-112">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="bcec6-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bcec6-113">PARAMETERS</span></span>

### <span data-ttu-id="bcec6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcec6-114">-DefaultProfile</span></span>
<span data-ttu-id="bcec6-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bcec6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcec6-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bcec6-116">-PassThru</span></span>
<span data-ttu-id="bcec6-117">Anzeigen von ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="bcec6-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="bcec6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcec6-118">-ResourceGroupName</span></span>
<span data-ttu-id="bcec6-119">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="bcec6-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="bcec6-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcec6-120">-ResourceId</span></span>
<span data-ttu-id="bcec6-121">Geben Sie eine Ressourcen-ID des Speicherkontos oder eine Blob-Diensteigenschaften-Ressourcen-ID ein.</span><span class="sxs-lookup"><span data-stu-id="bcec6-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="bcec6-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="bcec6-122">-StorageAccount</span></span>
<span data-ttu-id="bcec6-123">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="bcec6-123">Storage account object</span></span>

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

### <span data-ttu-id="bcec6-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bcec6-124">-StorageAccountName</span></span>
<span data-ttu-id="bcec6-125">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="bcec6-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="bcec6-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bcec6-126">-Confirm</span></span>
<span data-ttu-id="bcec6-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bcec6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcec6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcec6-128">-WhatIf</span></span>
<span data-ttu-id="bcec6-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bcec6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcec6-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bcec6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcec6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcec6-131">CommonParameters</span></span>
<span data-ttu-id="bcec6-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcec6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcec6-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcec6-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcec6-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bcec6-134">INPUTS</span></span>

### <span data-ttu-id="bcec6-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bcec6-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="bcec6-136">System.String</span><span class="sxs-lookup"><span data-stu-id="bcec6-136">System.String</span></span>

## <span data-ttu-id="bcec6-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bcec6-137">OUTPUTS</span></span>

### <span data-ttu-id="bcec6-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bcec6-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="bcec6-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bcec6-139">NOTES</span></span>

## <span data-ttu-id="bcec6-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bcec6-140">RELATED LINKS</span></span>
