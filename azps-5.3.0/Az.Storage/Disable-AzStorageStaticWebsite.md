---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
ms.openlocfilehash: a7814734f33e0a68fefacf4e465c1834cce17708
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460588"
---
# <span data-ttu-id="c19db-101">Disable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c19db-101">Disable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="c19db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c19db-102">SYNOPSIS</span></span>
<span data-ttu-id="c19db-103">Deaktivieren Sie die statische Website für das Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="c19db-103">Disable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="c19db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c19db-104">SYNTAX</span></span>

```
Disable-AzStorageStaticWebsite [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c19db-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c19db-105">DESCRIPTION</span></span>
<span data-ttu-id="c19db-106">Das **Cmdlet "Disable-AzStorageStaticWebsite"** deaktiviert die statische Website für das Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="c19db-106">The **Disable-AzStorageStaticWebsite** cmdlet disables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="c19db-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c19db-107">EXAMPLES</span></span>

### <span data-ttu-id="c19db-108">Beispiel 1: Deaktivieren der statischen Website für ein Azure -Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="c19db-108">Example 1: Disable static website for a Azure Storage account</span></span>
```
C:\PS>Disable-AzStorageStaticWebsite
```

<span data-ttu-id="c19db-109">Mit diesem Befehl wird die statische Website für ein Azure -Speicherkonto deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c19db-109">This command disables static website for a Azure Storage account.</span></span>

## <span data-ttu-id="c19db-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c19db-110">PARAMETERS</span></span>

### <span data-ttu-id="c19db-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c19db-111">-Context</span></span>
<span data-ttu-id="c19db-112">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="c19db-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="c19db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c19db-113">-DefaultProfile</span></span>
<span data-ttu-id="c19db-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c19db-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c19db-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c19db-115">-PassThru</span></span>
<span data-ttu-id="c19db-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c19db-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c19db-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c19db-117">-Confirm</span></span>
<span data-ttu-id="c19db-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c19db-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c19db-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c19db-119">-WhatIf</span></span>
<span data-ttu-id="c19db-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c19db-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c19db-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c19db-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c19db-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c19db-122">CommonParameters</span></span>
<span data-ttu-id="c19db-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c19db-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c19db-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c19db-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c19db-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c19db-125">INPUTS</span></span>

### <span data-ttu-id="c19db-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c19db-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c19db-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c19db-127">OUTPUTS</span></span>

### <span data-ttu-id="c19db-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="c19db-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="c19db-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c19db-129">NOTES</span></span>

## <span data-ttu-id="c19db-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c19db-130">RELATED LINKS</span></span>
