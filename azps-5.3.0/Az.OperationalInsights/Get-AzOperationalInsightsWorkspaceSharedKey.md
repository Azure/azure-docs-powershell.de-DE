---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacesharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
ms.openlocfilehash: 75c69c96b82cf71aa71d4ac89bb10c064af1f4f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473319"
---
# <span data-ttu-id="69215-101">Get-AzOperationalInsightsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="69215-101">Get-AzOperationalInsightsWorkspaceSharedKey</span></span>

## <span data-ttu-id="69215-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69215-102">SYNOPSIS</span></span>
<span data-ttu-id="69215-103">Ruft die freigegebenen Schlüssel für einen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="69215-103">Gets the shared keys for a workspace.</span></span>

## <span data-ttu-id="69215-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69215-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceSharedKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69215-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69215-105">DESCRIPTION</span></span>
<span data-ttu-id="69215-106">Im **Cmdlet "Get-AzOperationalInsightsWorkspaceSharedKey"** werden die freigegebenen Schlüssel für einen Arbeitsbereich aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="69215-106">The **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="69215-107">Die Schlüssel werden verwendet, um Operational Insights Agents mit dem Arbeitsbereich zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="69215-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="69215-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="69215-108">EXAMPLES</span></span>

### <span data-ttu-id="69215-109">Beispiel 1: Erhalten freigegebener Schlüssel nach Dem Namen des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="69215-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="69215-110">Dieser Befehl ruft die freigegebenen Schlüssel für den Arbeitsbereich mit dem Namen "MyWorkspace" in der Ressourcengruppe "ContosoResourceGroup" ab.</span><span class="sxs-lookup"><span data-stu-id="69215-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="69215-111">Beispiel 2: Erhalten freigegebener Schlüssel mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="69215-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceSharedKey
```

<span data-ttu-id="69215-112">Dieser Befehl ruft den Arbeitsbereich namens "MyWorkspace" mithilfe des Cmdlets Get-AzOperationalInsightsWorkspace ab und übergibt den Arbeitsbereich dann an das **Cmdlet "Get-AzOperationalInsightsWorkspaceSharedKey".**</span><span class="sxs-lookup"><span data-stu-id="69215-112">This command gets the workspace named MyWorkspace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet.</span></span>
<span data-ttu-id="69215-113">Der Befehl ruft die freigegebenen Schlüssel für diesen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="69215-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="69215-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69215-114">PARAMETERS</span></span>

### <span data-ttu-id="69215-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69215-115">-DefaultProfile</span></span>
<span data-ttu-id="69215-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="69215-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69215-117">-Name</span><span class="sxs-lookup"><span data-stu-id="69215-117">-Name</span></span>
<span data-ttu-id="69215-118">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="69215-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69215-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69215-119">-ResourceGroupName</span></span>
<span data-ttu-id="69215-120">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="69215-120">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69215-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69215-121">CommonParameters</span></span>
<span data-ttu-id="69215-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69215-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69215-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69215-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69215-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="69215-124">INPUTS</span></span>

### <span data-ttu-id="69215-125">System.String</span><span class="sxs-lookup"><span data-stu-id="69215-125">System.String</span></span>

## <span data-ttu-id="69215-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="69215-126">OUTPUTS</span></span>

### <span data-ttu-id="69215-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="69215-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="69215-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="69215-128">NOTES</span></span>

## <span data-ttu-id="69215-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="69215-129">RELATED LINKS</span></span>

[<span data-ttu-id="69215-130">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="69215-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="69215-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="69215-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


