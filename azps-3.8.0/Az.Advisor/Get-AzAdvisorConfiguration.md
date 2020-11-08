---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
ms.openlocfilehash: 1e2f1daa222714c23f394d362222f9ef1fd1bde4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996683"
---
# <span data-ttu-id="ee77a-101">Get-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="ee77a-101">Get-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="ee77a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ee77a-102">SYNOPSIS</span></span>
<span data-ttu-id="ee77a-103">Rufen Sie die Azure Advisor-Konfigurationen für das angegebene Abonnement oder die angegebene Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="ee77a-103">Get the Azure Advisor configurations for the given subscription or resource group.</span></span>

## <span data-ttu-id="ee77a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee77a-104">SYNTAX</span></span>

```
Get-AzAdvisorConfiguration [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee77a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee77a-105">DESCRIPTION</span></span>
<span data-ttu-id="ee77a-106">Die einem Abonnement zugeordneten Konfigurationen haben zwei Typen:</span><span class="sxs-lookup"><span data-stu-id="ee77a-106">The configurations associated with a subscription have two types:</span></span>

<span data-ttu-id="ee77a-107">Konfiguration auf Abonnementebene: für ein Abonnement kann nur eine Konfiguration dieses Typs vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="ee77a-107">Subscription level configuration: There can be only one configuration of this type for a subscription.</span></span> <span data-ttu-id="ee77a-108">LowCpuThreshold und Exclude sind die einzige Eigenschaft dieser Art von Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ee77a-108">LowCpuThreshold and Exclude are the only property of this type of configuration.</span></span>

<span data-ttu-id="ee77a-109">Konfiguration der ResourceGroup-Ebene: Es kann in einem Abonnement nur eine Konfiguration für jede ResourceGroup geben.</span><span class="sxs-lookup"><span data-stu-id="ee77a-109">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup in a subscription.</span></span> <span data-ttu-id="ee77a-110">Exclude ist die einzige Eigenschaft dieser Art von Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ee77a-110">Exclude is the only property of this type of configuration.</span></span>

## <span data-ttu-id="ee77a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ee77a-111">EXAMPLES</span></span>

### <span data-ttu-id="ee77a-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ee77a-112">Example 1</span></span>
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
<span data-ttu-id="ee77a-113">Ruft eine Liste der Azure Advisor-Konfiguration (en) ab.</span><span class="sxs-lookup"><span data-stu-id="ee77a-113">Retrieves a list of Azure Advisor Configuration(s).</span></span>

## <span data-ttu-id="ee77a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee77a-114">PARAMETERS</span></span>

### <span data-ttu-id="ee77a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee77a-115">-DefaultProfile</span></span>
<span data-ttu-id="ee77a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ee77a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee77a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee77a-117">-ResourceGroupName</span></span>
<span data-ttu-id="ee77a-118">Ressourcengruppenname der Konfiguration</span><span class="sxs-lookup"><span data-stu-id="ee77a-118">Resource Group name of the configuration</span></span>

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

### <span data-ttu-id="ee77a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee77a-119">CommonParameters</span></span>
<span data-ttu-id="ee77a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee77a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ee77a-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee77a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee77a-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ee77a-122">INPUTS</span></span>

### <span data-ttu-id="ee77a-123">Keine</span><span class="sxs-lookup"><span data-stu-id="ee77a-123">None</span></span>

## <span data-ttu-id="ee77a-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ee77a-124">OUTPUTS</span></span>

### <span data-ttu-id="ee77a-125">Microsoft. Azure. Commands. Advisor. Cmdlets. Models. PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="ee77a-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="ee77a-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="ee77a-126">NOTES</span></span>

## <span data-ttu-id="ee77a-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ee77a-127">RELATED LINKS</span></span>
