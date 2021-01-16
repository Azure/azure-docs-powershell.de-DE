---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
ms.openlocfilehash: e97e89c1ab7160f1eb06c9c94cd5620a48b0463e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376324"
---
# <span data-ttu-id="df45d-101">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="df45d-101">Enable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="df45d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df45d-102">SYNOPSIS</span></span>
<span data-ttu-id="df45d-103">Aktivieren Sie die statische Website für das Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="df45d-103">Enable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="df45d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df45d-104">SYNTAX</span></span>

```
Enable-AzStorageStaticWebsite [[-IndexDocument] <String>] [[-ErrorDocument404Path] <String>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df45d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df45d-105">DESCRIPTION</span></span>
<span data-ttu-id="df45d-106">Das **Cmdlet "Enable-AzStorageStaticWebsite"** aktiviert die statische Website für das Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="df45d-106">The **Enable-AzStorageStaticWebsite** cmdlet enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="df45d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="df45d-107">EXAMPLES</span></span>

### <span data-ttu-id="df45d-108">Beispiel 1: Aktivieren der statischen Website für das Azure -Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="df45d-108">Example 1: Enable static website for the Azure Storage account</span></span>
```
C:\PS>Enable-AzStorageStaticWebsite -IndexDocument $indexdoc -ErrorDocument404Path $errordoc
```

<span data-ttu-id="df45d-109">Dieser Befehl aktiviert die statische Website für das Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="df45d-109">This command enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="df45d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df45d-110">PARAMETERS</span></span>

### <span data-ttu-id="df45d-111">-Context</span><span class="sxs-lookup"><span data-stu-id="df45d-111">-Context</span></span>
<span data-ttu-id="df45d-112">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="df45d-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="df45d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df45d-113">-DefaultProfile</span></span>
<span data-ttu-id="df45d-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="df45d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df45d-115">-ErrorDocument404Path</span><span class="sxs-lookup"><span data-stu-id="df45d-115">-ErrorDocument404Path</span></span>
<span data-ttu-id="df45d-116">Der Pfad zu dem Fehlerdokument, der angezeigt werden soll, wenn ein 404-Fehler ausgegeben wird (d. h., wenn ein Browser eine Seite anfordert, die nicht vorhanden ist).</span><span class="sxs-lookup"><span data-stu-id="df45d-116">The path to the error document that should be shown when a 404 is issued (meaning, when a browser requests a page that does not exist.)</span></span>

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

### <span data-ttu-id="df45d-117">-IndexDocument</span><span class="sxs-lookup"><span data-stu-id="df45d-117">-IndexDocument</span></span>
<span data-ttu-id="df45d-118">Der Name des Indexdokuments in jedem Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="df45d-118">The name of the index document in each directory.</span></span>

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

### <span data-ttu-id="df45d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df45d-119">-PassThru</span></span>
<span data-ttu-id="df45d-120">Anzeigen der Einstellung "Statische Website" in "ServiceProperties"</span><span class="sxs-lookup"><span data-stu-id="df45d-120">Display Static Website setting in ServiceProperties.</span></span>

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

### <span data-ttu-id="df45d-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df45d-121">-Confirm</span></span>
<span data-ttu-id="df45d-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="df45d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df45d-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="df45d-123">-WhatIf</span></span>
<span data-ttu-id="df45d-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="df45d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df45d-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="df45d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df45d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df45d-126">CommonParameters</span></span>
<span data-ttu-id="df45d-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df45d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df45d-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df45d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df45d-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="df45d-129">INPUTS</span></span>

### <span data-ttu-id="df45d-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="df45d-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="df45d-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="df45d-131">OUTPUTS</span></span>

### <span data-ttu-id="df45d-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="df45d-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="df45d-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="df45d-133">NOTES</span></span>

## <span data-ttu-id="df45d-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="df45d-134">RELATED LINKS</span></span>
