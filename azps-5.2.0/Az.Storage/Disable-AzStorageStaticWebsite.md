---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
ms.openlocfilehash: a7814734f33e0a68fefacf4e465c1834cce17708
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304323"
---
# <span data-ttu-id="88627-101">Disable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="88627-101">Disable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="88627-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88627-102">SYNOPSIS</span></span>
<span data-ttu-id="88627-103">Deaktivieren Sie die statische Website für das Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="88627-103">Disable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="88627-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88627-104">SYNTAX</span></span>

```
Disable-AzStorageStaticWebsite [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88627-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="88627-105">DESCRIPTION</span></span>
<span data-ttu-id="88627-106">Das **Cmdlet "Disable-AzStorageStaticWebsite"** deaktiviert die statische Website für das Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="88627-106">The **Disable-AzStorageStaticWebsite** cmdlet disables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="88627-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="88627-107">EXAMPLES</span></span>

### <span data-ttu-id="88627-108">Beispiel 1: Deaktivieren der statischen Website für ein Azure -Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="88627-108">Example 1: Disable static website for a Azure Storage account</span></span>
```
C:\PS>Disable-AzStorageStaticWebsite
```

<span data-ttu-id="88627-109">Mit diesem Befehl wird die statische Website für ein Azure -Speicherkonto deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="88627-109">This command disables static website for a Azure Storage account.</span></span>

## <span data-ttu-id="88627-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88627-110">PARAMETERS</span></span>

### <span data-ttu-id="88627-111">-Context</span><span class="sxs-lookup"><span data-stu-id="88627-111">-Context</span></span>
<span data-ttu-id="88627-112">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="88627-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="88627-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88627-113">-DefaultProfile</span></span>
<span data-ttu-id="88627-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="88627-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88627-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88627-115">-PassThru</span></span>
<span data-ttu-id="88627-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="88627-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="88627-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88627-117">-Confirm</span></span>
<span data-ttu-id="88627-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="88627-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88627-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="88627-119">-WhatIf</span></span>
<span data-ttu-id="88627-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="88627-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88627-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88627-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88627-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88627-122">CommonParameters</span></span>
<span data-ttu-id="88627-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88627-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88627-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88627-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88627-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="88627-125">INPUTS</span></span>

### <span data-ttu-id="88627-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="88627-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="88627-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="88627-127">OUTPUTS</span></span>

### <span data-ttu-id="88627-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="88627-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="88627-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="88627-129">NOTES</span></span>

## <span data-ttu-id="88627-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="88627-130">RELATED LINKS</span></span>
