---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: ce40458262d095f0e1fe58def1cf3d4508a6c6b8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473327"
---
# <span data-ttu-id="cade8-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="cade8-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="cade8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cade8-102">SYNOPSIS</span></span>
<span data-ttu-id="cade8-103">Liste gelöschter Arbeitsbereiche auf.</span><span class="sxs-lookup"><span data-stu-id="cade8-103">List deleted workspaces.</span></span>

## <span data-ttu-id="cade8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cade8-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cade8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cade8-105">DESCRIPTION</span></span>
<span data-ttu-id="cade8-106">Liste gelöschter Arbeitsbereiche auf.</span><span class="sxs-lookup"><span data-stu-id="cade8-106">List deleted workspaces.</span></span>

## <span data-ttu-id="cade8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cade8-107">EXAMPLES</span></span>

### <span data-ttu-id="cade8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cade8-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="cade8-109">Liste gelöschter Arbeitsbereiche auf.</span><span class="sxs-lookup"><span data-stu-id="cade8-109">List deleted workspaces.</span></span>

## <span data-ttu-id="cade8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cade8-110">PARAMETERS</span></span>

### <span data-ttu-id="cade8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cade8-111">-DefaultProfile</span></span>
<span data-ttu-id="cade8-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cade8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cade8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cade8-113">-ResourceGroupName</span></span>
<span data-ttu-id="cade8-114">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cade8-114">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cade8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cade8-115">CommonParameters</span></span>
<span data-ttu-id="cade8-116">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cade8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cade8-117">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cade8-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cade8-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cade8-118">INPUTS</span></span>

### <span data-ttu-id="cade8-119">System.String</span><span class="sxs-lookup"><span data-stu-id="cade8-119">System.String</span></span>

## <span data-ttu-id="cade8-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cade8-120">OUTPUTS</span></span>

### <span data-ttu-id="cade8-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="cade8-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="cade8-122">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cade8-122">NOTES</span></span>

## <span data-ttu-id="cade8-123">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cade8-123">RELATED LINKS</span></span>
