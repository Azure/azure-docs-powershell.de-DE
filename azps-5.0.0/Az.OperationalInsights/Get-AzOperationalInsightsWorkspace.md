---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 1a0d36c2e871bd0495216bce18d84dff60e1044d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301330"
---
# <span data-ttu-id="87558-101">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="87558-101">Get-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="87558-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="87558-102">SYNOPSIS</span></span>
<span data-ttu-id="87558-103">Ruft Informationen zu einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="87558-103">Gets information about a workspace.</span></span>

## <span data-ttu-id="87558-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="87558-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87558-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87558-105">DESCRIPTION</span></span>
<span data-ttu-id="87558-106">Das Cmdlet " **Get-AzOperationalInsightsWorkspace** " Ruft Informationen zu einem vorhandenen Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="87558-106">The **Get-AzOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="87558-107">Wenn Sie einen Arbeitsbereichsnamen angeben, ruft dieses Cmdlet Informationen zu diesem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="87558-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="87558-108">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Arbeitsbereichen in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="87558-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="87558-109">Wenn Sie keinen Namen und keine Ressourcengruppe angeben, ruft dieses Cmdlet Informationen zu allen Arbeitsbereichen in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="87558-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="87558-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="87558-110">EXAMPLES</span></span>

### <span data-ttu-id="87558-111">Beispiel 1: Abrufen eines Arbeitsbereichs nach Name</span><span class="sxs-lookup"><span data-stu-id="87558-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="87558-112">Dieser Befehl ruft einen Arbeitsbereich mit dem Namen "myworkspace" in der Ressourcengruppe mit dem Namen ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="87558-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="87558-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="87558-113">PARAMETERS</span></span>

### <span data-ttu-id="87558-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87558-114">-DefaultProfile</span></span>
<span data-ttu-id="87558-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="87558-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87558-116">-Name</span><span class="sxs-lookup"><span data-stu-id="87558-116">-Name</span></span>
<span data-ttu-id="87558-117">Gibt den Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="87558-117">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="87558-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87558-118">-ResourceGroupName</span></span>
<span data-ttu-id="87558-119">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="87558-119">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="87558-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87558-120">CommonParameters</span></span>
<span data-ttu-id="87558-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87558-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87558-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87558-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87558-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="87558-123">INPUTS</span></span>

### <span data-ttu-id="87558-124">System. String</span><span class="sxs-lookup"><span data-stu-id="87558-124">System.String</span></span>

## <span data-ttu-id="87558-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="87558-125">OUTPUTS</span></span>

### <span data-ttu-id="87558-126">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="87558-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="87558-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="87558-127">NOTES</span></span>

## <span data-ttu-id="87558-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="87558-128">RELATED LINKS</span></span>

[<span data-ttu-id="87558-129">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="87558-129">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


