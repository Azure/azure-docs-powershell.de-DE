---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 93ca812f726e036d195e83170153f7b2df4a2352
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504033"
---
# <span data-ttu-id="f2c96-101">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="f2c96-101">Get-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="f2c96-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f2c96-102">SYNOPSIS</span></span>
<span data-ttu-id="f2c96-103">Ruft Power BI-Arbeitsbereichs Sammlungen ab.</span><span class="sxs-lookup"><span data-stu-id="f2c96-103">Gets Power BI workspace collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2c96-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2c96-104">SYNTAX</span></span>

### <span data-ttu-id="f2c96-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2c96-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmPowerBIWorkspaceCollection [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2c96-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2c96-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2c96-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2c96-107">DESCRIPTION</span></span>
<span data-ttu-id="f2c96-108">Das Cmdlet " **Get-AzureRmPowerBIWorkspaceCollection** " ruft Power BI-Arbeitsbereichs Auflistungen in Ihrem Azure-Abonnement und ihrer Ressourcengruppe oder nach dem Sammlungsnamen ab.</span><span class="sxs-lookup"><span data-stu-id="f2c96-108">The **Get-AzureRmPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="f2c96-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f2c96-109">EXAMPLES</span></span>

### <span data-ttu-id="f2c96-110">Beispiel 1: Abrufen aller Arbeitsbereichs Auflistungen in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f2c96-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="f2c96-111">Dieser Befehl ruft die Arbeitsbereichs Auflistungen ab, die zur Ressourcengruppe mit dem Namen ResourceGroup17 gehören.</span><span class="sxs-lookup"><span data-stu-id="f2c96-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="f2c96-112">Beispiel 2: Abrufen einer Arbeitsbereichs Sammlung unter Verwendung des Namens</span><span class="sxs-lookup"><span data-stu-id="f2c96-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="f2c96-113">Dieser Befehl ruft die Arbeitsbereichs Sammlung mit dem Namen WCN11 in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="f2c96-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="f2c96-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2c96-114">PARAMETERS</span></span>

### <span data-ttu-id="f2c96-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2c96-115">-ResourceGroupName</span></span>
<span data-ttu-id="f2c96-116">Gibt den Namen der Ressourcengruppe an, aus der dieses Cmdlet Arbeitsbereichs Sammlungen erhält.</span><span class="sxs-lookup"><span data-stu-id="f2c96-116">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

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

### <span data-ttu-id="f2c96-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="f2c96-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="f2c96-118">Gibt den Namen der Power BI-Arbeitsbereichs Sammlung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="f2c96-118">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f2c96-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2c96-119">-DefaultProfile</span></span>
<span data-ttu-id="f2c96-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f2c96-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2c96-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2c96-121">CommonParameters</span></span>
<span data-ttu-id="f2c96-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2c96-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2c96-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2c96-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2c96-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f2c96-124">INPUTS</span></span>

## <span data-ttu-id="f2c96-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f2c96-125">OUTPUTS</span></span>

### <span data-ttu-id="f2c96-126">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="f2c96-126">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="f2c96-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="f2c96-127">NOTES</span></span>

## <span data-ttu-id="f2c96-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f2c96-128">RELATED LINKS</span></span>

[<span data-ttu-id="f2c96-129">Neu – AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="f2c96-129">New-AzureRmPowerBIWorkspaceCollection</span></span>](./New-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="f2c96-130">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="f2c96-130">Remove-AzureRmPowerBIWorkspaceCollection</span></span>](./Remove-AzureRmPowerBIWorkspaceCollection.md)


