---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/enable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: 1d55c52b3c022e9e935051cdb1ad23aae32eecbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929291"
---
# <span data-ttu-id="76c3b-101">Enable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="76c3b-101">Enable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="76c3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76c3b-102">SYNOPSIS</span></span>
<span data-ttu-id="76c3b-103">Aktivieren Sie die Aufbewahrungsrichtlinie zum Löschen für den Azure Storage Blob-Dienst.</span><span class="sxs-lookup"><span data-stu-id="76c3b-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="76c3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76c3b-104">SYNTAX</span></span>

```
Enable-AzStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76c3b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76c3b-105">DESCRIPTION</span></span>
<span data-ttu-id="76c3b-106">Das **Cmdlet Enable-AzStorageDeleteRetentionPolicy** aktiviert die Löschaufbewahrungsrichtlinie für den Azure Storage Blob-Dienst.</span><span class="sxs-lookup"><span data-stu-id="76c3b-106">The **Enable-AzStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="76c3b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="76c3b-107">EXAMPLES</span></span>

### <span data-ttu-id="76c3b-108">Beispiel 1: Aktivieren der Löschaufbewahrungsrichtlinie für den Blobdienst</span><span class="sxs-lookup"><span data-stu-id="76c3b-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="76c3b-109">Dieser Befehl aktiviert die Löschaufbewahrungsrichtlinie für den Blobdienst und setzt gelöschte Blob-Aufbewahrungstage auf 3.</span><span class="sxs-lookup"><span data-stu-id="76c3b-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="76c3b-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="76c3b-110">PARAMETERS</span></span>

### <span data-ttu-id="76c3b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="76c3b-111">-Context</span></span>
<span data-ttu-id="76c3b-112">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="76c3b-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="76c3b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c3b-113">-DefaultProfile</span></span>
<span data-ttu-id="76c3b-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76c3b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76c3b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76c3b-115">-PassThru</span></span>
<span data-ttu-id="76c3b-116">Anzeigen von DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="76c3b-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="76c3b-117">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="76c3b-117">-RetentionDays</span></span>
<span data-ttu-id="76c3b-118">Legt die Anzahl der Aufbewahrungstage für deleteRetentionPolicy fest.</span><span class="sxs-lookup"><span data-stu-id="76c3b-118">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

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

### <span data-ttu-id="76c3b-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="76c3b-119">-Confirm</span></span>
<span data-ttu-id="76c3b-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76c3b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76c3b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76c3b-121">-WhatIf</span></span>
<span data-ttu-id="76c3b-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76c3b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76c3b-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76c3b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76c3b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c3b-124">CommonParameters</span></span>
<span data-ttu-id="76c3b-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76c3b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c3b-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76c3b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c3b-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="76c3b-127">INPUTS</span></span>

### <span data-ttu-id="76c3b-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="76c3b-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="76c3b-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="76c3b-129">OUTPUTS</span></span>

### <span data-ttu-id="76c3b-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="76c3b-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="76c3b-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="76c3b-131">NOTES</span></span>

## <span data-ttu-id="76c3b-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="76c3b-132">RELATED LINKS</span></span>
