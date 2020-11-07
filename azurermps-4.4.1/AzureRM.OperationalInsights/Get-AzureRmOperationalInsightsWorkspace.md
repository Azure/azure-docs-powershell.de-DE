---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 042597d8d300f57600680282dadb16e8ec221e59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663872"
---
# <span data-ttu-id="90742-101">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="90742-101">Get-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="90742-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="90742-102">SYNOPSIS</span></span>
<span data-ttu-id="90742-103">Ruft Informationen zu einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="90742-103">Gets information about a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90742-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="90742-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90742-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90742-105">DESCRIPTION</span></span>
<span data-ttu-id="90742-106">Das Cmdlet " **Get-AzureRmOperationalInsightsWorkspace** " Ruft Informationen zu einem vorhandenen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="90742-106">The **Get-AzureRmOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="90742-107">Wenn Sie einen Arbeitsbereichsnamen angeben, ruft dieses Cmdlet Informationen zu diesem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="90742-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="90742-108">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Arbeitsbereichen in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="90742-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="90742-109">Wenn Sie keinen Namen und keine Ressourcengruppe angeben, ruft dieses Cmdlet Informationen zu allen Arbeitsbereichen in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="90742-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="90742-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90742-110">EXAMPLES</span></span>

### <span data-ttu-id="90742-111">Beispiel 1: Abrufen eines Arbeitsbereichs nach Name</span><span class="sxs-lookup"><span data-stu-id="90742-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="90742-112">Dieser Befehl ruft einen Arbeitsbereich mit dem Namen "myworkspace" in der Ressourcengruppe mit dem Namen ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="90742-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="90742-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="90742-113">PARAMETERS</span></span>

### <span data-ttu-id="90742-114">-Name</span><span class="sxs-lookup"><span data-stu-id="90742-114">-Name</span></span>
<span data-ttu-id="90742-115">Gibt den Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="90742-115">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90742-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90742-116">-ResourceGroupName</span></span>
<span data-ttu-id="90742-117">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="90742-117">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90742-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90742-118">-DefaultProfile</span></span>
<span data-ttu-id="90742-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="90742-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90742-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90742-120">CommonParameters</span></span>
<span data-ttu-id="90742-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90742-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90742-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90742-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90742-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="90742-123">INPUTS</span></span>

## <span data-ttu-id="90742-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="90742-124">OUTPUTS</span></span>

### <span data-ttu-id="90742-125">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace]</span><span class="sxs-lookup"><span data-stu-id="90742-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace]</span></span>

### <span data-ttu-id="90742-126">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="90742-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="90742-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="90742-127">NOTES</span></span>

## <span data-ttu-id="90742-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="90742-128">RELATED LINKS</span></span>

[<span data-ttu-id="90742-129">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="90742-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


