---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsIntelligencePacks.md
ms.openlocfilehash: 56bc2dd74f17daa9a56eac8ebd5128e6f074fe13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481749"
---
# <span data-ttu-id="09d96-101">Get-AzureRmOperationalInsightsIntelligencePacks</span><span class="sxs-lookup"><span data-stu-id="09d96-101">Get-AzureRmOperationalInsightsIntelligencePacks</span></span>

## <span data-ttu-id="09d96-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="09d96-102">SYNOPSIS</span></span>
<span data-ttu-id="09d96-103">Ruft die verfügbaren Intelligence Packs ab.</span><span class="sxs-lookup"><span data-stu-id="09d96-103">Gets the available Intelligence Packs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09d96-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="09d96-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsIntelligencePacks [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09d96-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09d96-105">DESCRIPTION</span></span>
<span data-ttu-id="09d96-106">Das Cmdlet " **Get-AzureRmOperationalInsightsIntelligencePacks** " Ruft die verfügbaren Intelligence Packs ab.</span><span class="sxs-lookup"><span data-stu-id="09d96-106">The **Get-AzureRmOperationalInsightsIntelligencePacks** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="09d96-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09d96-107">EXAMPLES</span></span>

### <span data-ttu-id="09d96-108">Beispiel 1: Abrufen von Intelligence-Paketen</span><span class="sxs-lookup"><span data-stu-id="09d96-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzureOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="09d96-109">Dieser Befehl ruft die verfügbaren Intelligence Packs ab.</span><span class="sxs-lookup"><span data-stu-id="09d96-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="09d96-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="09d96-110">PARAMETERS</span></span>

### <span data-ttu-id="09d96-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09d96-111">-ResourceGroupName</span></span>
<span data-ttu-id="09d96-112">Gibt den Namen einer Azure-Ressourcengruppe an, die einen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="09d96-112">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="09d96-113">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="09d96-113">-WorkspaceName</span></span>
<span data-ttu-id="09d96-114">Gibt den Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="09d96-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="09d96-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09d96-115">-DefaultProfile</span></span>
<span data-ttu-id="09d96-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="09d96-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09d96-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09d96-117">CommonParameters</span></span>
<span data-ttu-id="09d96-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09d96-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09d96-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09d96-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09d96-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="09d96-120">INPUTS</span></span>

## <span data-ttu-id="09d96-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="09d96-121">OUTPUTS</span></span>

### <span data-ttu-id="09d96-122">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. OperationalInsights. Models. PSIntelligencePack]</span><span class="sxs-lookup"><span data-stu-id="09d96-122">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack]</span></span>

## <span data-ttu-id="09d96-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="09d96-123">NOTES</span></span>

## <span data-ttu-id="09d96-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="09d96-124">RELATED LINKS</span></span>

[<span data-ttu-id="09d96-125">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="09d96-125">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


