---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspacesharedkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
ms.openlocfilehash: 5fab6a3a0419047fef32f5bf32f52e1f7ee57d3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479658"
---
# <span data-ttu-id="71f55-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span><span class="sxs-lookup"><span data-stu-id="71f55-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span></span>

## <span data-ttu-id="71f55-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="71f55-102">SYNOPSIS</span></span>
<span data-ttu-id="71f55-103">Ruft die freigegebenen Schlüssel für einen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="71f55-103">Gets the shared keys for a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71f55-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71f55-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceSharedKeys [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71f55-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71f55-105">DESCRIPTION</span></span>
<span data-ttu-id="71f55-106">Das Cmdlet " **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** " listet die freigegebenen Schlüssel für einen Arbeitsbereich auf.</span><span class="sxs-lookup"><span data-stu-id="71f55-106">The **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="71f55-107">Die Schlüssel werden verwendet, um operative Einblicke-Agents mit dem Arbeitsbereich zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="71f55-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="71f55-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71f55-108">EXAMPLES</span></span>

### <span data-ttu-id="71f55-109">Beispiel 1: Abrufen von freigegebenen Schlüsseln nach Arbeitsbereichsnamen</span><span class="sxs-lookup"><span data-stu-id="71f55-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceSharedKeys -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="71f55-110">Dieser Befehl ruft die freigegebenen Schlüssel für den Arbeitsbereich mit dem Namen "myworkspace" in der Ressourcengruppe mit dem Namen ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="71f55-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="71f55-111">Beispiel 2: Abrufen von freigegebenen Schlüsseln mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="71f55-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureRmOperationalInsightsWorkspaceSharedKeys
```

<span data-ttu-id="71f55-112">Dieser Befehl ruft den Arbeitsbereich mit dem Namen "myworkspace" mithilfe des Get-AzureRmOperationalInsightsWorkspace-Cmdlets ab und übergibt dann den Arbeitsbereich an das Cmdlet " **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** ".</span><span class="sxs-lookup"><span data-stu-id="71f55-112">This command gets the workspace named MyWorkspace using the Get-AzureRmOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet.</span></span>
<span data-ttu-id="71f55-113">Der Befehl ruft die freigegebenen Schlüssel für diesen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="71f55-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="71f55-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="71f55-114">PARAMETERS</span></span>

### <span data-ttu-id="71f55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71f55-115">-DefaultProfile</span></span>
<span data-ttu-id="71f55-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="71f55-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71f55-117">-Name</span><span class="sxs-lookup"><span data-stu-id="71f55-117">-Name</span></span>
<span data-ttu-id="71f55-118">Gibt den Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="71f55-118">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71f55-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71f55-119">-ResourceGroupName</span></span>
<span data-ttu-id="71f55-120">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="71f55-120">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71f55-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71f55-121">CommonParameters</span></span>
<span data-ttu-id="71f55-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71f55-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71f55-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71f55-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71f55-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="71f55-124">INPUTS</span></span>

### <span data-ttu-id="71f55-125">Keine</span><span class="sxs-lookup"><span data-stu-id="71f55-125">None</span></span>
<span data-ttu-id="71f55-126">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="71f55-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="71f55-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="71f55-127">OUTPUTS</span></span>

### <span data-ttu-id="71f55-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="71f55-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="71f55-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="71f55-129">NOTES</span></span>

## <span data-ttu-id="71f55-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="71f55-130">RELATED LINKS</span></span>

[<span data-ttu-id="71f55-131">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="71f55-131">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="71f55-132">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="71f55-132">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


