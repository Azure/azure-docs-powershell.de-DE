---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
ms.openlocfilehash: b3bb193b47acf0f77851e5b9f4549d455a568b15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167028"
---
# <span data-ttu-id="8fdec-101">Get-AzSmartGroup</span><span class="sxs-lookup"><span data-stu-id="8fdec-101">Get-AzSmartGroup</span></span>

## <span data-ttu-id="8fdec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fdec-102">SYNOPSIS</span></span>
<span data-ttu-id="8fdec-103">Ruft Informationen zu intelligenten Gruppen ab</span><span class="sxs-lookup"><span data-stu-id="8fdec-103">Gets Smart Groups information</span></span>

## <span data-ttu-id="8fdec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8fdec-104">SYNTAX</span></span>

### <span data-ttu-id="8fdec-105">SmartGroupsListByFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="8fdec-105">SmartGroupsListByFilter (Default)</span></span>
```
Get-AzSmartGroup [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fdec-106">SmartGroupById</span><span class="sxs-lookup"><span data-stu-id="8fdec-106">SmartGroupById</span></span>
```
Get-AzSmartGroup -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fdec-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8fdec-107">DESCRIPTION</span></span>
<span data-ttu-id="8fdec-108">**Das Cmdlet "Get-AzLetsGroup"** ruft Intelligente Gruppeninformationen ab.</span><span class="sxs-lookup"><span data-stu-id="8fdec-108">**Get-AzSmartGroup** cmdlet gets smart groups information.</span></span>

## <span data-ttu-id="8fdec-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8fdec-109">EXAMPLES</span></span>

### <span data-ttu-id="8fdec-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8fdec-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroup -TimeRange "1h"
```

<span data-ttu-id="8fdec-111">Listet alle intelligenten Gruppen auf, die in der letzten Stunde gebildet wurden.</span><span class="sxs-lookup"><span data-stu-id="8fdec-111">List all smart groups formed in last 1 hour.</span></span> <span data-ttu-id="8fdec-112">Verwenden Format-List, um die vollständigen Details jeder intelligenten Gruppe in der Liste zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8fdec-112">Use Format-List to get the complete details of each smart group in list.</span></span>

### <span data-ttu-id="8fdec-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8fdec-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSmartGroup -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="8fdec-114">Smart Group Details nach ID (GUID) oder Ressourcen-ID (Complete ARM ID) erhalten</span><span class="sxs-lookup"><span data-stu-id="8fdec-114">Get Smart Group details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="8fdec-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8fdec-115">PARAMETERS</span></span>

### <span data-ttu-id="8fdec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fdec-116">-DefaultProfile</span></span>
<span data-ttu-id="8fdec-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8fdec-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fdec-118">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="8fdec-118">-SmartGroupId</span></span>
<span data-ttu-id="8fdec-119">Eindeutiger Bezeichner von SmartGroup/ResourceId von SmartGroup.</span><span class="sxs-lookup"><span data-stu-id="8fdec-119">Unique Identifier of SmartGroup / ResourceId of SmartGroup.</span></span>

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

### <span data-ttu-id="8fdec-120">-SortBy</span><span class="sxs-lookup"><span data-stu-id="8fdec-120">-SortBy</span></span>
<span data-ttu-id="8fdec-121">Warnungseigenschaft, die beim Sortieren verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="8fdec-121">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="8fdec-122">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="8fdec-122">-SortOrder</span></span>
<span data-ttu-id="8fdec-123">Sortierreihenfolge</span><span class="sxs-lookup"><span data-stu-id="8fdec-123">Sort Order</span></span>

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

### <span data-ttu-id="8fdec-124">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="8fdec-124">-TimeRange</span></span>
<span data-ttu-id="8fdec-125">Unterstützte Zeitbereichswerte – 1h, 1d, 7d, 30d (Standard ist 1d)</span><span class="sxs-lookup"><span data-stu-id="8fdec-125">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="8fdec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fdec-126">CommonParameters</span></span>
<span data-ttu-id="8fdec-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fdec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fdec-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8fdec-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fdec-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8fdec-129">INPUTS</span></span>

### <span data-ttu-id="8fdec-130">Keine</span><span class="sxs-lookup"><span data-stu-id="8fdec-130">None</span></span>

## <span data-ttu-id="8fdec-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8fdec-131">OUTPUTS</span></span>

### <span data-ttu-id="8fdec-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PS1Group</span><span class="sxs-lookup"><span data-stu-id="8fdec-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="8fdec-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8fdec-133">NOTES</span></span>

## <span data-ttu-id="8fdec-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8fdec-134">RELATED LINKS</span></span>
