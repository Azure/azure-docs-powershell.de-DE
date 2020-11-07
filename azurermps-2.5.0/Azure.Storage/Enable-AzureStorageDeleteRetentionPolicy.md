---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/enable-azurestoragedeleteretentionpolicy
schema: 2.0.0
ms.openlocfilehash: d94b5e21913112d9e7d29a3e4012909dd5c9c3c0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849455"
---
# <span data-ttu-id="8dd8c-101">Enable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8dd8c-101">Enable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="8dd8c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8dd8c-102">SYNOPSIS</span></span>
<span data-ttu-id="8dd8c-103">Aktivieren Sie die Aufbewahrungsrichtlinie für den Azure Storage-BLOB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="8dd8c-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8dd8c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8dd8c-104">SYNTAX</span></span>

```
Enable-AzureStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dd8c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8dd8c-105">DESCRIPTION</span></span>
<span data-ttu-id="8dd8c-106">Das Cmdlet **enable-AzureStorageDeleteRetentionPolicy** aktiviert die Aufbewahrungsrichtlinie für den Azure Storage-BLOB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="8dd8c-106">The **Enable-AzureStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="8dd8c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8dd8c-107">EXAMPLES</span></span>

### <span data-ttu-id="8dd8c-108">Beispiel 1: Aktivieren der Aufbewahrungsrichtlinie für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="8dd8c-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzureStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="8dd8c-109">Mit diesem Befehl können Sie die Aufbewahrungsrichtlinie für den BLOB-Dienst löschen und gelöschte Aufbewahrungstage für BLOB auf 3 festlegen.</span><span class="sxs-lookup"><span data-stu-id="8dd8c-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="8dd8c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8dd8c-110">PARAMETERS</span></span>

### <span data-ttu-id="8dd8c-111">-Context</span><span class="sxs-lookup"><span data-stu-id="8dd8c-111">-Context</span></span>
<span data-ttu-id="8dd8c-112">Azure-Speicherkontext Objekt</span><span class="sxs-lookup"><span data-stu-id="8dd8c-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="8dd8c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dd8c-113">-DefaultProfile</span></span>
<span data-ttu-id="8dd8c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8dd8c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dd8c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8dd8c-115">-PassThru</span></span>
<span data-ttu-id="8dd8c-116">DeleteRetentionPolicyProperties anzeigen</span><span class="sxs-lookup"><span data-stu-id="8dd8c-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="8dd8c-117">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="8dd8c-117">-RetentionDays</span></span>
<span data-ttu-id="8dd8c-118">Legt die Anzahl der Aufbewahrungstage für die DeleteRetentionPolicy fest.</span><span class="sxs-lookup"><span data-stu-id="8dd8c-118">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd8c-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8dd8c-119">-Confirm</span></span>
<span data-ttu-id="8dd8c-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8dd8c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dd8c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dd8c-121">-WhatIf</span></span>
<span data-ttu-id="8dd8c-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8dd8c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dd8c-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8dd8c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dd8c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dd8c-124">CommonParameters</span></span>
<span data-ttu-id="8dd8c-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dd8c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dd8c-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dd8c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dd8c-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8dd8c-127">INPUTS</span></span>

### <span data-ttu-id="8dd8c-128">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8dd8c-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8dd8c-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8dd8c-129">OUTPUTS</span></span>

### <span data-ttu-id="8dd8c-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8dd8c-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="8dd8c-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="8dd8c-131">NOTES</span></span>

## <span data-ttu-id="8dd8c-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8dd8c-132">RELATED LINKS</span></span>
