---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/disable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
ms.openlocfilehash: 12881d387d1e98bef8ca1fa00790b0332a338b7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929307"
---
# <span data-ttu-id="4574c-101">Disable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4574c-101">Disable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="4574c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4574c-102">SYNOPSIS</span></span>
<span data-ttu-id="4574c-103">Deaktivieren Sie die statische Website für das Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="4574c-103">Disable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="4574c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4574c-104">SYNTAX</span></span>

```
Disable-AzStorageStaticWebsite [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4574c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4574c-105">DESCRIPTION</span></span>
<span data-ttu-id="4574c-106">Das **Cmdlet Disable-AzStorageStaticWebsite** deaktiviert die statische Website für das Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="4574c-106">The **Disable-AzStorageStaticWebsite** cmdlet disables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="4574c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4574c-107">EXAMPLES</span></span>

### <span data-ttu-id="4574c-108">Beispiel 1: Deaktivieren der statischen Website für ein Azure Storage-Konto</span><span class="sxs-lookup"><span data-stu-id="4574c-108">Example 1: Disable static website for a Azure Storage account</span></span>
```
C:\PS>Disable-AzStorageStaticWebsite
```

<span data-ttu-id="4574c-109">Mit diesem Befehl wird die statische Website für ein Azure Storage-Konto deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4574c-109">This command disables static website for a Azure Storage account.</span></span>

## <span data-ttu-id="4574c-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4574c-110">PARAMETERS</span></span>

### <span data-ttu-id="4574c-111">-Context</span><span class="sxs-lookup"><span data-stu-id="4574c-111">-Context</span></span>
<span data-ttu-id="4574c-112">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="4574c-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="4574c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4574c-113">-DefaultProfile</span></span>
<span data-ttu-id="4574c-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4574c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4574c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4574c-115">-PassThru</span></span>
<span data-ttu-id="4574c-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4574c-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4574c-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4574c-117">-Confirm</span></span>
<span data-ttu-id="4574c-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4574c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4574c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4574c-119">-WhatIf</span></span>
<span data-ttu-id="4574c-120">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4574c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4574c-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4574c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4574c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4574c-122">CommonParameters</span></span>
<span data-ttu-id="4574c-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4574c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4574c-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4574c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4574c-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4574c-125">INPUTS</span></span>

### <span data-ttu-id="4574c-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4574c-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4574c-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4574c-127">OUTPUTS</span></span>

### <span data-ttu-id="4574c-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="4574c-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="4574c-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4574c-129">NOTES</span></span>

## <span data-ttu-id="4574c-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4574c-130">RELATED LINKS</span></span>
