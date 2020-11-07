---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSchema.md
ms.openlocfilehash: 1e1e56a4cf0e31af3d64377df05b6057354dd534
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662568"
---
# <span data-ttu-id="3219d-101">Get-AzureRmOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="3219d-101">Get-AzureRmOperationalInsightsSchema</span></span>

## <span data-ttu-id="3219d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3219d-102">SYNOPSIS</span></span>
<span data-ttu-id="3219d-103">Gibt das einem Arbeitsbereich zugeordnete Schema zurück.</span><span class="sxs-lookup"><span data-stu-id="3219d-103">Returns the schema associated with a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3219d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3219d-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3219d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3219d-105">DESCRIPTION</span></span>
<span data-ttu-id="3219d-106">Das Cmdlet " **Get-AzureRmOperationalInsightsSchema** " gibt das Schema zurück, das dem angegebenen Arbeitsbereich innerhalb dieser Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3219d-106">The **Get-AzureRmOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="3219d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3219d-107">EXAMPLES</span></span>

### <span data-ttu-id="3219d-108">Beispiel 1: Abrufen der Schemas für einen Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="3219d-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="3219d-109">Dieser Befehl ruft die Schemas ab, die einem Arbeitsbereich zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3219d-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="3219d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3219d-110">PARAMETERS</span></span>

### <span data-ttu-id="3219d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3219d-111">-DefaultProfile</span></span>
<span data-ttu-id="3219d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3219d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3219d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3219d-113">-ResourceGroupName</span></span>
<span data-ttu-id="3219d-114">Gibt den Namen einer Azure-Ressourcengruppe an, die einen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="3219d-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="3219d-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3219d-115">-WorkspaceName</span></span>
<span data-ttu-id="3219d-116">Gibt einen Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="3219d-116">Specifies a workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3219d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3219d-117">CommonParameters</span></span>
<span data-ttu-id="3219d-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3219d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3219d-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3219d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3219d-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3219d-120">INPUTS</span></span>

### <span data-ttu-id="3219d-121">Keine</span><span class="sxs-lookup"><span data-stu-id="3219d-121">None</span></span>
<span data-ttu-id="3219d-122">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="3219d-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3219d-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3219d-123">OUTPUTS</span></span>

### <span data-ttu-id="3219d-124">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="3219d-124">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="3219d-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="3219d-125">NOTES</span></span>

## <span data-ttu-id="3219d-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3219d-126">RELATED LINKS</span></span>

[<span data-ttu-id="3219d-127">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="3219d-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


