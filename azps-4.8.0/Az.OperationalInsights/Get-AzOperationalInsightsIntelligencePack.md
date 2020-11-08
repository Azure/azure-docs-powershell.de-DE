---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: e197a5df0993ffbb97415bdc4e72ed9ea7603713
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009624"
---
# <span data-ttu-id="33ee1-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="33ee1-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="33ee1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="33ee1-102">SYNOPSIS</span></span>
<span data-ttu-id="33ee1-103">Ruft die verfügbaren Intelligence Packs ab.</span><span class="sxs-lookup"><span data-stu-id="33ee1-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="33ee1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="33ee1-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33ee1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="33ee1-105">DESCRIPTION</span></span>
<span data-ttu-id="33ee1-106">Das Cmdlet " **Get-AzOperationalInsightsIntelligencePack** " Ruft die verfügbaren Intelligence Packs ab.</span><span class="sxs-lookup"><span data-stu-id="33ee1-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="33ee1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="33ee1-107">EXAMPLES</span></span>

### <span data-ttu-id="33ee1-108">Beispiel 1: Abrufen von Intelligence-Paketen</span><span class="sxs-lookup"><span data-stu-id="33ee1-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="33ee1-109">Dieser Befehl ruft die verfügbaren Intelligence Packs ab.</span><span class="sxs-lookup"><span data-stu-id="33ee1-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="33ee1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="33ee1-110">PARAMETERS</span></span>

### <span data-ttu-id="33ee1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33ee1-111">-DefaultProfile</span></span>
<span data-ttu-id="33ee1-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="33ee1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33ee1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33ee1-113">-ResourceGroupName</span></span>
<span data-ttu-id="33ee1-114">Gibt den Namen einer Azure-Ressourcengruppe an, die einen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="33ee1-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="33ee1-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="33ee1-115">-WorkspaceName</span></span>
<span data-ttu-id="33ee1-116">Gibt den Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="33ee1-116">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33ee1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33ee1-117">CommonParameters</span></span>
<span data-ttu-id="33ee1-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33ee1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33ee1-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33ee1-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33ee1-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="33ee1-120">INPUTS</span></span>

### <span data-ttu-id="33ee1-121">System. String</span><span class="sxs-lookup"><span data-stu-id="33ee1-121">System.String</span></span>

## <span data-ttu-id="33ee1-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="33ee1-122">OUTPUTS</span></span>

### <span data-ttu-id="33ee1-123">Microsoft. Azure. Commands. OperationalInsights. Models. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="33ee1-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="33ee1-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="33ee1-124">NOTES</span></span>

## <span data-ttu-id="33ee1-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="33ee1-125">RELATED LINKS</span></span>

[<span data-ttu-id="33ee1-126">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="33ee1-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


