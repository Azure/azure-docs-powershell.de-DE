---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
ms.openlocfilehash: c94486e33ac39bff9d378840a6ab0ad041fa998e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479625"
---
# <span data-ttu-id="cc13e-101">Get-AzureRmPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="cc13e-101">Get-AzureRmPowerBIWorkspace</span></span>

## <span data-ttu-id="cc13e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cc13e-102">SYNOPSIS</span></span>
<span data-ttu-id="cc13e-103">Ruft die Arbeitsbereiche in einer Power BI-Arbeitsbereichs Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="cc13e-103">Gets the workspaces in a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc13e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc13e-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc13e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc13e-105">DESCRIPTION</span></span>
<span data-ttu-id="cc13e-106">Das Cmdlet " **Get-AzureRmPowerBIWorkspace** " Ruft die Arbeitsbereiche in einer Power BI-Arbeitsbereichs Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="cc13e-106">The **Get-AzureRmPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="cc13e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc13e-107">EXAMPLES</span></span>

### <span data-ttu-id="cc13e-108">Beispiel 1: Abrufen von Arbeitsbereichen einer Arbeitsbereichs Sammlung</span><span class="sxs-lookup"><span data-stu-id="cc13e-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="cc13e-109">Dieser Befehl ruft die Arbeitsbereiche ab, die der Arbeitsbereichs Sammlung mit dem Namen WCN11 in der angegebenen Ressourcengruppe angehören.</span><span class="sxs-lookup"><span data-stu-id="cc13e-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="cc13e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc13e-110">PARAMETERS</span></span>

### <span data-ttu-id="cc13e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc13e-111">-DefaultProfile</span></span>
<span data-ttu-id="cc13e-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="cc13e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc13e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc13e-113">-ResourceGroupName</span></span>
<span data-ttu-id="cc13e-114">Gibt den Namen der Ressourcengruppe an, zu der die Arbeitsbereichs Sammlung gehört.</span><span class="sxs-lookup"><span data-stu-id="cc13e-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="cc13e-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="cc13e-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="cc13e-116">Gibt den Namen der Arbeitsbereichs Sammlung an, für die dieses Cmdlet Arbeitsbereiche abruft.</span><span class="sxs-lookup"><span data-stu-id="cc13e-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="cc13e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc13e-117">CommonParameters</span></span>
<span data-ttu-id="cc13e-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc13e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc13e-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc13e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc13e-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cc13e-120">INPUTS</span></span>

### <span data-ttu-id="cc13e-121">Keine</span><span class="sxs-lookup"><span data-stu-id="cc13e-121">None</span></span>
<span data-ttu-id="cc13e-122">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="cc13e-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cc13e-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cc13e-123">OUTPUTS</span></span>

### <span data-ttu-id="cc13e-124">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="cc13e-124">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="cc13e-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="cc13e-125">NOTES</span></span>

## <span data-ttu-id="cc13e-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cc13e-126">RELATED LINKS</span></span>

[<span data-ttu-id="cc13e-127">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="cc13e-127">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)


