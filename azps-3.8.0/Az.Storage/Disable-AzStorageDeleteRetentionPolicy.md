---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: c8a32cb86ace86cb0f2775db98f49f57408be6f4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995958"
---
# <span data-ttu-id="f51b7-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f51b7-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="f51b7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f51b7-102">SYNOPSIS</span></span>
<span data-ttu-id="f51b7-103">Deaktivieren Sie die Aufbewahrungsrichtlinie für den Azure Storage-BLOB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="f51b7-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="f51b7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f51b7-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f51b7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f51b7-105">DESCRIPTION</span></span>
<span data-ttu-id="f51b7-106">Das Cmdlet **Disable-AzStorageDeleteRetentionPolicy** deaktiviert die Aufbewahrungsrichtlinie für den Azure Storage-BLOB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="f51b7-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="f51b7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f51b7-107">EXAMPLES</span></span>

### <span data-ttu-id="f51b7-108">Beispiel 1: Deaktivieren der Aufbewahrungsrichtlinie für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="f51b7-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="f51b7-109">Mit diesem Befehl wird die Aufbewahrungsrichtlinie für den BLOB-Dienst deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f51b7-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="f51b7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f51b7-110">PARAMETERS</span></span>

### <span data-ttu-id="f51b7-111">-Context</span><span class="sxs-lookup"><span data-stu-id="f51b7-111">-Context</span></span>
<span data-ttu-id="f51b7-112">Azure-Speicherkontext Objekt</span><span class="sxs-lookup"><span data-stu-id="f51b7-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="f51b7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f51b7-113">-DefaultProfile</span></span>
<span data-ttu-id="f51b7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f51b7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f51b7-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f51b7-115">-PassThru</span></span>
<span data-ttu-id="f51b7-116">DeleteRetentionPolicyProperties anzeigen</span><span class="sxs-lookup"><span data-stu-id="f51b7-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="f51b7-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f51b7-117">-Confirm</span></span>
<span data-ttu-id="f51b7-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f51b7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f51b7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f51b7-119">-WhatIf</span></span>
<span data-ttu-id="f51b7-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f51b7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f51b7-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f51b7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f51b7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f51b7-122">CommonParameters</span></span>
<span data-ttu-id="f51b7-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f51b7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f51b7-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f51b7-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f51b7-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f51b7-125">INPUTS</span></span>

### <span data-ttu-id="f51b7-126">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f51b7-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f51b7-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f51b7-127">OUTPUTS</span></span>

### <span data-ttu-id="f51b7-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f51b7-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="f51b7-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="f51b7-129">NOTES</span></span>

## <span data-ttu-id="f51b7-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f51b7-130">RELATED LINKS</span></span>
