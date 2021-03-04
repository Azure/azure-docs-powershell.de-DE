---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/enable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
ms.openlocfilehash: 25526e7c83746b67a5272ab94f3d523947795c1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929272"
---
# <span data-ttu-id="2b17e-101">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2b17e-101">Enable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="2b17e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b17e-102">SYNOPSIS</span></span>
<span data-ttu-id="2b17e-103">Aktivieren Sie die statische Website für das Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="2b17e-103">Enable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="2b17e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b17e-104">SYNTAX</span></span>

```
Enable-AzStorageStaticWebsite [[-IndexDocument] <String>] [[-ErrorDocument404Path] <String>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b17e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b17e-105">DESCRIPTION</span></span>
<span data-ttu-id="2b17e-106">Das **Cmdlet Enable-AzStorageStaticWebsite** aktiviert die statische Website für das Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="2b17e-106">The **Enable-AzStorageStaticWebsite** cmdlet enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="2b17e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2b17e-107">EXAMPLES</span></span>

### <span data-ttu-id="2b17e-108">Beispiel 1: Aktivieren der statischen Website für das Azure Storage-Konto</span><span class="sxs-lookup"><span data-stu-id="2b17e-108">Example 1: Enable static website for the Azure Storage account</span></span>
```
C:\PS>Enable-AzStorageStaticWebsite -IndexDocument $indexdoc -ErrorDocument404Path $errordoc
```

<span data-ttu-id="2b17e-109">Mit diesem Befehl wird die statische Website für das Azure Storage-Konto aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2b17e-109">This command enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="2b17e-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2b17e-110">PARAMETERS</span></span>

### <span data-ttu-id="2b17e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="2b17e-111">-Context</span></span>
<span data-ttu-id="2b17e-112">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="2b17e-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="2b17e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b17e-113">-DefaultProfile</span></span>
<span data-ttu-id="2b17e-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2b17e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b17e-115">-ErrorDocument404Path</span><span class="sxs-lookup"><span data-stu-id="2b17e-115">-ErrorDocument404Path</span></span>
<span data-ttu-id="2b17e-116">Der Pfad zum Fehlerdokument, der angezeigt werden soll, wenn ein 404 ausgegeben wird (d. h., wenn ein Browser eine Seite anfordert, die nicht vorhanden ist.)</span><span class="sxs-lookup"><span data-stu-id="2b17e-116">The path to the error document that should be shown when a 404 is issued (meaning, when a browser requests a page that does not exist.)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b17e-117">-IndexDocument</span><span class="sxs-lookup"><span data-stu-id="2b17e-117">-IndexDocument</span></span>
<span data-ttu-id="2b17e-118">Der Name des Indexdokuments in jedem Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="2b17e-118">The name of the index document in each directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b17e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b17e-119">-PassThru</span></span>
<span data-ttu-id="2b17e-120">Anzeigen der Einstellung statische Website in ServiceProperties.</span><span class="sxs-lookup"><span data-stu-id="2b17e-120">Display Static Website setting in ServiceProperties.</span></span>

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

### <span data-ttu-id="2b17e-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2b17e-121">-Confirm</span></span>
<span data-ttu-id="2b17e-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b17e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b17e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b17e-123">-WhatIf</span></span>
<span data-ttu-id="2b17e-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2b17e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b17e-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2b17e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b17e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b17e-126">CommonParameters</span></span>
<span data-ttu-id="2b17e-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b17e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b17e-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b17e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b17e-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2b17e-129">INPUTS</span></span>

### <span data-ttu-id="2b17e-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2b17e-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2b17e-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2b17e-131">OUTPUTS</span></span>

### <span data-ttu-id="2b17e-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="2b17e-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="2b17e-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2b17e-133">NOTES</span></span>

## <span data-ttu-id="2b17e-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2b17e-134">RELATED LINKS</span></span>
