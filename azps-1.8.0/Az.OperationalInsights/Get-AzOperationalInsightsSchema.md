---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 077272f15d37645de86f144424fddd7e5f026908
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93662142"
---
# <span data-ttu-id="c96dd-101">Get-AzOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="c96dd-101">Get-AzOperationalInsightsSchema</span></span>

## <span data-ttu-id="c96dd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c96dd-102">SYNOPSIS</span></span>
<span data-ttu-id="c96dd-103">Gibt das einem Arbeitsbereich zugeordnete Schema zurück.</span><span class="sxs-lookup"><span data-stu-id="c96dd-103">Returns the schema associated with a workspace.</span></span>

## <span data-ttu-id="c96dd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c96dd-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c96dd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c96dd-105">DESCRIPTION</span></span>
<span data-ttu-id="c96dd-106">Das Cmdlet " **Get-AzOperationalInsightsSchema** " gibt das Schema zurück, das dem angegebenen Arbeitsbereich innerhalb dieser Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c96dd-106">The **Get-AzOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="c96dd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c96dd-107">EXAMPLES</span></span>

### <span data-ttu-id="c96dd-108">Beispiel 1: Abrufen der Schemas für einen Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="c96dd-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="c96dd-109">Dieser Befehl ruft die Schemas ab, die einem Arbeitsbereich zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c96dd-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="c96dd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c96dd-110">PARAMETERS</span></span>

### <span data-ttu-id="c96dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c96dd-111">-DefaultProfile</span></span>
<span data-ttu-id="c96dd-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c96dd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c96dd-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c96dd-113">-ResourceGroupName</span></span>
<span data-ttu-id="c96dd-114">Gibt den Namen einer Azure-Ressourcengruppe an, die einen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="c96dd-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="c96dd-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c96dd-115">-WorkspaceName</span></span>
<span data-ttu-id="c96dd-116">Gibt einen Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="c96dd-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="c96dd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c96dd-117">CommonParameters</span></span>
<span data-ttu-id="c96dd-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c96dd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c96dd-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c96dd-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c96dd-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c96dd-120">INPUTS</span></span>

### <span data-ttu-id="c96dd-121">System. String</span><span class="sxs-lookup"><span data-stu-id="c96dd-121">System.String</span></span>

## <span data-ttu-id="c96dd-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c96dd-122">OUTPUTS</span></span>

### <span data-ttu-id="c96dd-123">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="c96dd-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="c96dd-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="c96dd-124">NOTES</span></span>

## <span data-ttu-id="c96dd-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c96dd-125">RELATED LINKS</span></span>

[<span data-ttu-id="c96dd-126">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="c96dd-126">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


