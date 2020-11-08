---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
ms.openlocfilehash: b3bb193b47acf0f77851e5b9f4549d455a568b15
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176493"
---
# <span data-ttu-id="c94c9-101">Get-AzSmartGroup</span><span class="sxs-lookup"><span data-stu-id="c94c9-101">Get-AzSmartGroup</span></span>

## <span data-ttu-id="c94c9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c94c9-102">SYNOPSIS</span></span>
<span data-ttu-id="c94c9-103">Ruft Informationen zu intelligenten Gruppen ab</span><span class="sxs-lookup"><span data-stu-id="c94c9-103">Gets Smart Groups information</span></span>

## <span data-ttu-id="c94c9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c94c9-104">SYNTAX</span></span>

### <span data-ttu-id="c94c9-105">SmartGroupsListByFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="c94c9-105">SmartGroupsListByFilter (Default)</span></span>
```
Get-AzSmartGroup [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c94c9-106">SmartGroupById</span><span class="sxs-lookup"><span data-stu-id="c94c9-106">SmartGroupById</span></span>
```
Get-AzSmartGroup -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c94c9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c94c9-107">DESCRIPTION</span></span>
<span data-ttu-id="c94c9-108">Das Cmdlet " **Get-AzSmartGroup** " Ruft Informationen zu Smart Groups ab.</span><span class="sxs-lookup"><span data-stu-id="c94c9-108">**Get-AzSmartGroup** cmdlet gets smart groups information.</span></span>

## <span data-ttu-id="c94c9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c94c9-109">EXAMPLES</span></span>

### <span data-ttu-id="c94c9-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c94c9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroup -TimeRange "1h"
```

<span data-ttu-id="c94c9-111">Auflisten aller intelligenten Gruppen, die in der letzten 1 Stunde gebildet wurden</span><span class="sxs-lookup"><span data-stu-id="c94c9-111">List all smart groups formed in last 1 hour.</span></span> <span data-ttu-id="c94c9-112">Verwenden Sie Format-List, um die vollständigen Details jeder intelligenten Gruppe in der Liste abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c94c9-112">Use Format-List to get the complete details of each smart group in list.</span></span>

### <span data-ttu-id="c94c9-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c94c9-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSmartGroup -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="c94c9-114">Abrufen intelligenter Gruppendetails nach ID (GUID) oder Ressourcen-ID (vollständige Arm-ID)</span><span class="sxs-lookup"><span data-stu-id="c94c9-114">Get Smart Group details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="c94c9-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c94c9-115">PARAMETERS</span></span>

### <span data-ttu-id="c94c9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c94c9-116">-DefaultProfile</span></span>
<span data-ttu-id="c94c9-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c94c9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c94c9-118">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="c94c9-118">-SmartGroupId</span></span>
<span data-ttu-id="c94c9-119">Eindeutiger Bezeichner der smartgroup/Resourcen-ID von smartgroup.</span><span class="sxs-lookup"><span data-stu-id="c94c9-119">Unique Identifier of SmartGroup / ResourceId of SmartGroup.</span></span>

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

### <span data-ttu-id="c94c9-120">-Ordnennach</span><span class="sxs-lookup"><span data-stu-id="c94c9-120">-SortBy</span></span>
<span data-ttu-id="c94c9-121">Benachrichtigungs Eigenschaft, die beim Sortieren verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="c94c9-121">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="c94c9-122">-Sortierreihenfolge</span><span class="sxs-lookup"><span data-stu-id="c94c9-122">-SortOrder</span></span>
<span data-ttu-id="c94c9-123">Sortierreihenfolge</span><span class="sxs-lookup"><span data-stu-id="c94c9-123">Sort Order</span></span>

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

### <span data-ttu-id="c94c9-124">-Zeitraum</span><span class="sxs-lookup"><span data-stu-id="c94c9-124">-TimeRange</span></span>
<span data-ttu-id="c94c9-125">Unterstützte Zeitbereichs Werte – 1H, 1D, 7D, 30D (Standard ist 1D)</span><span class="sxs-lookup"><span data-stu-id="c94c9-125">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="c94c9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c94c9-126">CommonParameters</span></span>
<span data-ttu-id="c94c9-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c94c9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c94c9-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c94c9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c94c9-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c94c9-129">INPUTS</span></span>

### <span data-ttu-id="c94c9-130">Keine</span><span class="sxs-lookup"><span data-stu-id="c94c9-130">None</span></span>

## <span data-ttu-id="c94c9-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c94c9-131">OUTPUTS</span></span>

### <span data-ttu-id="c94c9-132">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="c94c9-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="c94c9-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="c94c9-133">NOTES</span></span>

## <span data-ttu-id="c94c9-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c94c9-134">RELATED LINKS</span></span>
