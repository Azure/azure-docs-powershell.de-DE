---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/get-azpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
ms.openlocfilehash: d9c93bc487817d99b217519453dea10543852a1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929923"
---
# <span data-ttu-id="aeef9-101">Get-AzPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="aeef9-101">Get-AzPowerBIWorkspace</span></span>

## <span data-ttu-id="aeef9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aeef9-102">SYNOPSIS</span></span>
<span data-ttu-id="aeef9-103">Ruft die Arbeitsbereiche in einer Power BI-Arbeitsbereichsammlung ab.</span><span class="sxs-lookup"><span data-stu-id="aeef9-103">Gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="aeef9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aeef9-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aeef9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aeef9-105">DESCRIPTION</span></span>
<span data-ttu-id="aeef9-106">Das **Get-AzPowerBIWorkspace-Cmdlet** ruft die Arbeitsbereiche in einer Power BI-Arbeitsbereichssammlung ab.</span><span class="sxs-lookup"><span data-stu-id="aeef9-106">The **Get-AzPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="aeef9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aeef9-107">EXAMPLES</span></span>

### <span data-ttu-id="aeef9-108">Beispiel 1: Anzeigen von Arbeitsbereichen einer Arbeitsbereichsammlung</span><span class="sxs-lookup"><span data-stu-id="aeef9-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="aeef9-109">Dieser Befehl ruft die Arbeitsbereiche ab, die zur Arbeitsbereichssammlung mit dem Namen WCN11 in der angegebenen Ressourcengruppe gehören.</span><span class="sxs-lookup"><span data-stu-id="aeef9-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="aeef9-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="aeef9-110">PARAMETERS</span></span>

### <span data-ttu-id="aeef9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeef9-111">-DefaultProfile</span></span>
<span data-ttu-id="aeef9-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="aeef9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aeef9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aeef9-113">-ResourceGroupName</span></span>
<span data-ttu-id="aeef9-114">Gibt den Namen der Ressourcengruppe an, zu der die Arbeitsbereichssammlung gehört.</span><span class="sxs-lookup"><span data-stu-id="aeef9-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="aeef9-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="aeef9-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="aeef9-116">Gibt den Namen der Arbeitsbereichssammlung an, für die dieses Cmdlet Arbeitsbereiche erhält.</span><span class="sxs-lookup"><span data-stu-id="aeef9-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="aeef9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeef9-117">CommonParameters</span></span>
<span data-ttu-id="aeef9-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aeef9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeef9-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aeef9-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeef9-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aeef9-120">INPUTS</span></span>

### <span data-ttu-id="aeef9-121">System.String</span><span class="sxs-lookup"><span data-stu-id="aeef9-121">System.String</span></span>

## <span data-ttu-id="aeef9-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aeef9-122">OUTPUTS</span></span>

### <span data-ttu-id="aeef9-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="aeef9-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="aeef9-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="aeef9-124">NOTES</span></span>

## <span data-ttu-id="aeef9-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="aeef9-125">RELATED LINKS</span></span>

[<span data-ttu-id="aeef9-126">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="aeef9-126">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)


