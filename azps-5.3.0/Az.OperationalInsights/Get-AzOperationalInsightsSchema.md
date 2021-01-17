---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 12c3e54725abfd5addf33a3d31edcb8f8016e9dd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473324"
---
# <span data-ttu-id="e99fa-101">Get-AzOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="e99fa-101">Get-AzOperationalInsightsSchema</span></span>

## <span data-ttu-id="e99fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e99fa-102">SYNOPSIS</span></span>
<span data-ttu-id="e99fa-103">Gibt das Schema zurück, das einem Arbeitsbereich zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e99fa-103">Returns the schema associated with a workspace.</span></span>

## <span data-ttu-id="e99fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e99fa-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e99fa-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e99fa-105">DESCRIPTION</span></span>
<span data-ttu-id="e99fa-106">Das **Cmdlet "Get-AzOperationalInsightsSchema"** gibt das Schema zurück, das dem angegebenen Arbeitsbereich innerhalb dieser Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e99fa-106">The **Get-AzOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="e99fa-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e99fa-107">EXAMPLES</span></span>

### <span data-ttu-id="e99fa-108">Beispiel 1: Erhalten der Schemas für einen Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="e99fa-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="e99fa-109">Mit diesem Befehl werden die Schemas einem Arbeitsbereich zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e99fa-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="e99fa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e99fa-110">PARAMETERS</span></span>

### <span data-ttu-id="e99fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e99fa-111">-DefaultProfile</span></span>
<span data-ttu-id="e99fa-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e99fa-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e99fa-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e99fa-113">-ResourceGroupName</span></span>
<span data-ttu-id="e99fa-114">Gibt den Namen einer Azure-Ressourcengruppe an, die einen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="e99fa-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="e99fa-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e99fa-115">-WorkspaceName</span></span>
<span data-ttu-id="e99fa-116">Gibt einen Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="e99fa-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="e99fa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e99fa-117">CommonParameters</span></span>
<span data-ttu-id="e99fa-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e99fa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e99fa-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e99fa-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e99fa-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e99fa-120">INPUTS</span></span>

### <span data-ttu-id="e99fa-121">System.String</span><span class="sxs-lookup"><span data-stu-id="e99fa-121">System.String</span></span>

## <span data-ttu-id="e99fa-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e99fa-122">OUTPUTS</span></span>

### <span data-ttu-id="e99fa-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="e99fa-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="e99fa-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e99fa-124">NOTES</span></span>

## <span data-ttu-id="e99fa-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e99fa-125">RELATED LINKS</span></span>

[<span data-ttu-id="e99fa-126">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="e99fa-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


