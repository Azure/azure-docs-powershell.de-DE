---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
ms.openlocfilehash: ed8f6bdada7a813c6811799c314f6ae494e9e07a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658899"
---
# <span data-ttu-id="318af-101">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="318af-101">Enable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="318af-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="318af-102">SYNOPSIS</span></span>
<span data-ttu-id="318af-103">Aktivieren der statischen Website für das Azure-Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="318af-103">Enable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="318af-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="318af-104">SYNTAX</span></span>

```
Enable-AzStorageStaticWebsite [-IndexDocument] <String> [-ErrorDocument404Path] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="318af-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="318af-105">DESCRIPTION</span></span>
<span data-ttu-id="318af-106">Das Cmdlet **enable-AzStorageStaticWebsite** ermöglicht die statische Website für das Azure-Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="318af-106">The **Enable-AzStorageStaticWebsite** cmdlet enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="318af-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="318af-107">EXAMPLES</span></span>

### <span data-ttu-id="318af-108">Beispiel 1: Aktivieren der statischen Website für das Azure-Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="318af-108">Example 1: Enable static website for the Azure Storage account</span></span>
```
C:\PS>Enable-AzStorageStaticWebsite -IndexDocument $indexdoc -ErrorDocument404Path $errordoc
```

<span data-ttu-id="318af-109">Mit diesem Befehl wird die statische Website für das Azure-Speicherkonto aktiviert.</span><span class="sxs-lookup"><span data-stu-id="318af-109">This command enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="318af-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="318af-110">PARAMETERS</span></span>

### <span data-ttu-id="318af-111">-Context</span><span class="sxs-lookup"><span data-stu-id="318af-111">-Context</span></span>
<span data-ttu-id="318af-112">Azure-Speicherkontext Objekt</span><span class="sxs-lookup"><span data-stu-id="318af-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="318af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="318af-113">-DefaultProfile</span></span>
<span data-ttu-id="318af-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="318af-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="318af-115">-ErrorDocument404Path</span><span class="sxs-lookup"><span data-stu-id="318af-115">-ErrorDocument404Path</span></span>
<span data-ttu-id="318af-116">Der Pfad zum Fehlerdokument, das angezeigt werden soll, wenn eine 404 ausgegeben wird (d. h., wenn ein Browser eine Seite anfordert, die nicht vorhanden ist).</span><span class="sxs-lookup"><span data-stu-id="318af-116">The path to the error document that should be shown when a 404 is issued (meaning, when a browser requests a page that does not exist.)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="318af-117">-IndexDocument</span><span class="sxs-lookup"><span data-stu-id="318af-117">-IndexDocument</span></span>
<span data-ttu-id="318af-118">Der Name des Index Dokuments in jedem Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="318af-118">The name of the index document in each directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="318af-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="318af-119">-PassThru</span></span>
<span data-ttu-id="318af-120">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="318af-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="318af-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="318af-121">-Confirm</span></span>
<span data-ttu-id="318af-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="318af-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="318af-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="318af-123">-WhatIf</span></span>
<span data-ttu-id="318af-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="318af-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="318af-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="318af-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="318af-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="318af-126">CommonParameters</span></span>
<span data-ttu-id="318af-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="318af-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="318af-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="318af-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="318af-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="318af-129">INPUTS</span></span>

### <span data-ttu-id="318af-130">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="318af-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="318af-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="318af-131">OUTPUTS</span></span>

### <span data-ttu-id="318af-132">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="318af-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="318af-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="318af-133">NOTES</span></span>

## <span data-ttu-id="318af-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="318af-134">RELATED LINKS</span></span>
