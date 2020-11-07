---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: c80278e460368ca6ec78efb4f5e74e456816df47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665031"
---
# <span data-ttu-id="5df1e-101">Get-AzureRmMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="5df1e-101">Get-AzureRmMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="5df1e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5df1e-102">SYNOPSIS</span></span>
<span data-ttu-id="5df1e-103">Ruft Nutzungs Verlaufsinformationen für einen angegebenen obligoplan ab.</span><span class="sxs-lookup"><span data-stu-id="5df1e-103">Retrieves usage history information for a specified commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5df1e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5df1e-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5df1e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5df1e-105">DESCRIPTION</span></span>
<span data-ttu-id="5df1e-106">Ruft Nutzungs Verlaufsinformationen für einen angegebenen obligoplan ab, einschließlich der verwendeten Ressourcen und der im Plan verbleibenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="5df1e-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="5df1e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5df1e-107">EXAMPLES</span></span>

### <span data-ttu-id="5df1e-108">--------------------------Beispiel 1: Abrufen des Verwendungs Verlaufs für einen bestimmten Verpflichtungs Plan--------------------------</span><span class="sxs-lookup"><span data-stu-id="5df1e-108">--------------------------  Example 1: Get usage history for a specific commitment plan  --------------------------</span></span>
<span data-ttu-id="5df1e-109">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="5df1e-109">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="5df1e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5df1e-110">PARAMETERS</span></span>

### <span data-ttu-id="5df1e-111">-Name</span><span class="sxs-lookup"><span data-stu-id="5df1e-111">-Name</span></span>
<span data-ttu-id="5df1e-112">Der Name des Azure-ml-obligoplan.</span><span class="sxs-lookup"><span data-stu-id="5df1e-112">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="5df1e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5df1e-113">-ResourceGroupName</span></span>
<span data-ttu-id="5df1e-114">Der Name der Ressourcengruppe für den Azure-ml-Verpflichtungs Plan.</span><span class="sxs-lookup"><span data-stu-id="5df1e-114">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="5df1e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5df1e-115">-DefaultProfile</span></span>
<span data-ttu-id="5df1e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5df1e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df1e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5df1e-117">CommonParameters</span></span>
<span data-ttu-id="5df1e-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5df1e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5df1e-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5df1e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5df1e-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5df1e-120">INPUTS</span></span>

## <span data-ttu-id="5df1e-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5df1e-121">OUTPUTS</span></span>

### <span data-ttu-id="5df1e-122">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. PlanUsageHistory []</span><span class="sxs-lookup"><span data-stu-id="5df1e-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory[]</span></span>

## <span data-ttu-id="5df1e-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="5df1e-123">NOTES</span></span>
<span data-ttu-id="5df1e-124">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="5df1e-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="5df1e-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5df1e-125">RELATED LINKS</span></span>

