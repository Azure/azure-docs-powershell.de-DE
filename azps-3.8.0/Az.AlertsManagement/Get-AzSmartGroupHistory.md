---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgrouphistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
ms.openlocfilehash: a8e827d678c7ac3b917ee7be09d030b193ffda24
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995905"
---
# <span data-ttu-id="c96fc-101">Get-AzSmartGroupHistory</span><span class="sxs-lookup"><span data-stu-id="c96fc-101">Get-AzSmartGroupHistory</span></span>

## <span data-ttu-id="c96fc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c96fc-102">SYNOPSIS</span></span>
<span data-ttu-id="c96fc-103">Ruft das Smart Group-Protokoll ab</span><span class="sxs-lookup"><span data-stu-id="c96fc-103">Gets smart group history</span></span>

## <span data-ttu-id="c96fc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c96fc-104">SYNTAX</span></span>

### <span data-ttu-id="c96fc-105">BySmartGroupId (Standard)</span><span class="sxs-lookup"><span data-stu-id="c96fc-105">BySmartGroupId (Default)</span></span>
```
Get-AzSmartGroupHistory -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c96fc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c96fc-106">ByInputObject</span></span>
```
Get-AzSmartGroupHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c96fc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c96fc-107">DESCRIPTION</span></span>
<span data-ttu-id="c96fc-108">Das Cmdlet " **Get-AzSmartGroupHistory** " Ruft das intelligente Gruppen Protokoll ab.</span><span class="sxs-lookup"><span data-stu-id="c96fc-108">**Get-AzSmartGroupHistory** cmdlet gets smart group history.</span></span>

## <span data-ttu-id="c96fc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c96fc-109">EXAMPLES</span></span>

### <span data-ttu-id="c96fc-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c96fc-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroupHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="c96fc-111">Ruft Informationen zu intelligenten Gruppen Protokollen ab.</span><span class="sxs-lookup"><span data-stu-id="c96fc-111">Gets smart group history details.</span></span>

## <span data-ttu-id="c96fc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c96fc-112">PARAMETERS</span></span>

### <span data-ttu-id="c96fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c96fc-113">-DefaultProfile</span></span>
<span data-ttu-id="c96fc-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c96fc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c96fc-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c96fc-115">-InputObject</span></span>
<span data-ttu-id="c96fc-116">Eingabeobjekt aus Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c96fc-116">Input object from pipeline.</span></span>

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

### <span data-ttu-id="c96fc-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="c96fc-117">-SmartGroupId</span></span>
<span data-ttu-id="c96fc-118">Eindeutiger Bezeichner von smartgroup/Resourcen of Alert.</span><span class="sxs-lookup"><span data-stu-id="c96fc-118">Unique Identifier of SmartGroup / ResourceId of alert.</span></span>

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

### <span data-ttu-id="c96fc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c96fc-119">CommonParameters</span></span>
<span data-ttu-id="c96fc-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c96fc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c96fc-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c96fc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c96fc-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c96fc-122">INPUTS</span></span>

### <span data-ttu-id="c96fc-123">Keine</span><span class="sxs-lookup"><span data-stu-id="c96fc-123">None</span></span>

## <span data-ttu-id="c96fc-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c96fc-124">OUTPUTS</span></span>

### <span data-ttu-id="c96fc-125">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSSmartGroupModification</span><span class="sxs-lookup"><span data-stu-id="c96fc-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span></span>

## <span data-ttu-id="c96fc-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="c96fc-126">NOTES</span></span>

## <span data-ttu-id="c96fc-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c96fc-127">RELATED LINKS</span></span>
