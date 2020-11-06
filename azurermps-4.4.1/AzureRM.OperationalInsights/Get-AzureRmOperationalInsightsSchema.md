---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSchema.md
ms.openlocfilehash: a4e4f1d86822a6c4ecd793576b1a5b68f2b2534f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497006"
---
# <span data-ttu-id="d8ece-101">Get-AzureRmOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="d8ece-101">Get-AzureRmOperationalInsightsSchema</span></span>

## <span data-ttu-id="d8ece-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d8ece-102">SYNOPSIS</span></span>
<span data-ttu-id="d8ece-103">Gibt das einem Arbeitsbereich zugeordnete Schema zurück.</span><span class="sxs-lookup"><span data-stu-id="d8ece-103">Returns the schema associated with a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8ece-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8ece-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8ece-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8ece-105">DESCRIPTION</span></span>
<span data-ttu-id="d8ece-106">Das Cmdlet " **Get-AzureRmOperationalInsightsSchema** " gibt das Schema zurück, das dem angegebenen Arbeitsbereich innerhalb dieser Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d8ece-106">The **Get-AzureRmOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="d8ece-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8ece-107">EXAMPLES</span></span>

### <span data-ttu-id="d8ece-108">Beispiel 1: Abrufen der Schemas für einen Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="d8ece-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="d8ece-109">Dieser Befehl ruft die Schemas ab, die einem Arbeitsbereich zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d8ece-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="d8ece-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8ece-110">PARAMETERS</span></span>

### <span data-ttu-id="d8ece-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8ece-111">-ResourceGroupName</span></span>
<span data-ttu-id="d8ece-112">Gibt den Namen einer Azure-Ressourcengruppe an, die einen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="d8ece-112">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="d8ece-113">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d8ece-113">-WorkspaceName</span></span>
<span data-ttu-id="d8ece-114">Gibt einen Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="d8ece-114">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="d8ece-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8ece-115">-DefaultProfile</span></span>
<span data-ttu-id="d8ece-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d8ece-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8ece-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8ece-117">CommonParameters</span></span>
<span data-ttu-id="d8ece-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8ece-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8ece-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8ece-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8ece-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d8ece-120">INPUTS</span></span>

## <span data-ttu-id="d8ece-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d8ece-121">OUTPUTS</span></span>

### <span data-ttu-id="d8ece-122">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="d8ece-122">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="d8ece-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="d8ece-123">NOTES</span></span>

## <span data-ttu-id="d8ece-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d8ece-124">RELATED LINKS</span></span>

[<span data-ttu-id="d8ece-125">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="d8ece-125">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


