---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsettingcategory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
ms.openlocfilehash: 2d1c4b2f272516af31fba17db50d33991dd1db50
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470397"
---
# <span data-ttu-id="7f638-101">Get-AzDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="7f638-101">Get-AzDiagnosticSettingCategory</span></span>

## <span data-ttu-id="7f638-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f638-102">SYNOPSIS</span></span>
<span data-ttu-id="7f638-103">Erhalten oder Auflisten der unterstützten Diagnoseeinstellungskategorie für die Azure-Ressource.</span><span class="sxs-lookup"><span data-stu-id="7f638-103">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="7f638-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f638-104">SYNTAX</span></span>

```
Get-AzDiagnosticSettingCategory -TargetResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f638-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f638-105">DESCRIPTION</span></span>
<span data-ttu-id="7f638-106">Erhalten oder Auflisten der unterstützten Diagnoseeinstellungskategorie für die Azure-Ressource.</span><span class="sxs-lookup"><span data-stu-id="7f638-106">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="7f638-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7f638-107">EXAMPLES</span></span>

### <span data-ttu-id="7f638-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7f638-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiagnosticSetting -TargetResourceId -TargetResourceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX
Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/VMProtectionAlerts
Name         : VMProtectionAlerts
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Logs

Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/AllMetrics
Name         : AllMetrics
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Metrics
```

<span data-ttu-id="7f638-109">Holen Sie sich unterstützte Diagnoseeinstellungskategorien für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="7f638-109">Get supported diagnostic setting categories for virtual network.</span></span>

## <span data-ttu-id="7f638-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f638-110">PARAMETERS</span></span>

### <span data-ttu-id="7f638-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f638-111">-DefaultProfile</span></span>
<span data-ttu-id="7f638-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f638-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f638-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7f638-113">-Name</span></span>
<span data-ttu-id="7f638-114">Name der Kategorie für Diagnoseeinstellungen</span><span class="sxs-lookup"><span data-stu-id="7f638-114">Name of diagnostic setting category</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f638-115">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="7f638-115">-TargetResourceId</span></span>
<span data-ttu-id="7f638-116">Zielressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="7f638-116">Target resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f638-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f638-117">CommonParameters</span></span>
<span data-ttu-id="7f638-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f638-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f638-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f638-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f638-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7f638-120">INPUTS</span></span>

### <span data-ttu-id="7f638-121">System.String</span><span class="sxs-lookup"><span data-stu-id="7f638-121">System.String</span></span>

## <span data-ttu-id="7f638-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7f638-122">OUTPUTS</span></span>

### <span data-ttu-id="7f638-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="7f638-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span></span>

## <span data-ttu-id="7f638-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7f638-124">NOTES</span></span>

## <span data-ttu-id="7f638-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7f638-125">RELATED LINKS</span></span>
