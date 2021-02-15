---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
ms.openlocfilehash: 1e2f1daa222714c23f394d362222f9ef1fd1bde4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167145"
---
# <span data-ttu-id="899b9-101">Get-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="899b9-101">Get-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="899b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="899b9-102">SYNOPSIS</span></span>
<span data-ttu-id="899b9-103">Holen Sie sich die Azure Advisor-Konfigurationen für das angegebene Abonnement oder die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="899b9-103">Get the Azure Advisor configurations for the given subscription or resource group.</span></span>

## <span data-ttu-id="899b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="899b9-104">SYNTAX</span></span>

```
Get-AzAdvisorConfiguration [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="899b9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="899b9-105">DESCRIPTION</span></span>
<span data-ttu-id="899b9-106">Die einem Abonnement zugeordneten Konfigurationen haben zwei Typen:</span><span class="sxs-lookup"><span data-stu-id="899b9-106">The configurations associated with a subscription have two types:</span></span>

<span data-ttu-id="899b9-107">Konfiguration auf Abonnementebene: Für ein Abonnement kann es nur eine Konfiguration dieses Typs geben.</span><span class="sxs-lookup"><span data-stu-id="899b9-107">Subscription level configuration: There can be only one configuration of this type for a subscription.</span></span> <span data-ttu-id="899b9-108">"LowCpuThreshold" und "Exclude" sind die einzige Eigenschaft dieses Konfigurationstyps.</span><span class="sxs-lookup"><span data-stu-id="899b9-108">LowCpuThreshold and Exclude are the only property of this type of configuration.</span></span>

<span data-ttu-id="899b9-109">Konfiguration auf Ressourcengruppenebene: In einem Abonnement kann es nur eine Konfiguration für jede Ressourcengruppe gibt.</span><span class="sxs-lookup"><span data-stu-id="899b9-109">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup in a subscription.</span></span> <span data-ttu-id="899b9-110">"Exclude" ist die einzige Eigenschaft dieses Konfigurationstyps.</span><span class="sxs-lookup"><span data-stu-id="899b9-110">Exclude is the only property of this type of configuration.</span></span>

## <span data-ttu-id="899b9-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="899b9-111">EXAMPLES</span></span>

### <span data-ttu-id="899b9-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="899b9-112">Example 1</span></span>
```powershell
PS C:\>$data = Get-AzAdvisorConfiguration
Id         : /subscriptions/{user_subscription}/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationProperties
Type       : Microsoft.Advisor/Configurations

Id         : /subscriptions/{user_subscription}/providers/Microsoft.Advisor/configurations/{user_subscription}-{resourceGroupName}
Name       : {user_subscription}-{resourceGroupName}
Properties : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationProperties
Type       : Microsoft.Advisor/Configurations

PS C:\>$data[0].Properties
AdditionalProperties :
Exclude              : False
LowCpuThreshold      : 20

PS C:\>$data[1].Properties
AdditionalProperties :
Exclude              : True
LowCpuThreshold      : null

```
<span data-ttu-id="899b9-113">Ruft eine Liste der Azure Advisor Configuration(s) ab.</span><span class="sxs-lookup"><span data-stu-id="899b9-113">Retrieves a list of Azure Advisor Configuration(s).</span></span>

## <span data-ttu-id="899b9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="899b9-114">PARAMETERS</span></span>

### <span data-ttu-id="899b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="899b9-115">-DefaultProfile</span></span>
<span data-ttu-id="899b9-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="899b9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="899b9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="899b9-117">-ResourceGroupName</span></span>
<span data-ttu-id="899b9-118">Ressourcengruppenname der Konfiguration</span><span class="sxs-lookup"><span data-stu-id="899b9-118">Resource Group name of the configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="899b9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="899b9-119">CommonParameters</span></span>
<span data-ttu-id="899b9-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="899b9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="899b9-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="899b9-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="899b9-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="899b9-122">INPUTS</span></span>

### <span data-ttu-id="899b9-123">Keine</span><span class="sxs-lookup"><span data-stu-id="899b9-123">None</span></span>

## <span data-ttu-id="899b9-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="899b9-124">OUTPUTS</span></span>

### <span data-ttu-id="899b9-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="899b9-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="899b9-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="899b9-126">NOTES</span></span>

## <span data-ttu-id="899b9-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="899b9-127">RELATED LINKS</span></span>
