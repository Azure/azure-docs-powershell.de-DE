---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/disable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: 656fe09054b1cfae90175cc4ea55370f80dfd8e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478109"
---
# <span data-ttu-id="553ed-101">Disable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="553ed-101">Disable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="553ed-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="553ed-102">SYNOPSIS</span></span>
<span data-ttu-id="553ed-103">Deaktivieren Sie die Aufbewahrungsrichtlinie für den Azure Storage-BLOB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="553ed-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="553ed-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="553ed-104">SYNTAX</span></span>

```
Disable-AzureStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="553ed-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="553ed-105">DESCRIPTION</span></span>
<span data-ttu-id="553ed-106">Das Cmdlet **Disable-AzureStorageDeleteRetentionPolicy** deaktiviert die Aufbewahrungsrichtlinie für den Azure Storage-BLOB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="553ed-106">The **Disable-AzureStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="553ed-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="553ed-107">EXAMPLES</span></span>

### <span data-ttu-id="553ed-108">Beispiel 1: Deaktivieren der Aufbewahrungsrichtlinie für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="553ed-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzureStorageDeleteRetentionPolicy
```

<span data-ttu-id="553ed-109">Mit diesem Befehl wird die Aufbewahrungsrichtlinie für den BLOB-Dienst deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="553ed-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="553ed-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="553ed-110">PARAMETERS</span></span>

### <span data-ttu-id="553ed-111">-Context</span><span class="sxs-lookup"><span data-stu-id="553ed-111">-Context</span></span>
<span data-ttu-id="553ed-112">Azure-Speicherkontext Objekt</span><span class="sxs-lookup"><span data-stu-id="553ed-112">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="553ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="553ed-113">-DefaultProfile</span></span>
<span data-ttu-id="553ed-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="553ed-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="553ed-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="553ed-115">-PassThru</span></span>
<span data-ttu-id="553ed-116">DeleteRetentionPolicyProperties anzeigen</span><span class="sxs-lookup"><span data-stu-id="553ed-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="553ed-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="553ed-117">-Confirm</span></span>
<span data-ttu-id="553ed-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="553ed-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="553ed-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="553ed-119">-WhatIf</span></span>
<span data-ttu-id="553ed-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="553ed-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="553ed-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="553ed-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="553ed-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="553ed-122">CommonParameters</span></span>
<span data-ttu-id="553ed-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="553ed-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="553ed-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="553ed-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="553ed-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="553ed-125">INPUTS</span></span>

### <span data-ttu-id="553ed-126">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="553ed-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="553ed-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="553ed-127">OUTPUTS</span></span>

### <span data-ttu-id="553ed-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="553ed-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="553ed-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="553ed-129">NOTES</span></span>

## <span data-ttu-id="553ed-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="553ed-130">RELATED LINKS</span></span>
