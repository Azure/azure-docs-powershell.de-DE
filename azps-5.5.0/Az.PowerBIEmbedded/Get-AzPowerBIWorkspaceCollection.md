---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: d3be067690b755014fe02840d355fc36e0d6aa20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151196"
---
# <span data-ttu-id="9b852-101">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="9b852-101">Get-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="9b852-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b852-102">SYNOPSIS</span></span>
<span data-ttu-id="9b852-103">Ruft Power BI-Arbeitsbereichssammlungen ab.</span><span class="sxs-lookup"><span data-stu-id="9b852-103">Gets Power BI workspace collections.</span></span>

## <span data-ttu-id="9b852-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b852-104">SYNTAX</span></span>

### <span data-ttu-id="9b852-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b852-105">ResourceGroupParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b852-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b852-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b852-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b852-107">DESCRIPTION</span></span>
<span data-ttu-id="9b852-108">Das **Cmdlet "Get-AzPowerBIWorkspaceCollection"** ruft Power BI-Arbeitsbereichssammlungen in Ihrem Abonnement und ihrer Ressourcengruppe oder nach Sammlungsnamen ab.</span><span class="sxs-lookup"><span data-stu-id="9b852-108">The **Get-AzPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="9b852-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9b852-109">EXAMPLES</span></span>

### <span data-ttu-id="9b852-110">Beispiel 1: Alle Arbeitsbereichssammlungen in einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="9b852-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="9b852-111">Dieser Befehl ruft die Arbeitsbereichssammlungen ab, die zur Ressourcengruppe "ResourceGroup17" gehören.</span><span class="sxs-lookup"><span data-stu-id="9b852-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="9b852-112">Beispiel 2: Erhalten einer Arbeitsbereichssammlung unter Verwendung des Namens</span><span class="sxs-lookup"><span data-stu-id="9b852-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="9b852-113">Dieser Befehl ruft die Arbeitsbereichssammlung mit dem Namen WCN11 in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="9b852-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="9b852-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b852-114">PARAMETERS</span></span>

### <span data-ttu-id="9b852-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b852-115">-DefaultProfile</span></span>
<span data-ttu-id="9b852-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="9b852-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b852-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b852-117">-ResourceGroupName</span></span>
<span data-ttu-id="9b852-118">Gibt den Namen der Ressourcengruppe an, aus der dieses Cmdlet Arbeitsbereichssammlungen erhält.</span><span class="sxs-lookup"><span data-stu-id="9b852-118">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b852-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="9b852-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="9b852-120">Gibt den Namen der Power BI-Arbeitsbereichssammlung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="9b852-120">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b852-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b852-121">CommonParameters</span></span>
<span data-ttu-id="9b852-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b852-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b852-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b852-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b852-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9b852-124">INPUTS</span></span>

### <span data-ttu-id="9b852-125">System.String</span><span class="sxs-lookup"><span data-stu-id="9b852-125">System.String</span></span>

## <span data-ttu-id="9b852-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9b852-126">OUTPUTS</span></span>

### <span data-ttu-id="9b852-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="9b852-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="9b852-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9b852-128">NOTES</span></span>

## <span data-ttu-id="9b852-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9b852-129">RELATED LINKS</span></span>

[<span data-ttu-id="9b852-130">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="9b852-130">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="9b852-131">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="9b852-131">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


