---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: ebb379217f9fd040aa3dcbd6c614a45dbdbba8c4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010406"
---
# <span data-ttu-id="f87cd-101">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f87cd-101">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="f87cd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f87cd-102">SYNOPSIS</span></span>
<span data-ttu-id="f87cd-103">Aktivieren Sie die Aufbewahrungsrichtlinie für den Azure Storage-BLOB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="f87cd-103">Enable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="f87cd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f87cd-104">SYNTAX</span></span>

### <span data-ttu-id="f87cd-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="f87cd-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RetentionDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f87cd-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="f87cd-106">AccountObject</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f87cd-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="f87cd-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f87cd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f87cd-108">DESCRIPTION</span></span>
<span data-ttu-id="f87cd-109">Das Cmdlet **enable-AzStorageBlobDeleteRetentionPolicy** aktiviert die Aufbewahrungsrichtlinie für den Azure Storage-BLOB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="f87cd-109">The **Enable-AzStorageBlobDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="f87cd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f87cd-110">EXAMPLES</span></span>

### <span data-ttu-id="f87cd-111">Beispiel 1: Aktivieren der Aufbewahrungsrichtlinie für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="f87cd-111">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru -RetentionDays 4

Enabled Days
------- ----
   True    4
```

<span data-ttu-id="f87cd-112">Mit diesem Befehl können Sie die Aufbewahrungsrichtlinie für den BLOB-Dienst löschen und gelöschte Aufbewahrungstage für BLOB auf 4 festlegen.</span><span class="sxs-lookup"><span data-stu-id="f87cd-112">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 4.</span></span>

## <span data-ttu-id="f87cd-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f87cd-113">PARAMETERS</span></span>

### <span data-ttu-id="f87cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f87cd-114">-DefaultProfile</span></span>
<span data-ttu-id="f87cd-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f87cd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f87cd-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f87cd-116">-PassThru</span></span>
<span data-ttu-id="f87cd-117">ServiceProperties anzeigen</span><span class="sxs-lookup"><span data-stu-id="f87cd-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="f87cd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f87cd-118">-ResourceGroupName</span></span>
<span data-ttu-id="f87cd-119">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f87cd-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="f87cd-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f87cd-120">-ResourceId</span></span>
<span data-ttu-id="f87cd-121">Geben Sie eine Ressourcen-ID des speicherkontos oder eine Ressourcen-ID für BLOB-Diensteigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="f87cd-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="f87cd-122">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="f87cd-122">-RetentionDays</span></span>
<span data-ttu-id="f87cd-123">Legt die Anzahl der Aufbewahrungstage für die DeleteRetentionPolicy fest.</span><span class="sxs-lookup"><span data-stu-id="f87cd-123">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

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

### <span data-ttu-id="f87cd-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f87cd-124">-StorageAccount</span></span>
<span data-ttu-id="f87cd-125">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="f87cd-125">Storage account object</span></span>

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

### <span data-ttu-id="f87cd-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f87cd-126">-StorageAccountName</span></span>
<span data-ttu-id="f87cd-127">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="f87cd-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="f87cd-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f87cd-128">-Confirm</span></span>
<span data-ttu-id="f87cd-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f87cd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f87cd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f87cd-130">-WhatIf</span></span>
<span data-ttu-id="f87cd-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f87cd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f87cd-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f87cd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f87cd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f87cd-133">CommonParameters</span></span>
<span data-ttu-id="f87cd-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f87cd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f87cd-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f87cd-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f87cd-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f87cd-136">INPUTS</span></span>

### <span data-ttu-id="f87cd-137">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f87cd-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="f87cd-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f87cd-138">System.String</span></span>

## <span data-ttu-id="f87cd-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f87cd-139">OUTPUTS</span></span>

### <span data-ttu-id="f87cd-140">Microsoft. Azure. Commands. Management. Storage. Models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="f87cd-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="f87cd-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="f87cd-141">NOTES</span></span>

## <span data-ttu-id="f87cd-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f87cd-142">RELATED LINKS</span></span>
