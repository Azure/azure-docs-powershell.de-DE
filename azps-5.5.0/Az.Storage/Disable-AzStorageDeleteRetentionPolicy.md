---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: c8a32cb86ace86cb0f2775db98f49f57408be6f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158145"
---
# <span data-ttu-id="14f06-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="14f06-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="14f06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14f06-102">SYNOPSIS</span></span>
<span data-ttu-id="14f06-103">Deaktivieren Sie die Löschaufbewahrungsrichtlinie für den Azure Storage Blob-Dienst.</span><span class="sxs-lookup"><span data-stu-id="14f06-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="14f06-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14f06-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14f06-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="14f06-105">DESCRIPTION</span></span>
<span data-ttu-id="14f06-106">Das **Cmdlet "Disable-AzStorageDeleteRetentionPolicy"** deaktiviert die Löschaufbewahrungsrichtlinie für den Azure Storage Blob-Dienst.</span><span class="sxs-lookup"><span data-stu-id="14f06-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="14f06-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="14f06-107">EXAMPLES</span></span>

### <span data-ttu-id="14f06-108">Beispiel 1: Deaktivieren der Löschaufbewahrungsrichtlinie für den Blob-Dienst</span><span class="sxs-lookup"><span data-stu-id="14f06-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="14f06-109">Dieser Befehl deaktiviert die Löschaufbewahrungsrichtlinie für den Blob-Dienst.</span><span class="sxs-lookup"><span data-stu-id="14f06-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="14f06-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14f06-110">PARAMETERS</span></span>

### <span data-ttu-id="14f06-111">-Context</span><span class="sxs-lookup"><span data-stu-id="14f06-111">-Context</span></span>
<span data-ttu-id="14f06-112">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="14f06-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="14f06-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14f06-113">-DefaultProfile</span></span>
<span data-ttu-id="14f06-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14f06-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14f06-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14f06-115">-PassThru</span></span>
<span data-ttu-id="14f06-116">DeleteRetentionPolicyProperties anzeigen</span><span class="sxs-lookup"><span data-stu-id="14f06-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="14f06-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14f06-117">-Confirm</span></span>
<span data-ttu-id="14f06-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="14f06-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14f06-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="14f06-119">-WhatIf</span></span>
<span data-ttu-id="14f06-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="14f06-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14f06-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="14f06-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14f06-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14f06-122">CommonParameters</span></span>
<span data-ttu-id="14f06-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14f06-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14f06-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14f06-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14f06-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="14f06-125">INPUTS</span></span>

### <span data-ttu-id="14f06-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="14f06-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="14f06-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="14f06-127">OUTPUTS</span></span>

### <span data-ttu-id="14f06-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="14f06-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="14f06-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="14f06-129">NOTES</span></span>

## <span data-ttu-id="14f06-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="14f06-130">RELATED LINKS</span></span>
