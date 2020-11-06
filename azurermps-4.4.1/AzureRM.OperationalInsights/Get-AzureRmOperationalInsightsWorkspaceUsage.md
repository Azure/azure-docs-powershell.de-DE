---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: dfbf5833bd045c40315cb06d2e954688229ac557
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497002"
---
# <span data-ttu-id="0ed8b-101">Get-AzureRmOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="0ed8b-101">Get-AzureRmOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="0ed8b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0ed8b-102">SYNOPSIS</span></span>
<span data-ttu-id="0ed8b-103">Ruft die Verwendungsdaten für einen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="0ed8b-103">Gets the usage data for a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ed8b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ed8b-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ed8b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ed8b-105">DESCRIPTION</span></span>
<span data-ttu-id="0ed8b-106">Mit dem Cmdlet **Get-AzureRmOperationalInsightsWorkspaceUsage werden** die Nutzungsdaten für einen Arbeitsbereich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0ed8b-106">The **Get-AzureRmOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="0ed8b-107">Dadurch wird festgestellt, wie viele Daten während eines bestimmten Zeitraums vom Arbeitsbereich analysiert wurden.</span><span class="sxs-lookup"><span data-stu-id="0ed8b-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="0ed8b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0ed8b-108">EXAMPLES</span></span>

### <span data-ttu-id="0ed8b-109">Beispiel 1: Abrufen von Nutzungsdaten nach Arbeitsbereichsnamen</span><span class="sxs-lookup"><span data-stu-id="0ed8b-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="0ed8b-110">Dieser Befehl ruft die Verwendungsdetails für den Arbeitsbereich mit dem Namen "myworkspace" in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="0ed8b-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="0ed8b-111">Beispiel 2: Abrufen von Verwendungsdaten mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="0ed8b-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="0ed8b-112">Dieser Befehl ruft den Arbeitsbereich mit dem Namen "myworkspace" mithilfe des Get-AzureRmOperationalInsightsWorkspace-Cmdlets ab und übergibt dann den Arbeitsbereich an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ed8b-112">This command gets the workspace named MyWorkSpace using the Get-AzureRmOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="0ed8b-113">Der Befehl ruft die Nutzungsdetails für diesen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="0ed8b-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="0ed8b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ed8b-114">PARAMETERS</span></span>

### <span data-ttu-id="0ed8b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0ed8b-115">-Name</span></span>
<span data-ttu-id="0ed8b-116">Gibt den Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="0ed8b-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="0ed8b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ed8b-117">-ResourceGroupName</span></span>
<span data-ttu-id="0ed8b-118">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0ed8b-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="0ed8b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ed8b-119">-DefaultProfile</span></span>
<span data-ttu-id="0ed8b-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0ed8b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ed8b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ed8b-121">CommonParameters</span></span>
<span data-ttu-id="0ed8b-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ed8b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ed8b-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ed8b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ed8b-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0ed8b-124">INPUTS</span></span>

## <span data-ttu-id="0ed8b-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0ed8b-125">OUTPUTS</span></span>

### <span data-ttu-id="0ed8b-126">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. OperationalInsights. Models. PSUsageMetric]</span><span class="sxs-lookup"><span data-stu-id="0ed8b-126">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric]</span></span>

## <span data-ttu-id="0ed8b-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="0ed8b-127">NOTES</span></span>

## <span data-ttu-id="0ed8b-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0ed8b-128">RELATED LINKS</span></span>

[<span data-ttu-id="0ed8b-129">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="0ed8b-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="0ed8b-130">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="0ed8b-130">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


