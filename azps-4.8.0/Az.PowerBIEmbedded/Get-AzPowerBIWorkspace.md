---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
ms.openlocfilehash: 06cbaf240214bb61fb6bceac2827b9ce04d956f4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166661"
---
# <span data-ttu-id="a4938-101">Get-AzPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="a4938-101">Get-AzPowerBIWorkspace</span></span>

## <span data-ttu-id="a4938-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a4938-102">SYNOPSIS</span></span>
<span data-ttu-id="a4938-103">Ruft die Arbeitsbereiche in einer Power BI-Arbeitsbereichs Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="a4938-103">Gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="a4938-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4938-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4938-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4938-105">DESCRIPTION</span></span>
<span data-ttu-id="a4938-106">Das Cmdlet " **Get-AzPowerBIWorkspace** " Ruft die Arbeitsbereiche in einer Power BI-Arbeitsbereichs Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="a4938-106">The **Get-AzPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="a4938-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a4938-107">EXAMPLES</span></span>

### <span data-ttu-id="a4938-108">Beispiel 1: Abrufen von Arbeitsbereichen einer Arbeitsbereichs Sammlung</span><span class="sxs-lookup"><span data-stu-id="a4938-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="a4938-109">Dieser Befehl ruft die Arbeitsbereiche ab, die der Arbeitsbereichs Sammlung mit dem Namen WCN11 in der angegebenen Ressourcengruppe angehören.</span><span class="sxs-lookup"><span data-stu-id="a4938-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="a4938-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4938-110">PARAMETERS</span></span>

### <span data-ttu-id="a4938-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4938-111">-DefaultProfile</span></span>
<span data-ttu-id="a4938-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a4938-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4938-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4938-113">-ResourceGroupName</span></span>
<span data-ttu-id="a4938-114">Gibt den Namen der Ressourcengruppe an, zu der die Arbeitsbereichs Sammlung gehört.</span><span class="sxs-lookup"><span data-stu-id="a4938-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="a4938-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="a4938-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="a4938-116">Gibt den Namen der Arbeitsbereichs Sammlung an, für die dieses Cmdlet Arbeitsbereiche abruft.</span><span class="sxs-lookup"><span data-stu-id="a4938-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="a4938-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4938-117">CommonParameters</span></span>
<span data-ttu-id="a4938-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4938-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4938-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4938-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4938-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a4938-120">INPUTS</span></span>

### <span data-ttu-id="a4938-121">System. String</span><span class="sxs-lookup"><span data-stu-id="a4938-121">System.String</span></span>

## <span data-ttu-id="a4938-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a4938-122">OUTPUTS</span></span>

### <span data-ttu-id="a4938-123">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a4938-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="a4938-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="a4938-124">NOTES</span></span>

## <span data-ttu-id="a4938-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a4938-125">RELATED LINKS</span></span>

[<span data-ttu-id="a4938-126">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="a4938-126">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)


