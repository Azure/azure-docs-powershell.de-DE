---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
ms.openlocfilehash: b3bb193b47acf0f77851e5b9f4549d455a568b15
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361849"
---
# <span data-ttu-id="47131-101">Get-AzSmartGroup</span><span class="sxs-lookup"><span data-stu-id="47131-101">Get-AzSmartGroup</span></span>

## <span data-ttu-id="47131-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47131-102">SYNOPSIS</span></span>
<span data-ttu-id="47131-103">Ruft Informationen zu intelligenten Gruppen ab</span><span class="sxs-lookup"><span data-stu-id="47131-103">Gets Smart Groups information</span></span>

## <span data-ttu-id="47131-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47131-104">SYNTAX</span></span>

### <span data-ttu-id="47131-105">SmartGroupsListByFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="47131-105">SmartGroupsListByFilter (Default)</span></span>
```
Get-AzSmartGroup [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47131-106">SmartGroupById</span><span class="sxs-lookup"><span data-stu-id="47131-106">SmartGroupById</span></span>
```
Get-AzSmartGroup -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47131-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47131-107">DESCRIPTION</span></span>
<span data-ttu-id="47131-108">**Das Cmdlet "Get-AzLetsGroup"** ruft Intelligente Gruppeninformationen ab.</span><span class="sxs-lookup"><span data-stu-id="47131-108">**Get-AzSmartGroup** cmdlet gets smart groups information.</span></span>

## <span data-ttu-id="47131-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="47131-109">EXAMPLES</span></span>

### <span data-ttu-id="47131-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="47131-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroup -TimeRange "1h"
```

<span data-ttu-id="47131-111">Listet alle intelligenten Gruppen auf, die in der letzten Stunde gebildet wurden.</span><span class="sxs-lookup"><span data-stu-id="47131-111">List all smart groups formed in last 1 hour.</span></span> <span data-ttu-id="47131-112">Verwenden Format-List, um die vollständigen Details jeder intelligenten Gruppe in der Liste zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="47131-112">Use Format-List to get the complete details of each smart group in list.</span></span>

### <span data-ttu-id="47131-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="47131-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSmartGroup -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="47131-114">Smart Group Details nach ID (GUID) oder Ressourcen-ID (Complete ARM ID) erhalten</span><span class="sxs-lookup"><span data-stu-id="47131-114">Get Smart Group details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="47131-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47131-115">PARAMETERS</span></span>

### <span data-ttu-id="47131-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47131-116">-DefaultProfile</span></span>
<span data-ttu-id="47131-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47131-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47131-118">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="47131-118">-SmartGroupId</span></span>
<span data-ttu-id="47131-119">Eindeutiger Bezeichner von SmartGroup/ResourceId von SmartGroup.</span><span class="sxs-lookup"><span data-stu-id="47131-119">Unique Identifier of SmartGroup / ResourceId of SmartGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47131-120">-SortBy</span><span class="sxs-lookup"><span data-stu-id="47131-120">-SortBy</span></span>
<span data-ttu-id="47131-121">Warnungseigenschaft, die beim Sortieren verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="47131-121">Alert property to use while sorting</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47131-122">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="47131-122">-SortOrder</span></span>
<span data-ttu-id="47131-123">Sortierreihenfolge</span><span class="sxs-lookup"><span data-stu-id="47131-123">Sort Order</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47131-124">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="47131-124">-TimeRange</span></span>
<span data-ttu-id="47131-125">Unterstützte Zeitbereichswerte – 1h, 1d, 7d, 30d (Standard ist 1d)</span><span class="sxs-lookup"><span data-stu-id="47131-125">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47131-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47131-126">CommonParameters</span></span>
<span data-ttu-id="47131-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47131-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47131-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47131-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47131-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="47131-129">INPUTS</span></span>

### <span data-ttu-id="47131-130">Keine</span><span class="sxs-lookup"><span data-stu-id="47131-130">None</span></span>

## <span data-ttu-id="47131-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="47131-131">OUTPUTS</span></span>

### <span data-ttu-id="47131-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PS1Group</span><span class="sxs-lookup"><span data-stu-id="47131-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="47131-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="47131-133">NOTES</span></span>

## <span data-ttu-id="47131-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="47131-134">RELATED LINKS</span></span>
