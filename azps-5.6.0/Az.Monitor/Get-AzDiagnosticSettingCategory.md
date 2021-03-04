---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azdiagnosticsettingcategory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
ms.openlocfilehash: df263698a913faf361e5f23bb12d0267be314106
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932643"
---
# <span data-ttu-id="f3c52-101">Get-AzDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="f3c52-101">Get-AzDiagnosticSettingCategory</span></span>

## <span data-ttu-id="f3c52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3c52-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c52-103">Hier können Sie unterstützte Diagnoseeinstellungskategorie für die Azure-Ressource erhalten oder auflisten.</span><span class="sxs-lookup"><span data-stu-id="f3c52-103">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="f3c52-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3c52-104">SYNTAX</span></span>

```
Get-AzDiagnosticSettingCategory -TargetResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3c52-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f3c52-105">DESCRIPTION</span></span>
<span data-ttu-id="f3c52-106">Hier können Sie unterstützte Diagnoseeinstellungskategorie für die Azure-Ressource erhalten oder auflisten.</span><span class="sxs-lookup"><span data-stu-id="f3c52-106">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="f3c52-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f3c52-107">EXAMPLES</span></span>

### <span data-ttu-id="f3c52-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f3c52-108">Example 1</span></span>
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

<span data-ttu-id="f3c52-109">Erhalten Sie unterstützte Diagnoseeinstellungskategorien für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="f3c52-109">Get supported diagnostic setting categories for virtual network.</span></span>

## <span data-ttu-id="f3c52-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f3c52-110">PARAMETERS</span></span>

### <span data-ttu-id="f3c52-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3c52-111">-DefaultProfile</span></span>
<span data-ttu-id="f3c52-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3c52-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3c52-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f3c52-113">-Name</span></span>
<span data-ttu-id="f3c52-114">Name der Diagnoseeinstellungskategorie</span><span class="sxs-lookup"><span data-stu-id="f3c52-114">Name of diagnostic setting category</span></span>

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

### <span data-ttu-id="f3c52-115">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f3c52-115">-TargetResourceId</span></span>
<span data-ttu-id="f3c52-116">Zielressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="f3c52-116">Target resource Id</span></span>

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

### <span data-ttu-id="f3c52-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c52-117">CommonParameters</span></span>
<span data-ttu-id="f3c52-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3c52-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c52-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3c52-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c52-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f3c52-120">INPUTS</span></span>

### <span data-ttu-id="f3c52-121">System.String</span><span class="sxs-lookup"><span data-stu-id="f3c52-121">System.String</span></span>

## <span data-ttu-id="f3c52-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f3c52-122">OUTPUTS</span></span>

### <span data-ttu-id="f3c52-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="f3c52-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span></span>

## <span data-ttu-id="f3c52-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f3c52-124">NOTES</span></span>

## <span data-ttu-id="f3c52-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f3c52-125">RELATED LINKS</span></span>
