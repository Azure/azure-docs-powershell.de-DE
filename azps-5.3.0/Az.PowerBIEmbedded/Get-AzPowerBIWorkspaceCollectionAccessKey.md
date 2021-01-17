---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: 9108f224297b23fd391e1a4c3afac4b826aa3dbf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468711"
---
# <span data-ttu-id="e239e-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="e239e-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="e239e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e239e-102">SYNOPSIS</span></span>
<span data-ttu-id="e239e-103">Ruft die aktuellen Zugriffstasten ab, die einer Power BI-Arbeitsbereichssammlung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e239e-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="e239e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e239e-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e239e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e239e-105">DESCRIPTION</span></span>
<span data-ttu-id="e239e-106">Das **Cmdlet "Get-AzPowerBIWorkspaceCollectionAccessKey"** ruft die aktuellen Zugriffstasten ab, die einer Power BI-Arbeitsbereichssammlung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e239e-106">The **Get-AzPowerBIWorkspaceCollectionAccessKey** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="e239e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e239e-107">EXAMPLES</span></span>

### <span data-ttu-id="e239e-108">Beispiel 1: Zugriffstasten erhalten</span><span class="sxs-lookup"><span data-stu-id="e239e-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="e239e-109">Dieser Befehl ruft Zugriffstasten für die Arbeitsbereichssammlung mit dem Namen WCN11 in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="e239e-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="e239e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e239e-110">PARAMETERS</span></span>

### <span data-ttu-id="e239e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e239e-111">-DefaultProfile</span></span>
<span data-ttu-id="e239e-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e239e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e239e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e239e-113">-ResourceGroupName</span></span>
<span data-ttu-id="e239e-114">Gibt den Namen der Ressourcengruppe der Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="e239e-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="e239e-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="e239e-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="e239e-116">Gibt den Namen der Power BI-Arbeitsbereichssammlung an, für die dieses Cmdlet verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e239e-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e239e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e239e-117">CommonParameters</span></span>
<span data-ttu-id="e239e-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e239e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e239e-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e239e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e239e-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e239e-120">INPUTS</span></span>

### <span data-ttu-id="e239e-121">System.String</span><span class="sxs-lookup"><span data-stu-id="e239e-121">System.String</span></span>

## <span data-ttu-id="e239e-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e239e-122">OUTPUTS</span></span>

### <span data-ttu-id="e239e-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="e239e-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="e239e-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e239e-124">NOTES</span></span>

## <span data-ttu-id="e239e-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e239e-125">RELATED LINKS</span></span>

[<span data-ttu-id="e239e-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="e239e-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Reset-AzPowerBIWorkspaceCollectionAccessKey.md)


