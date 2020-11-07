---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/disable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: d3de0cc49eb0e36572daa9e4cfbbb41c0db0936a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662388"
---
# <span data-ttu-id="2b7f8-101">Disable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2b7f8-101">Disable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="2b7f8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2b7f8-102">SYNOPSIS</span></span>
<span data-ttu-id="2b7f8-103">Deaktivieren Sie die Aufbewahrungsrichtlinie für den Azure Storage-BLOB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="2b7f8-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b7f8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b7f8-104">SYNTAX</span></span>

```
Disable-AzureStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b7f8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b7f8-105">DESCRIPTION</span></span>
<span data-ttu-id="2b7f8-106">Das Cmdlet **Disable-AzureStorageDeleteRetentionPolicy** deaktiviert die Aufbewahrungsrichtlinie für den Azure Storage-BLOB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="2b7f8-106">The **Disable-AzureStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="2b7f8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2b7f8-107">EXAMPLES</span></span>

### <span data-ttu-id="2b7f8-108">Beispiel 1: Deaktivieren der Aufbewahrungsrichtlinie für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="2b7f8-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzureStorageDeleteRetentionPolicy
```

<span data-ttu-id="2b7f8-109">Mit diesem Befehl wird die Aufbewahrungsrichtlinie für den BLOB-Dienst deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2b7f8-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="2b7f8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b7f8-110">PARAMETERS</span></span>

### <span data-ttu-id="2b7f8-111">-Context</span><span class="sxs-lookup"><span data-stu-id="2b7f8-111">-Context</span></span>
<span data-ttu-id="2b7f8-112">Azure-Speicherkontext Objekt</span><span class="sxs-lookup"><span data-stu-id="2b7f8-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="2b7f8-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b7f8-113">-PassThru</span></span>
<span data-ttu-id="2b7f8-114">DeleteRetentionPolicyProperties anzeigen</span><span class="sxs-lookup"><span data-stu-id="2b7f8-114">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="2b7f8-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2b7f8-115">-Confirm</span></span>
<span data-ttu-id="2b7f8-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b7f8-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b7f8-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b7f8-117">-WhatIf</span></span>
<span data-ttu-id="2b7f8-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2b7f8-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b7f8-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2b7f8-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b7f8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b7f8-120">CommonParameters</span></span>
<span data-ttu-id="2b7f8-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b7f8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b7f8-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b7f8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b7f8-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2b7f8-123">INPUTS</span></span>

### <span data-ttu-id="2b7f8-124">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2b7f8-124">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2b7f8-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2b7f8-125">OUTPUTS</span></span>

### <span data-ttu-id="2b7f8-126">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceMode. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="2b7f8-126">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceMode.PSSeriviceProperties</span></span>

## <span data-ttu-id="2b7f8-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="2b7f8-127">NOTES</span></span>

## <span data-ttu-id="2b7f8-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2b7f8-128">RELATED LINKS</span></span>

