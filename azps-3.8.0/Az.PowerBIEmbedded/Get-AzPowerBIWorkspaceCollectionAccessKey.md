---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: 9108f224297b23fd391e1a4c3afac4b826aa3dbf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995329"
---
# <span data-ttu-id="1cad3-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="1cad3-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="1cad3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1cad3-102">SYNOPSIS</span></span>
<span data-ttu-id="1cad3-103">Ruft die aktuellen Zugriffstasten ab, die einer Power BI-Arbeitsbereichs Sammlung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1cad3-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="1cad3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cad3-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cad3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1cad3-105">DESCRIPTION</span></span>
<span data-ttu-id="1cad3-106">Das Cmdlet " **Get-AzPowerBIWorkspaceCollectionAccessKey** " Ruft die aktuellen Zugriffstasten ab, die einer Power BI-Arbeitsbereichs Sammlung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1cad3-106">The **Get-AzPowerBIWorkspaceCollectionAccessKey** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="1cad3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1cad3-107">EXAMPLES</span></span>

### <span data-ttu-id="1cad3-108">Beispiel 1: Abrufen von Zugriffstasten</span><span class="sxs-lookup"><span data-stu-id="1cad3-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="1cad3-109">Dieser Befehl ruft Zugriffstasten für die Arbeitsbereichs Sammlung mit dem Namen WCN11 in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="1cad3-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="1cad3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1cad3-110">PARAMETERS</span></span>

### <span data-ttu-id="1cad3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cad3-111">-DefaultProfile</span></span>
<span data-ttu-id="1cad3-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1cad3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1cad3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cad3-113">-ResourceGroupName</span></span>
<span data-ttu-id="1cad3-114">Gibt den Namen der Ressourcengruppe der Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="1cad3-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="1cad3-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="1cad3-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="1cad3-116">Gibt den Namen der Power BI-Arbeitsbereichs Sammlung an, für die dieses Cmdlet fungiert.</span><span class="sxs-lookup"><span data-stu-id="1cad3-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="1cad3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cad3-117">CommonParameters</span></span>
<span data-ttu-id="1cad3-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cad3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cad3-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cad3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cad3-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1cad3-120">INPUTS</span></span>

### <span data-ttu-id="1cad3-121">System. String</span><span class="sxs-lookup"><span data-stu-id="1cad3-121">System.String</span></span>

## <span data-ttu-id="1cad3-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1cad3-122">OUTPUTS</span></span>

### <span data-ttu-id="1cad3-123">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="1cad3-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="1cad3-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="1cad3-124">NOTES</span></span>

## <span data-ttu-id="1cad3-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1cad3-125">RELATED LINKS</span></span>

[<span data-ttu-id="1cad3-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="1cad3-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Reset-AzPowerBIWorkspaceCollectionAccessKey.md)


