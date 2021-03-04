---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: 06e17c012f52883d5e160698bb6f858f4644af6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929920"
---
# <span data-ttu-id="75a43-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="75a43-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="75a43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75a43-102">SYNOPSIS</span></span>
<span data-ttu-id="75a43-103">Ruft die aktuellen Zugriffstasten ab, die einer Power BI-Arbeitsbereichssammlung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="75a43-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="75a43-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75a43-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75a43-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75a43-105">DESCRIPTION</span></span>
<span data-ttu-id="75a43-106">Das **Get-AzPowerBIWorkspaceCollectionAccessKey-Cmdlet** ruft die aktuellen Zugriffstasten ab, die einer Power BI-Arbeitsbereichssammlung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="75a43-106">The **Get-AzPowerBIWorkspaceCollectionAccessKey** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="75a43-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="75a43-107">EXAMPLES</span></span>

### <span data-ttu-id="75a43-108">Beispiel 1: Zugriffsschlüssel erhalten</span><span class="sxs-lookup"><span data-stu-id="75a43-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="75a43-109">Dieser Befehl ruft Zugriffstasten für die Arbeitsbereichssammlung mit dem Namen WCN11 in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="75a43-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="75a43-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="75a43-110">PARAMETERS</span></span>

### <span data-ttu-id="75a43-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a43-111">-DefaultProfile</span></span>
<span data-ttu-id="75a43-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="75a43-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75a43-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75a43-113">-ResourceGroupName</span></span>
<span data-ttu-id="75a43-114">Gibt den Namen der Ressourcengruppe der Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="75a43-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="75a43-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="75a43-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="75a43-116">Gibt den Namen der Power BI-Arbeitsbereichssammlung an, für die dieses Cmdlet verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="75a43-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75a43-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a43-117">CommonParameters</span></span>
<span data-ttu-id="75a43-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75a43-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a43-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75a43-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a43-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="75a43-120">INPUTS</span></span>

### <span data-ttu-id="75a43-121">System.String</span><span class="sxs-lookup"><span data-stu-id="75a43-121">System.String</span></span>

## <span data-ttu-id="75a43-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="75a43-122">OUTPUTS</span></span>

### <span data-ttu-id="75a43-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="75a43-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="75a43-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="75a43-124">NOTES</span></span>

## <span data-ttu-id="75a43-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="75a43-125">RELATED LINKS</span></span>

[<span data-ttu-id="75a43-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="75a43-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Reset-AzPowerBIWorkspaceCollectionAccessKey.md)


