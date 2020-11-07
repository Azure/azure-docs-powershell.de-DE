---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 19b1d1b0da719167d53739a8c92a97121656aa9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660018"
---
# <span data-ttu-id="eed61-101">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="eed61-101">Get-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="eed61-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eed61-102">SYNOPSIS</span></span>
<span data-ttu-id="eed61-103">Ruft Power BI-Arbeitsbereichs Sammlungen ab.</span><span class="sxs-lookup"><span data-stu-id="eed61-103">Gets Power BI workspace collections.</span></span>

## <span data-ttu-id="eed61-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eed61-104">SYNTAX</span></span>

### <span data-ttu-id="eed61-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="eed61-105">ResourceGroupParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eed61-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eed61-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eed61-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eed61-107">DESCRIPTION</span></span>
<span data-ttu-id="eed61-108">Das Cmdlet " **Get-AzPowerBIWorkspaceCollection** " ruft Power BI-Arbeitsbereichs Auflistungen in Ihrem Azure-Abonnement und ihrer Ressourcengruppe oder nach dem Sammlungsnamen ab.</span><span class="sxs-lookup"><span data-stu-id="eed61-108">The **Get-AzPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="eed61-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eed61-109">EXAMPLES</span></span>

### <span data-ttu-id="eed61-110">Beispiel 1: Abrufen aller Arbeitsbereichs Auflistungen in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="eed61-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="eed61-111">Dieser Befehl ruft die Arbeitsbereichs Auflistungen ab, die zur Ressourcengruppe mit dem Namen ResourceGroup17 gehören.</span><span class="sxs-lookup"><span data-stu-id="eed61-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="eed61-112">Beispiel 2: Abrufen einer Arbeitsbereichs Sammlung unter Verwendung des Namens</span><span class="sxs-lookup"><span data-stu-id="eed61-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="eed61-113">Dieser Befehl ruft die Arbeitsbereichs Sammlung mit dem Namen WCN11 in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="eed61-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="eed61-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="eed61-114">PARAMETERS</span></span>

### <span data-ttu-id="eed61-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eed61-115">-DefaultProfile</span></span>
<span data-ttu-id="eed61-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="eed61-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eed61-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eed61-117">-ResourceGroupName</span></span>
<span data-ttu-id="eed61-118">Gibt den Namen der Ressourcengruppe an, aus der dieses Cmdlet Arbeitsbereichs Sammlungen erhält.</span><span class="sxs-lookup"><span data-stu-id="eed61-118">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

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

### <span data-ttu-id="eed61-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="eed61-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="eed61-120">Gibt den Namen der Power BI-Arbeitsbereichs Sammlung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="eed61-120">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

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

### <span data-ttu-id="eed61-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eed61-121">CommonParameters</span></span>
<span data-ttu-id="eed61-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eed61-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eed61-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eed61-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eed61-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eed61-124">INPUTS</span></span>

### <span data-ttu-id="eed61-125">System. String</span><span class="sxs-lookup"><span data-stu-id="eed61-125">System.String</span></span>

## <span data-ttu-id="eed61-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eed61-126">OUTPUTS</span></span>

### <span data-ttu-id="eed61-127">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="eed61-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="eed61-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="eed61-128">NOTES</span></span>

## <span data-ttu-id="eed61-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eed61-129">RELATED LINKS</span></span>

[<span data-ttu-id="eed61-130">Neu – AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="eed61-130">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="eed61-131">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="eed61-131">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


