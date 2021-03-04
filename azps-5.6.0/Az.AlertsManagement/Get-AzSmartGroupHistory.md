---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/get-azsmartgrouphistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
ms.openlocfilehash: 7a581d81938a647d845d2220b27347c1b42fcb03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923112"
---
# <span data-ttu-id="a318f-101">Get-AzSmartGroupHistory</span><span class="sxs-lookup"><span data-stu-id="a318f-101">Get-AzSmartGroupHistory</span></span>

## <span data-ttu-id="a318f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a318f-102">SYNOPSIS</span></span>
<span data-ttu-id="a318f-103">Ruft den Intelligenten Gruppenverlauf ab</span><span class="sxs-lookup"><span data-stu-id="a318f-103">Gets smart group history</span></span>

## <span data-ttu-id="a318f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a318f-104">SYNTAX</span></span>

### <span data-ttu-id="a318f-105">BySmartGroupId (Standard)</span><span class="sxs-lookup"><span data-stu-id="a318f-105">BySmartGroupId (Default)</span></span>
```
Get-AzSmartGroupHistory -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a318f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a318f-106">ByInputObject</span></span>
```
Get-AzSmartGroupHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a318f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a318f-107">DESCRIPTION</span></span>
<span data-ttu-id="a318f-108">**Das Get-AzSmartGroupHistory-Cmdlet** erhält einen intelligenten Gruppenverlauf.</span><span class="sxs-lookup"><span data-stu-id="a318f-108">**Get-AzSmartGroupHistory** cmdlet gets smart group history.</span></span>

## <span data-ttu-id="a318f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a318f-109">EXAMPLES</span></span>

### <span data-ttu-id="a318f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a318f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroupHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="a318f-111">Ruft Details zum intelligenten Gruppenverlauf ab.</span><span class="sxs-lookup"><span data-stu-id="a318f-111">Gets smart group history details.</span></span>

## <span data-ttu-id="a318f-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a318f-112">PARAMETERS</span></span>

### <span data-ttu-id="a318f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a318f-113">-DefaultProfile</span></span>
<span data-ttu-id="a318f-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a318f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a318f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a318f-115">-InputObject</span></span>
<span data-ttu-id="a318f-116">Eingabeobjekt aus pipeline.</span><span class="sxs-lookup"><span data-stu-id="a318f-116">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a318f-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="a318f-117">-SmartGroupId</span></span>
<span data-ttu-id="a318f-118">Eindeutiger Bezeichner der SmartGroup/ResourceId der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="a318f-118">Unique Identifier of SmartGroup / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: BySmartGroupId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a318f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a318f-119">CommonParameters</span></span>
<span data-ttu-id="a318f-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a318f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a318f-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a318f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a318f-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a318f-122">INPUTS</span></span>

### <span data-ttu-id="a318f-123">Keine</span><span class="sxs-lookup"><span data-stu-id="a318f-123">None</span></span>

## <span data-ttu-id="a318f-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a318f-124">OUTPUTS</span></span>

### <span data-ttu-id="a318f-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span><span class="sxs-lookup"><span data-stu-id="a318f-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span></span>

## <span data-ttu-id="a318f-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a318f-126">NOTES</span></span>

## <span data-ttu-id="a318f-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a318f-127">RELATED LINKS</span></span>
