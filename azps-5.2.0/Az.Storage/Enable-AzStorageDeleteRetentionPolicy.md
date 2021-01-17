---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: 36176b16fab75b24549ceeb3d107114632703129
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304304"
---
# <span data-ttu-id="6f849-101">Enable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6f849-101">Enable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="6f849-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f849-102">SYNOPSIS</span></span>
<span data-ttu-id="6f849-103">Aktivieren Sie die Löschaufbewahrungsrichtlinie für den Azure Storage Blob-Dienst.</span><span class="sxs-lookup"><span data-stu-id="6f849-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="6f849-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f849-104">SYNTAX</span></span>

```
Enable-AzStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f849-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f849-105">DESCRIPTION</span></span>
<span data-ttu-id="6f849-106">Das **Cmdlet "Enable-AzStorageDeleteRetentionPolicy"** aktiviert die Löschaufbewahrungsrichtlinie für den Azure Storage Blob-Dienst.</span><span class="sxs-lookup"><span data-stu-id="6f849-106">The **Enable-AzStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="6f849-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6f849-107">EXAMPLES</span></span>

### <span data-ttu-id="6f849-108">Beispiel 1: Aktivieren der Löschaufbewahrungsrichtlinie für den Blob Service</span><span class="sxs-lookup"><span data-stu-id="6f849-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="6f849-109">Dieser Befehl aktiviert die Löschaufbewahrungsrichtlinie für den Blob-Dienst und setzt gelöschte Blob-Aufbewahrungstage auf 3.</span><span class="sxs-lookup"><span data-stu-id="6f849-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="6f849-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f849-110">PARAMETERS</span></span>

### <span data-ttu-id="6f849-111">-Context</span><span class="sxs-lookup"><span data-stu-id="6f849-111">-Context</span></span>
<span data-ttu-id="6f849-112">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="6f849-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="6f849-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f849-113">-DefaultProfile</span></span>
<span data-ttu-id="6f849-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6f849-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f849-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f849-115">-PassThru</span></span>
<span data-ttu-id="6f849-116">DeleteRetentionPolicyProperties anzeigen</span><span class="sxs-lookup"><span data-stu-id="6f849-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="6f849-117">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="6f849-117">-RetentionDays</span></span>
<span data-ttu-id="6f849-118">Legt die Anzahl der Aufbewahrungstage für "DeleteRetentionPolicy" fest.</span><span class="sxs-lookup"><span data-stu-id="6f849-118">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

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

### <span data-ttu-id="6f849-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f849-119">-Confirm</span></span>
<span data-ttu-id="6f849-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6f849-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f849-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6f849-121">-WhatIf</span></span>
<span data-ttu-id="6f849-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6f849-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f849-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6f849-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f849-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f849-124">CommonParameters</span></span>
<span data-ttu-id="6f849-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f849-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f849-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f849-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f849-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6f849-127">INPUTS</span></span>

### <span data-ttu-id="6f849-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6f849-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6f849-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6f849-129">OUTPUTS</span></span>

### <span data-ttu-id="6f849-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6f849-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="6f849-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6f849-131">NOTES</span></span>

## <span data-ttu-id="6f849-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6f849-132">RELATED LINKS</span></span>
