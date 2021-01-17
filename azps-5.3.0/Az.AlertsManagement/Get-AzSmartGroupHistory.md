---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgrouphistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
ms.openlocfilehash: a8e827d678c7ac3b917ee7be09d030b193ffda24
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471562"
---
# <span data-ttu-id="81bd8-101">Get-AzSmartGroupHistory</span><span class="sxs-lookup"><span data-stu-id="81bd8-101">Get-AzSmartGroupHistory</span></span>

## <span data-ttu-id="81bd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81bd8-102">SYNOPSIS</span></span>
<span data-ttu-id="81bd8-103">Ruft den intelligenten Gruppenverlauf ab</span><span class="sxs-lookup"><span data-stu-id="81bd8-103">Gets smart group history</span></span>

## <span data-ttu-id="81bd8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81bd8-104">SYNTAX</span></span>

### <span data-ttu-id="81bd8-105">ByIdoGroupId (Standard)</span><span class="sxs-lookup"><span data-stu-id="81bd8-105">BySmartGroupId (Default)</span></span>
```
Get-AzSmartGroupHistory -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81bd8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="81bd8-106">ByInputObject</span></span>
```
Get-AzSmartGroupHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="81bd8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81bd8-107">DESCRIPTION</span></span>
<span data-ttu-id="81bd8-108">**Das Cmdlet "Get-AzLetsGroupHistory"** erhält den intelligenten Gruppenverlauf.</span><span class="sxs-lookup"><span data-stu-id="81bd8-108">**Get-AzSmartGroupHistory** cmdlet gets smart group history.</span></span>

## <span data-ttu-id="81bd8-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="81bd8-109">EXAMPLES</span></span>

### <span data-ttu-id="81bd8-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="81bd8-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroupHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="81bd8-111">Ruft intelligente Details des Gruppenverlaufs ab.</span><span class="sxs-lookup"><span data-stu-id="81bd8-111">Gets smart group history details.</span></span>

## <span data-ttu-id="81bd8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81bd8-112">PARAMETERS</span></span>

### <span data-ttu-id="81bd8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81bd8-113">-DefaultProfile</span></span>
<span data-ttu-id="81bd8-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="81bd8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81bd8-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81bd8-115">-InputObject</span></span>
<span data-ttu-id="81bd8-116">Eingabeobjekt aus pipeline.</span><span class="sxs-lookup"><span data-stu-id="81bd8-116">Input object from pipeline.</span></span>

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

### <span data-ttu-id="81bd8-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="81bd8-117">-SmartGroupId</span></span>
<span data-ttu-id="81bd8-118">Eindeutiger Bezeichner der SmartGroup/ResourceId der Warnung.</span><span class="sxs-lookup"><span data-stu-id="81bd8-118">Unique Identifier of SmartGroup / ResourceId of alert.</span></span>

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

### <span data-ttu-id="81bd8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81bd8-119">CommonParameters</span></span>
<span data-ttu-id="81bd8-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81bd8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81bd8-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81bd8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81bd8-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="81bd8-122">INPUTS</span></span>

### <span data-ttu-id="81bd8-123">Keine</span><span class="sxs-lookup"><span data-stu-id="81bd8-123">None</span></span>

## <span data-ttu-id="81bd8-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="81bd8-124">OUTPUTS</span></span>

### <span data-ttu-id="81bd8-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSQuantGroupModification</span><span class="sxs-lookup"><span data-stu-id="81bd8-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span></span>

## <span data-ttu-id="81bd8-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="81bd8-126">NOTES</span></span>

## <span data-ttu-id="81bd8-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="81bd8-127">RELATED LINKS</span></span>
