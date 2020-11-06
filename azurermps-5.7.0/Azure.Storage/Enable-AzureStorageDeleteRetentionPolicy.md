---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/enable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: f8303a9d87a2bd5312732bd01eb3d42bd1e0a285
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478826"
---
# <span data-ttu-id="30925-101">Enable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="30925-101">Enable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="30925-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="30925-102">SYNOPSIS</span></span>
<span data-ttu-id="30925-103">Aktivieren Sie die Aufbewahrungsrichtlinie für den Azure Storage-BLOB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="30925-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30925-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="30925-104">SYNTAX</span></span>

```
Enable-AzureStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30925-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30925-105">DESCRIPTION</span></span>
<span data-ttu-id="30925-106">Das Cmdlet **enable-AzureStorageDeleteRetentionPolicy** aktiviert die Aufbewahrungsrichtlinie für den Azure Storage-BLOB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="30925-106">The **Enable-AzureStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="30925-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="30925-107">EXAMPLES</span></span>

### <span data-ttu-id="30925-108">Beispiel 1: Aktivieren der Aufbewahrungsrichtlinie für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="30925-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzureStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="30925-109">Mit diesem Befehl können Sie die Aufbewahrungsrichtlinie für den BLOB-Dienst löschen und gelöschte Aufbewahrungstage für BLOB auf 3 festlegen.</span><span class="sxs-lookup"><span data-stu-id="30925-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="30925-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="30925-110">PARAMETERS</span></span>

### <span data-ttu-id="30925-111">-Context</span><span class="sxs-lookup"><span data-stu-id="30925-111">-Context</span></span>
<span data-ttu-id="30925-112">Azure-Speicherkontext Objekt</span><span class="sxs-lookup"><span data-stu-id="30925-112">Azure Storage Context Object</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30925-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30925-113">-PassThru</span></span>
<span data-ttu-id="30925-114">DeleteRetentionPolicyProperties anzeigen</span><span class="sxs-lookup"><span data-stu-id="30925-114">Display DeleteRetentionPolicyProperties</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30925-115">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="30925-115">-RetentionDays</span></span>
<span data-ttu-id="30925-116">Legt die Anzahl der Aufbewahrungstage für die DeleteRetentionPolicy fest.</span><span class="sxs-lookup"><span data-stu-id="30925-116">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30925-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="30925-117">-Confirm</span></span>
<span data-ttu-id="30925-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="30925-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30925-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30925-119">-WhatIf</span></span>
<span data-ttu-id="30925-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="30925-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30925-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="30925-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30925-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30925-122">CommonParameters</span></span>
<span data-ttu-id="30925-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30925-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30925-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30925-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30925-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="30925-125">INPUTS</span></span>

### <span data-ttu-id="30925-126">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="30925-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="30925-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="30925-127">OUTPUTS</span></span>

### <span data-ttu-id="30925-128">Microsoft. WindowsAzure. Storage. shared. Protocol. DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="30925-128">Microsoft.WindowsAzure.Storage.Shared.Protocol.DeleteRetentionPolicyProperties</span></span>

## <span data-ttu-id="30925-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="30925-129">NOTES</span></span>

## <span data-ttu-id="30925-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="30925-130">RELATED LINKS</span></span>

