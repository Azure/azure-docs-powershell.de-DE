---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiworkspacecollectionaccesskeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: 11c1e3c19a6f5767fcfe1120cfa3561a73885f5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479614"
---
# <span data-ttu-id="bb30d-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="bb30d-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="bb30d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bb30d-102">SYNOPSIS</span></span>
<span data-ttu-id="bb30d-103">Ruft die aktuellen Zugriffstasten ab, die einer Power BI-Arbeitsbereichs Sammlung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bb30d-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb30d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb30d-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb30d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb30d-105">DESCRIPTION</span></span>
<span data-ttu-id="bb30d-106">Das Cmdlet " **Get-AzureRmPowerBIWorkspaceCollectionAccessKeys** " Ruft die aktuellen Zugriffstasten ab, die einer Power BI-Arbeitsbereichs Sammlung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bb30d-106">The **Get-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="bb30d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bb30d-107">EXAMPLES</span></span>

### <span data-ttu-id="bb30d-108">Beispiel 1: Abrufen von Zugriffstasten</span><span class="sxs-lookup"><span data-stu-id="bb30d-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="bb30d-109">Dieser Befehl ruft Zugriffstasten für die Arbeitsbereichs Sammlung mit dem Namen WCN11 in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="bb30d-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="bb30d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb30d-110">PARAMETERS</span></span>

### <span data-ttu-id="bb30d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb30d-111">-DefaultProfile</span></span>
<span data-ttu-id="bb30d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="bb30d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb30d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb30d-113">-ResourceGroupName</span></span>
<span data-ttu-id="bb30d-114">Gibt den Namen der Ressourcengruppe der Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="bb30d-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="bb30d-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="bb30d-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="bb30d-116">Gibt den Namen der Power BI-Arbeitsbereichs Sammlung an, für die dieses Cmdlet fungiert.</span><span class="sxs-lookup"><span data-stu-id="bb30d-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb30d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb30d-117">CommonParameters</span></span>
<span data-ttu-id="bb30d-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb30d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb30d-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb30d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb30d-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bb30d-120">INPUTS</span></span>

### <span data-ttu-id="bb30d-121">Keine</span><span class="sxs-lookup"><span data-stu-id="bb30d-121">None</span></span>
<span data-ttu-id="bb30d-122">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="bb30d-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bb30d-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bb30d-123">OUTPUTS</span></span>

### <span data-ttu-id="bb30d-124">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="bb30d-124">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="bb30d-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="bb30d-125">NOTES</span></span>

## <span data-ttu-id="bb30d-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bb30d-126">RELATED LINKS</span></span>

[<span data-ttu-id="bb30d-127">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="bb30d-127">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)


