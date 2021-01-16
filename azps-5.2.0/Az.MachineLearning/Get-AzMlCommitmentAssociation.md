---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
ms.openlocfilehash: 415645b1b4c1d0094b1466d833a29aa10b2b83b8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300179"
---
# <span data-ttu-id="3607b-101">Get-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="3607b-101">Get-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="3607b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3607b-102">SYNOPSIS</span></span>
<span data-ttu-id="3607b-103">Ruft die zusammenfassenden Informationen für eine oder mehrere Verpflichtungszuordnungen ab.</span><span class="sxs-lookup"><span data-stu-id="3607b-103">Retrieves the summary information for one or more commitment associations.</span></span>

## <span data-ttu-id="3607b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3607b-104">SYNTAX</span></span>

```
Get-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3607b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3607b-105">DESCRIPTION</span></span>
<span data-ttu-id="3607b-106">Ruft Informationen zur Verpflichtungs zuordnung ab.</span><span class="sxs-lookup"><span data-stu-id="3607b-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="3607b-107">Je nach den übergebenen Parametern gibt das Cmdlet eine bestimmte Verpflichtungszuordnung oder eine Sammlung von Verpflichtungszuordnungen für den angegebenen Verpflichtungsplan zurück.</span><span class="sxs-lookup"><span data-stu-id="3607b-107">Depending on the parameters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="3607b-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3607b-108">EXAMPLES</span></span>

### <span data-ttu-id="3607b-109">Beispiel 1: Erhalten einer bestimmten Verpflichtungs zuordnung</span><span class="sxs-lookup"><span data-stu-id="3607b-109">Example 1: Get a specific commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="3607b-110">Beispiel 2: Alle Verpflichtungszuordnungen für den angegebenen Verpflichtungsplan erhalten</span><span class="sxs-lookup"><span data-stu-id="3607b-110">Example 2: Get all commitment associations for the specified commitment plan</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="3607b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3607b-111">PARAMETERS</span></span>

### <span data-ttu-id="3607b-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="3607b-112">-CommitmentPlanName</span></span>
<span data-ttu-id="3607b-113">Der Name des Azure ML-Verpflichtungsplans, der über mindestens eine Verpflichtungszuordnung verfügt.</span><span class="sxs-lookup"><span data-stu-id="3607b-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="3607b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3607b-114">-DefaultProfile</span></span>
<span data-ttu-id="3607b-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3607b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3607b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="3607b-116">-Name</span></span>
<span data-ttu-id="3607b-117">Der Name der Azure ML-Verpflichtungs zuordnung.</span><span class="sxs-lookup"><span data-stu-id="3607b-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="3607b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3607b-118">-ResourceGroupName</span></span>
<span data-ttu-id="3607b-119">Der Name der Ressourcengruppe für die Azure ML-Verpflichtungszuordnung.</span><span class="sxs-lookup"><span data-stu-id="3607b-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="3607b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3607b-120">CommonParameters</span></span>
<span data-ttu-id="3607b-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3607b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3607b-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3607b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3607b-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3607b-123">INPUTS</span></span>

### <span data-ttu-id="3607b-124">Keine</span><span class="sxs-lookup"><span data-stu-id="3607b-124">None</span></span>

## <span data-ttu-id="3607b-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3607b-125">OUTPUTS</span></span>

### <span data-ttu-id="3607b-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="3607b-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="3607b-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3607b-127">NOTES</span></span>
<span data-ttu-id="3607b-128">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="3607b-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="3607b-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3607b-129">RELATED LINKS</span></span>
