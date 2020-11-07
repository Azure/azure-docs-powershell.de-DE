---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: e92f32dab72a4a96be03f800297194711f275d70
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "93665415"
---
# <span data-ttu-id="d4af6-101">Get-AzureRmMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="d4af6-101">Get-AzureRmMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="d4af6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4af6-102">SYNOPSIS</span></span>
<span data-ttu-id="d4af6-103">Ruft Nutzungs Verlaufsinformationen für einen angegebenen obligoplan ab.</span><span class="sxs-lookup"><span data-stu-id="d4af6-103">Retrieves usage history information for a specified commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4af6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4af6-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4af6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4af6-105">DESCRIPTION</span></span>
<span data-ttu-id="d4af6-106">Ruft Nutzungs Verlaufsinformationen für einen angegebenen obligoplan ab, einschließlich der verwendeten Ressourcen und der im Plan verbleibenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="d4af6-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="d4af6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4af6-107">EXAMPLES</span></span>

### <span data-ttu-id="d4af6-108">--------------------------Beispiel 1: Abrufen des Verwendungs Verlaufs für einen bestimmten Verpflichtungs Plan--------------------------</span><span class="sxs-lookup"><span data-stu-id="d4af6-108">--------------------------  Example 1: Get usage history for a specific commitment plan  --------------------------</span></span>
```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="d4af6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4af6-109">PARAMETERS</span></span>

### <span data-ttu-id="d4af6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4af6-110">-DefaultProfile</span></span>
<span data-ttu-id="d4af6-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d4af6-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4af6-112">-Name</span><span class="sxs-lookup"><span data-stu-id="d4af6-112">-Name</span></span>
<span data-ttu-id="d4af6-113">Der Name des Azure-ml-obligoplan.</span><span class="sxs-lookup"><span data-stu-id="d4af6-113">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4af6-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4af6-114">-ResourceGroupName</span></span>
<span data-ttu-id="d4af6-115">Der Name der Ressourcengruppe für den Azure-ml-Verpflichtungs Plan.</span><span class="sxs-lookup"><span data-stu-id="d4af6-115">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4af6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4af6-116">CommonParameters</span></span>
<span data-ttu-id="d4af6-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4af6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4af6-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4af6-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4af6-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4af6-119">INPUTS</span></span>

### <span data-ttu-id="d4af6-120">Keine</span><span class="sxs-lookup"><span data-stu-id="d4af6-120">None</span></span>
<span data-ttu-id="d4af6-121">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="d4af6-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d4af6-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4af6-122">OUTPUTS</span></span>

### <span data-ttu-id="d4af6-123">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. PlanUsageHistory []</span><span class="sxs-lookup"><span data-stu-id="d4af6-123">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory[]</span></span>

## <span data-ttu-id="d4af6-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4af6-124">NOTES</span></span>
<span data-ttu-id="d4af6-125">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="d4af6-125">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="d4af6-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4af6-126">RELATED LINKS</span></span>

