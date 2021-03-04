---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: dac884a0faf44380f19447f2d52af1e172feb9a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929312"
---
# <span data-ttu-id="8c04e-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8c04e-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="8c04e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c04e-102">SYNOPSIS</span></span>
<span data-ttu-id="8c04e-103">Deaktivieren Sie die Löschaufbewahrungsrichtlinie für den Azure Storage Blob-Dienst.</span><span class="sxs-lookup"><span data-stu-id="8c04e-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="8c04e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c04e-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c04e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8c04e-105">DESCRIPTION</span></span>
<span data-ttu-id="8c04e-106">Das **Cmdlet Disable-AzStorageDeleteRetentionPolicy** deaktiviert die Löschaufbewahrungsrichtlinie für den Azure Storage Blob-Dienst.</span><span class="sxs-lookup"><span data-stu-id="8c04e-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="8c04e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8c04e-107">EXAMPLES</span></span>

### <span data-ttu-id="8c04e-108">Beispiel 1: Deaktivieren der Löschaufbewahrungsrichtlinie für den Blobdienst</span><span class="sxs-lookup"><span data-stu-id="8c04e-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="8c04e-109">Mit diesem Befehl wird die Löschaufbewahrungsrichtlinie für den Blobdienst deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8c04e-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="8c04e-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8c04e-110">PARAMETERS</span></span>

### <span data-ttu-id="8c04e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="8c04e-111">-Context</span></span>
<span data-ttu-id="8c04e-112">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="8c04e-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="8c04e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c04e-113">-DefaultProfile</span></span>
<span data-ttu-id="8c04e-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c04e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c04e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c04e-115">-PassThru</span></span>
<span data-ttu-id="8c04e-116">Anzeigen von DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="8c04e-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="8c04e-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8c04e-117">-Confirm</span></span>
<span data-ttu-id="8c04e-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c04e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c04e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c04e-119">-WhatIf</span></span>
<span data-ttu-id="8c04e-120">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8c04e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c04e-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c04e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c04e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c04e-122">CommonParameters</span></span>
<span data-ttu-id="8c04e-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c04e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c04e-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c04e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c04e-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8c04e-125">INPUTS</span></span>

### <span data-ttu-id="8c04e-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8c04e-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8c04e-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8c04e-127">OUTPUTS</span></span>

### <span data-ttu-id="8c04e-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8c04e-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="8c04e-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8c04e-129">NOTES</span></span>

## <span data-ttu-id="8c04e-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8c04e-130">RELATED LINKS</span></span>
