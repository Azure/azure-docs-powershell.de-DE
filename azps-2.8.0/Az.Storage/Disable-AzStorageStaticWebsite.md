---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
ms.openlocfilehash: 4d5a12136dc23375e7ac5ea822c663c018f3bf68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825816"
---
# <span data-ttu-id="150df-101">Disable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="150df-101">Disable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="150df-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="150df-102">SYNOPSIS</span></span>
<span data-ttu-id="150df-103">Deaktivieren Sie die statische Website für das Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="150df-103">Disable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="150df-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="150df-104">SYNTAX</span></span>

```
Disable-AzStorageStaticWebsite [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="150df-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="150df-105">DESCRIPTION</span></span>
<span data-ttu-id="150df-106">Das Cmdlet **Disable-AzStorageStaticWebsite** deaktiviert die statische Website für das Azure-Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="150df-106">The **Disable-AzStorageStaticWebsite** cmdlet disables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="150df-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="150df-107">EXAMPLES</span></span>

### <span data-ttu-id="150df-108">Beispiel 1: Deaktivieren der statischen Website für ein Azure Storage-Konto</span><span class="sxs-lookup"><span data-stu-id="150df-108">Example 1: Disable static website for a Azure Storage account</span></span>
```
C:\PS>Disable-AzStorageStaticWebsite
```

<span data-ttu-id="150df-109">Mit diesem Befehl wird die statische Website für ein Azure Storage-Konto deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="150df-109">This command disables static website for a Azure Storage account.</span></span>

## <span data-ttu-id="150df-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="150df-110">PARAMETERS</span></span>

### <span data-ttu-id="150df-111">-Context</span><span class="sxs-lookup"><span data-stu-id="150df-111">-Context</span></span>
<span data-ttu-id="150df-112">Azure-Speicherkontext Objekt</span><span class="sxs-lookup"><span data-stu-id="150df-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="150df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="150df-113">-DefaultProfile</span></span>
<span data-ttu-id="150df-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="150df-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="150df-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="150df-115">-PassThru</span></span>
<span data-ttu-id="150df-116">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="150df-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="150df-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="150df-117">-Confirm</span></span>
<span data-ttu-id="150df-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="150df-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="150df-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="150df-119">-WhatIf</span></span>
<span data-ttu-id="150df-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="150df-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="150df-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="150df-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="150df-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="150df-122">CommonParameters</span></span>
<span data-ttu-id="150df-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="150df-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="150df-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="150df-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="150df-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="150df-125">INPUTS</span></span>

### <span data-ttu-id="150df-126">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="150df-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="150df-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="150df-127">OUTPUTS</span></span>

### <span data-ttu-id="150df-128">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="150df-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="150df-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="150df-129">NOTES</span></span>

## <span data-ttu-id="150df-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="150df-130">RELATED LINKS</span></span>
