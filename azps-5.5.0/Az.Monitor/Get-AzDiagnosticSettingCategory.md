---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsettingcategory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
ms.openlocfilehash: 29c65ef5f5ec3b2b54fb883da706ddc9a38e1d4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147409"
---
# <span data-ttu-id="1defc-101">Get-AzDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="1defc-101">Get-AzDiagnosticSettingCategory</span></span>

## <span data-ttu-id="1defc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1defc-102">SYNOPSIS</span></span>
<span data-ttu-id="1defc-103">Erhalten oder Auflisten der unterstützten Diagnoseeinstellungskategorie für die Azure-Ressource.</span><span class="sxs-lookup"><span data-stu-id="1defc-103">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="1defc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1defc-104">SYNTAX</span></span>

```
Get-AzDiagnosticSettingCategory -TargetResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1defc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1defc-105">DESCRIPTION</span></span>
<span data-ttu-id="1defc-106">Erhalten oder Auflisten der unterstützten Diagnoseeinstellungskategorie für die Azure-Ressource.</span><span class="sxs-lookup"><span data-stu-id="1defc-106">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="1defc-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1defc-107">EXAMPLES</span></span>

### <span data-ttu-id="1defc-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1defc-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiagnosticSettingCategory -TargetResourceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX
Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/VMProtectionAlerts
Name         : VMProtectionAlerts
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Logs

Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/AllMetrics
Name         : AllMetrics
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Metrics
```

<span data-ttu-id="1defc-109">Holen Sie sich unterstützte Diagnoseeinstellungskategorien für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="1defc-109">Get supported diagnostic setting categories for virtual network.</span></span>

## <span data-ttu-id="1defc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1defc-110">PARAMETERS</span></span>

### <span data-ttu-id="1defc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1defc-111">-DefaultProfile</span></span>
<span data-ttu-id="1defc-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1defc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1defc-113">-Name</span><span class="sxs-lookup"><span data-stu-id="1defc-113">-Name</span></span>
<span data-ttu-id="1defc-114">Name der Kategorie für Diagnoseeinstellungen</span><span class="sxs-lookup"><span data-stu-id="1defc-114">Name of diagnostic setting category</span></span>

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

### <span data-ttu-id="1defc-115">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="1defc-115">-TargetResourceId</span></span>
<span data-ttu-id="1defc-116">Zielressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="1defc-116">Target resource Id</span></span>

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

### <span data-ttu-id="1defc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1defc-117">CommonParameters</span></span>
<span data-ttu-id="1defc-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1defc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1defc-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1defc-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1defc-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1defc-120">INPUTS</span></span>

### <span data-ttu-id="1defc-121">System.String</span><span class="sxs-lookup"><span data-stu-id="1defc-121">System.String</span></span>

## <span data-ttu-id="1defc-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1defc-122">OUTPUTS</span></span>

### <span data-ttu-id="1defc-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="1defc-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span></span>

## <span data-ttu-id="1defc-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1defc-124">NOTES</span></span>

## <span data-ttu-id="1defc-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1defc-125">RELATED LINKS</span></span>
