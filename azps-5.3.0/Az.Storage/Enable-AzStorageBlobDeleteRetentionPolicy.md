---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: ebb379217f9fd040aa3dcbd6c614a45dbdbba8c4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374141"
---
# <span data-ttu-id="6963f-101">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6963f-101">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="6963f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6963f-102">SYNOPSIS</span></span>
<span data-ttu-id="6963f-103">Aktivieren Sie die Löschaufbewahrungsrichtlinie für den Azure Storage Blob-Dienst.</span><span class="sxs-lookup"><span data-stu-id="6963f-103">Enable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="6963f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6963f-104">SYNTAX</span></span>

### <span data-ttu-id="6963f-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6963f-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RetentionDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6963f-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="6963f-106">AccountObject</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6963f-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="6963f-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6963f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6963f-108">DESCRIPTION</span></span>
<span data-ttu-id="6963f-109">Das **Cmdlet "Enable-AzStorageBlobDeleteRetentionPolicy"** aktiviert die Löschaufbewahrungsrichtlinie für den Azure Storage Blob-Dienst.</span><span class="sxs-lookup"><span data-stu-id="6963f-109">The **Enable-AzStorageBlobDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="6963f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6963f-110">EXAMPLES</span></span>

### <span data-ttu-id="6963f-111">Beispiel 1: Aktivieren der Löschaufbewahrungsrichtlinie für den Blob-Dienst</span><span class="sxs-lookup"><span data-stu-id="6963f-111">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru -RetentionDays 4

Enabled Days
------- ----
   True    4
```

<span data-ttu-id="6963f-112">Dieser Befehl aktiviert die Löschaufbewahrungsrichtlinie für den Blob-Dienst und setzt gelöschte Blob-Aufbewahrungstage auf 4.</span><span class="sxs-lookup"><span data-stu-id="6963f-112">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 4.</span></span>

## <span data-ttu-id="6963f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6963f-113">PARAMETERS</span></span>

### <span data-ttu-id="6963f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6963f-114">-DefaultProfile</span></span>
<span data-ttu-id="6963f-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6963f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6963f-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6963f-116">-PassThru</span></span>
<span data-ttu-id="6963f-117">Anzeigen von ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="6963f-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="6963f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6963f-118">-ResourceGroupName</span></span>
<span data-ttu-id="6963f-119">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="6963f-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="6963f-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6963f-120">-ResourceId</span></span>
<span data-ttu-id="6963f-121">Geben Sie die Ressourcen-ID eines Speicherkontos oder eine Blob-Diensteigenschaften-Ressourcen-ID ein.</span><span class="sxs-lookup"><span data-stu-id="6963f-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="6963f-122">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="6963f-122">-RetentionDays</span></span>
<span data-ttu-id="6963f-123">Legt die Anzahl der Aufbewahrungstage für "DeleteRetentionPolicy" fest.</span><span class="sxs-lookup"><span data-stu-id="6963f-123">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

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

### <span data-ttu-id="6963f-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6963f-124">-StorageAccount</span></span>
<span data-ttu-id="6963f-125">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="6963f-125">Storage account object</span></span>

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

### <span data-ttu-id="6963f-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6963f-126">-StorageAccountName</span></span>
<span data-ttu-id="6963f-127">Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="6963f-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="6963f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6963f-128">-Confirm</span></span>
<span data-ttu-id="6963f-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6963f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6963f-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6963f-130">-WhatIf</span></span>
<span data-ttu-id="6963f-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6963f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6963f-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6963f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6963f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6963f-133">CommonParameters</span></span>
<span data-ttu-id="6963f-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6963f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6963f-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6963f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6963f-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6963f-136">INPUTS</span></span>

### <span data-ttu-id="6963f-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6963f-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="6963f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6963f-138">System.String</span></span>

## <span data-ttu-id="6963f-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6963f-139">OUTPUTS</span></span>

### <span data-ttu-id="6963f-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="6963f-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="6963f-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6963f-141">NOTES</span></span>

## <span data-ttu-id="6963f-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6963f-142">RELATED LINKS</span></span>
