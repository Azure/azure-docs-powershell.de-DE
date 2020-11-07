---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/disable-azurestoragedeleteretentionpolicy
schema: 2.0.0
ms.openlocfilehash: d899b34e2f880a0351ce4d10f360f7bc29011b0c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849456"
---
# <span data-ttu-id="4a865-101">Disable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4a865-101">Disable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="4a865-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4a865-102">SYNOPSIS</span></span>
<span data-ttu-id="4a865-103">Deaktivieren Sie die Aufbewahrungsrichtlinie für den Azure Storage-BLOB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="4a865-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a865-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a865-104">SYNTAX</span></span>

```
Disable-AzureStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a865-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a865-105">DESCRIPTION</span></span>
<span data-ttu-id="4a865-106">Das Cmdlet **Disable-AzureStorageDeleteRetentionPolicy** deaktiviert die Aufbewahrungsrichtlinie für den Azure Storage-BLOB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="4a865-106">The **Disable-AzureStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="4a865-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4a865-107">EXAMPLES</span></span>

### <span data-ttu-id="4a865-108">Beispiel 1: Deaktivieren der Aufbewahrungsrichtlinie für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="4a865-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzureStorageDeleteRetentionPolicy
```

<span data-ttu-id="4a865-109">Mit diesem Befehl wird die Aufbewahrungsrichtlinie für den BLOB-Dienst deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4a865-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="4a865-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a865-110">PARAMETERS</span></span>

### <span data-ttu-id="4a865-111">-Context</span><span class="sxs-lookup"><span data-stu-id="4a865-111">-Context</span></span>
<span data-ttu-id="4a865-112">Azure-Speicherkontext Objekt</span><span class="sxs-lookup"><span data-stu-id="4a865-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="4a865-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a865-113">-DefaultProfile</span></span>
<span data-ttu-id="4a865-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4a865-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a865-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a865-115">-PassThru</span></span>
<span data-ttu-id="4a865-116">DeleteRetentionPolicyProperties anzeigen</span><span class="sxs-lookup"><span data-stu-id="4a865-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="4a865-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4a865-117">-Confirm</span></span>
<span data-ttu-id="4a865-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4a865-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a865-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a865-119">-WhatIf</span></span>
<span data-ttu-id="4a865-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4a865-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a865-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4a865-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a865-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a865-122">CommonParameters</span></span>
<span data-ttu-id="4a865-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a865-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a865-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a865-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a865-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4a865-125">INPUTS</span></span>

### <span data-ttu-id="4a865-126">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4a865-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4a865-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4a865-127">OUTPUTS</span></span>

### <span data-ttu-id="4a865-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4a865-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="4a865-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="4a865-129">NOTES</span></span>

## <span data-ttu-id="4a865-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4a865-130">RELATED LINKS</span></span>
